---
author: tomaja
date: "2005-02-16T05:26:27Z"
excerpt: Piše mtm76:<i>"Primjetio sam da ljudi neopravdano zaziru od Slackware-a,
  i to zato jer im je neko rekao da je to &#8220;tamo neka distribucija&#8221;, koju
  instaliraju samo &#8220;tamo neki likovi&#8221; koji žele da se prave pametni...
  E kad na to dodamo ?injenicu da je instalacija u tekstualnom modu, i da ne postoje
  gotovo nikakvi grafi?ki alati za konfiguraciju, ve?ina potencijalih novih korisnika
  ve? diže ruke od ove distribucije... E ja se nadam da ?u bar malo to promijeniti
  sa ovim tekstom... ina?e sav ovaj tekst se odnosi na Slack10, ali ne bi trebalo
  da bude nekakve razlike i za ostale... a trebao bi da bude koristan prije svega
  za one koji ne vladaju baš engleskim jezikom, pa su prepušteni doma?im forumima
  na volju... "</i>
guid: https://forum.linuxo.org/2005/02/16/mali-vodi-kroz-slackware/
id: 751
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mali vodi? kroz Slackware
url: /mali-vodi-kroz-slackware/
---
Piše mtm76:_&#8222;Primjetio sam da ljudi neopravdano zaziru od Slackware-a, i to zato jer im je neko rekao da je to &#8220;tamo neka distribucija&#8221;, koju instaliraju samo &#8220;tamo neki likovi&#8221; koji žele da se prave pametni&#8230; E kad na to dodamo ?injenicu da je instalacija u tekstualnom modu, i da ne postoje gotovo nikakvi grafi?ki alati za konfiguraciju, ve?ina potencijalih novih korisnika ve? diže ruke od ove distribucije&#8230; E ja se nadam da ?u bar malo to promijeniti sa ovim tekstom&#8230; ina?e sav ovaj tekst se odnosi na Slack10, ali ne bi trebalo da bude nekakve razlike i za ostale&#8230; a trebao bi da bude koristan prije svega za one koji ne vladaju baš engleskim jezikom, pa su prepušteni doma?im forumima na volju&#8230; &#8222;_<!--break-->

