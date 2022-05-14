---
author: tomaja
date: "2002-06-01T13:19:59Z"
excerpt: |
  <p>Jedno od najčešćih pitanja koje postavljaju novi Linux korisnici je &quot;kako mogu da pokrenem Windows programe u linux-u ?&quot;.<br />
  A na to pitanje postoji više ogovora:<br />
  <b>Wine<br />
  VMware<br />
  Win4Lin</b><br />
  Kao dodatak ovom spisku, postoji i još nekoliko komercijalnih programa baziranih na Wine aplikaciji, podešenih za određene namene: <b>Crossover plugin</b> , <b>WineX</b> i <b>CrossoverOffice</b>. Svi ovi &quot;emulatori&quot; rade savršeno dobro na MandrakeLinux-u: Wine je deo osnovne distribucije, WineX se može naći na &quot;Gaming Edition ML 8.1&quot;, a demo verzije VMware, Win4Lin (v. 3), i Crossover plugin-a su uključene u komercijalne 8.2 pakete, koji se mogu skinuti (download-ovati) sa MandrakeClub sajta.
guid: https://forum.linuxo.org/2002/06/01/windows-programi-na-linux-u/
id: 184
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Windows programi na Linux-u
url: /windows-programi-na-linux-u/
---
Jedno od najčešćih pitanja koje postavljaju novi Linux korisnici je "kako mogu da pokrenem Windows programe u linux-u ?".  
A na to pitanje postoji više ogovora:  
**Wine  
VMware  
Win4Lin**  
Kao dodatak ovom spisku, postoji i još nekoliko komercijalnih programa baziranih na Wine aplikaciji, podešenih za određene namene: **Crossover plugin** , **WineX** i **CrossoverOffice**. Svi ovi "emulatori" rade savršeno dobro na MandrakeLinux-u: Wine je deo osnovne distribucije, WineX se može naći na "Gaming Edition ML 8.1", a demo verzije VMware, Win4Lin (v. 3), i Crossover plugin-a su uključene u komercijalne 8.2 pakete, koji se mogu skinuti (download-ovati) sa MandrakeClub sajta.<!--break-->

**Wine** je jedini besplatni (i u pogledu licence i cene) program u kategoriji "windows emulatora". Preciznije, Wine u stavri nije windows emulator, nego impementacija Windows Win32 i Win16 API-ja na X i Unix. Bilo kako bilo, Wine će vam dozvoliti da pokrenete Windows programe kao da su u osnovi linux aplikacije.

Čak šta više, Wine NE zahteva instaliran MS Windows, iako su mu ipak potrebne Windows DLL biblioteke. Kao što ste i mogli pretpostaviti, uvek postoji neko "ali": Wine je još uvek u fazi razvoja i nije najpogodniji za opštu upotrebu. Ipak, Wine je vredan pokušaja i treba ga probati pre ostalih komercijalnih alternativa &#8211; možda i nije najbolji, ali se može desiti da je dovoljno dobar za vas!

Kako je sam Windows dosta komplikovan i zatvoren, mnogo je lakše napraviti programe koji će omogućiti pokretanje određenih aplikacija jer je lakše definisati sve potrebne funkcije. Iza te ideje se krije i nastanak "Crossover Plugin" te "Crossover Office" sa jedne strane, te&nbsp; Transgaming WineX sa druge:

Crossover plugin je specijalna verzija Wine-a koja omogućava pokretanje&nbsp; plugin-a pod linux-om koji su napisani za MS Windows.  
Crossover Office je specijalna verzija Wine-a koja može da pokrene Microsoft Office  
Transgaming WineX je specijalna verzija Wine-a sa podrškom za DirectX, i pogodna je za pokretanje (nekih) Windows igara pod Linux-om. Nije mali je broj ljudi koji će se zadovoljiti jednim delom Windows programa&nbsp; (samo igrice, samo MS Office, ili samo plugins), a svi ovi derivati wine -a su nasledili jednu Wine osobinu: nije im potreban MS WIndows, što ih čini veoma korisnim za&nbsp; Linux korisnike koji nemaju MS Windows licencu.

**VMware** je prvi koji je doneo pouzdano rešenje za pokretanje Windows aplikacija na Linux-u. VMWare NIJE windows emulator, već bolje rečeno PC-emulator (ili "virtualna mašina", koja dozovoljava korisnicima da instaliraju i porenu nekoliko operativnih sistema na jedan&nbsp; PC u isto vreme.

Ovo je veoma korisno programerima, ali sve ima svoju cenu: Svaka virtuelna mašina zahteva dosta RAM-a sa pokretanje operativnog sistema (recimo neke verzije Windows-a) i aplikacije. Virtuelne mašine su , takođe, prilično sporije od realnog stanja (recimo stvarne Windows instalacije) a to usporenje se kreće u rasponu od 20-30%.

Na žalost, VMware će teško biti interesantan za obične korisnike jer je cena&nbsp; "VMWare Workstation" oko US $300.

**Win4Lin** je komercijalni program pomalo sličan Wine-u, sa cenom koja je ispod US $100. Evo i nekih prednosti nove verzije (4.0)  
Brzina: windows programi rade mnogo brže pod Win4Lin nego pod VMware, Wine,i&nbsp; wine-zbaziranim derivatima.  
Zahtevnost: Win4L traži mnogo manje resursa (RAM, CPU) od VMware.  
Kompatibilnost: Win4Lin emulacija je izgleda dovoljno dobra za veličinu aplikacija osim onih&nbsp;&nbsp;koje su grafički zahtevne, kao što su 3D igre.  
Na žalost, Win4Lin ima i dve mane":

**Zaključak:**

Igrači će najbolje proći sa WineX  
Ukoliko vas zanimaju windows plugins pod Linux-om&nbsp; Crossover plugin će vas učiniti srećnim.  
Veliki broj malih preduzeća se mogu zadovoljiti sa Microsoft Office-om na desktopu. "Crossover Office" je onda sve što im treba.  
Za neke, Wine će sam biti sasvim dovoljan".  
Oni koji imaju para neka potraže VMware  
a oni koji imaju instaliran neki Windows mogu odlično proći sa Win4Lin i sa manje para.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=184)