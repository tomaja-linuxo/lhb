---
author: tomaja
date: "2002-04-27T15:26:31Z"
excerpt: |
  <p>Nekoliko paketa je ažurirano sa ispravljenim bagovima i greškama Tu su: jmcce, nss_ldap, <b>Xtart</b>, <b>draktools</b> kao i <b>cdrecord/xcdroast</b>,<br />
  pax, eroaster, <b>mutt</b>, ghostscript, printer drivers, ...<br />
  Detaljnija objašnjenja možete naći dalje u tekstu.<br />
  Za ažuriranje možete koristiti <i>MandrakeUpdate</i> opciju ili možete i ručno da instalirate pakete<br />
  sa linka <a href="http://www.mandrakesecure.net/en/ftp.php">http://www.mandrakesecure.net/en/ftp.php</a>
guid: https://forum.linuxo.org/2002/04/27/mandrake-linux-8-2-paketi-za-azuriranje-update/
id: 174
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mandrake Linux 8.2 paketi za ažuriranje (update)
url: /mandrake-linux-8-2-paketi-za-azuriranje-update/
---
Nekoliko paketa je ažurirano sa ispravljenim bagovima i greškama Tu su: jmcce, nss_ldap, **Xtart**, **draktools** kao i **cdrecord/xcdroast**,  
pax, eroaster, **mutt**, ghostscript, printer drivers, &#8230;  
Detaljnija objašnjenja možete naći dalje u tekstu.  
Za ažuriranje možete koristiti _MandrakeUpdate_ opciju ili možete i ručno da instalirate pakete  
sa linka <http://www.mandrakesecure.net/en/ftp.php><!--break-->



Nekoliko paketa je ispravljeno od bagova i grešaka a koji se nalaze u Mandrake Linux 8.2 . To su:  
**jmcce**: jmcce paket je greškom izbačen iz ML 8.2 Download verzije.

**e2fsprogs**: Nova verzija ispravlja greške u e2fsck kodu, a ismounted kod proverava swap uređaj.

**nss_ldap**: Pretdhodni paket nije prikazivao listu suplementarnih grupa u kojima je korisnik član. Ovaj novi paket sada ima  
ugraÄ&lsquo;enu podršku za ids-uid RFC2307bis.

**Xtart**: Objavljeni Xtart paket koristi stari metod zainiciranje X -ova koji ne obežbeđuje kompletno okruženje za consolehelper; kao rezultat bilo koja aplikacija, kao što je **Mandrake Kontrolni Centar**, koja zateva consolehelper za pristup root ovlašćenjima ne može da se startuje.

**drakxtools**: Postojali su rayni problemi sa printerdrake i HP Multi-funkcionalnim uređajima. Ovo izdanje ispravlja sve greške

**Ažurirani (Updated) paketi:**

Treba da ažurirate sledeće pakete:

**Mandrake Linux 8.2:**

<pre>fdcfb20ee5bb43906ce21d03360183c7  8.2/RPMS/Xtart-1.1-2.1mdk.i586.rpm
      0041a2a4a380a043f6f78ab78ff7447b  8.2/RPMS/aspell-da-1.4.21-1mdk.i586.rpm
      a71bfbd2f905dda53f6acbeaaa857f99  8.2/RPMS/drakxtools-1.1.7-98.1mdk.i586.rpm
      115ee432de480e0bc2f301e8b14ee626  8.2/RPMS/drakxtools-http-1.1.7-98.1mdk.i586.rpm
      22dbee0ad124df72f04807ee0708347f  8.2/RPMS/drakxtools-newt-1.1.7-98.1mdk.i586.rpm
      253780af866608d2d126b99d16989c38  8.2/RPMS/e2fsprogs-1.27-1.1mdk.i586.rpm
      b1b318e282d670037d3ff175fdf0eb7f  8.2/RPMS/jmcce-1.3-10mdk.i586.rpm
      ce2afa09dbdef781b8da227742fc6624  8.2/RPMS/kde-i18n-da-2.2.2-2mdk.noarch.rpm
      14e20cc1ac15b827fb7e7d72fb79af62  8.2/RPMS/kde-i18n-sl-2.2.2-1mdk.noarch.rpm
      de26d383355f040bc8b1ade4db7a3005  8.2/RPMS/libext2fs2-1.27-1.1mdk.i586.rpm
      0459320945a795c638ee3f484b89e594  8.2/RPMS/libext2fs2-devel-1.27-1.1mdk.i586.rpm
      6dc393325ea9b982e24761cbae760db4  8.2/RPMS/nss_ldap-173-2.1mdk.i586.rpm
      d79cb75acecc91c40e81a61173e857ad  8.2/SRPMS/Xtart-1.1-2.1mdk.src.rpm
      798414049f4475c38a01fb3303bd5bae  8.2/SRPMS/aspell-da-1.4.21-1mdk.src.rpm
      50636c8316f929c3da07fcb8a8bf1f89  8.2/SRPMS/drakxtools-1.1.7-98.1mdk.src.rpm
      7aa20199787545344754372ce5d3a26c  8.2/SRPMS/e2fsprogs-1.27-1.1mdk.src.rpm
      bb9a2dd24675bd424dfa7b85e5fa70e3  8.2/SRPMS/jmcce-1.3-10mdk.src.rpm
      ed3e7148019726e5e02f97e5d3fbee25  8.2/SRPMS/kde-i18n-da-2.2.2-2mdk.src.rpm
      1c87f5c0b40450821b8c6378b3ff7469  8.2/SRPMS/kde-i18n-sl-2.2.2-1mdk.src.rpm
      8f5ca4f81321e35ce3e7799aa3de44fe  8.2/SRPMS/nss_ldap-173-2.1mdk.src.rpm
      </pre>

**Ažuriranje:**

Za automatsko ažuriranje koristite **MandrakeUpdate**.

Ukoliko želite da to obavite ručno, skinite ažurirane pakete sa jednog od [FTP server mirora](http://www.mandrakesecure.net/en/ftp.php) i ažurirajte ih pomoću "rpm -Fvh *.rpm" komade u konzoli.

**Verifikacija:**

Pre nego instaliratenove pakete nije loše proverite njihov integritet. To možete uraditi pomoću ove komade:

<pre>rpm --checksig package.rpm
      </pre>

Možete skinuti [GPG javni ključ?](https://www.mandrakesecure.net/RPM-GPG-KEYS) Mandrake Linux Security Tima da bi proverili GPG potpis svakog RPM paketa.

Ukoliko koristite MandrakeUpdate, verifikacija md5 checksum i GPG potpisa se izvodi automatski.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=174)