_Malo istorije 🙂  
Za neupu?ene Slackware je najstarija distribucija, koja je i dan danas preživjela. Pokrenuo ju je Patrick Volkerding, ina?e živa legenda open source zajednice, jedan od rijetkih kojih sve radi isklju?ivo volonterski, tj. iz ideoloških razloga (a ne kao neki koji bi za mnogo manje truda htjeli nekakvu nadoknadu&#8230;), koji i pored ozbiljno ugroženog zdravlja i dan danas nastavlja svoj rad. Ina?e Slackware je sleng rije? i ozna?ava slobodu, nezavisnost i mogu?nost slobodnog razmišljanja, što u današnjem svijetu postaje sve manje mogu?e. Slackware predstavlja sve ono što je GNU/Linux trebao biti, a što o?igledno svakim danom sve manje jeste. Takav kakav je suo?en je da &#8220;nigdje nije pristao&#8221;, tj. kao korisnici primjeti?ete da nidje ne postoji specijalizirani Slackware forum, ve? ste prisiljeni kao nomadi šlepati se uz ove komercijalne varijante. To je ina?e posljedica same prirode ove distribucije&#8230; nego da ne dužimo&#8230;</p> 

Instalacija

Kao prvo trebate nabaviti instalacione CD-ove (2-4), i podesiti da se sistem podiže sa CD-a (naj?eš?e u BIOS-u, mada može postojati i nekakva pre?ica na tastaturi). Prije toga bi možda trebali smanjiti potoje?e particije (sa Windowsom) pomo?u nekog specijaliziranog alata, da bi smanjili vjerovatno?u gubitka podataka. Prilkom podizanja sistema dobi?ete nekoliko jednostavnih poruka, pri ?emu je najvažnije koji ?ete kernel koristiti prilkom instalacije. Ako imate standardnu desktop &#8220;kantu&#8221;, najvjerovatnije da ?e sa bare.i kernelom sve dobro pro?i. Zatim dobijate root shell, kojim se obavlja ostatak instalacije. Ako imamo slobodnog (neformatiranog) prostora na disku, a trebali bi ako smo smanjili neku od particija, trebamo napraviti linux particije. To možemo obaviti pomo?u program?i?a cfdisk, tj. pokre?emo

cfdisk /dev/hda

(hda-pri master, hdb-pri slave, hdc-sec master, hdd-sec slave), a zatim dobijemo spisak postoje?ih particija, kao i informaciju o slobodnom prostoru (free space), koga ?emo particionisati. Treba nam swap i glavna particija. Veli?ina swap-a zvisi ponajviš o koli?ini RAM-a. Nekada je važilo duplo više, dok je danas situacija potpuno obrnuta. Zna?i više RAM-a, manji swap. Za 256 MB, nekih 200-300 MB swap prostora ?e biti dovoljno (osim ako ne mislite igrati neke igre, tipa UT :), dok recimo za 768 MB možeti staviti i manje od 100 MB&#8230; U ovom slu?aju, u 99% vremena swap ?e biti u potpunosti neiskorišten, a onaj 1% zauze?e ne?e biti ve?e od par MB. Kreiramo je tako što odaberemo New, a zatim Type 82 (Type 83 za glavnu particiju). Preporu?ljivo je da budu logi?ke particije. Zatim idemo na Write, pa na Quit.  
Sada pokre?emo setup. Naravo, ponovno dobijamo tekstualno su?elje sa opcijama. Primjeti?ete da za svaku postoji dataljan opis. Prva bitna nam je Adswap, gdje dodajemo particiju koju smo pripremili. Zatim ide Target gdje odabiramo glavnu particiju, na koju ?e biti izvršena instalacija. Poslije toga moramo odabrati Filesystem. Smatra se da su ext2&ext3 pouzdaniji (ali manje efikasni u pogledu korištenja prostora), dok se za reiserfs smatra da je brži. Poslije formatiranja dobijemo opciju da dodamo Windows particije i mijesta na kojima ?e biti mount-ovane. Kao izvor instalacije, setup ?e automatski pretražiti sve periferije i na?i ureÄ‘aj koji koristimo. Zatim ide odabir paketa koje želimo instalirati. Å ta ?ete izostaviti zavisi od vas samih, ali krajnje preporu?ljivo izvršiti potpunu instalaciju, jer je samo tako sigurno da su sve ovisnosti zadovoljene (tj. poštedi?ete sebe velike glavobolje ako tako uradite, jer na Slack-u ne postoji alat koji se brine o meÄ‘uzavisnostima paketa Smile ).  
  
Zatim se to sve instalira, poslije ?ega nas do?ekuje odabir kernela koji ?e biti postavljen na sistem. Ovdje opet zavisi od konfiguracije, ali može vam se desiti problem tipa da ra?unar ne želi da se ugasi, ukoliko odaberete bare.i, zbog toga odaberite bareacpi.i, ili šta vam ve? odgovara. Ina?e imena kernela govore dosta sama za sebe. 

Zatim se nastavlja konfigurisanje sistema. Zatim dobijemo pitanje da li želimo napraviti boot disketu. Ovo je preporu?ljivo, ali nije neophodno. Sljiedi pitanje u vezi sa modemom. Ovo ima zna?aj jedino ako imate hardverski modem, ina?e slobodno presko?ite. Zatim par pitanja o mišu, hardverskom satu, slovima koja ?e biti korištena u konzoli.  
Zatim ide možda i &#8220;najopasniji dio&#8221;. Instalacija bootloader-a (LILO). Odaberemo expert podešavanja, i konfigurišemo korak po korak. Zna?i odaberemo Linux particiju, zatim dodamo Windows particije, damo im odgovaraju?e oznake. Jako je bitno dodati hdx=ide-scsi, ako imamo CD/DVD reza?, a odlu?ili smo da koristimo kernel 2.4. Zatim ga instaliramo, najbolje u MBR, mada ?e vas upozoriti da je to potencijalno opasan korak (ali nije Smile ).  
Zatim ide i podešavanje mrežnih postavki, koje možete presko?iti i obaviti kad god želite pomo?u komande netconfig. Zatim birate servise koji ?e biti pokrenuti. Radi ve?e sigurnosti i brzine sistema preporu?ljivo je svesti ih na minimum. Tako da vam sigurno ne trebaju CUPS i lprng zajedno (za štampanje), ne treba vam samba ako niste umreženi, i sli?no. Najvažnije je i ako pogriešite da kasnije vrlo lako to možete popreviti, tj. uklju?iti/isklju?iti dati servis. O tome nešto kasnije.  
Zatim odreÄ‘ujemo grafi?ko su?elje koje ?emo koristiti. Ovde je izbor ?isto vaš. Možda je KDE za nijansu bolje od ostalih, prije svega jer kompenzira (u nekoj mjeri) nedostatak grafi?kih alata za konfiguraciju sa sopstvenim. Kasnije ga možete promijenit komandom xwmconfig, kojom ?e te dobiti ovaj isti prozor za konfigurisanje. Zatim dobijete opciju da postavite root lozinku. Poslije toga restartujete ra?unar (ctrl+alt+delete), i poslije par trenutak strepnje sistem se podiže, naravno, bez problema. Logujete se u konzoli, nakon ?ega možete (a i ne morate) dodati korisnika komandom adduser. Ina?e Slackware se instalira ponajviše sa ciljem da se nešto nau?i, a pri tome ?ete uglavnom morati imati root ovlasti, tako da ako samo vi koristite ra?unar, možete i presko?iti ovaj korak (mada to uglavnom nije preporu?ljivo za svakodnevni rad). Zatim još preostaje da konfigurišemo grafi?ko su?elje, najbolje komandom xorgconfig. Trebate paziti na maksimalnu rezoluciju, frekvenciju monitora (pogotovo vertikalnu, 60Hz je &#8220;sigurna&#8221; vrijednost) i grafi?ku karticu. I to je to. Ostaje nam samo još da ukucamo startx i podignemo grafi?ko okruženje.

Å ta dalje?

Dalje o uglavnom stvarima koje ?e vam najviše trebati, i o specifi?nostima Slack-a. Jako bitna stvar je da se snalazite sa konzolom, tj. da znate bar neke osnovne komande, preusmjeravanje, piping, i ostalo&#8230; ali to je zajedni?ka stvar za sve distribucije. Jedina razlika je što ?e vam ovdje biti nephodne 🙂 . Slijede naj?eš?a pitanja.

Å½elim se logovati iz grafi?kog su?elja&#8230;  
Treba promijeniti u datoteci /etc/inittab slede?i red  
id:3:initdefault u  
id:4:initdefault  
Ina?e init je prvi proces koji se izvršava prilikom podizanja sistema (otkucajte ps ax | grep 1), a on ?ita ono što se nalazi u initttab-u, koji mu govori u koji runlevel da ide, i gdje se konfiguracija za dati runlevel nalazi.

Å ta su runlevel-i?  
Runlevel je definisan od strane servisa koji su dostupni u datom trenutku, tj. za vrijeme izvršavanja datog runlevel-a. Evo šta koji predstavlja:  
  
runlevel 0 = zaustavljanje sistema  
  
runlevel 1 = jednokorisni?ki režim rada, koristi se za održavanje sistem  
  
runlevel 2 = ne koristi se na Slack-u  
  
runlevel 3 = multikorisni?ki režim rada sa login-om u konzoli  
  
runlevel 4 = multikorisni?ki režim rada sa grafi?kim okruženjem  
  
runlevel 5 = ne koristi se  
  
runlevel 6 = restart  
  
runlevel S ili s = jednokorisni?ki runlevel

Konfiguracija runlevel-a i ostalih servisa, BSD init skripte. Runlevel init skripte se nalaze u direktorijumu /etc/rc.d. Ovo je ina?e BSD na?in skripti, i Slack ga koristi po ugledu na BSD. Ostale GNU/Linux distribucije koriste System V init skripte. Ovo je ina?e i jedan od vje?nih &#8220;krstaških ratova&#8221; informati?ara, tj. pitanje koji je bolji. Pošto mi koristimo Slack, bolji je onaj BSD Smile . Drugi &#8220;krstaški rat&#8221; je rasprava: Å ta je bolje vi ili emacs Smile . Runlevel skripte su redom:

rc.0 = simboli?ki link na rc.6  
  
rc.M = zajedni?ka za višekorisni?ke runlevel-e 2 i 3  
  
rc.K = runlevel administratora, jednokorisni?ki  
sistem rada  
  
rc.S = inicijalizacijska skripta sistema  
  
rc.4 = za runlevel 4, podiže sistem direktno u grafi?ko okruženje

rc.6 = skripta koja se izvršava, prilokom restarta/gašenja re?unara  
Ostatak rc.* datoteka su servisi kao što su Samba, Apache, PCMCIA&#8230; Servisi se izvršavaju prilkom podizanja sistema, pod uslovom da su izvršni.

Kako uklju?iti/isklju?iti servis  
Komandom chmod 754 ime\_servisa uklju?iti a sa chmod 644 ime\_servisa isklju?iti. Ovo je jedan od na?ina.

Kako osposobiti hardver koji ne radi?  
Najbolji na?in je nabavka najnovijeg kernela i kompajliranje, iz prostog razloga što prili?an broj stvari nije uklju?en u onaj default-ni. Za po?etnike najve?e razo?arenje predstavlja ?injenica da im zvu?na kartica ne?e nikako ne radi, ili nešto sli?no, i zna se ?ak desiti da zbog toga odustanu od ove distibucije. Nije preporu?ljivo kompajlirati ve? postoju?i kernel, jer se može lako desiti da nešto krene pogrešno, i onda imamo mrtav sistem.

Kako kompajlirati kernel?  
Nešto sam ve? napisao, tako da se ne ponavljam. Pogledajte na adresi  
<http://www.lugzdk.ba/dokumentacija/kompajliranje_kernela.pdf>  
Obratite pažnju na to da kernel 2.6 koristi modprobe.conf umjesto modules.conf.

Eto zasad toliko. Nadam se da ?e nekom pomo?i&#8230; Naravno ima toga još mnogo, ali ne?u dalje ništa da pišem iz razloga što je mogu?e da je to ve? spomenuto na ovom forumu&#8230; a ako imate nekih sugestija i komentara slobodno ih napišite&#8230; ili još bolje napišite i vi nešto sli?no&#8230; 🙂</i>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=751)