---
author: tomaja
date: "2002-07-05T14:34:18Z"
excerpt: |
  Više bagova u Linux kernelima 2.2 i 2.4 je otkriveno i ispravljeno.<br>
  Otkriven je problem u CIPE (VPN tunnel) implementaciji Linux kernela<br>
  tako da (namerno)loše kreiran paket može dovesti do pada sistema. Ovaj bag<br>
  se javio u kernelu pa tako može uticati na sve Linux distribucije.<br>
  Andrew Griffiths je otkrio ovu grešku koja može dozvoliti remote mašinama<br>
  da pro?itaju random memoriju.  Ovaj bag se može javiti na verzijama kernela<br>
  pre v2.4.0-test6 i 2.2.18; svi Mandrake Linux 2.4 kerneli su otporni<br>
  <br>
  Još jedan problem je otkriven od strane Linux Netfilter tima u komponenti
guid: https://forum.linuxo.org/2002/07/05/kernel-2-2-i-2-4-sigurnosna-ispravka/
id: 194
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Kernel 2.2 i 2.4 &#8211; sigurnosna ispravka
url: /kernel-2-2-i-2-4-sigurnosna-ispravka/
---
Više bagova u Linux kernelima 2.2 i 2.4 je otkriveno i ispravljeno.  
Otkriven je problem u CIPE (VPN tunnel) implementaciji Linux kernela  
tako da (namerno)loše kreiran paket može dovesti do pada sistema. Ovaj bag  
se javio u kernelu pa tako može uticati na sve Linux distribucije.  
Andrew Griffiths je otkrio ovu grešku koja može dozvoliti remote mašinama  
da pro?itaju random memoriju. Ovaj bag se može javiti na verzijama kernela  
pre v2.4.0-test6 i 2.2.18; svi Mandrake Linux 2.4 kerneli su otporni

Još jedan problem je otkriven od strane Linux Netfilter tima u komponenti<!--break-->za

  
pra?enje IRC konekcije u netfilteru u Linux 2.4 kernelima. On uti?e na proveru  
  
IRC DCC konekcije kroz firewall to sa mnogo irim opsegom što može dovesti  
  
do otvaranja neželjenih portova nafirewall-u i omogu?iti nekontrolisane  
konekcije u zavisnosti od trenutno postavljenih firewall pravila.

2.2 i 2.4 kerneli su takoÄ‘e ranjivi od strane zlib double-free()  
problema pošto se rutine iz kompresione biblioteke koriste od strane  
funkcija koje nekompresovani fajl sistemi u?itavaju u ramdiskove.  
Kernel takoÄ‘e koristi kompresionu biblioteku u PPP lejeru kao i  
freeswan IPSec kernel modul.

TakoÄ‘e, ve?i broj drugih ne-sigurnosnih ispravki je prisutno u ovim kernelima,  
uklju?uju?i nove i poboljšane drajvere, LSB kompatibilnost i dr.

MandrakeSoft preporu?uje svim korisnicima da izvrše ažuriranje svojih  
kernela što je pre mogu?e na ove nove 2.2 i 2.4 kernele.

NAPOMENA: Ovo ažuriranje se ne može izvesti preko MandrakeUpdate;  
ono se mora izvesti iz konzole. To spe?ava instaliranje umesto ažuriranja  
kernela. Za ažuriranje kernela, prvo ažurirajte iptables, mkinitrd, i initscripts  
  
pakete ukoliko se mogu primeniti na vašem sistemu. Koristite 

&#8222;rpm -ivh kernel_package&#8220; za instaliranje novog kernela.

Pre restarta, proverite vaš /etc/lilo.conf,  
/boot/grub/menu.lst, ili /etc/yaboot.conf (samo zaPPC korisnike) da bi  
bili sigurni da ?ete mo?i da ispravno startujete i stari i novi kernel (ovo  
  
?e omogu?iti da podignete stari kernel u slu?aju da vam novi ne odgovara).

Oni koji koriste LILO kao boot starter treba da pokrenu &#8222;/sbin/lilo -v&#8220;,  
a oni koji koriste GRUB &#8222;sh /boot/grun/install.sh&#8220;, a PPC korisnici moraju  
  
da ukucaju &#8222;/sbin/ybin -v&#8220; da bi upisali boot record u cilju restarta u  
novom  
kernelu ukoliko ste napravili bilo kakvuizmenu u boot confi fajlovima.

Spisak FTP mirora sa kojim možete preuzeti fajlove za ažuriranje možete  
prona?i na linku:

