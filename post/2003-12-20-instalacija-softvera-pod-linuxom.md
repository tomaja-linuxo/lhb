---
author: tomaja
date: "2003-12-20T08:00:38Z"
excerpt: |
  <div align="left"><font face="Verdana, Arial, Helvetica, sans-serif"
  size="-1">Ovo upustvo je namenjeno onima koji se tek po?eli da se
  druže sa Linuxom. Jedan od naj?eš?ih problema koji se javlja pri
  prelasku sa Windowsa na Linux jeste instalacija softvera. Do sada je
  bio dovoljan jedan klik ili pritisak na taster Enter da bi se odreÄ‘eni
  program instalirao ali pod Linuxom su stvari malo druga?ije. Iako se
  recimo pri instalaciji sistema, na primer, odvija isti proces
  instalranja programa ipak ne znamo šta se ustvari dogaÄ‘a. Ovaj tekst ?e
  nam pomo?i da shvatimo kako se instaliraju programi u Linux OS.
guid: https://forum.linuxo.org/2003/12/20/instalacija-softvera-pod-linuxom/
id: 399
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instalacija softvera pod Linuxom
url: /instalacija-softvera-pod-linuxom/
---
<div align="left">
  <font face="Verdana, Arial, Helvetica, sans-serif"
 size="-1">Ovo upustvo je namenjeno onima koji se tek po?eli da se<br /> druže sa Linuxom. Jedan od naj?eš?ih problema koji se javlja pri<br /> prelasku sa Windowsa na Linux jeste instalacija softvera. Do sada je<br /> bio dovoljan jedan klik ili pritisak na taster Enter da bi se odreÄ‘eni<br /> program instalirao ali pod Linuxom su stvari malo druga?ije. Iako se<br /> recimo pri instalaciji sistema, na primer, odvija isti proces<br /> instalranja programa ipak ne znamo šta se ustvari dogaÄ‘a. Ovaj tekst ?e<br /> nam pomo?i da shvatimo kako se instaliraju programi u Linux OS.<!--break-->
  
  <br /> <span style="font-weight: bold;">1.</span> Prvo što treba re?i da zbog<br /> otvorenosti koda programa i njihove licence (GPL) svi <span
 style="font-weight: bold;">programi se mogu na?i u obliku izvornog koda</span><br /> tj. u nekompajliranom obliku. To su obi?no fajlovi koji se nalaze u<br /> obliku <span style="font-weight: bold;">tar.gz</span> i, <span
 style="font-weight: bold;">tar.bz2</span> ili sli?nim arhivama. Koja<br /> je prednost ovakog oblika distriburanja softvera ? Prvo, i ono<br /> najbitnije je da možete slobodno da izvršite izmene u samom kodu i<br /> bukvalno napravite svoj program ili samo da ga prilagodite svojim<br /> poltrebama ili recimo sami otklonite uo?enu grešku. Drugo, program u<br /> ovakvom obliku zauzima manje prostora pa je samim tim lakšte<br /> peuzeti program sa Interneta. Tre?e, programi u ovakvom obliku se mogu<br /> instalirati na velikom broju razli?itih Linux-Unix-BSD operativnih<br /> sistema. Koje su mane ? Prvenstveno sam postupak instalacije koji nije<br /> prost i preterano jednostavan a takoÄ‘e su potrebni odreÄ‘eni poreduslovi<br /> za instaalciju kao što su kompajleri i programske biblioteke.<br /> Postupak instalacije programa u obliku izvornog koda ?e biti objašnjen<br /> dalje u tekstu.</p> 
  
  <p>
    <span style="font-weight: bold;">2. </span>Pored programa koji dolaze<br /> u obliku izvornog koda veoma ?esto se koriste <span
 style="font-weight: bold;">binarni softverski paketi</span> koji su na<br /> neki na?in sli?ni programima koji se instalriju na MS Windows<br /> sistemima. U pitanju su ve? iskompajlirani programi koji jednostavno<br /> treba da se prekopiraju u sistem i ve? su spremi za pokretanje. Obi?no<br /> dolaze u obliku <span style="font-weight: bold;">rpm</span><br /> paketa. Instalacija ovakvih paketa je laka i obi?no<br /> se svodi na isti broj koraka koji smo imali i pod Windowsom. Pojedine<br /> Linux distribucije imaju svoje posebne grafi?ke programe za<br /> instalaciju ovih paketa, kao što je <span style="font-style: italic;">rpmdrake</span><br /> u Mandrake Linux distribuciji gde pored jednostavne instaliacije<br /> možete pregledati i opis programa koji instalirate. Koja je mana ovako<br /> distribuiranog softera ? Najve?a mana je to da su ovako pripremljeni<br /> paketi ograni?eni samo na jednu LInux distribuciju a veoma ?esto samo<br /> za jednu verziju kernela, odnosno jednu verziju LinuxOS-a (može se<br /> desiti da paket koji je predviÄ‘en za npr. RedHat 8.1 ne možete da<br /> instalirate na RedHat 9.0 ili obrnuto). Naravno, kako ve?ina grafi?kih<br /> programa u osnovi predstavlja samo grafi?ki interfejs mo?nih konzolnih<br /> programa red je da kažemo kako da iste pakete možemo da instaliramo u i<br /> iz konzole. Osnovna naredba za instalaciju rpm paketa je naravno <span
 style="font-style: italic;">rpm. </span>Osnovna sintaksa ove<br /> naredbe sa kojom se može instalirati gotovo svaki program u obliku rpm<br /> paketa je:<br /> <br style="font-style: italic;" /><br /> </font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1"><b>#<br /> </b></font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1"><span
 style="font-style: italic; font-weight: bold;">rpm -ivh<br /> ime_programa.rpm</span><span style="font-weight: bold;"> </span></p> 
    
    <p>
      Deinstalacija programa je takoÄ‘e veoma laka:
    </p>
    
    <p>
      </font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1"
 style="font-weight: bold;"><span style="font-style: italic;"># rpm<br /> -e ime_programa.rpm</span></font>
    </p>
    
    <p>
      <font face="Verdana, Arial, Helvetica, sans-serif" size="-1">Naravno, <span
 style="font-style: italic;">rpm</span> je mo?na alatka koja ima brojne<br /> mogu?nosti koje možete videti ukoliko pokrenete <span
 style="font-style: italic;">man rpm </span>. Mandrake Linux poseduje<br /> još jedan mo?an program za instalaciju rpm paketa <span
 style="font-style: italic;">urpmi </span>koji još više olakšava<br /> postupak instalacije rp paketa<span style="font-style: italic;">. </span>Ukucajte<br /> <span style="font-style: italic;">man urpmi</span> radi detaljnijeg<br /> objašnjenja komande a ja ?u samo pokazati kako se recimo instalira<br /> paket sysv:</p> 
      
      <p>
        <span style="font-style: italic;"><span style="font-weight: bold;">#<br /> urpmi sysv</span></p> 
        
        <p>
          </span>dakle, kao što vidimo veoma prosto. Nakon zadavanja ove komande<br /> sam program ?e tražiti od vas da ubacite CD na kome se nalazi rpm paket<br /> programa sysv i sam instalirati traženi program.<br /> Treba još napomenuti da programe možete da instalirate samo sa root<br /> ovlaš?enjima (bar po default postavkama sistema) ?ime se spre?ava<br /> ugrožavanje sigurnosti sistema. Otuda i znak # isperd naredbe što nam<br /> ukazuje da naredbu izvršavamo sa root ovlaš?enjima. Da bi u konzloli<br /> dobili root ovlaš?enja kucajte<br /> </font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1"><br /> <span style="font-style: italic;"><span style="font-weight: bold;">$<br /> su root</span><br /> </span></font><br /> <font face="Verdana, Arial, Helvetica, sans-serif" size="-1">a zatim<br /> ukucajte root lozinku</p> 
          
          <p>
            <b>3. Instalacija programa koji se nalaze u obliku izvornog<br /> koda </p> 
            
            <p>
              </b>Dakle, kao što smo rekli LInux softver ?esto dolazi u takozvanom<br /> tarball formatu (.tgz , tar.gz, tar.bz2 )<br /> Ovakvi fajlovi prvo moraju da se raspakuju (dekomresuju u bilo koji<br /> direktorijum) pomo?u naredbe<span
 style="font-style: italic; font-weight: bold;"> tar</span> . Za ovo<br /> možete koristiti i neki od grafi?kih interfejsa tar komande kao što je<br /> na primer <span style="font-style: italic;"><span
 style="font-weight: bold;">ark</span> , <span
 style="font-weight: bold;">karchiver</span> </span>ili neki drugi.<span
 style="font-style: italic;"> </span>Pomo?u naredbe<span
 style="font-style: italic;"> tar </span>falovi se raspakuju slede?im<br /> oblikom naredbe:
            </p>
            
            <p>
              <b><span style="font-style: italic;">$ tar xfvz<br /> game.tgz </span></b>(radi detaljnijem<br /> upoznavanje sa ovom naredbom u konzoli ukucajte <span
 style="font-weight: bold;">man tar</span> ili <span
 style="font-weight: bold;">tar &#8211;help</span> )<b></p> 
              
              <p>
                </b>Ova komanda ?e kreirati direktorijum u direktorijumu u kojem se<br /> trenutno nalazite i raspakovati sve fajlove u taj novi direktorijum.<br /> Kada ovo uradite postupak instalacije se u osnovi svodi na izvršavanje<br /> 3 sada ve? opšte poznate komande : configure, make i make install.</font><font
 face="Verdana, Arial, Helvetica, sans-serif" size="-1"> Ve?ina<br /> korisnika nakon izvršenja ovih komandi uspešno instalira željeni<br /> softver. Ipak, da malo objasnimo ove tri komande. </p> 
                
                <p>
                  Svaki softver dolazi sa nekoliko fajlova koji imaju svrhu pri samoj<br /> instalaciji. Jedan od njih je i skripta <span
 style="font-style: italic;"> configure</span> . Korisnik pokre?e ovu<br /> komandu u slede?em obliku
                </p>
                
                <p>
                  <b><span style="font-style: italic;">$ ./configure</span></p> 
                  
                  <p>
                    </b>Gore navedena komanda nareÄ‘uje shell-u da pokrene skriptu sa imenom<br /> &#8216; <i>configure</i><br /> &#8216; koja se nalayi u teku?em direktorijumu. Ta skripta u osnovi sadrži<br /> linije koda preko kojih se proverava sam ra?unar na koji treba<br /> insaliramo program. Proverava se softversko i hardversko okruženje.<br /> Ukoliko skripta pronaÄ‘e da neki uslovi za instalaciju programa nisu<br /> zadovoljeni izbaci?e poruku o tome šta to treba da se ubaci pre<br /> instalacije da bi ona bila uspešna. INstalacija ne?e biti nastavljena<br /> sve dotle dok se potrebni uslovi ne zadovolje.
                  </p>
                  
                  <p>
                    Glavni posao skripte <span style="font-style: italic;">configure</span><br /> je da napravi &#8216; <i>Makefile</i><br /> &#8216; . Ovo je veoma važan fajl u instalacionom postupku.<br /> U zavisnosti od rezultata proveta koje je izvršio skript <span
 style="font-style: italic;">configure</span> on sam ?e zapisati<br /> slede?e neophodne korake za kompajliranje softvera u fajl sa imemom <span
 style="font-style: italic;">Makefile</span>.
                  </p>
                  
                  <p>
                    Ukoliko se po završetku rada skripte <span style="font-style: italic;">configure</span><br /> ne pojave greše možete nastaviti postupak instalacije sa komandom
                  </p>
                  
                  <p>
                    <b>$ make</p> 
                    
                    <p>
                      </b>&#8216; <i>make</i> &#8216; je ustvari alatka koja postoji na gotovo svim<br /> Unixolikim sistemima. Da bi ovaj program radio potrebno je da postoji<br /> fajl Makefile u istom direktorijumu odakle pokre?ete naredbu <span
 style="font-style: italic;">make</span>.
                    </p>
                    
                    <p>
                      <span style="font-style: italic;">make</span> ?e iskoristiti upustva<br /> zapisana u fajlu <span style="font-style: italic;">Makefile</span> i<br /> nastaviti sa instalacijom. <span style="font-style: italic;">Makefile</span><br /> ukazuje na sekvence koje Linux mora da prati da bi kreirao razli?ite<br /> komponente /pod-programe za vaš softver. Sekvenca zavisi od na?ina<br /> na<br /> koji je softver dizajniran kao i od još nekoliko drugih faktora.<span
 style="font-style: italic;"> Makefile</span> u stvari poseduje mnogo<br /> oznaka (na neki na?in to su ustvari imena razli?itih delova ili<br /> sekcija). U osnovi alatka make kompajlira kompletan kod programa i<br /> kreira izvršne fajlove.
                    </p>
                    
                    <p>
                      <i>Jedna od oznaka prisutnih u Makefile se imenuje sa &#8216; <b>install</b><br /> &#8216; .</i>
                    </p>
                    
                    <p>
                      Ukoliko make završi svoj posao do kraja uspešno bez poruka o grešci,<br /> instalacija je gotovo zavrešna. Jedini korak koji nam je preostao je da<br /> obezbedimo root ovlaš?enja (ve? sam opisao kako) i pokrenemo
                    </p>
                    
                    <p>
                      </font><b><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">#<br /> make install</p> 
                      
                      <p>
                        </font></b><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">Kao<br /> što sam malopre rekao make koristi fajl Makefile u istom direktorijumu.<br /> Kada pokrenemo make bez parametara, izvršavaju se sve instrukcije u<br /> Makefile od po?etka do kraja onim redom kako je odredila skripta<br /> ./configure). Ali kada porenemo <i>make sa install kao prametrom, make<br /> traži oznaku install u fajlu Makefile, i izvršava samo tu sekciju fajla<br /> Makefile.</i></p> 
                        
                        <p>
                          </font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">Ova<br /> sekcija ustvari kopira izvršne fajlove koji su kreirani tokom<br /> kompajliranja programa u direktorijume iz kojih ?e se program pokretati<br /> . To su obi?no direktorijumi /usr/bin ili /usr/local/bin <br /> Treba re?i da program možete pokrenuti i ukoliko ne pokrenete make<br /> install ukoliko iz lokalnog direktorijuma, gde je program kompajliran,<br /> pokrenete izvršne fajlove.<br /> Ukoliko sa?uvate instalacioni direktorijum naredbom :</p> 
                          
                          <p>
                            </font><b><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">#<br /> make uninstall</p> 
                            
                            <p>
                              </font></b><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">možete<br /> deinstalirati program.</font><b><font
 face="Verdana, Arial, Helvetica, sans-serif" size="-1"><br /> </font></b><font face="Verdana, Arial, Helvetica, sans-serif" size="-1"> </p> 
                              
                              <p>
                                </font><font face="Verdana, Arial, Helvetica, sans-serif" size="-1">TO<br /> je to !! Nadam se da vam je sada proces instalacije softvera bar<br /> malo jasniji. </p> 
                                
                                <p>
                                  <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=399">Креирај тему форума везану за овај текст</a>
                                </p>