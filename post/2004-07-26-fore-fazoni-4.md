---
author: tomaja
date: "2004-07-26T03:37:09Z"
excerpt: |
  Evo nekih "fora i fazona" koje bi trebalo da nam olakšaju rad u konzoli
  a vrlo ?esto su najbolja rešenja. Ovog puta su sa leve strane date
  komande a sa desne je dat opis komande, tj. šta sa njom postižemo.
  Pozivamo i sve vas ukoliko imate svoje ili prikupljene tipove da nam ih
  pošaljete za objavljivanje ili to sami uradite preko <a
  href="modules.php?name=Submit_News">formulara za
  objavljivanje tekstova</a>. Za nastavak kliknite read more...
guid: https://forum.linuxo.org/2004/07/26/fore-fazoni-4/
id: 490
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Fore &#038; fazoni (4)
url: /fore-fazoni-4/
---
Evo nekih &#8222;fora i fazona&#8220; koje bi trebalo da nam olakšaju rad u konzoli  
a vrlo ?esto su najbolja rešenja. Ovog puta su sa leve strane date  
komande a sa desne je dat opis komande, tj. šta sa njom postižemo.  
Pozivamo i sve vas ukoliko imate svoje ili prikupljene tipove da nam ih  
pošaljete za objavljivanje ili to sami uradite preko [formulara za  
objavljivanje tekstova](modules.php?name=Submit_News). Za nastavak kliknite read more&#8230;<!--break-->

<table class="pixelbeat">
  <tr>
    <td
style="vertical-align: top; font-weight: bold; color: rgb(0, 0, 0); background-color: rgb(255, 255, 204);">
      KOMANDA
    </td>
    
    <td