<http://www.mandrakesecure.net/en/ftp.php>

a spisak fajlova za ažuriranje sledi (po verzijama Mandrake Linux-a od 7.1  
do 8.2) :

Linux-Mandrake 7.1:  
89a74479d4a0a685f88b5b49dd51b741 7.1/RPMS/alsa-2.2.19_0.5.10b-6.4mdk.i586.rpm  
1a212b6a82a3d69e89b9c04beba8c378 7.1/RPMS/alsa-source-2.2.19_0.5.10b-6.4mdk.i586.rpm  
6df92e7ba462cb3d7b18047b800b7b92 7.1/RPMS/kernel-2.2.19-6.4mdk.i586.rpm  
1b9e5b47ff585c2400db9d4a36369242 7.1/RPMS/kernel-doc-2.2.19-6.4mdk.i586.rpm  
388da5e5ab45099131ee2be2d1400700 7.1/RPMS/kernel-headers-2.2.19-6.4mdk.i586.rpm  
a2955bcbf45d9398dde4663dcb082154 7.1/RPMS/kernel-pcmcia-cs-2.2.19-6.4mdk.i586.rpm  
b12e2f865349de601f3e2504c96ca696 7.1/RPMS/kernel-secure-2.2.19-6.4mdk.i586.rpm  
5f97b418b9493e1d06bc4850ed2f0d29 7.1/RPMS/kernel-smp-2.2.19-6.4mdk.i586.rpm  
705081b8274b2975e863057b7dabf785 7.1/RPMS/kernel-source-2.2.19-6.4mdk.i586.rpm  
b1346849b552e0ea0ed7506f6feb7e71 7.1/RPMS/kernel-utils-2.2.19-6.4mdk.i586.rpm  
c528ec474457a7a25ded1bf1c2ada7eb 7.1/RPMS/reiserfs-utils-2.2.19_3.5.29-6.4mdk.i586.rpm  
53ed02aabbbc6b39499e9916722ee3b4 7.1/SRPMS/kernel-2.2.19-6.4mdk.src.rpm

Linux-Mandrake 7.2:  
3e82e3f62ec09628c8cbfcd14144df3f 7.2/RPMS/alsa-2.2.19_0.5.10b-6.4mdk.i586.rpm  
aa2e6331cab7608c2c53f35e727e49e0 7.2/RPMS/alsa-source-2.2.19_0.5.10b-6.4mdk.i586.rpm  
188d0fbedf71b069cb00d6b43dabece8 7.2/RPMS/kernel-2.2.19-6.4mdk.i586.rpm  
78e13bab41130b6a1f07831dc9dd89b7 7.2/RPMS/kernel-doc-2.2.19-6.4mdk.i586.rpm  
37299985c82a109f23ef9243a0297351 7.2/RPMS/kernel-headers-2.2.19-6.4mdk.i586.rpm  
ab7069405fe8b1bd613621ffb82e89bc 7.2/RPMS/kernel-pcmcia-cs-2.2.19-6.4mdk.i586.rpm  
a0f63847e48c8947b06459b8a7f83224 7.2/RPMS/kernel-secure-2.2.19-6.4mdk.i586.rpm  
1fd0b4d6bf8b7a6113eeb0ff85915ac7 7.2/RPMS/kernel-smp-2.2.19-6.4mdk.i586.rpm  
1732e14ced4ec669a0e939afe024382c 7.2/RPMS/kernel-source-2.2.19-6.4mdk.i586.rpm  
c70835ae90d4fce0f8111f5d29be1cf3 7.2/RPMS/kernel-utils-2.2.19-6.4mdk.i586.rpm  
5931d3bda493d937b26a5ad83b0263d6 7.2/RPMS/reiserfs-utils-2.2.19_3.5.29-6.4mdk.i586.rpm  
53ed02aabbbc6b39499e9916722ee3b4 7.2/SRPMS/kernel-2.2.19-6.4mdk.src.rpm

