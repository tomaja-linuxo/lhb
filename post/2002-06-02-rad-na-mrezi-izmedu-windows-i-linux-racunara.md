---
author: tomaja
date: "2002-06-02T10:33:36Z"
excerpt: 'Vrlo često se javlja problem kada se nađete u situaciji da sa va&scaron;e
  ma&scaron;ine  na kojoj je instaliran Linux želite da pristupite nekom računaru
  na  mreži u va&scaron;oj firmi, poslu , u kući i sl na kojem je instaliran neki
  Windows  OS. Ako imate takav slučaj onda je ovo tekst za vas. U konkretnom slučaju  na
  mojoj ma&scaron;ini je instaliran standardni Mandrake Linux 8.2 sistem na koju  želim
  da pristupim je instaliran neki od MS Windows operativnih sistema (Windows  XP). '
guid: https://forum.linuxo.org/2002/06/02/rad-na-mrezi-izmedu-windows-i-linux-racunara/
id: 186
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Rad na mreži između Windows i Linux računara
url: /rad-na-mrezi-izmedu-windows-i-linux-racunara/
---
Vrlo često se javlja problem kada se nađete u situaciji da sa va&scaron;e ma&scaron;ine na kojoj je instaliran Linux želite da pristupite nekom računaru na mreži u va&scaron;oj firmi, poslu , u kući i sl na kojem je instaliran neki Windows OS. Ako imate takav slučaj onda je ovo tekst za vas. U konkretnom slučaju na mojoj ma&scaron;ini je instaliran standardni Mandrake Linux 8.2 sistem na koju želim da pristupim je instaliran neki od MS Windows operativnih sistema (Windows XP). <!--break-->

#### Pripreme

  1. Instalirajte paket 'samba-client' pomoću&nbsp; Software Manager-a iz komandne linije kao 'root' sa komandom 
    <font color="red">urpmi samba-client</font>
    
    Zapamtite da pokretanje Samba servera NIJE potrebno da bi pristupili Windows direktorijumima. On je potreban u slučaju da želite da sa Windows ma&scaron;ine pristupite ma&scaron;ini na kojoj je instaliran Linux. 

  2. Kreirajte deljeni direktorijum (shared directory) na MS Windows-u. To možete da uradite tako &scaron;to ćete u Windows-u kliknuti desnim klikom na određeni direktorijum i izabrati 'Share &#8230;' . 

Za na&scaron; slučaj pretpostavimo da je SMB hostname za Windows 'win' a da je ime deljenog direktorijuma (shared directory) 'export'. 

#### Mogući izbor

Postoji vi&scaron;e načina da pristupite deljenim direktorijumima na Windows računaru: 

  1. pretraživanjem pomoću KDE 'konqueror' fajl menadžera; 
  2. kori&scaron;ćenjem aplikacija kao &scaron;to su Komba2, LinNeighboorhood ili Xsmbrowser ili
  3. pode&scaron;avanjem smb tački montirabha pomoću Mandrake Kontrolnog Centra.

#### Kori&scaron;ćenje 'Konqueror'-a

Da bi pristupili deljenim direktorijumu 'export' na ma&scaron;ini 'win', ukucajte

<font color="red">smb://win/export</font>

na mesto gde bi uneli URL i pritisnite taster 'Enter' key. Ukoliko je direktorijum za&scaron;tićen lozinkom, moraćete da je unesete . Posle samo nekoliko sekundi, direktorijum će se otvoriti.

Iako je ovaj metod veoma praktičan kada koristite Konqueror kao va&scaron; fajl menadžer, on ima nekoliko &#8211; prilično krupnih &#8211; nedostataka: 

  1. Spor je. Jednostavne operacije kao &scaron;to je kopiranje fajlova sa Windows ma&scaron;ine na Linux ma&scaron;inu može potrajati do večnosti. 
  2. Naporan je. Konqueror će nastaviti da od vas traži lozinku za svaku akciju. Iako možete postaviti default lozinku u&nbsp; Configuration &#8211; KDE &#8211; Network &#8211; Windows Shares, to je praktično samo ako pristupate istom direktorijumu ili svi direktorijumi imaju istu lozinku. 
  3. Nema detekcije MIME tipa. 
  4. Rasipanje resursa..Možda ovo i nije lokalni problem, ali izgleda da Konqueror ne mari za či&scaron;ćenje pokrenutih 'smbclient' procesa. Tako da svaki put kada pristupite nekom direktorijumu preko Konqueror, novi 'smbclient' proces se pokreće a stari ostaju aktivni. A to nije dobro. 

#### Komba2 i LinNeighboorhood

