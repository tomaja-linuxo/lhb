---
author: tomaja
date: "2018-10-30T20:09:40Z"
guid: /?p=88829
id: 88829
image: /wp-content/uploads/2018/10/fedora29-816x345.jpg
tinymce-comment-field_enabled:
- "1"
title: Објављена Fedora 29, стиже и RHEL 7.6
url: /objavljena-fedora-29-stigao-i-rhel-7-6/
---
Многи кажу најбоља до сада,  _**Fedora 29**_ доноси много новина од којих је можда и најзначајнија увођење [_Fedora Modularity_](https://docs.pagure.org/modularity/) опције која, укратко, омогућава да на истој верзији Федоре користимо различите верзије софтверских пакета. И неће бити потребе да се ажурира цео систем да би користили новију или старију верзију неке апликације.

Друге веће измене су нова, ажурирана верзија подразумеваног GNOME 3.30 десктоп окружења,  [ZRAM](https://fedoraproject.org/wiki/Changes/ZRAMforARMimages) за  ARM варијанте Федоре, као и _Vagrant_ за [Fedora Scientific](https://labs.fedoraproject.org/en/scientific/). Не треба заборавити огроман број ажурираних софтверских пакета.

У наредном периоду ће [Fedora CoreOS](https://fedoramagazine.org/announcing-fedora-coreos/) заменити _Atomic Host_ као контејер орјентисано издање,  а планира се [IoT](https://docs.fedoraproject.org/en-US/iot/) издање за Fedora-у 30. Као и [Fedora Silverblue](https://docs.fedoraproject.org/en-US/fedora-silverblue/)  који би у наредним верзијама требао потпуно да буде спреман за продукцијски ниво рада.

Нова Федора је доступна у великом броју едиција, почевши од [Радне станице](https://getfedora.org/en/workstation/download/), [Сервера](https://getfedora.org/en/server/download/), [Atomic Host](https://getfedora.org/en/atomic/download/) едиције, разноврсних <a href="https://spins.fedoraproject.org/" target="_blank" rel="noopener">Десктоп спинова</a> (_KDE, Xfce, Mate-Compiz, LXQT, Cinnamon, LXDE, SOAS_). [Labs](https://labs.fedoraproject.org/)-си су ту за посебне намене, као и  варијанте за [Cloud](https://alt.fedoraproject.org/cloud/) и [ARM уређаје](https://arm.fedoraproject.org/), као и друге хардверске палтформе.

Ако нисте сигурни шта вам од овог свега навише одговара потражите оно право на [getfedora.org](https://getfedora.org/) . Ако већ имате инсталирану Федору, ажурирање система је све што вам треба &#8211; упуство за [ажурирање](https://fedoramagazine.org/upgrading-fedora-27-fedora-28/) (en).

#### RHEL 7.6

Сви су већ чули за највећу трансакцију у свету отвореног кода, и преласку <a href="https://linuxo.org/ibm-kupuje-red-hat-za-34-milijarde-dolara/" target="_blank" rel="noopener"><em>Red Hat</em>-a под окриље <em>IBM</em></a>-a. Да цела прича била још потпунија, _Red Hat Inc_. je објавио нову верзију **Red Hat Enterprise Linux****-a 7.6**

Вероватно последња верзија система без елемената утицаја новог власника, RHEL се базирао на појачање безбедности увођењем  подршке за TPM 2.0 као и интеграцију _nftables firewall_ технологије, која је при томе отвореног кода.<figure id="attachment_1430" aria-describedby="caption-attachment-1430" style="width: 81px" class="wp-caption alignright">

<img class="size-full wp-image-1430" src="/wp-content/uploads/2006/11/redhat.png" alt="RedHat" width="91" height="94" /> <figcaption id="caption-attachment-1430" class="wp-caption-text">** **</figcaption></figure> 

Red Hat такође уводи нови пројекат у оквиру својих контејнерских алатки преко Podman-а. Помоћу њега, контејнери се могу сада покретати изван Кубернета што корисницима омогућава да креирају, постављају, проналазе и деле _cloud-native_ апликације много лакше. Ето зашто је, између осталог, IBM спреман да да онолике паре !

<a href="https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/7.6_release_notes/" target="_blank" rel="noopener">Званична објава издања</a> и [објава за медије](https://www.redhat.com/en/about/press-releases/red-hat-refines-hybrid-cloud-innovation-latest-version-world%E2%80%99s-leading-enterprise-linux-platform)

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88829)