Mandrake Linux 8.0:  
6a8e28c0d1c8d2b3ce3e26a304b3f146 8.0/RPMS/initscripts-5.83-7.1mdk.i586.rpm  
15a22adbed6ba7939acce1129fc08c63 8.0/RPMS/iptables-1.2.5-1.1mdk.i586.rpm  
18d0f2803934688bdb00c3833daceb00 8.0/RPMS/iptables-ipv6-1.2.5-1.1mdk.i586.rpm  
280ff798cc5215a8e5d0ba600e56735c 8.0/RPMS/kernel-2.4.18.8.2mdk-1-3mdk.i586.rpm  
c5e21fba0203a05179b8c4bd7eddb0d6 8.0/RPMS/kernel-2.4.18.8.2mdk-pcmcia-cs-1-3mdk.i586.rpm  
4aff00e0df570a380be6b8f5c0803a3c 8.0/RPMS/kernel-BOOT-2.4.18.8.2mdk-1-3mdk.i586.rpm  
074a3539369e8a3324fd3881b8b7811e 8.0/RPMS/kernel-doc-2.4.18-8.2mdk.i586.rpm  
b8a3586edf1003e150848203e676ee2f 8.0/RPMS/kernel-doc-html-2.4.18-8.2mdk.i586.rpm  
df5af818d1ee2c765061bd43869d3e5a 8.0/RPMS/kernel-doc-pdf-2.4.18-8.2mdk.i586.rpm  
9a33086e43750f0f687f97130f9fa590 8.0/RPMS/kernel-doc-ps-2.4.18-8.2mdk.i586.rpm  
76a496110a624afac0ffe2fdaaa89e47 8.0/RPMS/kernel-enterprise-2.4.18.8.2mdk-1-3mdk.i586.rpm  
1b827d3e66e19d30629923cf0365a37b 8.0/RPMS/kernel-secure-2.4.18.8.2mdk-1-3mdk.i586.rpm  
b958d00f0d3bb37228328a838133f76a 8.0/RPMS/kernel-smp-2.4.18.8.2mdk-1-3mdk.i586.rpm  
0092267146ac3a774a77bb85d8c40109 8.0/RPMS/kernel-source-2.4.18-8.2mdk.i586.rpm  
0a18529d9bbb8f4f8dd7210f7878cc15 8.0/RPMS/kernel22-2.2.20-9.2mdk.i586.rpm  
a47458e6cdc0bc3741714c70f393cb35 8.0/RPMS/kernel22-smp-2.2.20-9.2mdk.i586.rpm  
e76c465f909695ddf0221e8100dde47a 8.0/RPMS/kernel22-source-2.2.20-9.2mdk.i586.rpm  
795dbae0b1befb5e5ea040c465b94a31 8.0/RPMS/mkinitrd-3.1.6-28.1mdk.i586.rpm  
4deb9724b61a696185ae7153d71aad40 8.0/SRPMS/initscripts-5.83-7.1mdk.src.rpm  
7ac99ba7e3baf59966a22d3bad5a860a 8.0/SRPMS/iptables-1.2.5-1.1mdk.src.rpm  
cbac2540c632f2c03b9b82f187086614 8.0/SRPMS/kernel-2.4.18.8.2mdk-1-3mdk.src.rpm  
8b3994c11c9c024744c319ad621a4b13 8.0/SRPMS/kernel22-2.2.20-9.2mdk.src.rpm  
441cb1f8eaefc707ad1ba47da5224de7 8.0/SRPMS/mkinitrd-3.1.6-28.1mdk.src.rpm

