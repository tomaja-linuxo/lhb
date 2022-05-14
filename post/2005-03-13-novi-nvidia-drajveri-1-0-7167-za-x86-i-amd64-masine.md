---
author: tomaja
date: "2005-03-13T04:48:23Z"
excerpt: |
  NVIDIA je objavila <a href="http://www.nvidia.com/linux">nove drajvere</a>,
  verzija 1.0-7167 za <a
  href="http://www.nvidia.com/object/linux_display_ia32_1.0-7167.html">x86</a>
  i <a
  href="http://www.nvidia.com/object/linux_display_amd64_1.0-7167.html">AMD64</a>
  platforme. Koje su to nove ili ispravljene stvari u odnosu na prethodnu
  verziju možete pogledati dalje u tekstu. U svakom slu?aju ukoliko imate
  NVIDIAkarticu a koristite Linux sistem sa XOrg grafi?kim serverom
  preporu?ujemo da instalirate najnoviju verziju drajvera.
guid: https://forum.linuxo.org/2005/03/13/novi-nvidia-drajveri-1-0-7167-za-x86-i-amd64-masine/
id: 780
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Novi NVIDIA drajveri (1.0-7167) za x86 i AMD64 mašine
url: /novi-nvidia-drajveri-1-0-7167-za-x86-i-amd64-masine/
---
NVIDIA je objavila [nove drajvere](http://www.nvidia.com/linux),  
verzija 1.0-7167 za [x86](http://www.nvidia.com/object/linux_display_ia32_1.0-7167.html)  
i [AMD64](http://www.nvidia.com/object/linux_display_amd64_1.0-7167.html)  
platforme. Koje su to nove ili ispravljene stvari u odnosu na prethodnu  
verziju možete pogledati dalje u tekstu. U svakom slu?aju ukoliko imate  
NVIDIAkarticu a koristite Linux sistem sa XOrg grafi?kim serverom  
preporu?ujemo da instalirate najnoviju verziju drajvera.<!--break-->

  
\# Podrška za GeForce 6200 sa TurboCache&#8482; GPU  
\# Poboljšane performanse OpenGL-a.  
\# Dodana je podrška za XRandR rotaciju; pogledajte Appendix W u README  
fajlu.  
\# Dodana ExactModeTimingsDVI X config opcija za davanje direktne  
kontrole nad mode timings koji se koristi na Flat Panelima.  
\# Dodana podrška za Xorg dlloader.  
\# Promenjeno ponašanje drajvera tako da se PAT (Page Attribute Table)  
koristi kada je mogu?e umesto MTRR-a.  
\# Dodana je patch za X server bag sa PCI-E GeForce 6800 i GeForce 6600;  
fix su omogu?ili XFree86 i XOrg.  
\# Ispravljeni su problemi sa stabilnoš?u na x86_64 PCI-E sistemima.  
\# Ispravljeni su problemi sa 2D rendering-om na nekim starijim  
grafi?kim ?ipovima.  
\# UnapreÄ‘ena kompatibilnost sa Linux 2.6 kernelima.  
\# Ispravljeni su problemi kompatibilnosti sa nekim SWIOTLB em64t  
sistemima.  
\# Ispravljen je bag koji se pojavljivao sa greškom:  
&#8222;ioctl32(doom.x86:6747): Unknown cmd fd(16) cmd(c0384642){00}  
arg(ffffc75c) on /dev/nvidiactl&#8220;  
\# Ispravljena je NvAGP inkompatibilnost sa najnovijim Linux 2.6  
kernelima.  
\# UnapreÄ‘ena je interakcija sa udev fajl sistemom.  
\# UnapreÄ‘ene su performanse PCI kartica na Linux 2.6 sistemima.  
\# Obnovljena dokumentacija. Pogledajte [README](ftp://download.nvidia.com/XFree86/Linux-x86/1.0-7167/README.txt)  
fajl.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=780)