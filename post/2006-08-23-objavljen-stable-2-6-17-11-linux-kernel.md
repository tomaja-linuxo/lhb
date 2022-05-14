---
author: tomaja
date: "2006-08-23T00:02:43Z"
excerpt: '<p>Linux Kernel 2.6.17.10 u sebi uključuje sigurnosne ispravke za SCTP,
  UDF, te za propust vezan za local root user manipulacije. UDF deadlock može uticati
  na korišenje nekih DVD aplikacija, pa zainteresovani mogu pogledati link na Wikipediji
  za detaljnije objašnjenje. (<a href="http://pcburn.com/article.php?sid=1719">2.6.17.10
  Changelog</a>) (<a href="http://kernel.org/pub/linux/kernel/v2.6/patch-2.6.17.10.bz2">Patch</a>)
  (<a href="http://kernel.org/pub/linux/kernel/v2.6/linux-2.6.17.10.tar.bz2">Full
  Kernel</a>) (<a href="http://en.wikipedia.org/wiki/Universal_Disk_Format" target="blank">UDF@Wikipedia</a>)</p><p><em><strong>UPDATE</strong></em>:
  Danas je objavljen i <strong>novi stable 2.6.17.11 kernel</strong> koji donosi ispravke
  i još po nešto. Spisak izmena (u orginalu) kao i linkovi za download slede u nastavku
  teksta. &nbsp;</p><p>&nbsp;</p>'
guid: https://forum.linuxo.org/2006/08/23/objavljen-stable-2-6-17-11-linux-kernel/
id: 1262
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Objavljen stable 2.6.17.11 Linux kernel
url: /objavljen-stable-2-6-17-11-linux-kernel/
---
Linux Kernel 2.6.17.10 u sebi uključuje sigurnosne ispravke za SCTP, UDF, te za propust vezan za local root user manipulacije. UDF deadlock može uticati na korišenje nekih DVD aplikacija, pa zainteresovani mogu pogledati link na Wikipediji za detaljnije objašnjenje. ([2.6.17.10 Changelog](http://pcburn.com/article.php?sid=1719)) ([Patch](http://kernel.org/pub/linux/kernel/v2.6/patch-2.6.17.10.bz2)) ([Full Kernel](http://kernel.org/pub/linux/kernel/v2.6/linux-2.6.17.10.tar.bz2)) (<a href="http://en.wikipedia.org/wiki/Universal_Disk_Format" target="blank">UDF@Wikipedia</a>)

_**UPDATE**_: Danas je objavljen i **novi stable 2.6.17.11 kernel** koji donosi ispravke i još po nešto. Spisak izmena (u orginalu) kao i linkovi za download slede u nastavku teksta. &nbsp;

&nbsp;

<!--break-->

  _Za download: ([2.6.17.11 Changelog](http://pcburn.com/article.php?sid=1724)) ([Patch](http://kernel.org/pub/linux/kernel/v2.6/patch-2.6.17.11.bz2)) ([Full Kernel](http://kernel.org/pub/linux/kernel/v2.6/linux-2.6.17.11.tar.bz2))_ &nbsp; 

Summary of changes from v2.6.17.10 to v2.6.17.11  
================================================ 

Alexey Kuznetsov:  
Fix ipv4 routing locking bug 

Andrew Morton:  
disable debugging version of write_lock() 

Daniel Ritz:  
PCI: fix ICH6 quirks 

Danny Tholen:  
1394: fix for recently added <a href="http://pcburn.com/article.php?sid=1724#" target="_top"><font style="color: blue ! important; position: relative; font-family: Arial,Helvetica,sans-serif; font-weight: 400; font-size: 13.3333px" color="blue"><span style="color: blue ! important; position: relative; font-family: Arial,Helvetica,sans-serif; font-weight: 400; font-size: 13.3333px" class="kLink">firewire</span></font></a> patch that breaks things on ppc 

David Miller:  
Fix IFLA_ADDRESS handling 

Diego Calleja:  
Fix BeFS slab corruption 

Dmitry Mishin:  
Fix timer race in dst GC code 

Eric Sandeen:  
Have ext3 reject file handles with bad inode numbers early 

Greg Kroah-Hartman:  
<a href="http://pcburn.com/article.php?sid=1724#" target="_top"><font style="color: blue ! important; position: relative; font-family: Arial,Helvetica,sans-serif; font-weight: 400; font-size: 13.3333px" color="blue"><span style="color: blue ! important; position: relative; font-family: Arial,Helvetica,sans-serif; font-weight: 400; font-size: 13.3333px" class="kLink">Linux</span></font></a> 2.6.17.11 

Kirill Korotaev:  
Kill HASH_HIGHMEM from route cache hash sizing  
sys_getppid oopses on debug kernel  
IA64: local DoS with corrupted ELFs 

Kylene Jo Hall:  
tpm: interrupt clear fix 

Mark Huang:  
ulog: fix panic on SMP kernels 

Michal Miroslaw:  
dm: BUG/OOPS fix 

NeilBrown:  
MD: Fix a potential NULL dereference in md/raid1 

Olaf Hering:  
SERIAL: icom: select FW_LOADER 

Patrick McHardy:  
ip\_tables: fix table locking in ipt\_do_table 

Rafael J. Wysocki:  
swsusp: Fix swap\_type\_of 

Stephen Hemminger:  
sky2: phy power problem on 88e805x  
ipx: header length validation needed

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1262)