Mandrake Linux 8.0/ppc:  
f6290470bdff3220ecc3ede9ba21b147 ppc/8.0/RPMS/initscripts-5.83-7.1mdk.ppc.rpm  
1eed80705d99d242d47f75878822c690 ppc/8.0/RPMS/iptables-1.2.5-1.1mdk.ppc.rpm  
7ba74fffc19c7d7587f5d9efcb99357e ppc/8.0/RPMS/iptables-ipv6-1.2.5-1.1mdk.ppc.rpm  
50b3fe21d25c8842819f7dba157c6681 ppc/8.0/RPMS/kernel-2.4.18.8.2mdk-1-3mdk.ppc.rpm  
aae89320d2d41b2caf1e6c7b9ef8d756 ppc/8.0/RPMS/kernel-2.4.18.8.2mdk-pcmcia-cs-1-3mdk.ppc.rpm  
cee26bdf384252b87c10baf9f273bdfa ppc/8.0/RPMS/kernel-doc-2.4.18-8.2mdk.ppc.rpm  
8f2417c851137bfe3ffb89e328709cac ppc/8.0/RPMS/kernel-doc-html-2.4.18-8.2mdk.ppc.rpm  
542e188fb022174c9fb3bfb7fac263c8 ppc/8.0/RPMS/kernel-doc-pdf-2.4.18-8.2mdk.ppc.rpm  
6a2bf33e2e1448c1fa711dfcaaaec59f ppc/8.0/RPMS/kernel-doc-ps-2.4.18-8.2mdk.ppc.rpm  
b905355774f5449e1e9ccd33ee4bda4d ppc/8.0/RPMS/kernel-enterprise-2.4.18.8.2mdk-1-3mdk.ppc.rpm  
f116d2c4fdbca61e387a2f5af4cd9e70 ppc/8.0/RPMS/kernel-smp-2.4.18.8.2mdk-1-3mdk.ppc.rpm  
dd070919e6b9a1c6b32dcdc63cdf193c ppc/8.0/RPMS/kernel-source-2.4.18-8.2mdk.ppc.rpm  
8540df4b8fd1410132e55a88b709a388 ppc/8.0/RPMS/kernel22-2.2.20-9.2mdk.ppc.rpm  
2ed0bb03780967c0a954f3945e155ff5 ppc/8.0/RPMS/kernel22-smp-2.2.20-9.2mdk.ppc.rpm  
9a64bcbcc95395dd17907102c9da44e8 ppc/8.0/RPMS/kernel22-source-2.2.20-9.2mdk.ppc.rpm  
b3d983312e9f964ef765e007451131a6 ppc/8.0/RPMS/mkinitrd-3.1.6-28.1mdk.ppc.rpm  
4deb9724b61a696185ae7153d71aad40 ppc/8.0/SRPMS/initscripts-5.83-7.1mdk.src.rpm  
7ac99ba7e3baf59966a22d3bad5a860a ppc/8.0/SRPMS/iptables-1.2.5-1.1mdk.src.rpm  
cbac2540c632f2c03b9b82f187086614 ppc/8.0/SRPMS/kernel-2.4.18.8.2mdk-1-3mdk.src.rpm  
8b3994c11c9c024744c319ad621a4b13 ppc/8.0/SRPMS/kernel22-2.2.20-9.2mdk.src.rpm  
441cb1f8eaefc707ad1ba47da5224de7 ppc/8.0/SRPMS/mkinitrd-3.1.6-28.1mdk.src.rpm

Mandrake Linux 8.1:  
05c5b96aafcf2fd0d4dabbaed8e5bb72 8.1/RPMS/iptables-1.2.5-1.1mdk.i586.rpm  
e51e1c114518bf35db324a80b52f6f80 8.1/RPMS/iptables-ipv6-1.2.5-1.1mdk.i586.rpm  
ff744515582a1c4aaf086db157c4206f 8.1/RPMS/kernel-2.4.18.8.2mdk-1-3mdk.i586.rpm  
134c6b5b65568b932d76c1fabd3deffc 8.1/RPMS/kernel-2.4.18.8.2mdk-pcmcia-cs-1-3mdk.i586.rpm

d13a440bf10b438a3af314b60d7a865c 8.1/RPMS/kernel-doc-2.4.18-8.2mdk.i586.rpm  
309676e8e0d8df03d05ca7d5ec8619ec 8.1/RPMS/kernel-doc-html-2.4.18-8.2mdk.i586.rpm  
5f51054a2e39beab7bb8e04992f65458 8.1/RPMS/kernel-doc-pdf-2.4.18-8.2mdk.i586.rpm  
c6a78308ecd332a7e7134e41761a35ba 8.1/RPMS/kernel-doc-ps-2.4.18-8.2mdk.i586.rpm  
81886f368c2d1b7fc7fe1b1494bd55eb 8.1/RPMS/kernel-enterprise-2.4.18.8.2mdk-1-3mdk.i586.rpm  
65a86c68e312349b7525f15eba9648d2 8.1/RPMS/kernel-secure-2.4.18.8.2mdk-1-3mdk.i586.rpm  
cf0f8237835f21ee9ff611966094296e 8.1/RPMS/kernel-smp-2.4.18.8.2mdk-1-3mdk.i586.rpm  
bd8ba58d623f1467a41f764e20378dc3 8.1/RPMS/kernel-source-2.4.18-8.2mdk.i586.rpm  
54dbc921dfd376e073f2fa4cbdd99f43 8.1/RPMS/kernel22-2.2.20-9.2mdk.i586.rpm  
0a1abeec31a25fe2120d9968c8ef0d90 8.1/RPMS/kernel22-smp-2.2.20-9.2mdk.i586.rpm  
f0e89d7e072078d2435d6957908ef1f5 8.1/RPMS/kernel22-source-2.2.20-9.2mdk.i586.rpm  
10f7e9c656fb926439addbb1705aa77a 8.1/RPMS/mkinitrd-3.1.6-28.1mdk.i586.rpm  
7ac99ba7e3baf59966a22d3bad5a860a 8.1/SRPMS/iptables-1.2.5-1.1mdk.src.rpm  
cbac2540c632f2c03b9b82f187086614 8.1/SRPMS/kernel-2.4.18.8.2mdk-1-3mdk.src.rpm  
8b3994c11c9c024744c319ad621a4b13 8.1/SRPMS/kernel22-2.2.20-9.2mdk.src.rpm  
  
