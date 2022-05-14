---
author: tomaja
date: "2011-02-06T06:34:20Z"
excerpt: |
  Nakon 24 meseca stalnog rada na na novoj verziji, Projekat Debian sa ponosom predstavlja novu stabilnu verziju: <strong>Debian GNU/Linux 6.0</strong> (kodno ime “<strong>Squeeze</strong>”). Debian 6.0 je slobodan operativni sistem koji po prvi put dolazi u dve varijante. Pored uobičajenog Debian GNU/Linux-a, sada imamo i <strong>Debian GNU/kFreeBSD</strong> koji se u ovoj verziji predstavlja kao “technology preview”.

  Debian 6.0 uključuje KDE Plasma Desktop i prateće aplikacije, zatim GNOME, Xfce, i LXDE desktop okruženja kao i sve vrste serverskih aplikacija.
guid: https://forum.linuxo.org/2011/02/06/debian-6-squeeze/
id: 2485
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Debian 6 &#8222;Squeeze&#8220;
url: /debian-6-squeeze/
---
Nakon 24 meseca stalnog rada na na novoj verziji, Projekat Debian sa ponosom predstavlja novu stabilnu verziju: **Debian GNU/Linux 6.0** (kodno ime “**Squeeze**”). Debian 6.0 je slobodan operativni sistem koji po prvi put dolazi u dve varijante. Pored uobičajenog Debian GNU/Linux-a, sada imamo i **Debian GNU/kFreeBSD** koji se u ovoj verziji predstavlja kao “technology preview”.

Debian 6.0 uključuje KDE Plasma Desktop i prateće aplikacije, zatim GNOME, Xfce, i LXDE desktop okruženja kao i sve vrste serverskih aplikacija. On takođe poseduje kompatibilnost sa FHS v2.3 i softver razvijen sa 3.2 verziju LSB-a.

Debian se može pokrenuti na raznovrsnim računarima, počevši od palmtop-ova i ručnih uređaja pa sve do super račuara, narvno, i na svemu što se nalazi između ovih ekstrema. Ukupno 9 hardverskih arhitektura je podržano od strane Debian GNU/Linux-a: 32-bit PC / Intel IA-32 (i386), 64-bit PC / Intel EM64T / x86-64 (amd64), Motorola/IBM PowerPC (powerpc), Sun/Oracle SPARC (sparc), MIPS (mips (big-endian) i mipsel (little-endian)), Intel Itanium (ia64), IBM S/390 (s390), and ARM EABI (armel).

Debian 6.0 “Squeeze” predstavlja tehnička predizdanja dva nova porta sa FreeBSD kernelima upakovanim sa Debian/GNU korisničkim okruženjem: Debian GNU/kFreeBSD za 32-bit PC (kfreebsd-i386) i 64-bit PC (kfreebsd-amd64). Ovi portovi su prvi ikada uključeni u Debian izdanje, a da nisu bazirani na Linux kernelu. Podrška za uobičajeni serverski softver je jaka, i kombinuje se sa postojećim mogućnostima Debiana baziranog na Linux-u sa jedistvenim osobinama iz BSD sveta. Ipak, ovo izdanje ima ograničenja: na primer, neka napredne desktop opcije nisu još implamentirane.

