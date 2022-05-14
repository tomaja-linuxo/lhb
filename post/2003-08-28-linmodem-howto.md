---
author: tomaja
date: "2003-08-28T17:24:13Z"
excerpt: 'Odli?an tekst koji je napisao brankilla. Radi se o objašnjenju kako podesiti
  modem i dial up konekciju. Tekst je i odli?no grafi?ki obraÄ‘en tako da vrlo slikovito
  i dobro opisuje sam postupak. '
guid: https://forum.linuxo.org/2003/08/28/linmodem-howto/
id: 369
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linmodem-HOWTO
url: /linmodem-howto/
---
Odli?an tekst koji je napisao brankilla. Radi se o objašnjenju kako podesiti modem i dial up konekciju. Tekst je i odli?no grafi?ki obraÄ‘en tako da vrlo slikovito i dobro opisuje sam postupak. <!--break-->

<div type="HEADER">
  <p style="margin-bottom: 0cm;">
    *Information wants to be FREE*
  </p>
</div>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  LINMODEM HOW-TO &nbsp;&nbsp;<br /> &nbsp;&nbsp; &nbsp;&nbsp; <img
 src="http://www.mandrake.co.yu/images/linmodems/TUX.png" title=""
 alt="" style="width: 67px; height: 84px;" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  *Namena ovog<br /> dokumenta je da svima onima koji su u trenutku neznanja kupili &#8220;<br /> jeftin, a dobar&#8220; softmodem omogu&#263;i da ga pokrenu pod pravim OS-om,<br /> GNU/Linux-om : ). Naravno, za to &#263;e vam pre svega biti potreban<br /> odgovaraju&#263;i drajver, koji moÂžete na&#263;i i download-ovati sa lokacije <a
 href="http://www.linmodems.org/">http://www.linmodems.org</a>. Sa ovog<br /> sajta moÂžete skinuti i sktiptu scanmodem koja &#263;e vam re&#263;i da li je vaÂš<br /> modem podrÂžan. Ne&#263;e baÂš svi imati sre&#263;e, jer vlasnici novih Lucent/Agere<br /> softmodema na primer,naj&#269;eÂš&#263;e ne mogu da iskoriste Lucent drajver, jer<br /> ovaj se odnosi na Lucent LT winmodeme ( zato sam ja zamenio Agere za LT<br /> ; ) ). Conexant modemi su tako&#273;e podrÂžani, i na sajtu <a
 href="http://www.linuxant.com/">http://www.linuxant.com</a> moÂžete<br /> prona&#263;i kvalitetne drajvere za ove modeme; ovaj how-to &#263;e pre svega<br /> govoriti o ova dva modela, jer sa njima imam direktnog iskustva, ali bi<br /> trebalo da podeÂšavanja budu dovoljno sli&#269;na i za druge modele softmodema.
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  START
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  *Pre svega, morate<br /> instalirati kernel source, jer bez njega drajver ne&#263;e funkcionisati, a<br /> zatim instalirajte KPPP, program koji &#263;e vam posluÂžiti da izvrÂšite<br /> potrebna podeÂšavanja i da se konektujete na Internet. Ako instalirate<br /> drajver u *rpm obliku, najjednostavniji na&#269;in je dvoklik na dati fajl,<br /> posle kojeg &#263;e se pojaviti dijalog koji traÂži upisivanje root lozinke;<br /> upiÂšite lozinku i pritisnite OK, zatim potvrdite da Âželite instalaciju,<br /> a takodje recite OK kada budete pitani da li Âželite da instalirate ovaj<br /> fajl bez PGP klju&#269;a. Takodje, instalacija se moÂže obaviti i iz komandnog<br /> okruÂženja, kada ukucate rpm -ivh imefajla.rpm. Ako imate fajl u<br /> tar.gz/bz2/tgz obliku, pratite uputstva koja se nalaze u paketu. Kada<br /> instalirate drajver i pokrenete KPPP, dobi&#263;ete slede&#263;i dialogue box:
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot23.png"
 name="Graphic1" align="left"
 style="border: 0px solid ; width: 437px; height: 275px;" title=""
 alt="" /><br clear="left" />
</p>