Verovatno najbolji način za jednostavan pristup Windows particijama i direktorijumima je preko ove dve aplikacije. Obe možete naći na instalacionim diskovima (3 CD set) Mandrake Linux 8.2 i kada ih instalirate možete ih pokrenuti preko 'Networking &#8211; Other'. 

[Komba2](http://komba.sourceforge.net/) detektuje i prikazuje dostupne direktorijuma pri podizanju sistema .Ukoliko su direktorijumi za&scaron;tićeni lozinkom, morate prvo da kliknete na 'lock' ikonu i unesete va&scaron;e SMB korisničko ime i lozinku za taj direktorijum. Ukoliko to ne uradite, nećete uspeti da montirate i da pristupite deljenim direktorijumima.

Označite direktorijum koji želite da montiratte i kliknite na 'mount' ikonu. Po default-u, komba će montirati direktorijum u&nbsp; '~/komba/[MACHINE]/[SHARE]', a u na&scaron;em primeru '~/komba/WIN/EXPORT'. Takođe će pokrenuti i Konqueror fajl menadžer u tom direktorijumu. Obe opcije i sve druge se mogu podesiti i prilagoditi.

Da bi demontirali deljene direktorijume sa Windows ma&scaron;ine zatvorite prvo Konqueror window i onda kliknite na 'unmount' taster.

[LinNeighboorhood](http://www.bnro.de/%7Eschmidjo/) radi na sličan način. Nakon starta podesite radnu grupu ('workgoup') u&nbsp; 'Preferences' prozoru. Sada desnim klikom kliknite na unos za va&scaron;u ma&scaron;inu u denjem prozoru i izaberite 'rescan group'. Ovo može i potrajati, posebno kada je u pitanju&nbsp; Windows XP ma&scaron;ina.

Kada ste pristupili odreženom direktorijumu pojaviće se i prozor gde možete &#8211; ako želite &#8211; da podesite neke opcije. Po default-u, deljeni direktorijum biće montiran kao '~/mnt/[MACHINE]/[share]', a u na&scaron;em slu?aju&nbsp; '~/mnt/WIN/export'.

&Scaron;ta da izaberete? Pa, 'Komba2' je brži, dok&nbsp; 'LinNeighboorhood' nudi vi&scaron;e opcija. 'Komba2' koristi Qt, dok 'LinNeighboorhood' koristi 'GTK' &scaron;to ga čini po izgledu vi&scaron;e GNOME programom.. Probajte i sami 😉

Možda se odlučite i za Xsmbrowser koji radi odlično i najvi&scaron;e podseća na "Network Neighborhood" iz Windows-a 

#### Pode&scaron;avanje smb tački montiranja (mount points) preko Mandrake Kontrolnog Centra

Ovo je staromodan način za pode&scaron;avanje statičkih tački montiranja.  
Otvorite Mandrake Kontrolni Centar i izaberite 'Mount Points &#8211; Samba Mount Points'. Sačekajte malo jer skeniranje može potrajati. Ukoliko se ne pojavi ni jedna ma&scaron;ina, kliknite na 'Search Servers' tab u gornjem levom uglu. Kada se ma&scaron;ina pojavi, dvokliknite na njen ispis i pojaviće se deljeni direktorijumi koji se nalaze na njoj.  
Iz nekog razloga MCC nije prikazao direktorijume na Windows XP ma&scaron;ini, ali će možda kod vas to i uraditi. 

Označite direktorijum i kliknite na 'Mount point'. Odredite direktorijum za montiranje (ukoliko ne postoji, biće kreiran). Zatim kliknite na&nbsp; 'Options' i na&nbsp; 'Advanced'. 

Opcija 'user' može biti korisna kada želite da obi?ni korisnici mogu pristupiti deljenim direktorijumima. 'noauto' je koristan kada deljeni direktorijum nije dostupan pri startanju.  
Možete odrediti va&scaron;e SMB korisničko ime i lozinku u&nbsp; 'advanced' opcijama. Trebalo bi biti očigledno ovo može biti sigurnosni problem, jer će se i ime i lozinka pojaviti kao tekst u&nbsp; '/etc/fstab'. Ali ukoliko niko osim vas nema pristup tom fajlu onda vam to i nije toliko bitno.

Kada zavr&scaron;ite pritisnite 'OK' i 'Done'. Novi unos ?e biti upisan u&nbsp; '/etc/fstab' fajlu i sada ?ete mo?i da taj fajl sistem kao i bilo koji drugi lokalni fajl sistem.

<font color="#999999">Izvor: MUO, 2002</font> 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=186)