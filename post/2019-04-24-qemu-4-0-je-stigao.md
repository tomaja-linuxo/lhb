---
author: tomaja
date: "2019-04-24T11:18:05Z"
guid: /?p=88978
id: 88978
image: /wp-content/uploads/2019/04/qemu-logo.png
tinymce-comment-field_enabled:
- "1"
title: QEMU 4.0 је стигао
url: /qemu-4-0-je-stigao/
---
<a href="https://qemu.org" rel="noopener noreferrer" target="_blank">QEMU</a> &#8211; генерички емулатор и виртуелизатор отвореног кода доживео је ново и велико, округло издање: 4.0. Ово издање садржи преко 3100 допуна кода од преко 220 аутора. 

**QEMU 4.0** је битан пре свега на пољу АРМ архитектуре, додавањем подршке за многе ARMv8 екстензије (SB, PredInv, HPD, LOR, FHM, AA32HPD, PAuth, JSConv, CondM, FRINT, and BTI).AArch64 процесори могу покретати кернеле од преко 4GB-а смештене у RAM-у. Многе друге процесорске архитектуре попут PowerPC-a, RISC-V, I6500 и I7200, s390. Ту је и x86 где је подршка за MPX уклоњена, a HAX акцелератор је сада подржан и на другим POSIX хостовима, укључујући Линукс и NetBSD.

Званична објава се може погледати на <a href="https://www.qemu.org/2019/04/24/qemu-4-0-0/" rel="noopener noreferrer" target="_blank">qemu блог страници</a>, а комплетна листа промена на <a href="https://wiki.qemu.org/ChangeLog/4.0" rel="noopener noreferrer" target="_blank">званичној вики страници</a>.

Нову верзију емулатора можете преузети <a href="https://www.qemu.org/download/" rel="noopener noreferrer" target="_blank">овде</a>, или инсталирањем/ажурирањем преко пакет менаџера своје Линукс дистрибуције.

Некада давно, [писали смо о верзији 0.70](/qemu-0-7-0/) 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88978)