441cb1f8eaefc707ad1ba47da5224de7 8.1/SRPMS/mkinitrd-3.1.6-28.1mdk.src.rpm

Mandrake Linux 8.2:  
a784430846ca56b52151b64f74744528 8.2/RPMS/devfsd-1.3.25-1.1mdk.i586.rpm  
32969698f7badf0c3bc7fa3e4f278977 8.2/RPMS/kernel-2.4.18.8.1mdk-1-3mdk.i586.rpm  
8780d75e33c52ddc0fee1c84fcab35b3 8.2/RPMS/kernel-BOOT-2.4.18.8.1mdk-1-3mdk.i586.rpm  
09998125ec43033ec81857713a0c8426 8.2/RPMS/kernel-doc-2.4.18-8.1mdk.i586.rpm  
885b857618b0aa899b6d0a4fe6f0b111 8.2/RPMS/kernel-doc-html-2.4.18-8.1mdk.i586.rpm  
4129c6390bf04f90e910904748dc53ea 8.2/RPMS/kernel-doc-pdf-2.4.18-8.1mdk.i586.rpm  
a7a833d162893b3afe5e082a9bcbffe5 8.2/RPMS/kernel-doc-ps-2.4.18-8.1mdk.i586.rpm  
a1ba4d745bf80add95b73006634fcbc6 8.2/RPMS/kernel-enterprise-2.4.18.8.1mdk-1-3mdk.i586.rpm  
cf7a7343bff1a12796d68fe7b12c5403 8.2/RPMS/kernel-secure-2.4.18.8.1mdk-1-3mdk.i586.rpm  
215e844621ba72e68b73756d1fad4ff3 8.2/RPMS/kernel-smp-2.4.18.8.1mdk-1-3mdk.i586.rpm  
b40235a56e88bef36e827fd3baec374c 8.2/RPMS/kernel-source-2.4.18-8.1mdk.i586.rpm  
d19ee6183a1fad278df1990b8c23e9bb 8.2/RPMS/kernel22-2.2.20-9.1mdk.i586.rpm  
5bd5d0df44876a9252869ce39a63a675 8.2/RPMS/kernel22-smp-2.2.20-9.1mdk.i586.rpm  
6f34d89907d78997c2cd55a31ed4e86e 8.2/RPMS/kernel22-source-2.2.20-9.1mdk.i586.rpm  
6abfb4e1be1194616f267eb624065491 8.2/SRPMS/devfsd-1.3.25-1.1mdk.src.rpm  
883ac7630080a1120323adabf2f80113 8.2/SRPMS/kernel-2.4.18.8.1mdk-1-3mdk.src.rpm  
5583ac07de85a815e9947304c32fa1c1 8.2/SRPMS/kernel22-2.2.20-9.1mdk.src.rpm

Mandrake Linux 8.2/ppc:  
3e845487107a567eef546362d274acc4 ppc/8.2/RPMS/kernel-2.4.18.8.1mdk-1-3mdk.ppc.rpm  
5c5d749e10f85c2759e4726f1bef988b ppc/8.2/RPMS/kernel-doc-2.4.18-8.1mdk.ppc.rpm  
f30e3ae0f42e9ac4936f8e4aaf3c7255 ppc/8.2/RPMS/kernel-doc-html-2.4.18-8.1mdk.ppc.rpm  
abc3f86f3c264bf4e329bba78a7f0b35 ppc/8.2/RPMS/kernel-doc-pdf-2.4.18-8.1mdk.ppc.rpm  
09c27bae3001380592e5a30b64b3a7b3 ppc/8.2/RPMS/kernel-doc-ps-2.4.18-8.1mdk.ppc.rpm  
86f8dccb5db21ba9161e23a65a580186 ppc/8.2/RPMS/kernel-enterprise-2.4.18.8.1mdk-1-3mdk.ppc.rpm  
ec7f88601b5d1de1d56b6e52c7f75b8b ppc/8.2/RPMS/kernel-smp-2.4.18.8.1mdk-1-3mdk.ppc.rpm  
4c57b54857d78250c12b0c4f886bbc8b ppc/8.2/RPMS/kernel-source-2.4.18-8.1mdk.ppc.rpm  
2ba95aa5905599843be289616f57610f ppc/8.2/RPMS/kernel22-2.2.20-9.1mdk.ppc.rpm  
85b9d2407847420d73fe3b5220c575b3 ppc/8.2/RPMS/kernel22-smp-2.2.20-9.1mdk.ppc.rpm  
38f6a6bed062f20afadf6fd485633b29 ppc/8.2/RPMS/kernel22-source-2.2.20-9.1mdk.ppc.rpm  
883ac7630080a1120323adabf2f80113 ppc/8.2/SRPMS/kernel-2.4.18.8.1mdk-1-3mdk.src.rpm  
5583ac07de85a815e9947304c32fa1c1 ppc/8.2/SRPMS/kernel22-2.2.20-9.1mdk.src.rpm

