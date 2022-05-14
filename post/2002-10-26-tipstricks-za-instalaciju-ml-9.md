---
author: tomaja
date: "2002-10-26T06:22:52Z"
excerpt: |
  Pošto su neki od korisnika imali odreÄ‘enih
  problema sa instalacijom
  ili koriš?enjem verzije 9.0 usled specifi?nih konfiguracionih situacija (odreÄ‘enih
  specifi?nih hardverskih ili softverskih komponenti) MandrakeSoft je za te
  slu?ajeve kreirao
  patch-eve koji ?e pomo?i da otklonite eventualne problemekoji se mogu pojaviti.
  Javili su se neki problemi vezani za podešavanje modema, miševa, raid kontrolera,...<br>
  Rešenja za vaše probleme možete na?i dalje u tekstu
guid: https://forum.linuxo.org/2002/10/26/tipstricks-za-instalaciju-ml-9/
id: 228
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Tips&#038;tricks za instalaciju ML 9
url: /tipstricks-za-instalaciju-ml-9/
---
Pošto su neki od korisnika imali odreÄ‘enih  
problema sa instalacijom  
ili koriš?enjem verzije 9.0 usled specifi?nih konfiguracionih situacija (odreÄ‘enih  
specifi?nih hardverskih ili softverskih komponenti) MandrakeSoft je za te  
slu?ajeve kreirao  
patch-eve koji ?e pomo?i da otklonite eventualne problemekoji se mogu pojaviti.  
Javili su se neki problemi vezani za podešavanje modema, miševa, raid kontrolera,&#8230;  
Rešenja za vaše probleme možete na?i dalje u tekstu<!--break-->

<p align="justify">
  <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><b>Napomena o koriš?enju patch-eva:</b><br /> Da bi koristili jedan od dole prikazanih <i>patch.pl</i> morate kopirati<br /> odreÄ‘eni patch na disketu, sa imenom patch.pl. Zatim treba da pokrenete<br /> ili butujete direktno sa CD-ROMa sa komandom &#8222;patch&#8220; u boot promptu (koji<br /> sepojavljuje kada kliknete na F1 pri pozdravnom ili splash ekranu), i<br /> naravno da ste ve? ubacili disketu sa disketom koja sadrži željeni patch.pl.<br /> Ukoliko butujete sa diskete umesto sa CD-ROMa, kopirajte patch.pl na vašu<br /> boot disketu a zatim pokrenite sistem sa diskete i pri promptu ukucajte komandu<br /> &#8222;patch&#8220;.</font></font>
</p>

<font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif">Na ovoj stranici ?ete prona?i :</p> 

<li>
  <a href="file:///home/tomaja/errata.php3#install">Mandrake Linux 9.0<br /> Instalacione Napomene</a>
</li>
<li>
  <a href="file:///home/tomaja/errata.php3#usage">Mandrake Linux 9.0 Napomene<br /> za koriš?enje</a>
</li>
<p>
  </font></font>
</p>

