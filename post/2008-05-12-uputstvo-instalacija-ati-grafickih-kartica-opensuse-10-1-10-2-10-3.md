---
author: gandalf
date: "2008-05-12T16:41:19Z"
excerpt: <p>Po&scaron;to se uglavnom svi muce sa ATI drajverima za Linux, evo jedno
  veoma malo i lagano re&scaron;enje za OpenSuse korisnike. Samo sledite sledeća uputstva
  i sve ce biti ok (nadam se)... Uđete u Yast, i dodate sledece repozitorijume.<br
  /><br /> Za verziju 10.3 &gt;&gt;&gt; <a href="http://www2.ati.com/suse/10.3" target="_blank">http://www2.ati.com/suse/10.3</a><br
  /> <br /> Za verziju 10.2 &gt;&gt;&gt; <a href="http://www2.ati.com/suse/10.2" target="_blank">http://www2.ati.com/suse/10.2</a><br
  /> <br /> Za verziju 10.1 &gt;&gt;&gt; <a href="http://www2.ati.com/suse/sle10"
  target="_blank">http://www2.ati.com/suse/sle10</a><br /><br /> Uđete u bilo koji
  terminal i kao root ukucate sledecu komandu:<strong> <span class="quote">yast2&nbsp;--install&nbsp;x11-video-fglrxG01&nbsp;ati-fglrxG01-kmp-`uname&nbsp;-r
  </span></strong><br /><strong><span class="quote">|&nbsp;awk&nbsp;-F&quot;-&quot;&nbsp;&#39;{print&nbsp;$NF}&#39;`</span></strong><span
  class="quote">(upisati sve kao jednu liniju/naredbu)</span> <br />Kada se instalacija
  zavr&scaron;i, isto kao root kucate sledeću komandu :&nbsp;&nbsp; <strong><span
  class="quote">sax2&nbsp;-r</span></strong>Kada zavr&scaron;ite sa konfigurisanjem
  sax-a , restartujte X. Kako se resetuje X? Ctrl+Alt+Backspace, kada se X ponovo
  podigne opet u bilo kom terminalu kucajte sledeće :<strong><span class="quote">glxgears</span></strong>
  To bi bilo to, uživajte, ako neko bude imao problema čudne prirode neka se javi
  u ovoj temi.&nbsp;</p>
guid: https://forum.linuxo.org/2008/05/12/uputstvo-instalacija-ati-grafickih-kartica-opensuse-10-1-10-2-10-3/
id: 2016
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Uputstvo &#8211; Instalacija ATI grafičkih kartica &#8211; OpenSuse 10.1, 10.2,
  10.3
url: /uputstvo-instalacija-ati-grafickih-kartica-opensuse-10-1-10-2-10-3/
---
Po&scaron;to se uglavnom svi muce sa ATI drajverima za Linux, evo jedno veoma malo i lagano re&scaron;enje za OpenSuse korisnike. Samo sledite sledeća uputstva i sve ce biti ok (nadam se)&#8230; Uđete u Yast, i dodate sledece repozitorijume.

Za verziju 10.3 >>> <a href="http://www2.ati.com/suse/10.3" target="_blank">http://www2.ati.com/suse/10.3</a>

Za verziju 10.2 >>> <a href="http://www2.ati.com/suse/10.2" target="_blank">http://www2.ati.com/suse/10.2</a>

Za verziju 10.1 >>> <a href="http://www2.ati.com/suse/sle10" target="_blank">http://www2.ati.com/suse/sle10</a>

Uđete u bilo koji terminal i kao root ukucate sledecu komandu: **<span class="quote">yast2&nbsp;&#8211;install&nbsp;x11-video-fglrxG01&nbsp;ati-fglrxG01-kmp-`uname&nbsp;-r </span>**  
**<span class="quote">|&nbsp;awk&nbsp;-F"-"&nbsp;'{print&nbsp;$NF}'`</span>**<span class="quote">(upisati sve kao jednu liniju/naredbu)</span>  
Kada se instalacija zavr&scaron;i, isto kao root kucate sledeću komandu :&nbsp;&nbsp; **<span class="quote">sax2&nbsp;-r</span>**Kada zavr&scaron;ite sa konfigurisanjem sax-a , restartujte X. Kako se resetuje X? Ctrl+Alt+Backspace, kada se X ponovo podigne opet u bilo kom terminalu kucajte sledeće :**<span class="quote">glxgears</span>** To bi bilo to, uživajte, ako neko bude imao problema čudne prirode neka se javi u ovoj temi.&nbsp;

<!--break-->

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2016)