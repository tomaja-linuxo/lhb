---
author: tomaja
date: "2019-02-16T13:39:59Z"
guid: /?p=88939
id: 88939
image: /wp-content/uploads/2019/02/ubuntu_18_04_default_.jpg
tinymce-comment-field_enabled:
- "1"
title: Aжурирајте свој Убунту &#8211; 18.04.2 LTS је стигао
url: /azurirajte-svoj-ubuntu-18-04-2-lts-je-stigao/
---
Након мањег кашњења, <a href="https://www.canonical.com/" targer="_blank">Canonical</a> је објавио друго по реду ажурирање своје актуелне LTS верзије оперативног система, **Ubuntu 18.04.2 LTS (Bionic Beaver)**. Кашњење је проузроковано <a href="https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1814555" rel="noopener" target="_blank">отркивеним багом</a> у Линукс кернелу 4.18 који спречава покретање система на одређеним графичким картицама. Иначе, ово је друга ажурирана вертзија основног Убунту 18.04 LTS издања, [које ће бити ажурирано у наредних 10 година](/podrska-za-ubuntu-18-04-lts-do-2028-godine/). 

Ова грешка је успешно отклоњена како на 18.04 тако и на 18.10 верзијама. Поред ове и других исправки и унапређења битно је напоменути следеће:  
Ubuntu 18.04 сада омогућава нови &#8222;HWE&#8220; подсистем за детекцију хардвера који је преузет са новије верзије &#8211; из Ubuntu-а 18.10. Ова новина омогућава новијем Линукс 4.18 кернелу бољу подршку за хардвер и нове могућности самог кернела. Mesa пакети су такође ажурирани ради бољег рада графичких драјвера. Вреди пробати, зар не ? 

Као додатак, ово ново ажурирано издање доноси и подршку за <a href="https://www.raspberrypi.org/" rel="noopener" target="_blank">Raspberry Pi 3</a> рачунаре. As expected, all the other flavors contain the same core updates and various improvements and bug fixes.

Наравно, нова, ажурирана верзија се односи на сва званична Canonical-ова издања: **Ubuntu 18.04.2 LTS, Kubuntu 18.04.2 LTS, Xubuntu 18.04.2 LTS, Lubuntu 18.04.2 LTS, Ubuntu MATE 18.04.2 LTS, Ubuntu Budgie 18.04.2 LTS, и Ubuntu Kylin 18.04.2 LTS.**  
Да напоменем да, уколико већ користите Ubuntu 18.04 LTS или неки од горе поменутих варијетета, нема потребе да преузимате комплетну инсталацију, односно <a href="http://releases.ubuntu.com/18.04/" target="_blank" class="btn btn-default">нови ISO image</a> да би ажурирали систем. Довољно је да у терминалу покренете:

`#sudo apt-get update && apt-get upgrade`

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88939)