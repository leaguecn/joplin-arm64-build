## Step 1 Clone the git repo 
`git clone https://github.com/laurent22/joplin.git`

## Step 2 Install the dependencies
```
apt-get update && apt-get dist-upgrade -y && apt-get -y install curl && curl -sL https://deb.nodesource.com/setup_14.x | bash - && apt-get -y install nodejs build-essential git jq libsecret-1-dev rsync python ruby ruby-dev libnss3
<!--npm install -g npm-->
npm install npm@6 -g
gem install --no-document fp
```

> Perhaps, you need install electron and libvips
+ Electron https://stackoverflow.com/questions/31162671/install-electron-on-ubuntu
	 + Updated the npm package to latest:
	`sudo npm install npm@latest -g`
 	+ Installed electron with following switches:
	`sudo npm install electron -g –-verbose --unsafe-perm=true --allow-root`
+ Libvips https://libvips.github.io/libvips/install.html#building-libvips-from-a-source-tarball
```sh
git clone git://github.com/jcupitt/libvips.git

./autogen.sh 
make 
sudo make install

sudo ldconfig
```
Or install by tarball
```sh
wget https://github.com/libvips/libvips/releases/download/v8.10.5/vips-8.10.5.tar.gz

tar xf vips-x.y.z.tar.gz 
cd vips-x.y.z 
./configure

make 
sudo make install 
sudo ldconfig
```

## Step 3 modify the json file
```sh
cd joplin
sed -i '/"husky": ".*"/d' package.json
export LANG=en_US.utf8
```

## Step 4 build project by npm
`npm install`

## Step 5 package the built file
+ Direct to app-desktop fold
`cd packages/app-desktop`
+ build AppImage
`npm run dist -- --publish=never --linux --arm64`
+ Build deb
```
jq '.author |= {"name": "Laurent Cozic", "email": "laurent@cozic.net"}' package.json > package_new.json

jq '.build += {"deb": {"compression": "gz"}}' package_new.json > package.json
jq '.name = "Joplin"' package.json > package_new.json

mv package_new.json package.json
export USE_SYSTEM_FPM=true

npm run dist -- --arm64 --linux deb
```

## 参考资料/references
+ https://github.com/MichaelDavidHarry/joplin-armv7l

+ https://github.com/joesfer/joplin-arm64/blob/main/build.sh

+ https://github.com/alfredopalhares/arch-pkgbuilds


+ https://www.beekeeperstudio.io/blog/electron-apps-for-arm-and-raspberry-pi

+ https://www.reddit.com/r/PINE64official/comments/fh3xou/install_joplin_notes_on_stock_os_of_pinebook_pro/

+ https://github.com/joesfer/joplin-arm64


|时间|地点|修改人|备注
-----|----|-----|----
|2021-03-07|佛山禅城|lee|首发
|2021-03-14|佛山禅城|lee|修订
|2021-10-12|foshan chancheng|lee|add reference


