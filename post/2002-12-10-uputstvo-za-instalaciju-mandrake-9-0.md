---
author: tomaja
date: "2002-12-10T21:19:55Z"
excerpt: |
  Primetio sam da fali jedno pravo pocetnicko-korisnicko uputstvo za instaliranje Mandrake-a 9.0, pa ?u ga sad izložiti.Kad god sam radio na ovaj nacin, uvek mi je uspela instalacija:
  <br />
  Kao prvo i osnovno PREPORU?UJEM da se pre svega hard disk podeli na dve particije. Veli?inu particije za Linux odredite sami, ali bi bilo najbolje da bude 3 do 3,5 Gb.
guid: https://forum.linuxo.org/2002/12/10/uputstvo-za-instalaciju-mandrake-9-0/
id: 248
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Uputstvo za instalaciju Mandrake 9.0
url: /uputstvo-za-instalaciju-mandrake-9-0/
---
Primetio sam da fali jedno pravo pocetnicko-korisnicko uputstvo za instaliranje Mandrake-a 9.0, pa ?u ga sad izložiti.Kad god sam radio na ovaj nacin, uvek mi je uspela instalacija:  
  
Kao prvo i osnovno PREPORU?UJEM da se pre svega hard disk podeli na dve particije. Veli?inu particije za Linux odredite sami, ali bi bilo najbolje da bude 3 do 3,5 Gb.

<!--break-->Ako Linux ne?e da se podigne sa CD-a, napravite boot disketu na slede?i na?in:

1. ubacite instalacioni CD1, zatim otvorite &#8222;My Computer&#8220;, desni klik na CDROM drive ikonu i odaberete &#8222;Open&#8220;  
  
2. odete na &#8222;dosutils&#8220; direktorijum i dupli klik na &#8222;rawwritewin&#8220; ikonu  
  
3. ubacite prazan floppy u floppy drive  
  
4. odaberete &#8222;D:imagescdrom.img&#8220; u &#8222;Image File&#8220; polju (pod pretpostavkom da je &#8222;D:&#8220; CDROM drajv, a ako ne &#8222;D:&#8220; zamenete pravim slovom koje predstavlja CDROM drajv)  
  
5. odaberete &#8222;A:&#8220; u &#8222;Floppy Drive&#8220; polju i onda kliknete na &#8222;Write&#8220;.

Zatim sledi instalacija. Ostavite i CD1 i floppy u ra?unaru i restartujte ga. NAPOMENA: da bi ovo radilo, pre toga morate oti?i u BIOS i podesiti da se ra?unar prvo podiže sa floppy disk-a! Nadam se da za ovo ne treba uputstvo.

Sada kre?e prava pri?a:

1. Kad se podigne instalacioni program za Mandrake 9.0, prvo ?e Vas pitati koji jezik želite da koristite prilikom instalacije, ostavite engleski,  
  
2. Prilikom odabira na?ina instalacije, pretpostavljena vrednost je RECOMENDED, ali Vi odaberite EXPERT mode,  
  
3. Posle toga ce Vam tražiti da odaberete SCSI diskove, pa ako ih nemate (kao što ih ni ja nemam), kliknete na NO,  
  
4. Slede?i bitan korak je odabir particije. Tu ?ete videti Vaše dve particije pod imenima mnt/windows\_c i mnt/windows\_d. Odaberite klikom na nju, particiju mnt/windows_d i u opcijama koje ?e se tad pojaviti sa leve strane odaberite Mount point da bude /, Type da bude Linux native i ako je particija npr. 3,5Gb, uradite Resize gde možete kliza?em definisati kolika ?e Vam biti Linux particija. Preporu?ujem da to bude vrednost oko 3Gb. Nakon toga na ostatku slobodnog prostora kreirajte Swap particiju i to klikom na slobodni prostor, a u meniju koji se nakon toga dobija samo definišete Type kao Linux swap. Kad ste sve završili, kliknete na DONE,  
  
5. Zatim sledi odabir instalacionih paketa. Za osnovno upoznavanje odaberite: Office Workstation, Game Station, Multimedia Station, Internet Station i Development Station. Ovo poslednje je bitno zbog kasnijeg instaliranja ( kompajliranja ) odgovaraju?ih kernela za Nvidia grafi?ke kartice i sli?no.  
  
6. TakoÄ‘e se u istom prozoru odabira i grafi?ko okruženje ( Graphical Enviroment )koje ?e se pojaviti nakon instalacije. Predložene opcije su KDE i GNOME, ali slobodno možete odabrati i tre?u opciju,  
  
