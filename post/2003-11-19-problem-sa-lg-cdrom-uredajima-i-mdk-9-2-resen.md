---
author: tomaja
date: "2003-11-19T03:50:28Z"
excerpt: '<p><font face="Arial, sans-serif"><font color="blue"><strong>Ažurirano 14
  novembra 2003:</strong> LG je izbacio firmware update-ove za veći broj modela (i
  za one  koji nisu navedeni u listi dole), kao i proceduru oporavka uređaja koji
  su pogođeni ovim bagom (opis problema dalje u tekstu). Preporučujemo svim korisnicima
  da , ukoliko su im uređaji eventualno bili pogođeni ovim bagom da odrade ovaj postupak
  oporavka uređaja. Svi ostali koji poseduju LG CD čitače treba da upgrade-uju firmware
  svog uređaja i da nakon toga izvr&scaron;e instalaciju ili ažuriranje Mandrake Linux
  9.2.</font></font></p> <p><font face="Arial, sans-serif">Firmware updateovi i procedura
  oporavka su dostupni na <a href="http://us.lgservice.com/">LG-ijevom veb sajtu </a>
  i na <a href="http://support.dell.com/">Dell Support</a>. Da bi prona&scaron;li
  potreban firmware na LG veb stranici, kliknite na  &quot;Product Support&quot; a
  zatim izaberite  &quot;Device Driver&quot; sa levog navigacionog menija, zatim izaberite
  &quot;CD-ROM&quot; proizvod i imaćete mogućnost izbora različitih zip fajlova koji
  sadrže ispravljene firmware  updateove. Firmware se može aktivirati jedino sa  MS-DOS
  6.0 boot diskete. <br /> </font></p> <p><font face="Arial, sans-serif">Ukoliko nemate
  MS-DOS flopi (a verovatno je tako) , onda skinite <a href="http://www.freedos.org/">FreeDOS
  floppy image</a> i kreirajte boot disketu sa naredbom  &quot;dd if=FDBOOT.IMG of=/dev/fd0
  bs=1440k&quot;.</font></p> <p><font face="Arial, sans-serif"><font color="blue"><strong>NAPOMENA:</strong>
  Na osnovu informacije koja je dobijena od LG Electronics&#39; tehni?ke službe samo
  su CD-ROM modeli ugroženi ovim bagom . DVD-ROM/R/RW i  CD-RW modeli <span style="font-weight:
  bold">nisu</span> ugroženi.</font></font></p> <p><font face="Arial, sans-serif">Problem
  sa  LG CD-ROM uređajima je otkriven nakon objavljivanja kernela koji dolazi sa Mandrake
  Linux 9.2 . Ovaj problem se sastojao u tome &scaron;to je kernel slao instrukciju  FLUSH_CACHE
  LG CD-ROM uređaju...</font></p>'
guid: https://forum.linuxo.org/2003/11/19/problem-sa-lg-cdrom-uredajima-i-mdk-9-2-resen/
id: 392
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Problem sa LG cdrom uređajima i MDK 9.2 rešen
url: /problem-sa-lg-cdrom-uredajima-i-mdk-9-2-resen/
---
<font face="Arial, sans-serif"><font color="blue"><strong>Ažurirano 14 novembra 2003:</strong> LG je izbacio firmware update-ove za veći broj modela (i za one koji nisu navedeni u listi dole), kao i proceduru oporavka uređaja koji su pogođeni ovim bagom (opis problema dalje u tekstu). Preporučujemo svim korisnicima da , ukoliko su im uređaji eventualno bili pogođeni ovim bagom da odrade ovaj postupak oporavka uređaja. Svi ostali koji poseduju LG CD čitače treba da upgrade-uju firmware svog uređaja i da nakon toga izvr&scaron;e instalaciju ili ažuriranje Mandrake Linux 9.2.</font></font>

<font face="Arial, sans-serif">Firmware updateovi i procedura oporavka su dostupni na <a href="http://us.lgservice.com/">LG-ijevom veb sajtu </a> i na <a href="http://support.dell.com/">Dell Support</a>. Da bi prona&scaron;li potreban firmware na LG veb stranici, kliknite na "Product Support" a zatim izaberite "Device Driver" sa levog navigacionog menija, zatim izaberite "CD-ROM" proizvod i imaćete mogućnost izbora različitih zip fajlova koji sadrže ispravljene firmware updateove. Firmware se može aktivirati jedino sa MS-DOS 6.0 boot diskete. <br /> </font>

<font face="Arial, sans-serif">Ukoliko nemate MS-DOS flopi (a verovatno je tako) , onda skinite <a href="http://www.freedos.org/">FreeDOS floppy image</a> i kreirajte boot disketu sa naredbom "dd if=FDBOOT.IMG of=/dev/fd0 bs=1440k".</font>

<font face="Arial, sans-serif"><font color="blue"><strong>NAPOMENA:</strong> Na osnovu informacije koja je dobijena od LG Electronics' tehni?ke službe samo su CD-ROM modeli ugroženi ovim bagom . DVD-ROM/R/RW i CD-RW modeli <span style="font-weight: bold">nisu</span> ugroženi.</font></font>

<font face="Arial, sans-serif">Problem sa LG CD-ROM uređajima je otkriven nakon objavljivanja kernela koji dolazi sa Mandrake Linux 9.2 . Ovaj problem se sastojao u tome &scaron;to je kernel slao instrukciju FLUSH_CACHE LG CD-ROM uređaju&#8230;</font>

