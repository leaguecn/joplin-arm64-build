# joplin arm64 build
This repo is for storage of joplin arm build.
When i get my PI400 mini computer, i was so surprised for it. After installing the display device, i used it as the browser for searching some work information.
Then, one day, i wanna make some note for my searching result, testing on some open sources softwares. But there are a few builts for arm64 devices.
Joplin is one of pretty beautiful softwares. Yep, that time i cannot find any built for my PI400. So i tried to build one for my arm64 device.
After a long building time went away, including my spare time and break time. Different building methods, searching from internet, had been tried. Finally, i made it, suffering lack of the npm dependencies. p.s. the packages were build on ubuntu18 deploy on my oneplus7 via [Linux Deploy](https://github.com/meefik/linuxdeploy) app
## Build file links
+ [Joplin-arm64.dep](https://cumteducn-my.sharepoint.com/:u:/g/personal/liguinan_cumt_edu_cn/ETOpehbT4mVImciGQwBHmuABS2ENoB-XxHEXFckfMiN8Lw?e=elWzxW)
+ [Joplin-arm64.AppImage](https://cumteducn-my.sharepoint.com/:u:/g/personal/liguinan_cumt_edu_cn/EfGOAO6y6KdLoDilM1upJRkBfAxjFR9lorGF5pB7iFLiCQ?e=Odtpxv)

> update build sometimes
+ [v1.8.2(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EnddWEWykR9Mhv4Yb2Q3Ch4BWNXSBOvw5vQzbBS8Gdl1_Q?e=2ds6N), 2021/05/04
+ [v2.0.2(armv7l&arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EhdQEzHjFcZLnUdzayr1p08BM1eF2kR-syYCbNsrg0SwVQ?e=j8ZyLY), 2021/05/29
+ [v2.1.0(armv7l&arm64](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EhmwU5IWJZNGsu6anI01O-MBfOrzuvvtk_0If2f3QWr04Q?e=iUb4pJ), 2021/06/20
+ [v2.2.0(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EmoaUeqbDYpFhtEHvjzan0sBBtZNiZ0FV0cLZDb-2_5U1g?e=nxrhQV), 2021/07/24
+ [v2.2.2(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Eq2DjihbU75OlPVpJZPr-RQBl9y515MRJ_tZ31p-Ng4ETA), 2021/07/26
+ [v2.4.1(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EoAJ_B3EVs1Bs1B1crEX_IIBLChq43zZ8eLDbydc2bMx8g?e=LUhRoe), 2021/08/26
+ [v2.5.1(arm64&armv7l)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EtVGRYHRbEVOj91m2DACbssBnBTBLZKKJkVg2uWkRwBsOA?e=6AwV1a), 2021/10/12
+ [v2.8.8(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EjslzODy9sdIq8e3qfEKqWsBzk-00IL5GhJs-R7v3XUS4g?e=41QLFe), 2022/10/12 AM, build os centos7

> pre version build
- [v2.9.4(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Eh2wl_YcKElKu0VSwbTwvvsBvecdGwELqOnbuoKSB19MWw?e=ebrf9d), 2022/10/12 Midnight, build os centos7
- [v2.9.17(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EleNrHEty_JEplr0SewMRkYBrzYrDJ6zuA3IsqgKGJIeCw?e=WSK6pW), 2022/12/15 noon, build os opensuse_leap_15.4
- [v2.10.4(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EnKmV6rGmhNKgR4nh8wWqbMBHtwZQnb5bxZvlJl6fm8XLw?e=a6XwJJ), 2023/01/21 afternoon, build os: opensuse_leap_15.4

official release note: https://github.com/laurent22/joplin/releases


## Instruction
How to install the binary file for arm devices?
```sh
sudo dpkg -i xxx.deb

```
or you can run the AppImage file directly.
```sh
sudo chmod a+x yyy.AppImage
./yyy.AppImage

```
Good luck to you, guys. i really hope you can run joplin in your arm devices, making some tips note.



* * *
## Misc

### My build note

[How to build joplin for arm64 devices?](https://github.com/leaguecn/joplin-arm64-build/blob/main/how-to-build-joplin-for-arm64-devices.md)

### Update the build note

[how-to-build-joplin-for-arm64-update](https://github.com/leaguecn/joplin-arm64-build/blob/main/how-to-build-joplin-for-arm64-update.md)


### Build issues fixed list

+ [lzma-native@npm:8.0.6 compile fail](https://github.com/laurent22/joplin/issues/7270)
