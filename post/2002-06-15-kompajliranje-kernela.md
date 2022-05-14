---
author: tomaja
date: "2002-06-15T05:35:16Z"
excerpt: |
  <p>Kako je sve više novih korisnika Linux OS, mislim da treba da se i oni upoznaju sa<br />
  mogućnošću izmena u osnovi sistema, tj. u kernelu pogotovo ako neko želi da recimo<br />
  omogući podršku za svoju zvučnu ili TV karticu, podesi mrežne opcije, prilagodi sistem<br />
  novim komponentama, omogući pristup NTFS particijama, ... Ovaj tekst opisuje postupak<br />
  kompajliranja kernela pod u Mandrake<a> </a><a>L</a>inux-om ali je postupak sličan onom u drugim distribucijama.<br />
  Tekst se sastoji od 5 delova a to su:<br />
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=22#config">Podešavanje kernela</a>, <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=22#inst">Kompajliranje i instalacija kernela</a>, <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=22#conf">Podešavanje sistema</a><br />
  (nakon instalacije kernela), <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=22#lilo">Podešavanje lilo startera</a> (boot loader-a),<br />
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=22#grub">Podešavanje GRUB startera</a>.<br />
  <br />
  Sva dodatna pitanja možete postaviti na <a href="http://www.linuxo.org/forum">forumu</a>