7. Nakon ovog se od Vas traži da detaljno potvrdite Vaš malopreÄ‘ašnji izbor, pa to i uradite otvaranjem podmenija na Workstation i Graphical Enviroment i otka?injanjem opcija koje Vam se nude. Kad to završite kliknete na Install,  
  
8. Tada dobijate prozor u kome piše: You have selected the following server(s): FreeWnn, MySQL, cups, postfix. &#8230;&#8230; Pa zatim pitanje: Do You really want to install these servers? Odaberite šta god želite, ne uti?e bitno na rad Mandrake-a posle instalacije, a ni na samu instalaciju,  
  
9. Nakon toga kona?no instalacija po?inje. Kad za to doÄ‘e vreme, Mandrake ?e izbaciti CD1 i zamoliti Vas da ubacite CD2, a nakon toga i CD3. Ovim podrazumevam da imate sva tri CD-a, a instalacija je ve? ovo proverila u jednom od ranijih koraka koje nisam spomenuo, a taj korak se zvao Searching for installation packages i tad Vam je bilo ponuÄ‘eno da odaberete, odnosno potvrdite koje instalacione CD-e imate,  
  
10. Slede?a stvar koja Vas ?eka je podešavanje root password-a. Ovo je OBAVEZNO! Nemojte nikako ostaviti tu opciju bez lozinke iako se i takva opcija nudi. Naravno tu lozinku dobro zapamtite jer je veoma bitna za kasniji rad!  
  
11. Odmah potom dolazi na red i kreiranje korisnika. TakoÄ‘e je OBAVEZNO! Unesete sve za ?ega postoje prazna polja i NIKAKO nemojte da date istu lozinku korisniku kao što je root lozinka. Kada ste uneli sve podatke, kliknete na DONE,  
  
12. Na red dolazi podešavanje mreže i tu je pretpostavljena vrednost automatski, ali nemojte to tako uraditi. Nako što poništite taj izbor, dobi?ete nov prozor za odabir vrste mreže/konekcije koju imate. Pretpostavljam da svi obi?ni korisnici koriste Normal Modem Connection, pa to i odaberite. U slede?em koraku ?e Vas pitati na kom COM portu se nalazi modem i onda osnovna podešavanja, ali to je ve? dovoljno o?igledno,  
  
13. Iza toga sledi Summary, gde možete promenuti podešavanja: miša, tastature, vremenske zone i printera.  
  
14. Slede?e je podešavanje boot loader-a i tu ostavite sve kao što je ponuÄ‘eno, jedino preporu?ujem da se Boot Loader Delay sa 10 pove?a na 15,  
  
15. Kona?no, ve? pri kraju dolazimo da podešavanja monitora i video karte. Prilikom odabira monitora, pokušajte da pod Vendors naÄ‘ete Vaš model, baza monitora je impresivna, a zatim treba da podesite i video kartu. Ako imate kao ja Nvidia GeForce 2 MX400 sa 64Mb SDRAM-a, instalacija ?e prepoznati NvidiaGeForce2MX400DDR(generic). Tu u ovom momentu pomo?i nema, tek nakon instalacije možete instaliranjem odgovaraju?ih drajvera dobiti stvarne perfomanse ove kartice. S obzirom da sam na tom polju pao ve? nekoliko puta, sa?ekajte drugi deo uputstva, koje ?e se odnositi samo na podešavanje video karte,  
  
16. Nakon ovoga je ostalo samo još nekoliko potvrda, instalacija se sama restartuje i to je to. Naravno, pre restarta izvadite floppy iz drajva, da se ne bi ponovo podigla instalacija. CD možete ostaviti, ali bi bilo dobro da i njega izvadite,  
  
17. Posle restarta se pojavljuje grafi?ki meni za odabir operativnog sistema koji želite da startujete i tu naravno odaberete Linux,  
  
18. Pošto odradi inicijalizaciju, do?i ?ete u First time wizard, koji možete a i ne morate presko?iti i još vrlo malo i otvori?e Vam se Vaše radno okruženje, pretpostavljam KDE, pošto je ono svuda prvo pri odabiru.  
  
19. Još jedna mala napomena, u KDE okruženju se sve otvara sa jednim klikom, što se naravno lako menja, ali za sada uživajte.

DOBRODOÅ LI U SVET MANDRAKE 9.0

P.S. Kao što ste možda primetili, neke sitnije korake sam ispustio, ali se nadam da su to stvari koje se manje više podrazumevaju. Svako ko je bar par puta instalirao/reinstalirao Windows ?e se veoma lako sna?i.  


Ako treba još neko pojašnjenje, pogledajte Forume u okviru ovog sajta, ili mi pošaljite pitanje. Napominjem da nisam Linux profesionalac, samo sam ovo što je napisano uradio nekoliko puta i to je ?isto li?no iskustvo.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=248)