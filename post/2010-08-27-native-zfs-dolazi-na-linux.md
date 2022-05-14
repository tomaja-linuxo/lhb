---
author: tomaja
date: "2010-08-27T18:39:52Z"
excerpt: |
  <strong>ZFS</strong> se do sada nije našao na nama omiljenom operativnom sistemu zbog problema sa licencama. Naime, Sun (sada Oracle), kao kreator ovog odličnog fajl sistema koristi <strong>CDDL licencu</strong> koja nije kompatibilna sa GNU GPL licencom pod kojom se objavljujem Linux kernel. Do sada se ZFS mogao koristiti preko <strong>Linux FUSE</strong> modula koje je stavljao fajl sistem u korisnički prostor, ali je time bile limitirane mogućnosti fajl sistema i brzina rada.
  Kako se sada čini, izgleda da je mukama došao kraj. Pored sve boljeg <a href="http://en.wikipedia.org/wiki/Btrfs">btrfs</a> za koji se očekuje da postane default fajl sistem za Linux moguće je da će i ZFS zauzetni značajno mesto a da se dokazao to najbolje mogu potvrditi korisnici Open Solarisa, Free i NetBSD-a
guid: https://forum.linuxo.org/2010/08/27/native-zfs-dolazi-na-linux/
id: 2358
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Native ZFS dolazi na Linux
url: /native-zfs-dolazi-na-linux/
---
**ZFS** se do sada nije našao na nama omiljenom operativnom sistemu zbog problema sa licencama. Naime, Sun (sada Oracle), kao kreator ovog odličnog fajl sistema koristi **CDDL licencu** koja nije kompatibilna sa GNU GPL licencom pod kojom se objavljujem Linux kernel. Do sada se ZFS mogao koristiti preko **Linux FUSE** modula koje je stavljao fajl sistem u korisnički prostor, ali je time bile limitirane mogućnosti fajl sistema i brzina rada.  
Kako se sada čini, izgleda da je mukama došao kraj. Pored sve boljeg [btrfs](http://en.wikipedia.org/wiki/Btrfs) za koji se očekuje da postane default fajl sistem za Linux moguće je da će i ZFS zauzetni značajno mesto a da se dokazao to najbolje mogu potvrditi korisnici Open Solarisa, Free i NetBSD-a

Naime, indijska IT firma **KQ Infotech** je uspela da kreira native ZFS port za Linux koji će i dalje biti objavljivan pod uslovima CDDL licence i neće se direktno integrisati u Linux kernel već će objaviti izvorni kod kao kernel modul za korisnike osiguravajući da ne koristi bilo koji od GPL-only simbola čime bi došlo do konflika licenci.

KQ Infotech verzija porta već ima implementiran ZFS POSIX sloj koji se može koristiti. Ovaj port je baziran na ZFS Pool 18, koji je ralativno nov ali mu nedostaje podrška za de-duplikaciju i druge novine koje su se mogu naći u baznom kodu OpenSolaris-a pre nego je ovaj napušten od strane Oracle-a.

<p class="info">
  Više informacija na <a href="http://www.phoronix.com/scan.php?page=article&#038;item=zfs_linux_coming&#038;num=1">Phoronix-u</a>
</p>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2358)