<p style="margin-bottom: 0cm;">
  Da biste napravili funkcionalnu<br /> konekciju, pritisnite dugme setup i vide&#263;ete slede&#263;e :
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/linmodems/snapshot2.png"
 name="Graphic2" align="left"
 style="border: 0px solid ; width: 454px; height: 239px;" title=""
 alt="" />
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Izaberite dugme<br /> Dialogue Setup a zatim, po otvaranju novog dijaloga, prvu karticu, tj.<br /> Dial; tu &#263;ete upisati ime konekcije u prvom praznom polju, zatim<br /> kliknuti na Add i upisati broj telefona svog provajdera.Ostala polja<br /> ostavite kao Âšto vidite na slici.
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot3.png"
 name="Graphic3" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<div style="text-align: justify;">
  Tri naredne kartice su IP, Gateway i<br /> DNS; tu &#263;ete izabrati 1) Dynamic IP address, 2) Default gateway i 3)<br /> Automatic. U slu&#269;aju da vaÂš provajder koristi DNS servere, &#269;ekirajte<br /> opciju Manual i unesite adrese servera tako Âšto &#263;ete ih upisati u prazno<br /> polje, a zatim kliknuti na Add. U primeru na slici date su adrese DNS<br /> servera provajdera PTT; ukoliko posle konektovanja nije mogu&#263;e<br /> surfovanje i otvaranje web stranica, editujte datoteku /etc/resolv.conf<br /> upisuju&#263;i
</div>

<p style="margin-bottom: 0cm;">
  nameserver 212.62.32.1
</p>

<div style="text-align: justify;">
  nameserver 212.62.32.5, za PTT,<br /> odnosno odgovaraju&#263;e adrese svog provajdera.
</div>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot4.png"
 name="Graphic4" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br /> <br clear="left" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot5.png"
 name="Graphic5" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
  *Gateway
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot6.png"
 name="Graphic6" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br clear="left" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot7.png" title=""
 alt="" style="width: 424px; height: 476px;" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Slede kartice Login<br /> Script i Execute koje &#263;ete ostaviti praznim; NE UPISUJTE niÂšta, jer bi<br /> tu trebalo da se nalaze skripte i komande koje naÂše mreÂže ne podrÂžavaju<br /> pa biste samo mogli da pokvarite posao.
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot8.png"
 name="Graphic7" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot9.png"
 name="Graphic8" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<div style="text-align: justify;">
  Naredna kartica nosi naziv Accounting<br /> i sluÂži za pra&#263;enje potroÂšnje telefonskih impulsa dok ste na Internetu;<br /> u pitanju je opciona kartica, jer ova mogu&#263;nost nije neophodna, ali<br /> budu&#263;i da je i Jugoslavija na listi podrÂžanih zemalja, moÂžete izabrati<br /> Enable accounting i na listi odrediti da li &#263;ete pratiti cenu poziva na<br /> lokalnoj, me&#273;ugradskoj ili 041 mreÂži.
