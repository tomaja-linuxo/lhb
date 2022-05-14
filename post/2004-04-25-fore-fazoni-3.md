---
author: tomaja
date: "2004-04-25T08:10:19Z"
excerpt: |
  Ovim kratkim upustvima možete u mnogome olakšati neke poslove i zadatke
  sa kojima se sre?ete prilikom rada na Linux sistemima. Kada je u
  pitanju rad sa fajlovima, procesima, itd. uvek se pitamo da li neke
  stvari mogu da se urade jednostavnije, jer ipak, koristimo  Linux
  a ne ko zna kakav drugi OS :) , e pa evo par "fora i fazona"
  koji uvek mogu biti od koristi:
guid: https://forum.linuxo.org/2004/04/25/fore-fazoni-3/
id: 439
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: '&#8222;Fore &#038; fazoni&#8220; (3)'
url: /fore-fazoni-3/
---
Ovim kratkim upustvima možete u mnogome olakšati neke poslove i zadatke  
sa kojima se sre?ete prilikom rada na Linux sistemima. Kada je u  
pitanju rad sa fajlovima, procesima, itd. uvek se pitamo da li neke  
stvari mogu da se urade jednostavnije, jer ipak, koristimo Linux  
a ne ko zna kakav drugi OS 🙂 , e pa evo par &#8222;fora i fazona&#8220;  
koji uvek mogu biti od koristi:<!--break-->

  
<span style="font-weight: bold;">1.<br /> </span><span style="font-weight: bold; text-decoration: underline;">Kovertovanje<br /> formata</span><span style="text-decoration: underline;"><br /> (jpg, gif,..)</span>

Kako da brzo i jednostavno konvertujete format a da ne morate da  
pokre?ete ve?e aplikacije (recimo gimp). Vrlo jednostavno, pomo?u  
komande <span style="font-style: italic;">convert . </span>Na primer,  
ukoliko imate jpg sliku image1.jpg a želite da je  
konvertujete u gif format to možete uraditi sa naredbom:  
<span style="font-style: italic;"><span style="font-weight: bold;">convert<br /> image1.jpg image1.gif </span> <br /> </span>Naravno, uvek pro?itajte i man stranicu <span
style="font-style: italic;">(man convert)</p> 

<p>
  </span><span style="font-weight: bold;">2. <span
style="text-decoration: underline;">Kako odrediti kom RPM paketu<br /> pripada odreÄ‘eni fajl ?</span></p> 
  
  <p>
    </span><br /> Ukoliko želite da otkrijete kojem rpm<br /> paketu pripada odreÄ‘eni fajl treba da pokrenete slede?u komandu:<br /> <span style="font-style: italic; font-weight: bold;">rpm -qf imefajla</span><br /> Ukoliko želite da vidite i informacije o samom paketu kojem taj fajl<br /> pripada pokrenite komandu:<br /> <span style="font-style: italic; font-weight: bold;">rpm -qfi imefajla</span><br /> Ukoliko želite da vidite sve fajlove koji pripadaju RPM paketu,<br /> pokrenite:<br style="text-decoration: underline;" /><br /> <span
style="font-style: italic; font-weight: bold; text-decoration: underline;">rpm<br /> -qlp<br /> ime_paketa.rpm</p> 
    
    <p>
      </span><span style="font-weight: bold;">3.<br /> </span><span style="font-weight: bold; text-decoration: underline;">Kako<br /> instalirati (iskompajlirati) SRPM pakete ?</p> 
      
      <p>
        </span>SRPM paketi predstavljaju softverske pakete sa izvornim<br /> programskim kodom. Da bi iskompajlirali i instalirali sadržaj src.rpm<br /> paketa morate pokrenuti komandu:<br /> <span style="font-style: italic; font-weight: bold;">rpm &#8211;recompile<br /> ime_paketa.src.rpm</span><br /> Ova naredba kompajlira izvorni kodi instalira binarne fajlove. Ukoliko<br /> želite da kreirate binarni, tj klasi?ni rpm paket morate pokrenuti rpm<br /> komandu sa slede?im parametrima:<br /> <span style="font-style: italic; font-weight: bold;">rpm &#8211;rebuild<br /> ime_paketa.src.rpm</span>
      </p>
      
      <p>
        <span style="font-weight: bold;">4. </span><span
style="font-weight: bold; text-decoration: underline;">Pronalaženje<br /> aktivnih procesa pomo?u komande </span><span
style="font-style: italic; font-weight: bold; text-decoration: underline;">pstree</span>
      </p>
      
      <p>
        Ukoliko ne možete da &#8222;ubijete&#8220; proces ?ak i sa naredbom <span