<p>
  <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="install"></p> 
  
  <h2>
    <b>Mandrake Linux 9.0 Instalacione Napomene</b>
  </h2>
  
  <p>
    </a> </font></font>
  </p>
  
  <ul>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#raid">Raid on / neuspešno podizanje<br /> sistema</a> </font></font>
    </li>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#blankimg">instalacije bazirane na<br /> blank.img-ne funkcionišu</a></font></font>
    </li>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#viac3">Problemi sa instalacijom na<br /> VIA C3 procesor</a></font></font>
    </li>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#cpqarray">Ne mogu da instaliram drajver<br /> na sistem sa Compaq Smart Array kontrolerom</a></font></font>
    </li>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#nvinstall">loše podešen X11 window<br /> sistem na nekim Nvidia &#8211; graf?kim karticama</a></font></font>
    </li>
    <li>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#imps2">Miš poludi kada se selektuje<br /> PS2 miš sa to?ki?em</a></font></font>
    </li>
  </ul>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="raid"></a><i>Greška:</i> <b>Kada<br /> se koristi raid on / na mašini sa prethodno instaliranim raid on /, pokretanje<br /> novoinstaliranog sistema nije uspešno.</b><br /> <i>Razlog:</i> Instaler pogrešno konfiguriše /etc/raidtab fajl kada pokušava<br /> da detektuje postoje?i raid.<br /> <i>Rešenje:</i> Formatirajte disketu sa DOS fajl sistemom(u Linux&#8217;u, možete<br /> koristiti komandu &#8222;mkdosfs /dev/fd0&#8220;). Kopirajte <a
 href="http://www.mandrakelinux.com/patches/9.0/raidtab/patch.pl">patch.pl</a><br /> na disketu. Izbacite disetu i restartujte sistem koriste?i Mandrake Linux<br /> 9.0 CD1 da bi pokrenuli CD-ROM instalaciju. Tokom podizanja pritisnite<br /> F1 pri splash ekranu, ubacite vašu disketu koja sadrži patch.pl. U promptu<br /> ukucajte &#8222;patch&#8220;, a zatim nastavite instalaciju kao u obi?ajenom postupku.</font></font>
  </p>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="blankimg"></a><i>Greška:</i><br /> <b>Instalacije birane na blank.img- ne rade (greška prilikom pribavljanja<br /> /lib/modules.cz&#8230;)</b><br /> <i>Razlog:</i> KOd za upravljanje modulima je izmenjen u odnosu na verziju<br /> 8.2 i nije više kompatibilan sa blank.img-instalacijama.<br /> <i>Razlog:</i> Skinite patch-ovan <a
 href="http://www.mandrakelinux.com/patches/9.0/blank/blank.img">blank.img</a><br /> i specijalni <a
 href="http://www.mandrakelinux.com/patches/9.0/blank/blank.iso">ISO</a><br /> (koji sadrži samo instalacioni program). md5sum za ISO je:<br /> </font></font>
  </p>
  
  <pre><font face="Helvetica, Arial, sans-serif">&lt;font
 face="Helvetica, Arial, sans-serif">7845b7641192cd897bb4dc70df41a39f  blank.iso<br /></font>&lt;/font></pre>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="viac3"></a><i>Greška:</i> <b>Greška<br /> se javlja prilikom instalacije ukoliko imate VIA C3 procesor (greška pri<br /> instalaciji XFree86 ili nekih drugih paketa)</b><br /> <i>Razlog:</i> Kernel neispravno prijavljuje Intel kompatibilnost procesora.<br /> <i>Rešenje:</i> Da bi izveli instalaciju, koristite boot flopi image<i>/images/alternatives/cdrom.img-2.2.19-BADZ5</i><br /> na prvom CD-ROMu (ili bilo koji .img sa 2.2.19 kernelom, za mrežne<br /> instalacije i sl.); kada od vas ra?unar zatraži root lozinku preÄ‘ite na #2<br /> (CTRL-ALT-F2) i ukucajte &#8222;rm -rf /mnt/lib/i686&#8220;, zatim se vratite na konzolu<br /> #7 (CTRL-ALT-F7) i završite instalaciju.</font></font>
  </p>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="cpqarray"></a><i>Greška:</i><br /> <b>Na mašini sa Compaq Smart Array kontrolerom, instaler prikazuje da ne<br /> može da instalira &#8222;sym53c8xx&#8220; drajver.</b><br /> <i>Razlog:</i> Smart Array&#8217;s drajver se nekorektno detektuje kao sym53c8xx.<br /> <br /> <i>Rešenje:</i> Formatirajte disketu sa DOS fajl sistemom(u Linuxu možete<br /> koristiti naredbu &#8222;mkdosfs /dev/fd0&#8220;). Kopirajte <a
 href="http://www.mandrakelinux.com/patches/9.0/cpqarray/patch.pl">patch.pl</a><br /> na disketu. TakoÄ‘e kopirajte <a
 href="http://www.mandrakelinux.com/patches/9.0/cpqarray/ldetect-0.4.6-7.cpqarray.1amdk.i586.rpm">ldetect-0.4.6-7.cpqarray.1amdk.i586.rpm</a><br /> na istu disketu. Izbacite disketu i restartujte sistem koriste?i Mandrake<br /> Linux 9.0 CD1 da bi pokernuli CD-ROM instalaciju. TOkom podizanja sistema,<br /> pritisnite F1 zatim ubacite disketu koja sadrži patch.pl. U promptu ukucajte<br /> &#8222;patch&#8220;, a zatim nastavite normalnu instalaciju sve dok ra?unar ne<br /> zatraži root lozinku. Kada se to desi preÄ‘ite na konzolu #2 (CTRL-ALT-F2)<br /> i pokrenite slede?e komande:</font></font>
  </p>
  
  <pre><font face="Helvetica, Arial, sans-serif">&lt;font
 face="Helvetica, Arial, sans-serif"># chroot /mnt<br /># mount /dev/fd0 /mnt/floppy<br /># rpm -Fvh /mnt/floppy/ldetect*<br /># umount /mnt/floppy<br /># exit</font>&lt;/font></pre>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif">Zatim se vratite na konzolu #7 (CTRL-ALT-F7)<br /> i završite instalaciju.</font></font>
  </p>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="nvinstall"></a><i>Greška:</i><br /> <b>Kada pri instalaciji koristite Nvidia kartice sa odreÄ‘enim monitorima<br /> X11 se loše konfiguriše i ne može da se pokrene.</b><br /> <i>Razlog:</i> Instater pogrešno detektuje Plug&#8217;n Play monitor i nepravilno<br /> podešava Monitor sekciju u XF86Config-4.<br /> <i>Rešenje:</i> Formatirajte disketu sa DOS fajl sistemom (u Linux-u, možete<br /> koristiti komandu &#8222;mkdosfs /dev/fd0&#8220;). Kopirajte <a
 href="http://www.mandrakelinux.com/patches/9.0/nvinstall/patch.pl">patch.pl</a><br /> na disketu. Uklonite disketu i restartujte sistem koriste?i Mandrake Linux<br /> 9.0 CD1 da bi pokrenuli CD-ROM instalaciju. Tokom startanja pritisnite F1<br /> i ubacite disketu na kojoj se nalazi patch.pl. U promptu ukucajte &#8222;patch&#8220;,<br /> a zatim nastavite instalaciju kao i obi?no.</font></font>
  </p>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="imps2"></a><i>Greška:</i> <b>Kada<br /> se menja protokol za miša sa PS2 (obi?ni PS2 miš) u IMPS2 (PS2 miš sa to?ki?em),<br /> miš poludi.</b><br /> <i>Razlog:</i> Još uvek nije jasan razlog, kod nekih miševa se nakon testiranja<br /> sve vrati u normalu (kada program za instalaciju zatraži da &#8222;MOVE YOUR WHEEL&#8220;).<br /> Kod nekih miševa, ovo iygleda da ne funkcioniše.<br /> <i>Rešenje:</i> Formatirajte disketu sa DOS fajl sistemom(u Linux-u, možete<br /> koristiti komandu &#8222;mkdosfs /dev/fd0&#8220;). Kopirajte <a
 href="http://www.mandrakelinux.com/patches/9.0/imps2/patch.pl">patch.pl</a><br /> na disketu. Izbacite je i restartujte sistem koriste?u Mandrake Linux 9.0<br /> CD1 da bi pokrenuli CD-ROM instalaciju. Tokom startanja pritisnite F1 i<br /> zatim ubacite pripremljenu disketu. Pri promptu ukucajte &#8222;patch&#8220;, za zatim<br /> normalno nastavite instalaciju.</font></font>
  </p>
  
  <p>
    <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="usage"></p> 
    
    <h2>
      <b>Mandrake Linux 9.0 Napomene pri koriš?enju</b>
    </h2>
    
    <p>
      </a></font></font>
    </p>
    
    <ul>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font

 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#nforce">Problemi sa nforce audio karicama</a><br /> </font></font>
      </li>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#xhang">X-ovi se ponekad zamrznu posle<br /> ve?eg perioda neaktivnosti</a></font></font>
      </li>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#apic">Na nekim sistemima dolazi do<br /> blokiranja ili gašenja mašine pri restartu X servera</a></font></font>
      </li>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#urpmi">&#8222;package not found&#8220; greške<br /> kod urpmi ili rpmdrake programa</a></font></font>
      </li>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#postfix">Postfix ne pokre?e DNS lookup</a></font></font>
      </li>
      <li>
        <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"> <a
 href="file:///home/tomaja/errata.php3#gateway">Problemi sa konektovanjem<br /> na Interenet sa lokalnim LAN i modemom za ISP</a></font></font>
      </li>
    </ul>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="nforce"></a><i>Greška:</i><br /> <b>Neke zvu?ne kartice se blokiraju za OSS drajverima</b><br /> <i>Razlog:</i> nforce audio je veoma sli?an i810 audio ?ipovima pa zbog toga<br /> bi (trebali) da rade sa OSS ili i810 drajverima. MeÄ‘utim, ovo i nije slu?aj<br /> sa odreÄ‘enim mati?nim plo?ama.<br /> <i>Rešenje:</i> Instalirajte NVIDIA_nforce pakete (što se ina?e obavlja rpmsrate<br /> kada je kartica u mašini). Formatirajte disketu sa DOS fajlsistemom i kopirajte<br /> <a href="http://www.mandrakelinux.com/patches/9.0/nforce/patch.pl">patch.pl</a><br /> na disketu. Izbacite disketu, restartujete sistem i ponovo a podignite ali<br /> sada koriste?i Mandrake Linux 9.0 CD1 radi CD-ROM instalacije. Tokom startanja<br /> pritisnite F1 i zatim ubacite pripremljenu disketu. U propmptu ukucajte<br /> &#8222;patch&#8220;, i zatim nastavite instalaciju. Ovo ?e zameniti i810_audio drajver<br /> sa odgovaraju?im nvaudio.o drajverom. Ukoliko ve? iamte instaliran<br /> 9.0 i ne želite da ga ponovo instalirate možete da startujete sistem u single<br /> modu (pri boot-u pritisnite esc taster i ukucajte: linux -s) i pokrenite:<br /> </font></font>
    </p>
    
    <pre><font face="Helvetica, Arial, sans-serif">&lt;font
 face="Helvetica, Arial, sans-serif">perl -pi -e 's/i810_audio/nvaudio/g' /etc/modules.conf<br /></font>&lt;/font></pre>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="xhang"></a><i>Greška:</i> <b>X<br /> se ruši nakon kra?eg perioda neaktivnosti. Mogu?e je pokrenuti kursor sa<br /> mišem ali se komande sa tastature ignorišu.</b><br /> <i>Razlog:</i> Podrška za DRI može biti nestabilna za rage-128 kartice (mogu?e<br /> i neke druge)<br /> <i>Rešenje:</i> Kao root, izmenite /etc/X11/XF86Config-4 i komentirajte ili<br /> izbrišite slede?u liniju:</font></font>
    </p>
    
    <pre><font face="Helvetica, Arial, sans-serif">&lt;font
 face="Helvetica, Arial, sans-serif">    Load "dri"<br /></font>&lt;/font></pre>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif">a zatim restartujte X server.</font></font>
    </p>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="apic"></a><i>Greška:</i> <b>Sistem<br /> se blokira bez vidiljivog razloga ili se automatski gasi kada se restartuje<br /> XFree86 server.</b><br /> <i>Razlog</i>: Neke mati?ne plo?e ne saraÄ‘uju sa podrškom za APIC u kernelu<br /> <i>Rešenje:</i> Možete pokrenuti sistem sa &#8222;noapic&#8220; opcijom u LILO promptu.<br /> Ukoliko ovo rešava problem izmenite /etc/lilo.conf i dodajte<br /> &#8222;noapic&#8220; opciju append= liniju za vaš kernel. Ako root, pokrenite &#8222;lilo&#8220;<br /> u komandnoj liniji.</font></font>
    </p>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="urpmi"></a><i>Greška:</i> <b>Kada<br /> se koriste urpmi ili rpmdrake, javlja se greška package not found pre pristupa<br /> CD-ROMu.</b><br /> <i>Razlog:</i> Instaler je pogrešno podesio opis medija za Contribution pakete.<br /> <i>Rešenje:</i> Ubacite instalacioni CD (CD-ROM #1) i pokernite komandu &#8222;urpmi.update<br /> cdrom8&#8220; kao root.</font></font>
    </p>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="postfix"></a><i>Greška:</i><br /> <b>Postfix ne uspeva da izvrši DNS lookups pri prijemu dolaze?e konekcije.</b><br /> <br /> <i>Razlog:</i> Nedostaju simboli?ki linkovi u chroot, /var/spool/postfix/lib.<br /> <br /> <i>Rešenje:</i> Pokrenite slede?u komandu kao root: &#8222;ldconfig -n /var/spool/postfix/lib&#8220;.<br /> </font></font>
    </p>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><a name="gateway"></a><i>Greška:</i><br /> <b>Imate mrežnu karticu za LAN i modem za pristup Internetu i ne možete da<br /> se konektujete na Internet.</b><br /> <i>Razlog:</i> Drakconnect pogrešno postavlja upit za gateway, i ppp ne može<br /> da postavi v<br /> ašu modemski konekciju kao default rutu.<br /> <i>Rešenje:</i> Kao root, izmenite /etc/sysconfig/network i ru?no uklonite<br /> GATEWAY unos.</font></font>
    </p>
    
    <p>
      <font face="Helvetica, Arial, sans-serif"><font
 face="Helvetica, Arial, sans-serif"><font size="1"></p> 
      
      <p>
        <span class="small"></span></font></font></font>
      </p>
      
      <p>
        <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=228">Креирај тему форума везану за овај текст</a>
      </p>