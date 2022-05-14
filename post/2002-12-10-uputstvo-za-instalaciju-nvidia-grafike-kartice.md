---
author: tomaja
date: "2002-12-10T21:22:30Z"
excerpt: |
  UPUTSTVO ZA INSTALACIJU NVIDIA GeForce2 MX400 VIDEO KARTICE
  <br />
  Ovim redosledom:
  <br />
  -1. Instalirate kernel source za MDK, ( ako to niste uradili pri samoj instalaciji Mandrake-a, odabirom Development Station opcije ) a to se radi iz konzole, sa opcijom add software, gde odaberete od ponuÄ‘enih paketa kernel_source_..mdk... , uz ?ega ?e Mandrake traziti jos jedan fajl koji ide uz njega, a nalaze se na 2. i 3. instalacionom CD-u. Za one koji su ve? nešto pokušavali, pa im se zablokirao Mandrake u tekstualnom modu, preporu?ujem novu instalaciju, sa formatiranjem particije na kojoj se nalazi Mandrake i kao dodatnu opciju prilikom instalacije odaberite i Development paket,
  <br />
  -2. Zatim odete na internet i skinete sa Nvidijinog sajta, u odeljku za Linux, skroz dole(NVIDIA_kernel-1.0-3123.src.rpm). Kada ste ga skinuli ( kao i NVIDIA_GLX-1.0-3123.i386.rpm - drajver ) odete u direktorijum gde se nalazi novi kernel  koji ste skinuli sa internet i upisete kao root:
  <br />
  rpm --rebuild NVIDIA_kernel-1.0-3123.src.rpm,
  <br />
  -3. Taj novi kernel ?e se nalaziti u /usr/src/RPM/RPMS/i586/ NVIDIA_kernel-1.0-3123.i586.rpm,
  <br />
  -4. Tad odete u taj direktorijum i otkucate kao root: rpm -ivh NVIDIA_kernel-1.0-3123.i586.rpm,
  <br />
  -5. Nakon toga instalirate driver - NVIDIA_GLX-1.0-3123.i386.rpm komandom: rpm -ivh NVIDIA_GLX-1.0-3123.i386.rpm, što naravno podrazumeva da ste otišli u direktorijum gde se taj drajver nalazi,
  <br />
  -6. Odete do XF86Config-4 fajla (/etc/X11/XF86Config-4) i uz pomo? mc-a, tamo gde piše driver &#8220;nv&#8221;, upišete &#8220;nvidia&#8221;, zapamtite izmene ( save ),
  <br />
  -7. i onda reboot.
  <br />
  SREÄ†NO
guid: https://forum.linuxo.org/2002/12/10/uputstvo-za-instalaciju-nvidia-grafike-kartice/
id: 250
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Uputstvo za instalaciju NVIDIA grafi?ke kartice
url: /uputstvo-za-instalaciju-nvidia-grafike-kartice/
---
UPUTSTVO ZA INSTALACIJU NVIDIA GeForce2 MX400 VIDEO KARTICE  
  
Ovim redosledom:  
  
-1. Instalirate kernel source za MDK, ( ako to niste uradili pri samoj instalaciji Mandrake-a, odabirom Development Station opcije ) a to se radi iz konzole, sa opcijom add software, gde odaberete od ponuÄ‘enih paketa kernel\_source\_..mdk&#8230; , uz ?ega ?e Mandrake traziti jos jedan fajl koji ide uz njega, a nalaze se na 2. i 3. instalacionom CD-u. Za one koji su ve? nešto pokušavali, pa im se zablokirao Mandrake u tekstualnom modu, preporu?ujem novu instalaciju, sa formatiranjem particije na kojoj se nalazi Mandrake i kao dodatnu opciju prilikom instalacije odaberite i Development paket,  
  
-2. Zatim odete na internet i skinete sa Nvidijinog sajta, u odeljku za Linux, skroz dole(NVIDIA\_kernel-1.0-3123.src.rpm). Kada ste ga skinuli ( kao i NVIDIA\_GLX-1.0-3123.i386.rpm &#8211; drajver ) odete u direktorijum gde se nalazi novi kernel koji ste skinuli sa internet i upisete kao root:  
  
rpm &#8211;rebuild NVIDIA_kernel-1.0-3123.src.rpm,  
  
-3. Taj novi kernel ?e se nalaziti u /usr/src/RPM/RPMS/i586/ NVIDIA_kernel-1.0-3123.i586.rpm,  
  
-4. Tad odete u taj direktorijum i otkucate kao root: rpm -ivh NVIDIA_kernel-1.0-3123.i586.rpm,  
  
-5. Nakon toga instalirate driver &#8211; NVIDIA\_GLX-1.0-3123.i386.rpm komandom: rpm -ivh NVIDIA\_GLX-1.0-3123.i386.rpm, što naravno podrazumeva da ste otišli u direktorijum gde se taj drajver nalazi,  
  
-6. Odete do XF86Config-4 fajla (/etc/X11/XF86Config-4) i uz pomo? mc-a, tamo gde piše driver &#8220;nv&#8221;, upišete &#8220;nvidia&#8221;, zapamtite izmene ( save ),  
  
-7. i onda reboot.  
  
SREÄ†NO<!--break-->100% radi.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=250)