guid: https://forum.linuxo.org/2002/06/15/kompajliranje-kernela/
id: 188
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Kompajliranje kernela
url: /kompajliranje-kernela/
---
Kako je sve više novih korisnika Linux OS, mislim da treba da se i oni upoznaju sa  
mogućnošću izmena u osnovi sistema, tj. u kernelu pogotovo ako neko želi da recimo  
omogući podršku za svoju zvučnu ili TV karticu, podesi mrežne opcije, prilagodi sistem  
novim komponentama, omogući pristup NTFS particijama, &#8230; Ovaj tekst opisuje postupak  
kompajliranja kernela pod u Mandrake <a></a><a>L</a>inux-om ali je postupak sličan onom u drugim distribucijama.  
Tekst se sastoji od 5 delova a to su:  
[Podešavanje kernela](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=22#config), [Kompajliranje i instalacija kernela](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=22#inst), [Podešavanje sistema](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=22#conf)  
(nakon instalacije kernela), [Podešavanje lilo startera](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=22#lilo) (boot loader-a),  
[Podešavanje GRUB startera](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=22#grub).

Sva dodatna pitanja možete postaviti na [forumu](http://www.linuxo.org/forum) <!--break-->

### <a id="config" name="config">Podešavanje kernela</a>

Ukoliko želite da kompajlirate orginalni source sa [kernel.org](https://linuxo.org/?taxonomy=freetags&term=kernel), onda je bolje da instalacioni source kernela koji se nalazi u '/usr/src/linux' ne dirate već da novi kernel kompajlirate i instalirate iz svog home direktorijuma (jer su 'root' ovlašćenja potrebna samo za instalaciju kernela).

Pokrenite `tar <i>xfzC [kernel-source].tar.gz</i>` u konzoli(terminalu). Ova naredba će otpakovati source u 'linux' direktorijum.

Ukoliko ste već kompajlirali kernel iz ovih source-ova, prvo pokrenite _`make mrproper`_ da bi uklonili stare postavke . Zapamtite da 'mrproper' briše i prethodni '.config' fajl, pa ako vam je bitan bilo bi dobro da ga negde pre toga prekopirate.

Podešavanje kernela se odvija u novom 'linux' direktorijumu. U osnovi, postoje dva načina da to uradite, kraći koji se sastoji od izmene '.config' fajla i duži koji se sastoji od upotrebe jednog od ponuđenih konfiguracionih alata. Moram reći da je za početnike i nove u linux svetu ova druga mnogo bolje rešenje. (U Mandrake linux 8.2 to možete uraditi iz KDE Kontrolnog centra. Startujte ga a zatim otiđite na Sistem pa na Podešavanje kernela ili ako koristite engl. lokalizaciju System pa Kernel Configuration).

Pri pristup je ustvari editovanje iliti izmena kopije default kernel konfiguracionog fajla '/usr/src/linux-[&#8230;]/arch/[i386|ppc]/defconfig'. On je posebno uređen za situacije kada treba samo da izmenite nekoliko opcija i kada znate šta radite.  
Kopirajte 'defconfig' fajl u vašem tekućem direktorijumu i promenite mu ime u '.config'. Ukoliko već imate '.config' fajl od prethodnog kompajlirnja, možete da koristite i taj, mada nije loše uraditi i backup tog fajla.  
U samom fajlu pronaći ćete tri tipa unosa, koji odgovaraju za tri stanja koja su moguća (ne moraju uvek da budu sva tri !): 'build into the kernel', 'build as a kernel module' i 'not included':

  * `[OPTION]=y`
  * `[OPTION]=m`
  * `# [OPTION] is not set`

Dakle, da bi promenili opciju sa 'build as a module' na 'build into the kernel' morate da izmenite liniju

`[OPTION]=m`

u

`[OPTION]=y`

Objašnjenja za većinu opcija možete pronaći u 'linux/Documentation/Configure.help'.  
Izmenite sve što želite, zatim sačuvajte izmene a onda pređite na sledeće poglavlje ovog teksta.

Drugi pristup koristi jedan od ponuđenih kernelovih konfiguracionih alata. Kako ste u 'linux' direktorijumu, ili pokrenite _`make config`_ (konzolni alat), ili _`make menuconfig`_ (takođe konzolni ali sa boljim izgledom i funkcionalnošću menija) ili `make xconfig` (ako ste navikli na prozore, dobar X meni, ali malo zahtevniji po pitanju memorije).

Par saveta za dobro konfigurisanje:

  * Pročitajte dostupnu i online dokumentaciju.
  * Budite pažljivi sa eksperimentalnim opcijama. Samo ime govori za sebe.
  * Kreirajte module. Manji kernel je bolji, ali budite pažljivi da ne izbacite nešto što vam je potrebno pri startanju sistema Online HOWTO vam može pomoći u vezi sa tim: 
    [MdkReference, 14](http://www.linux-mandrake.com/en/doc/72/en/ref.html/compiling.html)  
    [The Linux Kernel HOWTO](http://www.ibiblio.org/mdw/HOWTO/Kernel-HOWTO.html)  
    [KernelTrap](http://www.kerneltrap.org/)  
    [Jeffrey Borg: Compiling a New Kernel](http://jgo.local.net/LinuxGuide/linux-kernel.html)

  * Ukoliko niste sigurni, nemojte menjati već podešene opcije. Zavisnosti su ponekada veoma tanane i teško se podešavaju. Bolje je da je kernel za koji kilobajt i veći nego kernel koji ne radi dobro.

Ako imate dodatnih pitanja možete ih postaviti na našem [forumu](http://www.linuxo.org/forum).

<p class="smallright">
  <a href="http://www.mandrakeuser.org/docs/install/kupgrade3.html#top">na početak</a>
</p>

### <a id="inst" name="inst">Kompajliranje i instalacija kernela</a>

Sada sačuvajte izmene u novoj konfiguraciji. Izmenite i fajl 'Makefile' u nekom od editora i popunite vrednost za 'EXTRAVERSION' ili vam se može desiti da dobijete dva različita kernela sa istim imenom.

Pokrenite

_`make dep && make clean && make bzImage && make modules`_

Vreme kompajliranja zavisi od sistema (količine memorije, procesora&#8230;) i konfiguracije kernela. Na većini mašina, kompajliranje traje između 15 i 45 minuta (PREPORUKA: kada podesite sve izmene, zatvorite X-ove i kompajlirajte kernel u konzoli).  
Ako se kompajliranje završi uspešno, postanite root pomoću komande _`su`_ i instalirajte kernel i njegove module:

<p class="rev" title="Reversed command order on Oct. 15, 2001">
  <i><code>make modules_install && make install</code></i>
</p>

<p class="rev" title="Added glob about installkernel script, some changes further down to reflect this on Oct. 15, 2001">
  Poslednja komanda će pozvati '/sbin/installkernel' skriptu preko 'linux/arch/i386/boot/install.sh' &#8211; što će opet pokrenuti skripte u '/usr/share/loader' za:
</p>

  1. instaliranje kernela u '/boot/vmlinuz-[Version]',
  2. kreiranje initrd image u '/boot' ukoliko je potrebno,
  3. i dodati unose za novi kernel u '/etc/lilo.conf', '/boot/grub/menu.lst' ili '/etc/yaboot.conf' (na PPC mašinama).

Ako imate dodatnih pitanja možete ih postaviti na našem [forumu](http://www.linuxo.org/forum).

<p class="smallright">
  <a href="http://www.mandrakeuser.org/docs/install/kupgrade3.html#top">na po?etak</a>
</p>

### <a id="conf" name="conf">Podešavanje sistema </a>

Ukoliko je sve prošlo kako treba, trebalo bi da sada imate dva nova fajla u '/boot': 'System.map-[new version]' i 'vmlinuz-[new version]'.  
Proverite da li su fajlovi 'System.map', 'vmlinuz' i (u starijim Mandrake verzijama) 'modules.info' u '/boot' diremtorijumu. Ovi 'fajlovi' su ustavari samo linkovi. Dve stvari možete da uradite:

  1. Ostavite ih takve kakvi su jer bi Mandrake-ov init script treba da stavri postavi na pravi način, tj. da izmeni ove linkove za kernel koji startujete.
  2. Izbrišite ih i izmenite konfiguracioni fajl vašeg startera (npr. lilo) da koristi tačno određenu verziju kernela.

Ukoliko su vam potrebni SCSI uređaju pri startanju sistema (npr. SCSI hard disk) a imate iskompajliranu podršku za SCSI kao modul, 'installkernel' skripta bi trebala da kreira novi initrd image u '/boot' direktorijumu kao i da doda potrebne linije u konf. fajl vašeg startera.  
Ukoliko radije želite da sami kreirate ovaj image, to možete uraditi pomoću naredbe _`mkinitrd /boot/[name of image] [new kernel version]`_. Možete izabrati bilo koje ime za image, sve dok se ono razlikuje od imena već postojećeg fajla. Naravno, kada ga kreirate morate da izmenite i kofig. fajlove LiLo ili GNU GRUB startera da bi znali za ovaj image.  
Ako imate dodatnih pitanja možete ih postaviti na našem [forumu](http://www.linuxo.org/forum).

<p class="smallright">
  <a href="http://www.mandrakeuser.org/docs/install/kupgrade3.html#top">na početak</a>
</p>

### <a id="lilo" name="lilo">Podešavanje LiLo</a>

'installkernel' skripta će sama detektovati vaš starter (boot loader) i podestiti njegov konfiguracioni fajl. Ukoiko ste zainteresovani kako to sami da uradite, evo kako:

Podešavanje LiLo startera se završava sa izmenom '/etc/lilo.conf' fajla, bilo da ga editujete u editoru ili pomoću 'DrakBoot' alata iz 'Mandrake Kontrolnog Centra' (iliti 'DrakConf'). Prvo izmenite postavku starog kernela:

  * promenite _`image=/boot/vmlinuz`_ u puno ime kernela (starog) kernel image-a. Ovo je potrebno samo onda ako ste izbrisali 'vmlinuz' link u '/boot'.

  * promenite _`label=linux`_ u nešto tipa _`label``=starilinx`_. Ovo će vam omogućiti da pokrenete i stari kernel ukucavanjem _`starilinx`_ u boot promptu.

Zatim dodajte linije za novi kernel na kraju fajla:

<pre><i>image=/boot/vmlinuz-[new kernel version]
label=linux
root=/dev/[root partition]
initrd=/boot/[initrd image]
readonly</i>
</pre>

'root partition' je ista kao i za stari kernel. Oznaka _`label=linux`_ će po default pokrenuti novi kernel.  
`initrd="/boot/[initrd image]"` će vam biti potreban samo ako se vaša instalacija GNU/Linux sistema system nalazi na SCSI disku i ako je SCSI podrška uključena kao modul. Ako je to slučaj **apsolutno** je **neophodno** da kreirate novi 'initrd' image sa

_`mkinitrd /boot/[initrd image] [new kernel version]`_

Ime novog ne sme da se poklapa sa imenom starog initrd image-a. Zatim uputite `initrd` liniju novog kernela u '/etc/lilo.conf' na ovaj novi image.

Pokrenite _`l ilo`_. **Ovo morate da uradite!** Ukoliko ne dobijete poruku o grešci, možete da restartujete mašinu.  
Ako imate dodatnih pitanja možete ih postaviti na našem [forumu](http://www.linuxo.org/forum).

<p class="smallright">
  <a href="http://www.mandrakeuser.org/docs/install/kupgrade3.html#top">na početak</a>
</p>

### <a id="grub" name="grub">Podešavanje GNU GRUB</a>

Ukoliko koristite GNU GRUB kao starter (boot loader), dodajte ove linije u '/boot/menu.lst' (ili koristite 'DrakBoot' u 'Mandrake Kontrolnom Centru'):

<pre><i>title [menu entry]
kernel (hd[x],[y])/boot/[kernel] root=/dev/[z]</i>
</pre>

`title` određuje kako će se zvati vaš novi kernel na meniju pri podizanju sistema. 'x' i 'y' govore GNU GRUB -u gde je '/boot', koji sadrži kernel image, lociran: 'x' označava broj hard diska (u zavisnosti da li je u pitanju IDE ili SCSI disk) počevši od '0', 'y' je broj particije, takođe počinje od '0'. Pa tako, `(hd0,0)` govori GNU GRUB-u: "potraži prvu particiju na prvom hard disku u boot lancu". Kada jednom pronađe particiju, GNU GRUB mora da zna o lokaciju i ime kernela, npr. _`/boot/mynewkernel`_.  
Kako 'init', inicijalni GNU/Linux boot proces, takođe mora da zna na kojoj se particiji nalazi kernel, onda morate da mu kažete sa _`root=/dev/hda1`_. Ukoliko ste kreirali ramdisk image, dodajte _`initrd /boot/[name of initrd image]`_ kao i bilo koji drugi kernel parametar(e) koji su vam potrebni.  
Zapamtite da ukoliko se '/boot' nalazi na prvoj logičkoj particiji na hardu (/dev/hda5), linija mora da bude `(hd0,4)`, u zavisnosti od broja primarnih particija na disku.

<p class="smallright">
  Izmenom broja u <code>default</code> polju (ili kreiranjem polja u 'DrakBoot'), možete reći GNU GRUB-u da startuje kernel po default-u. Zapamtite da GNU GRUB pošinje da broji od '0', pa da bi pokrenulinovi kernel treba da promenite, u '/boot/grub/menu.lst', broj u '1'.<br /> Nakon svega, sačuvajte izmene i restartujte mašinu.
</p>

<p class="smallright">
  Ako imate dodatnih pitanja možete ih postaviti na našem <a href="http://www.linuxo.org/forum">forumu</a>.<br /> &nbsp;
</p>

<p class="smallright">
  <a href="http://www.mandrakeuser.org/docs/install/kupgrade3.html#top">na početak</a>
</p>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=188)