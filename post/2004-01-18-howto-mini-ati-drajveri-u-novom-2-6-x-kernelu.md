---
author: tomaja
date: "2004-01-18T13:44:36Z"
excerpt: |
  U ovom mini FAQ-u objasnjeno je kako instalirati zvanicne ATI drajvere u novoj grani kernela.<br />
  Najnovija verzija kernela 2.6.x moze se skinuti sa http://www.kernel.org, a fglrx drajveri sa http://www.ati.com . Postupak instalacije kernela nije tema mini FAQ-a, i pretpostavljam da svi vi koji citate ovo znate kako se ceo postupak obavlja.
guid: https://forum.linuxo.org/2004/01/18/howto-mini-ati-drajveri-u-novom-2-6-x-kernelu/
id: 408
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: HOWTO mini &#8211; ATI drajveri u novom 2.6.x kernelu
url: /howto-mini-ati-drajveri-u-novom-2-6-x-kernelu/
---
U ovom mini FAQ-u objasnjeno je kako instalirati zvanicne ATI drajvere u novoj grani kernela.  
Najnovija verzija kernela 2.6.x moze se skinuti sa http://www.kernel.org, a fglrx drajveri sa http://www.ati.com . Postupak instalacije kernela nije tema mini FAQ-a, i pretpostavljam da svi vi koji citate ovo znate kako se ceo postupak obavlja.<!--break-->1. Sta treba ukljuciti/iskljuciti u kernelu

Prilikom kompajliranja kernela i pravljenja .config fajla, bilo sa  
&#8216;make config&#8217;, &#8216;make menuconfig&#8217; ili &#8216;make xconfig&#8217;,&nbsp;  
potrebno je uraditi sledece da bi vas ATI proradio:

&#8211; ukljuciti MTRR; lokacija &#8211; Procesor type and features-> MTRR  
(Memory Type Range Register) support  
&#8211; ukljuciti agpgart; lokacija &#8211; u Device Drivers-> Character  
Devices-> /dev/agpgart (AGP Support), izaberete vas cipset, i  
izaberite da se drajver kompajlira kao MODUL! ( i agpgart i drajver za  
cipset)  
-iskljuciti DRM; lokacija &#8211;&nbsp; Device Drivers-> Character  
Devices-> Direct Rendering Manager (XFree 4.1.0 and higher support)  
&#8211; iskljuciti radeon podrsku za frame buffer : lokacija &#8211; u Device  
Drivers-> Graphic Support-> Support for frame buffer Devices,  
iskljuciti sve drajvere osim podrske za VESA VGA i VGA 16-color .

2. Instalacija drajvera iz rpm paketa

Skinute drajvere sa ATI-jevog sajta instalirajte klasicim  
&nbsp; rpm -Uhv <package_name>.rpm  
&nbsp;ili ako bude problema  
&nbsp; rpm -i &#8211;force <ati\_package\_name>.rpm  
&nbsp;ili ako bude jos nekih problema ubacite &#8216;&#8211;nodeps&#8217; switch&#8217; .  
Vise o tome moze se naci u readme fajlu, na istom mestu odakle ste  
download-ovali drajver.

3. Patch-ovanje drajvera

Drajver kao takav nije prilagodjen novom kernelu, i mora se patchovati.  
Obavezni patch koji ispravlja VMALLOC gresku, dug je samo 10 redova :

root@sale:/lib/modules/fglrx# cat fglrx-2.6-vmalloc-vmaddr.patch

diff -ruN build\_mod.orig/firegl\_public.c build\_mod/firegl\_public.c  
&#8212; build\_mod.orig/firegl\_public.c&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  
2003-09-05 00:45:33.539384168 +0200  
+++ build\_mod/firegl\_public.c&nbsp;&nbsp; 2003-09-05 00:47:13.193234480  
+0200  
@@ -129,7 +129,9 @@  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #define  
pte\_offset&nbsp; pte\_offset_map  
&nbsp;&nbsp;&nbsp;&nbsp; #endif  
&nbsp;#endif  
&#8211;  
+#ifndef VMALLOC_VMADDR  
+#define VMALLOC_VMADDR(x)&nbsp; ((unsigned long)(x))  
+#endif  
&nbsp;// ============================================================  
&nbsp;#ifndef TRUE  
&nbsp;#define TRUE 1

