---
author: tomaja
date: "2011-10-25T05:59:12Z"
excerpt: Између многих нових могућности које су укључене у Линуx кернел 3.1 можемо
  да напоменемо подршку за опен соурце OpenRISC процесоре, различита слаб аллоцатор
  и writeback throttling унапређења, нову iSCSI имплементацију, подршку за NFC (Near-Field
  Communication) чипове и подршку за Wii контролер.
guid: https://forum.linuxo.org/2011/10/25/linux-kernel-3-1/
id: 2551
image: /wp-content/uploads/2011/10/kernel_1.jpg
layout_key:
- ""
post_slider_check_key:
- "0"
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:5:"88128";s:11:"_thumb_type";s:5:"thumb";}
title: Линукс кернел 3.1
url: /linux-kernel-3-1/
---
Између многих нових могућности које су укључене у **Линукс кернел 3.1** можемо да напоменемо подршку за опен соурце OpenRISC процесоре, различита _слаб аллоцатор_ и _writeback throttling_ унапређења, нову _iSCSI_ имплементацију, подршку за **NFC** (Near-Field Communication) чипове и подршку за Wii контролер.

Поред наведеног, нови Линукс кернел 3.1 омогућава боље управљање енергијом преко нових _cpupowerutils userspace_ алата, ЕXТ3 фајл систем је добио активиране баријере по дефаулт-у, а много других драјвера је додано или унапређено (нпр. Интелове графике су добиле акцелерацију активирану по дефолт-у).

Иако није наведено у званичној Линусовој најави зна се за подршку _Intel Ivy Bridge_ чиповимма, _Cedar Trail_-у,унапређењима за _GMA500_, и много тога другог.

Линуx кернел 3.1 такође доноси већи број унапређења за различите фајл системе попут trfs, NFS, XFS, FAT, HFS+ или SquashFS-a. Pci Backend драјвер за Xen је такође присутан, као и подршка за Nested VMX(АМД виртуелизацију).

Комплетна листа ново подржаних уређаја, нових драјвера и других унпређења се може видети на [Линукс кернел 3.1 DriverArch страници](http://kernelnewbies.org/Linux_3.1_DriverArch) као и на [changelog](http://kernelnewbies.org/Linux_3.1)-у.

<p class="download">
  Преузмите нови Линукс кернел 3.1 са <a href="http://kernel.org"><del>kernel.org</del></a>
</p>

Док се сервери не буду ажурирани нови кернел се може преузети са <http://git.kernel.org/?p=linux/kernel/git/torvalds/linux.git;a=commit;h=c3b92c8787367a8bb53d57d9789b558f1295cc96>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2551)