</div>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot10.png"
 name="Graphic9" align="left"
 style="border: 0px solid ; width: 424px; height: 476px;" title=""
 alt="" /><br /> <br clear="left" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Kada je podeÂšavanje<br /> IP naloga klikom na OK zavrÂšeno, predjite na dijalog KPPP Configuration,<br /> i izaberite karticu Device &#8211; tu &#263;ete odabrati gde vam se nalazi modem,<br /> Âšto &#263;e naj&#269;eÂš&#263;e biti na /dev/modem, jer pri instalaciji drajvera Linux<br /> po pravilu automatski pravi simboli&#269;ku vezu ka toj lokaciji. Kontrolu<br /> protoka stavite na hardware, prekid linije CR, a brzinu veze na 57600,<br /> Âšto su ina&#269;e i ponu&#273;ene vrednosti.&#268;ekirajte opciju use lock file i<br /> ostavite modem timeout na 60 sekundi.
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot11.png"
 name="Graphic10"
 style="border: 0px solid ; width: 350px; height: 416px;" title=""
 alt="" />
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Slede&#263;a kartica je<br /> bitna; u pitanju je kartica Modem. Za ve&#263;inu modema treba od&#269;ekirati<br /> opciju Wait for dial tone da bi ovaj uopÂšte po&#269;eo da bira broj. Slede&#263;e<br /> Âšto treba uraditi<br /> je pritisnuti dugme Modem Commands gde treba promeniti<br /> par komandi da bi izgledale kao na slikama; u polju Initialisation<br /> string treba da stoji ATX3, dok za tonsku centralu Dial string mora da<br /> bude ATDT, a za pulsnu ATDP.
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot12.png"
 name="Graphic11"
 style="border: 0px solid ; width: 350px; height: 416px;" title=""
 alt="" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  *Izgled komandne table za konekciju preko tonske centrale
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot15.png"
 name="Graphic12" align="left"
 style="border: 0px solid ; width: 609px; height: 679px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  *Izgled komandne table za konekciju<br /> preko pulsne centrale
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot14.png"
 title="" alt="" style="width: 609px; height: 643px;" />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Me&#273;utim, sve ovo ne<br /> vredi vam previÂše ako instalacija modema nije uspela, odn. ako modem<br /> nije prepoznat. To &#263;ete najbolje proveriti ako pritisnete dugme Query<br /> modem&#8230; &#8211; ako sve bude u redu vide&#263;ete poruku &#8222;modem ready&#8220; i<br /> o&#269;itavanja ATI &#8211; ja, posle kojih &#263;e uslediti neÂšto poput ovoga na slici.<br /> NaÂžalost, moÂže se desiti da vam KPPP poÂšalje poruku &#8222;unable to open<br /> modem&#8220;; ovo naj&#269;eÂš&#263;e zna&#269;i da ste neÂšto propustili , zato proverite da<br /> li ste instalirali kernel i drajvere, ili probajte da skriptom<br /> scanmodem utvrdite da li je vaÂš modem podrÂžan. Ponekad je potrebno<br /> restartovati maÂšinu da bi stvari doÂšle na svoje mesto. Takodje,u<br /> slu&#269;aju da imate ovih problema kada su u pitanju Conexant modemi, u<br /> konzoli posle instalacije drajvera otkucajte hsfconfig, odn.<br /> hcfpciconfig, u zavisnosti koji model modema imate. MoÂže biti korisna i<br /> komanda lspci jer &#263;ete videti kako sistem prepoznaje vaÂš modem.U<br /> slu&#269;aju Agere modema, Query moÂže dati naizgled uspeÂšne rezultate, ali<br /> ne&#263;ete sti&#263;i dalje od prozora na kome piÂše dialling &#8230;, dok modem u<br /> stvari ne okre&#263;e broj; dobi&#263;ete poruku NO CARRIER, Âšto je kona&#269;ni dokaz<br /> da vaÂš model ne moÂže da radi sa ovim drajverom.
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot13.png"
 name="Graphic14" align="left"
 style="border: 0px solid ; width: 286px; height: 289px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  Slede&#263;a kartica je bez zna&#269;aja i moÂžete<br /> je ostaviti nepromenjenom:
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot16.png"
 name="Graphic15" align="left"
 style="border: 0px solid ; height: 416px; width: 350px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm; text-align: justify;">
  Poslednja kartica<br /> je Misc gde moÂžete podesiti ponaÂšanje KPPP- a po uspostavljanju veze,<br /> tako da se pojavi u panelu po konektovanju, automatski ponovo okrene<br /> broj ako se veza prekine i sli&#269;no.
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot17.png"
 name="Graphic16" align="left"
 style="border: 0px solid ; width: 334px; height: 394px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
</p>

<div style="text-align: justify;">
  Kada ste sve ovo zavrÂšili, spremni<br /> ste za prvo povezivanje na Internet iz GNU/Linux-a. PoÂšto se pojavi<br /> glavni dijalog, upiÂšte svoje korisni&#269;ko ime i Âšifru, i pritisnite dugme<br /> Connect .
</div>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot18.png"
 name="Graphic17" align="left"
 style="border: 0px solid ; width: 415px; height: 230px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  Ako je sve u redu, &#269;u&#263;ete kako modem<br /> okre&#263;e broj i videti slede&#263;e prozore programa KPPP:
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot19.png"
 name="Graphic18" align="left"
 style="border: 0px solid ; width: 332px; height: 105px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
  <img
 src="http://www.mandrake.co.yu/images/linmodems/snapshot21.png"
 name="Graphic19" align="left"
 style="border: 0px solid ; width: 410px; height: 402px;" title=""
 alt="" /><br clear="left" /><br />
</p>

<p style="margin-bottom: 0cm;">
</p>

<p style="margin-bottom: 0cm;">
  Po uspostavljanju veze, startujte svoj<br /> omiljeni browser, i iskusite lepotu sigurnog surfovanja iz GNU/Linux-a.<br /> UÂživajte!
</p>

<p style="margin-bottom: 0cm; font-style: italic;">
  *Best viewed in Mozilla & Konqueror*
</p>

<p style="margin-bottom: 0cm;">
</p>

* Made in mdk9.1 GNU/Linux using ooffice & Mozilla Composer by  
BrainkillA *

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=369)