Snimite ovih 10-ak redova od diff naredbe do kraja u  
/lib/modules/fglrx/fglrx-2.6-vmalloc-vmaddr.patch  
i patchujte firegl_public.c sa  
&nbsp; &#8216;patch -p0 < fglrx-2.6-vmalloc-vmaddr.patch&#8217;

U slucaju da imate AMD procesor potrebno je primeniti i sledeci patch :

root@sale:/lib/modules/fglrx/build_mod# cat  
fglrx-3.2.8-fix-amd-adv-spec.patch

&#8212; firegl_public.c.orig&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  
2003-09-22 04:43:30.000000000 +0200  
+++ firegl_public.c&nbsp;&nbsp;&nbsp;&nbsp; 2003-10-09  
00:14:41.337778176 +0200  
@@ -3106,7 +3108,7 @@

&nbsp;int _\_ke\_amd\_adv\_spec\_cache\_feature(void)  
&nbsp;{  
-#if ( (PAGE\_ATTR\_FIX == 1) || (LINUX\_VERSION\_CODE ==  
KERNEL_VERSION(2,4,19)) )  
+#if ( (PAGE\_ATTR\_FIX == 1) || (LINUX\_VERSION\_CODE >=  
KERNEL_VERSION(2,4,19)) )  
&nbsp;/* the kernel already does provide a fix for the AMD Athlon  
&nbsp;&nbsp;&nbsp; big page attribute / cache flush data consistency  
system bug on its own.  
&nbsp;&nbsp;&nbsp; (AMD claimed that CPU cache behaviour for such pages  
is not specified.)

Ovaj patch snimite u  
/lib/modules/fglrx/build_mod/fglrx-3.2.8-fix-amd-adv-spec.patch  
i patchujte ponovo firegl_public.c sa  
&nbsp; &#8216;patch -p0 < fglrx-3.2.8-fix-amd-adv-spec.patch&#8217;

Nakon zavrsenog patchovanja, pokrenite make skriptu u  
/lib/modules/fglrx/build_mod  
&nbsp; &#8216;/lib/modules/fglrx/build_mod/make.sh&#8217;  
i kad build-ovanje modula bude zavrseno i make_install direktorijum  
iznad :  
&nbsp; &#8216;/lib/modules/fglrx/make_install.sh&#8217;

Ukoliko se ne pojave poruke sa greskama, kompajliranje i ubacivanje  
fglrx modula u kernel uspesno je zavrseno; da li je modul ucitan  
proverite sa &#8216;lsmod | grep fglrx&#8217;

XF98Config-4 fajl koji je radio sa starim kernelom radice bez ikakvih  
izmena i problema, a ako zelite da ga ponovo napravite, startujte  
&#8216;fglrxconfig&#8217;

Na kraju, ubacite u u /etc/modules.conf ili u rc.local ili negde drugde  
u startup skriptama liniju &#8216;modprobe fglrx&#8217; kako bi se modul ucitavao  
pri startovanju sistema.

Restartujte sistem sa novim kernelom, startujte X i proverite radi li  
3d akceleracija :  
root@sale:/# uname -a  
Linux sale 2.6.1 #2 Sun Jan 18 12:17:40 CET 2004 i686 unknown unknown  
GNU/Linux  
root@sale:/# glxinfo | grep direct  
direct rendering: Yes  
root@sale:/# glxgears  
13464 frames in 5.0 seconds = 2692.800 FPS  
14375 frames in 5.0 seconds = 2875.000 FPS  
14377 frames in 5.0 seconds = 2875.400 FPS  
14378 frames in 5.0 seconds = 2875.600 FPS

Autor: salac <salac at etf.bg.ac.yu>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=408)