Sa druge strane, osnovna Linux verzija Debiana je sada sa [kompletno slobodnim Linux kernelom](http://linuxo.org/content/novi-gnu-debian-squeeze-kernel-isključivo-sa-oss-softverom), koji više ne sadrži problematične firmware fajlove. Oni su odvojeni u posebne softverske pakete koji su premešteni u non-free repozitorijume, koji nisu odmah dostupni, po default-u. Na ovaj način Debianovi korisnici imaju mogućnost korišćenja potpuno slobodnog operativnog sistema, sa mogućnošću upotrebe non-free firmware fajlova , ukoliko su im neophodni (a verovatno jesu). Firmware fajlovi potrebni prilikom instalacije se mogu učitati kroz sam program za instalaciju; posebni CD image-i i tarball fajlovi za USB instalaciju su takođe dostupni. 

<p class="info">
  Više informacija se može pronaći na <a href="http://wiki.debian.org/Firmware">Debian Firmware wiki stranici</a>.
</p>

Dalje, Debian 6.0 predstavlja sistem za pokretanje sistem baziran na međuzavisnostima, čineći pokretanje sistema bržim i otpornijim zahvaljujući paralelnom pokretanju boot skripti i ispravnom praćenju međuzavinsosti između njih. Razne druge izmene čine Debian više pogodnim za manje forme računara, poput notebook-ova, poput uključenja KDE Plasma Netbook shell-a.

Ovo izdanje uključuje brojne ažurirane softverske pakete, kao što su:

<ul class="check-list">
  <li>
    KDE Plasma Radni prostori i KDE Aplikacije 4.4.5
  </li>
  <li>
    ažurirano GNOME desktop okruženje 2.30
  </li>
  <li>
    Xfce 4.6 desktop okruženje
  </li>
  <li>
    LXDE 0.5.0
  </li>
  <li>
    X.Org 7.5
  </li>
  <li>
    OpenOffice.org 3.2.1
  </li>
  <li>
    GIMP 2.6.11
  </li>
  <li>
    Iceweasel 3.5.16 (nebrendiranu verziju Mozilla Firefox-a)
  </li>
  <li>
    Icedove 3.0.11 (nebrendiranu verziju Mozilla Thunderbird-a)
  </li>
  <li>
    PostgreSQL 8.4.6
  </li>
  <li>
    MySQL 5.1.49
  </li>
  <li>
    GNU kolekciju kompajlera 4.4.5
  </li>
  <li>
    Linux (kernel) 2.6.32
  </li>
  <li>
    Apache 2.2.16
  </li>
  <li>
    Samba 3.5.6
  </li>
  <li>
    Python 2.6.6, 2.5.5 i 3.1.3
  </li>
  <li>
    Perl 5.10.1
  </li>
  <li>
    PHP 5.3.3
  </li>
  <li>
    Asterisk 1.6.2.9
  </li>
  <li>
    Nagios 3.2.3
  </li>
  <li>
    Xen Hypervisor 4.0.1 (podrška za dom0 kao i domU)
  </li>
  <li>
    OpenJDK 6b18
  </li>
  <li>
    Tomcat 6.0.18 i
  </li>
  <li>
    više od 29,000 drugih, spremnih za korišćenje, softverskih paketa, kreiranih iz gotovo 15,000 izvornih paketa.
  </li>
</ul>

Debian 6.0 uključuje preko 10,000 novih paketa poput internet pretraživača **Chromium**, rešenja za monitoring **Icinga**, GUI aplikaciju za rad sa softverskim paketima **Software Center**, mrežnog menadžera **wicd**, Linux container alata **lxc** i cluster framework-a **Corosync**. 

Sa ovim širokim izborom softvera, Debian još jednom ostaje čvrsto pri svom cilju a to je da bude univerzalini operativni sistem. Pogodan je za mnoge različite namene: od desktop sistema do netbook računara; od razvojnih servera do cluster sistema; od servera za baze podataka do servera za smeštanje podataka. U isto vreme, napori na dodatnom osiguranju kvaliteta, poput **automatske instalacije i upgrade testova za sve pakete** u Debianovoj arhivi osigurava da će Debian 6.0 ispuniti visoka očekivanja koji korisnici imaju od stabilnog Debian izdanja. A ono je veoma stabilno i strogo istestirano. 

Počevši od Debiana 6.0, “**Custom Debian Distributions**” su preimenovane u “**Debian Pure Blends**”. Njihov broj je uvećan jer Debian 6.0 dodaje **Debian Accessibility, DebiChem, Debian EzGo, Debian GIS** i **Debian Multimedi**a već postojećim **Debian Edu, Debian Med** i **Debian Science** “pure blends”. Puni sadržaj svih varijanti se može pretražiti, uključujući i prateće pakete koje korisnici mogu nominovati za uključivanje u narednu verziju.

Debian se može instalirati sa različitih instalacionih medija poput Blu-ray diskova, DVDa, CDa i USB memorija ili preko mreže. **GNOME predstavlja default desktop** okruženje i nalazi se na prvom CDu. Druga desktop okruženja— KDE Plasma Desktop i Aplikacije, Xfce, ili LXDE — se mogu instalirati preko alternativnih CD image fajlova. Željeno desktop okruženje se takođe može izabrati iz startnog menija sa CDa/DVDa. Ponovo dostupno sa Debianom 6.0 su multi-architecture CD-ovi i DVD-ovi koji podržavaju instalaciju na više hardverskih arhitektura sa jednog diska. Kreiranje butabilne USB instalacije je značajno pojednostavljeno; 

<p class="info">
  Pogledajte <a href="http://debian.org/releases/squeeze/installmanual">Vodič za instalaciju</a> za više detalja.
</p>

Kao dodatak standardnim instalacionim medijima, Debian GNU/Linux se može direktno koristiti bez prethodne instalacije. Pesebni image fajlovi, poznatiji kao live image fajlovi, su dostupni za CD, USB memorije i netboot setup-ove. Na početku, oni su obezbeđeni samoza amd64 i i386 arhitekture. Takođe je moguće koristiti ove live image fajlove za instalaciju Debian GNU/Linux-a.

<div class="info-box">
  Instalacioni proces za Debian GNU/Linux 6.0 je unapređen na razne načine, uključujući laki izbor jezika i rasporeda tastature, particionisanje logičkih particija, RAID i kriptovanih sistema. <strong>Dodana je podrška za ext4 i Btrfs fajl sisteme i &#8211; za kFreeBSD arhitekturu — Zettabyte fajl sistem (ZFS)</strong>. Instalacioni sistem za Debian GNU/Linux je sada dostupan na 70 različitih jezika.
</div>

<p class="download">
  Debianovi instalacioni image fajlovi se mogu preuzeti odmah preko <a href="http://debian.org/CD/torrent-cd/">BitTorrent</a>-a (preporučeni metod), <a href="http://debian.org/CD/jigdo-cd/#which">jigdo</a> ili <a href="http://debian.org/CD/http-ftp/">HTTP</a>-a; pogledajte D<a href="http://debian.org/CD/">ebian na CD</a>-u za više informacija. Uskoro će biti dostupan i na fizičkim DVD, CD-ROM i Blu-ray diskovima.
</p>

Ažuriranje na Debian GNU/Linux 6.0 na prethodne verzije, Debian GNU/Linux 5.0 (kodno ime “Lenny”), se obavlja automatski preko **apt-get** package alata i većina poešavanja, a do određenog stepena i preko _aptitude_ alata za upravljanje paketima. Kao i uvek, Debian GNU/Linux sistemi se mogu ažurirati bez problema, na licu mesta, bez restartovanja sistema, ali se svakako preporučuje da pročitate [Napomene o izdanju](http://debian.org/releases/squeeze/releasenotes) kao i [Vodič za instalaciju](http://debian.org/releases/squeeze/installmanual) radi eventualnih uočenih problema, kao i zbog detaljnih upustava za instalaciju i ažuriranje sistema. Napomene o izdanju će biti i na dalje unapređivanje i prevođene na dodatne jezike u nedeljama koje dolaze.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2485)