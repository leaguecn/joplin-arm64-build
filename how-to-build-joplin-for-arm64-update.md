## how to build joplin for arm devices?

It seems that the [official build instruction](https://github.com/laurent22/joplin/blob/dev/BUILD.md) use yarn not npm command to build this software package.
Yep, as you know that npm command run usually become endless during tons of typescript compiling. So they
choose the better toolkit and method to fix it, packing bigger joplin.


## About yarn

Yarn is a package manager for your code. It allows you to use and share code with other developers from
around the world. Yarn does this quickly, securely, and reliably so you don't ever have to worry.

If you wanna get more about yarn, plz go to the [official website](https://yarnpkg.com/)

## What is the relative of yarn and npm

Yarn command based on npm, so before installation yarn, you should install npm.

## Prepare the sources tarball

### download source codes project

```sh
# go to thread https://github.com/laurent22/joplin/releases
# choose one stable version, and download it
wget https://github.com/laurent22/joplin/archive/refs/tags/v2.8.8.tar.gz

```

> when it go to compile stage, i have to change build operation system into centos7.
> If you choose ubuntu18 as the operation system, the following instruction will be a little different.


### install the requirement dependencies

+ build-essential for centos7
```sh
yum install make automake gcc gcc-c++ kernel-devel
# alternative method
yum groupinstall "Development Tools" "Development Libraries"
```

+ libnss3
```sh
sudo yum install nss
```

+ jq
```sh
# install repo
yum install epel-release
# list some lib like as jq
yum list jq
# install jq
yum install jq
```

+ nodejs
```sh
# remove the lower version nodejs
yum remove nodejs npm -y
# download the setup file
curl --silent --location https://rpm.nodesource.com/setup_16.x | sudo bash
# install nodejs by yum
sudo yum -y install nodejs
# view the version
node -v
npm -v
```
+ yarn

```sh
# download the repo file
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
# install yarn after update the renew repo
sudo yum install yarn
# alternative method
sudo dnf install yarn
# view installed package version
yarn --version
```

+ install libvips
```sh
# get the tarball of release version
wget https://github.com/libvips/libvips/releases/download/v8.10.5/vips-8.10.5.tar.gz
# unpacke into fold
tar xf vips-x.y.z.tar.gz
# configure the build environment
cd vips-x.y.z
./configure
# compile the project
make
# install compiled binary files
sudo make install
sudo ldconfig
```

### update the build essential tools

+ update gcc and g++

```sh
# since version 2.8.8 require gcc && g++ version highter than 4.8, you better update gcc && g++
# 1. Install a package with repository for your system:
# On CentOS, install package centos-release-scl available in CentOS repository:
$ sudo yum install centos-release-scl

# On RHEL, enable RHSCL repository for you system:
$ sudo yum-config-manager --enable rhel-server-rhscl-7-rpms

# 2. Install the collection:
$ sudo yum install devtoolset-8

# 3. Start using software collections:
$ scl enable devtoolset-8 bash
```

+ update ruby and gem

```sh
yum install -y centos-release-scl-rh

# search the ruby relative software
yum search ruby
# install ruby26 and the dev version
yum install -y rh-ruby26 rh-ruby26-ruby-devel
# make it valid temporarily
scl enable rh-ruby26 bash
# view the version activated
ruby -v

```

+ install fpm by gem
```sh
# delete the invalid
gem sources --remove https://rubygems.org/
# add one valid
gem sources -a https://gems.ruby-china.com/
# or the another one
gem sources --add https://mirrors.tuna.tsinghua.edu.cn/rubygems/
# list all the sources
gem sources -l
# update gem source
gem sources -u
# install fpm
gem install fpm
```


### compile steps

+ mod the files

```sh
cd joplin
sed -i '/"husky": ".*"/d' package.json
export LANG=en_US.utf8
```
+ start install the typescripts by yarn

```sh
yarn install
```

+ build the desktop app

```sh
cd packages/app-desktop
# build AppImage
yarn run dist -- --publish=never --linux --arm64
# build deb
# mod the files
jq '.author |= {"name": "Laurent Cozic", "email": "laurent@cozic.net"}' package.json > package_new.json
jq '.build += {"deb": {"compression": "gz"}}' package_new.json > package.json
jq '.name = "Joplin"' package.json > package_new.json
# mod file save
mv package_new.json package.json
# build it now
export USE_SYSTEM_FPM=true
npm run dist -- --arm64 --linux deb
```

## Note on the end


When you encount some bug or abnormal issue, you should search for the solution in the internet firstly, using the search engine, such as goolge and bing. Then, try to fix it by yourself, step by step to solve one by one issue. Finally you will get it work. Of course, you should have some experience in the whole processing
for guessing what kind of bug is lead to invoke processing execution stop and exit. Yep, all the abnormal issue come from the build log, which you should read more carefully.


## references
https://blog.csdn.net/a1452302285/article/details/104328843    
https://blog.csdn.net/weixin_42194239/article/details/91046297    
https://blog.csdn.net/markximo/article/details/80449626    
https://www.jianshu.com/p/959ca0e5495a    
https://blog.csdn.net/chending_cd/article/details/100555955    
https://www.cnblogs.com/technicianafei/p/14765531.html    
https://www.softwarecollections.org/en/scls/rhscl/devtoolset-8/     
https://blog.51cto.com/34144451/3773031     
https://blog.csdn.net/adley_app/article/details/111733908     
https://github.com/leaguecn/joplin-arm64-build/blob/main/how-to-build-joplin-for-arm64-devices.md



+ update note

|time-stamp|place|editor|memo
-----|----|-----|----
|2022-10-12|foshan chancheng|lee|complete note
|2022-10-16|foshan chancheng|lee|upload to github

