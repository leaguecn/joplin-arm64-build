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
+ [v2.12.18(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Es6mabKT2mVOviMRPlhiW20BbAb-bCd3JkcdAzcLfeqWBQ?e=JjQAnX), 2023/09/24 PM, build os opensuse_leap_15.4 (only AppImage)
+ [v2.13.10(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EvjXWwfB0ZdGvu0teeo-LVgBZm9nGlk2mEJkGSAeMc6Mew?e=Jp7we0), 2023/12/24 PM, build os opensuse_leap_15.4 (only AppImage)
+ [v2.14.20(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Egow_wRY0gFFgzrqrkgrJ8IBkATfwoFMtcZzhf_GKA_5jw?e=yrcP32), 2024/03/27 PM, build OS: ubuntu 23.10
+ [v3.0.15(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EtbJo-yXMOdDvfHSASwhdUwB0wTY2DGjXYHOO8lufPJs7g?e=6qwyam), 2024/11/17 afternoon, build os: ubuntu 23.10
+ [v3.1.20(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EmFJSJhwmBdNoJOceOeWpkgBBhe-OC4wTuyc7o-FGNGwpA?e=acbQB4), 2024/11/17 afternoon, build os: ubuntu 23.10

* * *

> pre version build
- [v2.9.4(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Eh2wl_YcKElKu0VSwbTwvvsBvecdGwELqOnbuoKSB19MWw?e=ebrf9d), 2022/10/12 Midnight, build os centos7
- [v2.9.17(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EleNrHEty_JEplr0SewMRkYBrzYrDJ6zuA3IsqgKGJIeCw?e=WSK6pW), 2022/12/15 noon, build os opensuse_leap_15.4
- [v2.10.4(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EnKmV6rGmhNKgR4nh8wWqbMBHtwZQnb5bxZvlJl6fm8XLw?e=a6XwJJ), 2023/01/21 afternoon, build os: opensuse_leap_15.4
- [v2.10.13(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EnoSLtcRkuhJmCO7Ko24pl8B8SseWCExvgOfr8ppuSOeKQ?e=61G8kP), 2023/04/05 night, build os: opensuse_leap_15.4
- [v2.11.6(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Eim5oiUdjLlArfmDn9fhlc4BS8cSnylxFMlcPXu3iIzEUA?e=jnHu6N), 2023/06/04 night, build os: opensuse_leap_15.4
- [v2.12.7(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/Evhah1VPCgJPvKb5xDVE8NABggVmDFTm4f55T0mL9xNRKA?e=XV8mBu), 2023/07/19 night, build os: opensuse_leap_15.4
- [v2.12.10(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EpPFhAZNZnNGkWSlO-MIc3kBBLmf2sz0vWrLNjiRBiQTmg?e=Jd2OfH), 2023/08/06 afternoon, build os: opensuse_leap_15.4
- [v2.14.11(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EhseWci_gBRIpMKwpmJQRSMBkqWehFQx8PCjpp2l4afm8w?e=mRSQFc), 2024/02/03 night, build os: ubuntu 23.10
- [v3.0.6(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EksE9kpwyPlOl55vBfUXa2oBnphLKbv-JiS8uSyoE1nZdg?e=d1eT7h), 2024/05/02 night, build os: ubuntu-lts 22.04.3
- [v3.0.10(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EuhMqhgUw4JCrXl1Ac1_zYcBjnUWottKIGvoYcAktvaTfA?e=VqChFd), 2024/06/27 morning, build os: ubuntu-lts 22.04.3 
- [v3.2.1(arm64)](https://cumteducn-my.sharepoint.com/:f:/g/personal/liguinan_cumt_edu_cn/EveylK8AozhFsOXVLalNcrsByK6jCMvExxI0Hgfe13eGSg?e=u12DLU), 2024/11/16 afternoon, build os: ubuntu 23.10


* * *

P.S.: As test on my pi400 machine, some issues showed up on deb package. So i recommend you just use AppImage package if you need the new version. 2023/08/06


When I try to build package in ubuntu 23.10(deploy via termux in my new phone OPPO K11), issues on deb package had disappear just now. So the deb file is valid now. 2024/02/03

Now, I switch the build environment into my oneplus 7(ubuntu 23.10 deployed via termux app), then test cases in the AppImage and deb packages are well, just enjoy taking notes! 2024/03/28

Yep, I try to build joplin latest version in new environment, using my old phone Redmi Note7 Pro(ubuntu 22.04.3 deployed via termux app), and it works after fix some issues lack of libxxx. Test cases in the AppImage and deb package show that most of functions are normal. Cheer up, guys! 2024/05/03


- Joplin official release note: https://github.com/laurent22/joplin/releases
- Termux official website: https://termux.dev/en/



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