<!--break-->koja je činila da uređaj postane neupotrebljiv jer mu je birisala firmware. Ovo se de&scaron;avalo usled toga &scaron;to LG CD-ROM uređaji nisu kompatibilni sa ATAPI specifikacijama. Specifikacija koja ne zahteva implementaciju FLUSH\_CACHE komande u drajveru, i vraćajući gre&scaron;ku (ili ne čineći ni&scaron;ta) bi bilo ispravno pona&scaron;anje uređaja. Nasuprot tome, ponovno kori&scaron;ćenje komande je suprotno specifikaciji i LG ponovo koristi komandu FLUSH\_CACHE da bi izmenio firmware uređaja. Ova FLUSH\_CACHE komanda je podržana samo kod CD-RW ili DVD-RW uređaja; LG-based CD-ROM uređaji razumeju ovu komandu kao UPLOAD\_FIRMWARE komandu.

&nbsp;

<font face="Arial, sans-serif">Da bi odredili koji model CD-ROMa imate u računaru, možete da iskoristite <em>dmesg</em>. Na primer, ukoliko je va&scaron; CD-ROM na /dev/hdc, možete da iskoristite komandu <em>"dmesg|grep hdc</em>" . Takođe možete da iskoristite <em>hdparm</em> da bi videli detalje o va&scaron;em uređaju, koji će takođe ispisati i verziju firmware.Na primer <em>hdparm -i /dev/hdc</em> . Ovim ćete utvrditi da li ćete imati problema sa uređajem i pre instlacije Mandrake 9.2.</font>

<font face="Arial, sans-serif">Takođe možete da utvrdite model i firmware revision i iz BIOSa pri startanju raćunara.</font>

<font face="Arial, sans-serif">Pod Windows-om, možete da dobijete te informacije pomoću programa <a href="http://cd-rw.org/software/cdr_software/cdr_tools/nero_info_tool.cfm">Ner InfoTool</a>.</font>

<font face="Arial, sans-serif"><strong>Status modela:</strong> u zavisnosti od verzije firmware-a, isti model može ali i ne mora biti ugrožen. </font>

<font face="Arial, sans-serif"><font size="-1"> </p> 

<li>
  CRD-8160B (unknown status)
</li>
<li>
  CRD-8161B (unknown status)
</li>
<li>
  CRD-8240B (unknown status)
</li>
<li>
  CRD-8241B (unknown status)
</li>
<li>
  CRD-8320B (unknown status)
</li>
<li>
  CRD-8322B (<font color="red">Affected</font>: Compaq, IBM Aptiva 2158-125, firmware not reported) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8400B (<font color="red">Affected</font>: Dell Optiplex gx1, IBM PC 300 PL, Compaq, IBM Netvista, firmware 1.12) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8400C (<font color="red">Affected</font>: COMPAQ firmware not reported) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8401B (<font color="red">Affected</font>: firmware 1.06D)
</li>
<li>
  CRD-8402B (<font color="red">Affected</font>: Dell XPS T650r firmware not reported) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8480B (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8480C (<font color="red">Affected</font>: firmware 1.01, firmware 1.04, firmware 1.06) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8481B (<font color="red">Affected</font>: firmware 2.05) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8482B (<font color="red">Affected</font>: Dell Optiplex GX1, HP Vectra VL400 firmware 1.01, Dell Precision 220 rom 1.05) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRD-8483B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  CRD-8484B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  CRD-8485B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  CRD-8520B (<font color="green">Not Affected</font>: firmware 1.00, firmware 2.00)
</li>
<li>
  CRD-8521B (<font color="green">Not Affected</font>: firmware 1.03)
</li>
<li>
  CRD-8522B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  CRD-8523B (<font color="blue">Firmware update available</font>)
</li>
<li>
  CRN-8240E (unknown status)
</li>
<li>
  GCD-R200B (unknown status)
</li>
<li>
  GCD-R300B (unknown status)
</li>
<li>
  GCD-R320B (unknown status)
</li>
<li>
  GCD-R400B (unknown status)
</li>
<li>
  GCD-R420B (unknown status)
</li>
<li>
  GCD-R520B (unknown status)
</li>
<li>
  GCD-R540B (unknown status)
</li>
<li>
  GCD-R540C (unknown status)
</li>
<li>
  GCD-R542B (unknown status)
</li>
<li>
  GCD-R560B (unknown status)
</li>
<li>
  GCD-R580B (unknown status)
</li>
<li>
  GCE-8160B (<font color="green">Not Affected</font>: firmware 1.01, firmware 2.01)
</li>
<li>
  GCE-8320B (<font color="green">Not Affected</font>: firmware 1.02)
</li>
<li>
  GCE-8483B (<font color="green">Not Affected</font>: firmware 1.01, report by HP Labs)
</li>
<li>
  GCE-8520B (<font color="green">Not Affected</font>: firmware not reported)
</li>
<li>
  GCR-8480B (<font color="green">Not affected</font> according to LG) by HP Labs)
</li>
<li>
  GCR-8481B (<font color="red">Affected</font>: Dell Optiplex gx270; rom 1.06; date: Jun 2003) (<font color="green">Not Affected</font>: firmware not reported) (<font color="blue">Firmware update available</font>)
</li>
<li>
  GCR-8482B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  GCR-8520B (<font color="green">Not affected</font> according to LG) by HP Labs)
</li>
<li>
  GCR-8521B (<font color="red">Affected</font>: firmware 1.00, firmware 1.02) (<font color="blue">Firmware update available</font>)
</li>
<li>
  GCR-8522B (<font color="green">Not affected</font> according to LG)
</li>
<li>
  GCR-8523B (<font color="red">Affected</font>: firmware 1.00, OEM in custom-built computer) (<font color="blue">Firmware update available</font>)
</li>
<p>
  </font></font><span class="small"><font face="Arial, sans-serif"><br /> Poslednja izmena liste: Pon Nov 17 10:46:56 2003</font></span>
</p>

<p>
  <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=392">Креирај тему форума везану за овај текст</a>
</p>