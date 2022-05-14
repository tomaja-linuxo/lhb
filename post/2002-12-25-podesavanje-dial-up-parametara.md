---
author: tomaja
date: "2002-12-25T20:21:25Z"
excerpt: |
  Uputstvo za podešavanje Dial-up parametara na Mandrake 9.0 OS i u KDE okruženju
  <br />
  <br />
  Klik na Start - Networking - Remote access - KPPP (Internet Dial-up Tool)
  <br />
  Opcija Podešavanja
  <br />
  Kartica Nalozi - opcija Novi
  <br />
  Dialog podešavanja (NE ?AROBNJAK)
  <br />
  Kartica Pozovi
guid: https://forum.linuxo.org/2002/12/25/podesavanje-dial-up-parametara/
id: 256
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Podešavanje Dial-up parametara
url: /podesavanje-dial-up-parametara/
---
Uputstvo za podešavanje Dial-up parametara na Mandrake 9.0 OS i u KDE okruženju

Klik na Start &#8211; Networking &#8211; Remote access &#8211; KPPP (Internet Dial-up Tool)  
  
Opcija Podešavanja  
  
Kartica Nalozi &#8211; opcija Novi  
  
Dialog podešavanja (NE ?AROBNJAK)  
  
Kartica Pozovi  
<!--break-->1. polje Naziv veze: EUnet

  
  
2. polje Broj telefona: 4897777(za Novi Sad) &#8211; Dodaj, ako ima još brojeva,  
  
ukucati ih ponovo u drugo polje i posle svakog klik na Dodaj.  
  
3. polje Na?in prijavljivanja: PAP/CHAP i ?ekirati opciju Sa?uvaj lozinku

Kartica IP  
  
Odabrati Dinami?ka IP adresa

Kartica Gateway  
  
Odabrati Predefinisani Gateway

Kartica DNS

1. Naziv domena: eunet.yu  
  
Zatim odabrati Podešavanje DNS servera: Ru?no  
  
2. IP adresa DNS servera: 194.247.192.33 &#8211; Dodaj, zatim ukucati slede?u  
  
194.247.192.1 pa Dodaj

Zatim klik na OK i to je prvi deo, pa povratak na KPPP Podešavanja i odabir  
  
kartice UreÄ‘aj  
  
1. Port modema: /dev/modem  
  
2. Kontrola toka: CRTSCTS  
  
3. Završetak linije: CR  
  
4. Brzina veze: zavisno od ra?unara, ja sam stavio 115200  
  
?ekirati opciju Zaklju?aj ureÄ‘aj

Zatim prelazak na karticu Modem u prozoru KPPP Podešavanja  
  
Klik na dugme Komande modema i tu treba da piše slede?e:  
  
1. Initialization string0: ATX3  
  
2. Initialization string1:  
  
3. Init odgovor: OK  
  
4. No Dial Tone Detection: ATX3  
  
5. String za povezivanje: ATDT (za tonsko biranje) ili ATDP (za pulsno biranje)  
  
6. Odgovor da je povezivanje u toku: CONNECT  
  
7. Odgovor da je linija zauzeta: BUSY  
  
8. Odgovor da nema carrier: NO CARRIER  
  
9. No Dial Tone Response: NO DIALTONE  
  
10. String za podizanje slušalice: +++ATH  
  
11. Odgovor da je slušalica podignuta: OK  
  
12. String za odgovor: ATA  
  
13. Odgovor da telefon zvoni: RING  
  
14. Odgovor da ste dobili vezu: CONNECT  
  
15. String za izlazak: +++  
  
16. Odgovor da izlazite: OK  
  
17. Ja?ina isklju?eno/nisko/visoko: M0L0/M1L1/M1L3  
  
Klik na OK i tada može da se testira modem odabirom odgovaraju?eg dugmeta.

Kada i to odradi, klik na OK dugme i zatim dugme Završi.

KRAJ



[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=256)