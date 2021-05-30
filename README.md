# joplin arm64 build
This repo is for storage of joplin arm64 build.
When i get my PI400 mini computer, i was so surprised for it. After installing the display device, i used it as the browser for searching some work information.
Then, one day, i wanna make some note for my searching result, testing on some open sources softwares. But there are a few builts for arm64 devices.
Joplin is one of pretty beautiful softwares. Yep, that time i cannot find any built for my PI400. So i tried to build one for my arm64 device.
After a long building time went away, including my spare time and break time. Different building methods, searching from internet, had been tried. Finally, i made it, suffering the npm dependencies lack fixed.
## Build file links
+ [Joplin-arm64.dep](https://cumteducn-my.sharepoint.com/:u:/g/personal/liguinan_cumt_edu_cn/ETOpehbT4mVImciGQwBHmuABS2ENoB-XxHEXFckfMiN8Lw?e=elWzxW)
+ [Joplin-arm64.AppImage](https://cumteducn-my.sharepoint.com/:u:/g/personal/liguinan_cumt_edu_cn/EfGOAO6y6KdLoDilM1upJRkBfAxjFR9lorGF5pB7iFLiCQ?e=Odtpxv)

> update build sometimes
+ [v1.8.2(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EnddWEWykR9Mhv4Yb2Q3Ch4BWNXSBOvw5vQzbBS8Gdl1_Q?e=2ds6N)
+ [v2.0.2(armv7l&armv64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EhdQEzHjFcZLnUdzayr1p08BM1eF2kR-syYCbNsrg0SwVQ?e=j8ZyLY)upuu


## Instruction
How to install the binary file for arm64 devices?
```sh
sudo dpkg -i Joplin-arm64.deb

```
or you can run the AppImage file directly.
```sh
sudo chmod a+x Joplin-arm64.AppImage
./Joplin-arm64.AppImage

```
Good luck to you, guys. i really hope you can run joplin in your arm64 devices, making some tips note.

## my build note

[How to build joplin for arm64 devices?](https://github.com/leaguecn/joplin-arm64-build/blob/main/how-to-build-joplin-for-atm64-devices.md)