style="vertical-align: top; font-weight: bold; color: rgb(0, 0, 0); background-color: rgb(255, 255, 204);">
      OPIS
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      apropos word
    </td>
    
    <td>
      prikazuje komande koje se imaju re?: word
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      gpg -c file
    </td>
    
    <td>
      ekriptuje fajl
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      gpg file.gpg
    </td>
    
    <td>
      dekriptuje fajl
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      look wordprefix
    </td>
    
    <td>
      brzo pretraživanje re?nika
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      grep &#8211;color word /usr/share/dict/words
    </td>
    
    <td>
      ozna?ava mesta re?i u re?niku
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      nice command
    </td>
    
    <td>
      pokre?e ne prioritetnu komandu
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      renice 19 -p $$
    </td>
    
    <td>
      stavlja teku?i shell u stanje niskog prioriteta
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      echo &#8222;wget url&#8220; | at 01:00
    </td>
    
    <td>
      download-ujte url u 1 posle pono?i u teku?i direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      echo &#8222;mail -s &#8216;get the train&#8217;<br /> P@draigBrady.com < /dev/null" | at 17:45
    </td>
    
    <td>
      email podsetnik
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      printf &#8222;%&#8217;d<br /> &#8220; 1234
    </td>
    
    <td>
      prikaoj sa grupisanjem na hiljaditi deo
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      watch -n1 &#8222;cat /proc/interrupts&#8220;
    </td>
    
    <td>
      gledajte promene podataka neprekidno
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      time command
    </td>
    
    <td>
      prikazuje koliko je komandi vremena potrebno
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      alias hd=&#8217;od -Ax -tx1z -v&#8217;
    </td>
    
    <td>
      pogodni hexdump alias
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      which command
    </td>
    
    <td>
      prikazuje punu putanju komande
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ls | pr -T9 -W$COLUMNS
    </td>
    
    <td>
      prikazuje u 9 kolona u širini terminala
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      touch -c -t 0304050607 file
    </td>
    
    <td>
      podešava vremensku marku(YYMMDDhhmm)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      pstree -p
    </td>
    
    <td>
      prikazuje hierarhiju procesa
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      lsof /dir/file
    </td>
    
    <td>
      prokazuje koji proces koristi dati fajl
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>prostor na disku<br /> </b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ls -lSr
    </td>
    
    <td>
      prikazuje fajlove, najve?i ?e biti poslednji
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      du -sh file dir
    </td>
    
    <td>
      prikazuje iskoriš?enost diska po fajlovima i diretorijumima
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      df -h
    </td>
    
    <td>
      prikazuje slobodan prostor na disku
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      df -i
    </td>
    
    <td>
      prikazujeslobodne inodes
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      fdisk -l
    </td>
    
    <td>
      prikazuje veli?inu particija na diskovima (kao root)
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>kretanje kroz direktorijume<br /> </b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      cd &#8211;
    </td>
    
    <td>
      vra?a nam u prethodni direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      cd
    </td>
    
    <td>
      vra?a nas u home direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      (cd dir && command)
    </td>
    
    <td>
      ide u direktorijum, izvršava komandu i vra?a nas u trenutni<br /> direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      pushd /usr
    </td>
    
    <td>
      stavlja trenutni direktorijum u pozadinu i ulazi u /usr ali<br /> se možemo vratiti u teku?i komandom <b>popd</b>
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>CD</b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      dd bs=1M if=/dev/cdrom | gzip ><br /> cdrom.iso.gz
    </td>
    
    <td>
      kopira i ?uva podatke sa CDa
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      mkisofs -r dir | gzip > cdrom.iso.gz
    </td>
    
    <td>
      kreira cdrom image iz direktorijuma
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      mount -oloop cdrom.iso /mnt/dir
    </td>
    
    <td>
      montira cdrom image u /mnt/dir (za pregled/editovanje)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      gzip -dc cdrom.iso.gz | cdrecord dev=0,0,0 &#8211;
    </td>
    
    <td>
      reže cdrom image
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      cdparanoia -B
    </td>
    
    <td>
      ripuje audiotrake sa CD u wav fajlove u trenutni direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      cdrecord dev=0,0,0 -audio *.wav
    </td>
    
    <td>
      kreira audio CD od svih wav fajlova u trenutnom<br /> direktorijumu
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      oggenc &#8211;tracknum=&#8220;track&#8220; track.cdda.wav -o<br /> &#8222;track.ogg&#8220;
    </td>
    
    <td>
      kreira ogg fajl od wav fajla
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <span style="font-weight: bold;">arhiviranje</span>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      tar c dir/ | bzip2 > dir.tar.bz2
    </td>
    
    <td>
      kreira arhivu celog dir/
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      bzip2 -dc dir.tar.bz2 | tar x
    </td>
    
    <td>
      raspakivanje arhive
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      find dir/ -name &#8222;*.png&#8220; | xargs tar rf<br /> dir.tar; bzip2 dir.tar
    </td>
    
    <td>
      kreira arhivu fajla *.png u dir/
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ( tar cf &#8211; /dir/to/copy ) | ( cd /where/to/<br /> && tar xf &#8211; )
    </td>
    
    <td>
      kopira (sa dozvolama) copy/ diretorijum u /where/to/
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ( cd /dir/to/copy && tar cf &#8211; . ) | (<br /> cd /where/to/ && tar xf &#8211; )
    </td>
    
    <td>
      kopira (sa dozvolama) sadržaj copy/ direktorijuma<br /> u /where/to/<br /> direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ( tar cf &#8211; /dir/to/copy ) | gzip | ssh<br /> user@remote &#8216;cd /where/to/ && gzip -dc | tar xf -&#8216;
    </td>
    
    <td>
      kopira (sa dozvolama) copy/ direktorijum u mrežni :/where/to/<br /> direktorijum
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      dd bs=1M if=/dev/hda | gzip | ssh user@remote<br /> &#8216;dd of=hda.gz&#8217;
    </td>
    
    <td>
      bakapuje hard disk na udaljenu mašinu (na mreži)
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>pretraživanje fajlova<br /> </b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      alias l=&#8217;ls -l &#8211;color=auto&#8217;
    </td>
    
    <td>
      przi listing direktorijuma
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ls -lrt
    </td>
    
    <td>
      prikazuje fajlove po datumu
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      find -name &#8222;*.[ch]&#8220; | xargs grep -E &#8222;search<br /> string&#8220;
    </td>
    
    <td>
      pretražuje *.c and *.h zbog &#8222;search string&#8220; u teku?em i nižim<br /> direktorijumima
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      find -type f | xargs grep -E &#8222;search string&#8220;
    </td>
    
    <td>
      pretražuje sve regularne fajlove zbog &#8222;search string&#8220; u<br /> teku?em i nižim direktorijumima
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      find -type f -maxdepth 1 | xargs grep -E<br /> &#8222;search string&#8220;
    </td>
    
    <td>
      pretražuje sve regularne fajlove zbog &#8222;search string&#8220; u ovom<br /> direktorijumu
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      locate -r &#8216;file[^/]*.txt&#8217;
    </td>
    
    <td>
      pretražuje keširani indeks zbog imena fajlova.
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>Kalendar</b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      cal -3
    </td>
    
    <td>
      prikazuje kalendar
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      date &#8211;date=&#8217;25 Dec&#8217; +%A
    </td>
    
    <td>
      prikazuje na koji dan pada boži? u teku?oj godini
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      date &#8211;date &#8216;1970-01-01 UTC 130204800 seconds&#8217;
    </td>
    
    <td>
      konvertuje proj sekundi od zadatog datuma
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      TZ=&#8220;Europe/Belgrade&#8220; date
    </td>
    
    <td>
      Koje je vreme u Beogradu (koristi tzselect da bi dobio TZ )
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>Umrežavanje</b> (Note ifconfig, route,<br /> mii-tool, nslookup commands are obsolete)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ip link show
    </td>
    
    <td>
      prikazuje mrežne interfejse
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ethtool interface
    </td>
    
    <td>
      prikazuje status mrežnih interfejsa
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ip link set dev eth0 name wan
    </td>
    
    <td>
      menja ime eth0 u wan
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ip addr add 1.2.3.4/24 brd + dev eth0
    </td>
    
    <td>
      dodaje ip i masku(255.255.255.0)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ip link set dev interface up
    </td>
    
    <td>
      startuje interfejs (ili ga zaustavlja)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      ip route add default via 1.2.3.254
    </td>
    
    <td>
      postavlja default gateway na 1.2.3.254
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      host name
    </td>
    
    <td>
      pretražuje ip adresu za ime ili obrnuto
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      netstat -lp &#8211;inet
    </td>
    
    <td>
      prikazuje internet servise na sistemu
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      netstat -p &#8211;inet
    </td>
    
    <td>
      prikazuje listu aktivnih konekcija na/sa sistema
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <span style="font-weight: bold;">Matematika</span>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      echo &#8222;(321-123)/123&#8220; | bc -l
    </td>
    
    <td>
      brzo ra?unanje
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      echo &#8222;print (10E3-123)/123&#8220; | python
    </td>
    
    <td>
      ra?unanje i prikaz preko<br /> pythona
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      echo &#8222;obase=16;ibase=10;123&#8220; | bc
    </td>
    
    <td>
      osnovne konverzije (decimal u hex)
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>RPM</b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -ivh packages(s).rpm
    </td>
    
    <td>
      instalira rpm fajl(ove)
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -Uvh packages(s).rpm
    </td>
    
    <td>
      upgrade-uje sistem sa rpms-ovima
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -e package
    </td>
    
    <td>
      uklanja paket
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q package
    </td>
    
    <td>
      prikazuje verziju instaliranog paketa
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q -i package
    </td>
    
    <td>
      sprikazuje opis paketa
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q -f /path/file
    </td>
    
    <td>
      prikazuje kojem paketu dati fajl pripada
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q -l package
    </td>
    
    <td>
      prikazuje gde su fajlovi instalirani
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q -l -p package.rpm
    </td>
    
    <td>
      prikazuje gde ?e fajlovi biti instalirani
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q &#8211;requires package
    </td>
    
    <td>
      prikazuje fajlove/pakete koji su paketu potrebni
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q &#8211;whatrequires package
    </td>
    
    <td>
      prikazuje pakete koji zahtevaju dati paket
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      rpm -q -a &#8211;queryformat<br /> &#8222;%10{SIZE} %{NAME}<br /> &#8220; | sort -k1,1n
    </td>
    
    <td>
      prikazuje pakete po veli?ini
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <b>editovanje teksta</b>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      sed &#8216;s/string1/string2/g&#8217;
    </td>
    
    <td>
      menja string1 sa string2
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      sed &#8216;/ *#/d; /^ *$/d&#8217;
    </td>
    
    <td>
      uklanja komentare i prazne linije
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      sed &#8216;s/[ ]*$//&#8217;
    </td>
    
    <td>
      uklanja trailing prostore iz linija
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      tr -d &#8216;<br /> &#8216;
    </td>
    
    <td>
      konvertuje dos kraj linije u unix kraj linije
    </td>
  </tr>
  
  <tr class="pbtitle">
    <td colspan="2">
      <span style="font-weight: bold;">programi</span>
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      <a
href="http://www.iol.ie/%7Epadraiga/lkdb/mc.html">mc</a>
    </td>
    
    <td>
      veoma mo?an fajl menadžer
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      <a
href="http://www.iol.ie/%7Epadraiga/lkdb/screen.html">screen</a>
    </td>
    
    <td>
      virtuelni terminali sa detach opcijom
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      lynx
    </td>
    
    <td>
      konzolni web pretraživa?
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      gnuplot
    </td>
    
    <td>
      interactive/scriptable iscrtavanje
    </td>
  </tr>
  
  <tr>
    <td nowrap="nowrap">
      octave
    </td>
    
    <td>
      okruženje sli?no matlab-u
    </td>
  </tr>
</table>

Tipovi skupljeni sa newsforge.com

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=490)