style="font-style: italic;">kill -9</span>, to zna?i da imate zombie<br /> proces i da ga ne možete ubiti sve dok ne ubijete osnovni proces. Da bi<br /> videli familije procesa pokrenite naredbu <br /> <span style="font-style: italic; font-weight: bold;">pstree</span><br /> Ve?ina distribucija je instalira po default-u. Ukoliko je nemate<br /> potražite je na linku <a href="http://psmisc.sourceforge.net">http://psmisc.sourceforge.net<br /> </a><br /> <br style="font-weight: bold;" /><br /> <span style="font-weight: bold;">5.</span> <span
style="font-weight: bold; text-decoration: underline;">Å ta mi to<br /> &#8222;jede&#8220; prazan prostor na hard disku ?</p> 
        
        <p>
          </span>?esto nam se ?ini ili je stvarno tako da je prostor na disku sve<br /> manji i manji a da mi nismo uzrok tome. Da bi utvrdili koji su to<br /> direktorijumi i fajlovi koji zauzimaju najve?i prostor na disku<br /> dovoljno je da pokrenemo nekoliko shell k<span
style="font-weight: bold; font-style: italic;">omandi zajedno:</span><br
style="font-weight: bold; font-style: italic;" /><br /> <br style="font-weight: bold; font-style: italic;" /><br /> <span style="font-weight: bold; font-style: italic;">du -x<br /> &#8211;block-size=1024K | sort -nr | head -20</span>
        </p>
        
        <p>
          Ova naredba ?e na, pokazati20 najve?ih direktorijuma i fajlova ispod<br /> teku?eg direktorijuma što zna?i da, ukoliko želite da vidite najve?e<br /> &#8222;guta?e&#8220; na celoj particiji morate da budete u osnovnom direktorijumu.
        </p>
        
        <p>
          <span style="font-weight: bold;">6.</span><span
style="font-weight: bold;"> </span><span
style="text-decoration: underline; font-weight: bold;">Naredba </span><span
style="font-style: italic; text-decoration: underline; font-weight: bold;">watch</p> 
          
          <p>
            </span>Sa komandom watch, možete pratiti program, u odreÄ‘enom<br /> vremenskom intervalu (dafault su 2 sekunde). Na primer, naredba <br /> <span style="font-style: italic; font-weight: bold;">watch lpq</span> <br /> ?e pratiti sve trenutne poslove štampa?a, u intervalima od po 2<br /> sekunde. Interval možete sami odrediti parametrom n:<br /> <span style="font-style: italic; font-weight: bold;">-n [secs]</span><br /> pa ?e naredba <span style="font-style: italic; font-weight: bold;">watch<br /> -n 10 w</span> prikazivati koje prijavljen na ra?unar i update-ovati<br /> prikaz svakih 10 sekundi.
          </p>
          
          <p>
            <span style="font-weight: bold;">7. <span
style="text-decoration: underline;">Rekurzivna naredba </span></span><span
style="font-style: italic; font-weight: bold; text-decoration: underline;">grep</span><br /> <span style="font-weight: bold; text-decoration: underline;"><br /> </span><span style="text-decoration: underline;"></span>Ukoliko želite<br /> da pretražujete odreÄ‘eni string kroz listu direktorijuma možete za to<br /> iskoristiti naredbu <span
style="font-style: italic; font-weight: bold;">rgrep</span><br /> <span style="font-weight: bold; font-style: italic;">rgrep</span> ?e<br /> pretraživati kroz celu listu pod-direktorijuma na isti na?in kao što <span
style="font-style: italic; font-weight: bold;">grep</span> pretražuje<br /> fajlove.<span style="font-style: italic; font-weight: bold;"></p> 
            
            <p>
              </span><span style="font-weight: bold;">8.</span><span
style="font-style: italic; font-weight: bold;"> </span><span
style="font-weight: bold; text-decoration: underline;">Kako automatski<br /> izbrisati core fajlove</p> 
              
              <p>
                </span> Ako želite da automatski pronaÄ‘ete i izbrišete core<br /> fajlove možete u vaš /etc/cron.daily direktorujum ubaciti slede?u<br /> liniju u novi fajl (fajl mora biti izvršan tj. chmod 755):
              </p>
              
              <p>
                <span style="font-weight: bold; font-style: italic;">find / -name core<br /> -atime +2 -exec rm -f &#8222;{}&#8220; &#8216;;&#8217;</span>
              </p>
              
              <p>
                Ova linija ?e prona?i sve fajlove sa imenom &#8216;core&#8217; koji nisu menjani u<br /> poslednja 2 dana i automatski ih izbrisati.<br /> Naravno, ovde podrazumevam da je pokrenut cron demon .<br /> Nadam se da ne treba da napominjem da na ovaj na?in možete pokretati i<br /> druge naredbe.
              </p>
              
              <p>
                nastavi?e se&#8230;<br /> <big><font size="-1"><big></p> 
                
                <p>
                  <span style="font-weight: bold; text-decoration: underline;"></span><span
style="font-style: italic; font-weight: bold;"></span></big></font></big><span
style="font-weight: bold;"></span><span style="font-style: italic;"></span>
                </p>
                
                <p>
                  <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=439">Креирај тему форума везану за овај текст</a>
                </p>