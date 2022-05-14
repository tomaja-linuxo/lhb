---
author: tomaja
date: "2003-02-04T15:40:59Z"
excerpt: |
  MySQL programeri su ispravili DoS ranjivost u nedavno objavljenoj novoj verziji
  3.23.55.  Greška vezana za double free() pokazivaš u mysql_change_user()
  bi dozvolila specijalnom hakovanom mysql klijentu da sruši glavni  mysqld
  server. Ova ranjivost se može iskoristiti samo pri prvom prijavljivanju na
  validni korisni?i ra?un. Više o ovome možete pro?itati na <a
  href="http://www.mysql.com/doc/en/News-3.23.55.html">http://www.mysql.com/doc/en/News-3.23.55.html</a><br>
  Ranjivost u paketu vim koju je otkrio Georgi Guninski dozovoljava izvršenje
  bilo koje komande koriš?enjem libcall opcije. Patch koji rešava ovaj problem
  je prestavljen u verziji  vim 6.1 patchlevel 265. Detaljnije o ovom
  bagu možete pro?itati...
guid: https://forum.linuxo.org/2003/02/04/sigurnosne-ispravke-mysql-i-vim/
id: 286
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Sigurnosne ispravke &#8211; MySQL i vim
url: /sigurnosne-ispravke-mysql-i-vim/
---
MySQL programeri su ispravili DoS ranjivost u nedavno objavljenoj novoj verziji  
3.23.55. Greška vezana za double free() pokazivaš u mysql\_change\_user()  
bi dozvolila specijalnom hakovanom mysql klijentu da sruši glavni mysqld  
server. Ova ranjivost se može iskoristiti samo pri prvom prijavljivanju na  
validni korisni?i ra?un. Više o ovome možete pro?itati na <http://www.mysql.com/doc/en/News-3.23.55.html>  
Ranjivost u paketu vim koju je otkrio Georgi Guninski dozovoljava izvršenje  
bilo koje komande koriš?enjem libcall opcije. Patch koji rešava ovaj problem  
je prestavljen u verziji vim 6.1 patchlevel 265. Detaljnije o ovom  
bagu možete pro?itati&#8230;<!--break-->

  
na slede?im linkovima:

[http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-1377  
](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-1377) <http://www.guninski.com/vim1.html>