Corporate Server 1.0.1:  
89a74479d4a0a685f88b5b49dd51b741 1.0.1/RPMS/alsa-2.2.19_0.5.10b-6.4mdk.i586.rpm  
1a212b6a82a3d69e89b9c04beba8c378 1.0.1/RPMS/alsa-source-2.2.19_0.5.10b-6.4mdk.i586.rpm  
6df92e7ba462cb3d7b18047b800b7b92 1.0.1/RPMS/kernel-2.2.19-6.4mdk.i586.rpm  
1b9e5b47ff585c2400db9d4a36369242 1.0.1/RPMS/kernel-doc-2.2.19-6.4mdk.i586.rpm  
388da5e5ab45099131ee2be2d1400700 1.0.1/RPMS/kernel-headers-2.2.19-6.4mdk.i586.rpm  
a2955bcbf45d9398dde4663dcb082154 1.0.1/RPMS/kernel-pcmcia-cs-2.2.19-6.4mdk.i586.rpm  
b12e2f865349de601f3e2504c96ca696 1.0.1/RPMS/kernel-secure-2.2.19-6.4mdk.i586.rpm  
5f97b418b9493e1d06bc4850ed2f0d29 1.0.1/RPMS/kernel-smp-2.2.19-6.4mdk.i586.rpm  
705081b8274b2975e863057b7dabf785 1.0.1/RPMS/kernel-source-2.2.19-6.4mdk.i586.rpm  
b1346849b552e0ea0ed7506f6feb7e71 1.0.1/RPMS/kernel-utils-2.2.19-6.4mdk.i586.rpm  
c528ec474457a7a25ded1bf1c2ada7eb 1.0.1/RPMS/reiserfs-utils-2.2.19_3.5.29-6.4mdk.i586.rpm  
53ed02aabbbc6b39499e9916722ee3b4 1.0.1/SRPMS/kernel-2.2.19-6.4mdk.src.rpm

Single Network Firewall 7.2:  
188d0fbedf71b069cb00d6b43dabece8 snf7.2/RPMS/kernel-2.2.19-6.4mdk.i586.rpm  
78e13bab41130b6a1f07831dc9dd89b7 snf7.2/RPMS/kernel-doc-2.2.19-6.4mdk.i586.rpm  
37299985c82a109f23ef9243a0297351 snf7.2/RPMS/kernel-headers-2.2.19-6.4mdk.i586.rpm  
ab7069405fe8b1bd613621ffb82e89bc snf7.2/RPMS/kernel-pcmcia-cs-2.2.19-6.4mdk.i586.rpm  
a0f63847e48c8947b06459b8a7f83224 snf7.2/RPMS/kernel-secure-2.2.19-6.4mdk.i586.rpm  
1fd0b4d6bf8b7a6113eeb0ff85915ac7 snf7.2/RPMS/kernel-smp-2.2.19-6.4mdk.i586.rpm  
1732e14ced4ec669a0e939afe024382c snf7.2/RPMS/kernel-source-2.2.19-6.4mdk.i586.rpm  
c70835ae90d4fce0f8111f5d29be1cf3 snf7.2/RPMS/kernel-utils-2.2.19-6.4mdk.i586.rpm  
5931d3bda493d937b26a5ad83b0263d6 snf7.2/RPMS/reiserfs-utils-2.2.19_3.5.29-6.4mdk.i586.rpm  
53ed02aabbbc6b39499e9916722ee3b4 snf7.2/SRPMS/kernel-2.2.19-6.4mdk.src.rpm  
Novi kerneli za Mandrake Linux 8.1/IA64 ?e uskoro biti dostupni.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=194)