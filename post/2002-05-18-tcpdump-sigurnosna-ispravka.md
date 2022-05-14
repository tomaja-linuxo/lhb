---
author: tomaja
date: "2002-05-18T14:20:45Z"
excerpt: '<p>Nekoliko buffer overflow problema je pronađeno u tcpdump paketu koji
  razvijaju FreeBSD developeri i to u verzijama koje prethode verziji 3.5. Međutim,novija
  verzije tcpdump, uključujući i 3.6.2, su takođe ranjive na još jedan buffer overflow
  u AFS RPC decoding funkcijama, što je otkrio Nik Kliton. Novu verziju možete instalirati
  pomoću MandrakeUpdate opcije. '
guid: https://forum.linuxo.org/2002/05/18/tcpdump-sigurnosna-ispravka/
id: 178
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: tcpdump &#8211; sigurnosna ispravka
url: /tcpdump-sigurnosna-ispravka/
---
Nekoliko buffer overflow problema je pronađeno u tcpdump paketu koji razvijaju FreeBSD developeri i to u verzijama koje prethode verziji 3.5. Međutim,novija verzije tcpdump, uključujući i 3.6.2, su takođe ranjive na još jedan buffer overflow u AFS RPC decoding funkcijama, što je otkrio Nik Kliton. Novu verziju možete instalirati pomoću MandrakeUpdate opcije. <!--break-->Ove ranjivosti mogu biti iskorištene od napadača sa mreže koji može srušiti tcpdump proces ili ga čak iskoristiti za izvršavanje nekog koda kao što korisnik pokreće tcpdump, a t je obično root.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=178)