Pakete koje treba da update-ujete možete pogledati dole, a sve njih možete  
ažurirati uz pomo? programa **_MandrakeUpdate_** ili to možete uraditi  
i ru?no  
ako skinete pakete sa nekog od Mandrake mirora na <http://www.mandrakesecure.net/en/ftp.php>  
sa komandom &#8222;rpm -Fvh *.rpm&#8220;[  
](http://www.mandrakesecure.net/en/ftp.php) **  
MySQL**

Mandrake Linux 8.0/PPC:  
926ee5252994fe0a29524121103725d5 ppc/8.0/RPMS/MySQL-3.23.36-2.3mdk.ppc.rpm  
cdfa13b86f231bc8caf1ac14ba2b0db3 ppc/8.0/RPMS/MySQL-bench-3.23.36-2.3mdk.ppc.rpm  
27de6cbecb726095e345cc9866908520 ppc/8.0/RPMS/MySQL-client-3.23.36-2.3mdk.ppc.rpm  
263ff27104820e6413c0758627c6d283 ppc/8.0/RPMS/MySQL-devel-3.23.36-2.3mdk.ppc.rpm  
d74e18d7baf1d4b91cdc7fe6acdd7c43 ppc/8.0/RPMS/MySQL-shared-3.23.36-2.3mdk.ppc.rpm  
7a2aeac7740ecc34db7a794c6928fbcb ppc/8.0/SRPMS/MySQL-3.23.36-2.3mdk.src.rpm

Mandrake Linux 8.1:  
8c41c02e9154202ee24b4a6c7dd2d5d8 8.1/RPMS/MySQL-3.23.41-5.3mdk.i586.rpm  
efe74fb794a8ed7d0069f075b8ccc892 8.1/RPMS/MySQL-bench-3.23.41-5.3mdk.i586.rpm  
8027c12246c3c07137f7507ed3643177 8.1/RPMS/MySQL-client-3.23.41-5.3mdk.i586.rpm  
bae66fe96c1d1756cc562e932a11f323 8.1/RPMS/MySQL-devel-3.23.41-5.3mdk.i586.rpm  
c78af586765e35becd9af176b1253626 8.1/RPMS/MySQL-shared-3.23.41-5.3mdk.i586.rpm  
a8ba59c7fe788779b97af683db9b08b8 8.1/SRPMS/MySQL-3.23.41-5.3mdk.src.rpm

Mandrake Linux 8.1/IA64:  
e421b83e8476b59a64dae5d3ebb9c208 ia64/8.1/RPMS/MySQL-3.23.41-5.3mdk.ia64.rpm  
5d78fccdeb0876e5441287b5dc77cc53 ia64/8.1/RPMS/MySQL-bench-3.23.41-5.3mdk.ia64.rpm  
59d604e7dfb6ac945d2f0f05eaec0a57 ia64/8.1/RPMS/MySQL-client-3.23.41-5.3mdk.ia64.rpm  
1a59779bd26b2480b6913741dc8ee5b1 ia64/8.1/RPMS/MySQL-devel-3.23.41-5.3mdk.ia64.rpm  
3f4c5e8bef6445f8a1ce037a3b8213fa ia64/8.1/RPMS/MySQL-shared-3.23.41-5.3mdk.ia64.rpm  
a8ba59c7fe788779b97af683db9b08b8 ia64/8.1/SRPMS/MySQL-3.23.41-5.3mdk.src.rpm

Mandrake Linux 8.2:  
ec6dbc415b424a25c29909b984de64ce 8.2/RPMS/libmysql10-3.23.47-5.3mdk.i586.rpm  
c18da1c2d5cede8022a26b875c09b136 8.2/RPMS/libmysql10-devel-3.23.47-5.3mdk.i586.rpm  
3c283667d8175ff75b183254f8535ec6 8.2/RPMS/MySQL-3.23.47-5.3mdk.i586.rpm  
eab6e4de9ef2de755e67f796fafd4ccd 8.2/RPMS/MySQL-bench-3.23.47-5.3mdk.i586.rpm  
639e03c66d6fbd8059d33a481b6ff9d9 8.2/RPMS/MySQL-client-3.23.47-5.3mdk.i586.rpm  
394487ebcf063f310eb7719d637b26da 8.2/SRPMS/MySQL-3.23.47-5.3mdk.src.rpm

Mandrake Linux 8.2/PPC:  
dbbe494b3581f8fbdd663acf0ff321ff ppc/8.2/RPMS/libmysql10-3.23.47-5.3mdk.ppc.rpm  
39d434dfefe8dcb505ea13d001ab43f6 ppc/8.2/RPMS/libmysql10-devel-3.23.47-5.3mdk.ppc.rpm  
ef09c1c6cf68f09cf8798635a4f7aea6 ppc/8.2/RPMS/MySQL-3.23.47-5.3mdk.ppc.rpm  
f714db18658d1079354ca66a9c38c718 ppc/8.2/RPMS/MySQL-bench-3.23.47-5.3mdk.ppc.rpm  
3ea6463cb34fcfcb9fb12d86f1bcc2a8 ppc/8.2/RPMS/MySQL-client-3.23.47-5.3mdk.ppc.rpm  
394487ebcf063f310eb7719d637b26da ppc/8.2/SRPMS/MySQL-3.23.47-5.3mdk.src.rpm

Mandrake Linux 9.0:  
04000c84cfc2c86923ef61b11948dfe6 9.0/RPMS/libmysql10-3.23.52-1.3mdk.i586.rpm  
9948baccb444b39f76897aa8f5777cb8 9.0/RPMS/libmysql10-devel-3.23.52-1.3mdk.i586.rpm  
cefb16d65faf472ea479ab5b77ac9b91 9.0/RPMS/MySQL-3.23.52-1.3mdk.i586.rpm  
599910eab67704489f360b569d2a1eb6 9.0/RPMS/MySQL-Max-3.23.52-1.3mdk.i586.rpm  
369ea8520e4207160e5655575f74da86 9.0/RPMS/MySQL-bench-3.23.52-1.3mdk.i586.rpm  
ba34172fbaa94f5a5c125c62dd1b0abe 9.0/RPMS/MySQL-client-3.23.52-1.3mdk.i586.rpm  
c2ceb1881525baeaff85c554376b6247 9.0/SRPMS/MySQL-3.23.52-1.3mdk.src.rpm

**vim**

Mandrake Linux 8.0:  
4d9f0bfee91838d6c53a9f309610ffad 8.0/RPMS/vim-X11-6.1-34.1mdk.i586.rpm  
a210af2a18f4ba042376c922e6a536fc 8.0/RPMS/vim-common-6.1-34.1mdk.i586.rpm  
a31f7d72537c6c3b62df50503641a2c3 8.0/RPMS/vim-enhanced-6.1-34.1mdk.i586.rpm  
47270a4e22cbfe26f17c956543579af3 8.0/RPMS/vim-minimal-6.1-34.1mdk.i586.rpm  
6b905a4b36354e315449ce7da6ce7622 8.0/SRPMS/vim-6.1-34.1mdk.src.rpm

Mandrake Linux 8.0/PPC:  
ebeca31f7c4b907fd5fda1689c2384e8 ppc/8.0/RPMS/vim-X11-6.1-34.1mdk.ppc.rpm  
34834a9c4e4c172f2c1499b7767ee103 ppc/8.0/RPMS/vim-common-6.1-34.1mdk.ppc.rpm  
afe96fb6447a6ef42360a35c2a383de9 ppc/8.0/RPMS/vim-enhanced-6.1-34.1mdk.ppc.rpm  
2b8fc174cdaf6563951405cce723531c ppc/8.0/RPMS/vim-minimal-6.1-34.1mdk.ppc.rpm  
6b905a4b36354e315449ce7da6ce7622 ppc/8.0/SRPMS/vim-6.1-34.1mdk.src.rpm

Mandrake Linux 8.1:  
d42a33d13880ce5c1dd9c285691f41fa 8.1/RPMS/vim-X11-6.1-34.1mdk.i586.rpm  
4ed951a7f9b053a7a9d24e7ea1be67c9 8.1/RPMS/vim-common-6.1-34.1mdk.i586.rpm  
61a0f648cdc42753672d2702b226e5e0 8.1/RPMS/vim-enhanced-6.1-34.1mdk.i586.rpm  
4d36b92829b9258d0591fcc8e7401f10 8.1/RPMS/vim-minimal-6.1-34.1mdk.i586.rpm  
6b905a4b36354e315449ce7da6ce7622 8.1/SRPMS/vim-6.1-34.1mdk.src.rpm

Mandrake Linux 8.1/IA64:  
4159e1bcf5f22cd150610e3f5d88a0d0 ia64/8.1/RPMS/vim-X11-6.1-34.1mdk.ia64.rpm  
ed436066882de3fdce84851706a3ea65 ia64/8.1/RPMS/vim-common-6.1-34.1mdk.ia64.rpm  
1d2c6e773b971c7fce8fe264f2493b3b ia64/8.1/RPMS/vim-enhanced-6.1-34.1mdk.ia64.rpm  
9c099217dba8ebffee5f7fe626db9026 ia64/8.1/RPMS/vim-minimal-6.1-34.1mdk.ia64.rpm  
6b905a4b36354e315449ce7da6ce7622 ia64/8.1/SRPMS/vim-6.1-34.1mdk.src.rpm

Mandrake Linux 8.2:  
a6d2071eb37105aec6242c1ceeca979b 8.2/RPMS/vim-X11-6.1-34.1mdk.i586.rpm  
a111ab20a77dcb625c20d1874b0ce91d 8.2/RPMS/vim-common-6.1-34.1mdk.i586.rpm  
77c31c1ebc1eb41c6f9f3b78c9f00b34 8.2/RPMS/vim-enhanced-6.1-34.1mdk.i586.rpm  
61ca6d154283f12fbf2eb417103c03e7 8.2/RPMS/vim-minimal-6.1-34.1mdk.i586.rpm  
6b905a4b36354e315449ce7da6ce7622 8.2/SRPMS/vim-6.1-34.1mdk.src.rpm

Mandrake Linux 8.2/PPC:  
993235cea1a3535697cd8a47d8064766 ppc/8.2/RPMS/vim-X11-6.1-34.3mdk.ppc.rpm  
ff1ddc1f0df266eece315314ea3e1b0b ppc/8.2/RPMS/vim-common-6.1-34.3mdk.ppc.rpm  
3d71a31270ac817c84cb9db1df4ba53d ppc/8.2/RPMS/vim-enhanced-6.1-34.3mdk.ppc.rpm  
278380bf389d2c0a58771a61f82251ea ppc/8.2/RPMS/vim-minimal-6.1-34.3mdk.ppc.rpm  
eab938b78ab2aa578979c86e44aaf4a9 ppc/8.2/SRPMS/vim-6.1-34.3mdk.src.rpm

Mandrake Linux 9.0:  
5e7eac6c390caf51751b7dea6ba6a1a5 9.0/RPMS/vim-X11-6.1-34.1mdk.i586.rpm  
1526a529ac06942ff5b34935d71d48e9 9.0/RPMS/vim-common-6.1-34.1mdk.i586.rpm  
bf9fda1e219dad2497efe0b8d42ef263 9.0/RPMS/vim-enhanced-6.1-34.1mdk.i586.rpm  
fbb42d4346a7dbbda450896c46b30e2b 9.0/RPMS/vim-minimal-6.1-34.1mdk.i586.rpm  
6b905a4b36354e315449ce7da6ce7622 9.0/SRPMS/vim-6.1-34.1mdk.src.rpm

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=286)