---
author: tomaja
date: "2004-07-11T04:48:29Z"
excerpt: |
  <a href="http://www.linuxo.com/user.php?op=userinfo&amp;uname=zuja">zuja</a>
  piše: "<span style="font-style: italic;">Ovaj patch je odgovor Open
  Source zajednice na Linuxant drajvere za
  Conexant HCF/HSF modeme. Trebalo bi da radi sa drajverima verzije ve?e
  od 1.0</span><br style="font-style: italic;">
  <span style="font-style: italic;">Testiran je uspesno na HCF drajveru
  ver.
  hcfpcimodem-1.01lnxt04031300full. Patch koristite na sopstvenu
  odgovornost.</span><br style="font-style: italic;">
  <span style="font-style: italic;">Uputstvo za upotrebu</span>:
guid: https://forum.linuxo.org/2004/07/11/linuxant-drajveri-bez-ogranienja/
id: 479
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linuxant drajveri bez ograni?enja
url: /linuxant-drajveri-bez-ogranienja/
---
[zuja](http://www.linuxo.com/user.php?op=userinfo&uname=zuja)  
piše: &#8222;<span style="font-style: italic;">Ovaj patch je odgovor Open<br /> Source zajednice na Linuxant drajvere za<br /> Conexant HCF/HSF modeme. Trebalo bi da radi sa drajverima verzije ve?e<br /> od 1.0</span><br style="font-style: italic;" />  
<span style="font-style: italic;">Testiran je uspesno na HCF drajveru<br /> ver.<br /> hcfpcimodem-1.01lnxt04031300full. Patch koristite na sopstvenu<br /> odgovornost.</span><br style="font-style: italic;" />  
<span style="font-style: italic;">Uputstvo za upotrebu</span>:<!--break-->

<span style="font-style: italic;">1. Ukoliko ve? imate instaliran<br /> drajver bilo koje verzuje,<br /> DEINSTALIRAJTE ga. Ukoliko ne znate kako, konsultujte dokumentaciju,<br /> jer to nije tema ovog dokumenta. </span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">2. Idite na www.linuxant.com i<br /> skinite odgovaraju?i driver u tar.gz<br /> formatu, zna?i ne rpm za specifi?ne linux distribucije</span><br
style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">3. Otpakujte driver u neki folder sa</span><br
style="font-style: italic;" />  
<span style="font-style: italic;">tar -xzf vas_driver.tar.gz ili<br /> koristite ark, file roler ili bilo šta<br /> prigodno&#8230;</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">4. U otpakovani folder<br /> iskopirajte patch </span><br
style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">5. Ukoliko ste skinuli HSF<br /> Driver pokrenite samo ./hsfpatch<br /> bez ikakvih parametara. Sa?ekajte da završi svoj posao i da dobijete<br /> poruku o uspešnom patchovanju. Ukoliko ste skinuli HCF Driver<br /> pokrenite ./hsfpatch -c. Sa?ekajte da zavrsi<br /> svoj posao i da dobijete poruku o uspešnom patchovanju.</span><br
style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">6. Instalirajte driver. Ukoliko ne<br /> znate kako, konsultujte<br /> dokumentaciju, jer to nije tema ovog dokumenta. </span><br
style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">7. Po završetku instalacije potrebno<br /> je kao root pokrenuti<br /> konfiguracioni alat drivera</span><br style="font-style: italic;" />  
    <span style="font-style: italic;">hcfpciconfig<br /> &#8211; u slu?aju HCF<br /> drivera </span><br style="font-style: italic;" />  
    <span style="font-style: italic;">hsfpciconfig<br /> &#8211; u slu?aju HSF drivera</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">8. Kao zemlju u?ukati USA (ako<br /> se da greece ili sta drugo postoji<br /> sansa da ne?e da radi,</span><br style="font-style: italic;" />  
    <span style="font-style: italic;">bug se javlja samo<br /> kod patchovanog drajvera i to ne<br /> uvek, a sa USA uvek lepo radi)</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">9. Kao e-mail adresu<br /> dati: tux@kernel.org<br /> </span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">10. Kao registracioni kod<br /> dati: BADCAFE4742B</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">11. Odgovoriti na ostala pitanja (ako<br /> ih bude)</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">12. Neophodno je u vaš omiljeni<br /> dialer ubaciti init string odgovaraju?e</span><br
style="font-style: italic;" />  
<span style="font-style: italic;"><br /> sadržine ina?e ?e modem i dalje<br /> funcionisati na 14.400 k. Pod </span><br style="font-style: italic;" />  
<span style="font-style: italic;"><br /> pretpostavkom da koristite kpp:</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;"><br /> Sekvenca (init) 1 : AT<br /> &FW3+MS=V92,1,28800,33600,28800,56000 </span><br
style="font-style: italic;" />  
<span style="font-style: italic;"><br /> Sekvenca (init) 2 : ATX3</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">13. Ende</span><br
style="font-style: italic;" />  
<br style="font-style: italic;" />  
<span style="font-style: italic;">Patchovani driver možete arhivirati<br /> za neku kasniju upotrebu ili slanje<br /> dragim osobama</span><br style="font-style: italic;" />  
<span style="font-style: italic;">(niste ga platili pa ne moraju ni oni<br /> :)).</span><br style="font-style: italic;" />  
<br style="font-style: italic;" />  
  <span style="font-style: italic;">Driver<br /> hcfpcimodem-1.01lnxt04031300full je uspešno testiran sa<br /> sve patchom na slede?im </span><br style="font-style: italic;" />  
  <span style="font-style: italic;">distribucijama: Mandrake 9.1,<br /> Mandrake 10.0 , Slackware 8.1.<br /> Trebalo bi da radi na svim</span><br style="font-style: italic;" />  
  <span style="font-style: italic;">2.2 2.4<br /> i 2.6 kernelima. Pod Mandrakom<br /> 10.0 preporu?ujem upotebu 2.6.3-4mdkenterprise</span><br
style="font-style: italic;" />  
  <span style="font-style: italic;">kernela kao i Nvidia<br /> 6106 drivera (ko ima Nvidia karticu<br /> normalno). Pri toj kombinaciji ne dolazi</span><br
style="font-style: italic;" />  
  <span style="font-style: italic;">do izletanja 3rd party<br /> drivera. </span>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=479)