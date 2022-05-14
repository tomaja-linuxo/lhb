---
author: tomaja
date: "2003-11-30T15:53:03Z"
excerpt: |
  <font face="helvetica,arial">Ovaj dokument treba da pruži osnovna
  znanja za koriš?enje konzole u shell modu. Nije neohodno da ?italac ima
  bilo kakvo prethodno znanje o tome kako linux funkcioniše, ali u tom
  slu?aju treba da pro?ita ovaj tekst od po?etka. Spisak komandi služi da
  se upoznamo sa osnovnim Linux komandama: Komande su prikazane po tipu
  posla koji obavljaju. Završni deo teksta se bavi nekim naprednim
  mogu?nostima koje mogu da pokažu kako da iskoristite mo?an sistem kakav
  je Linux.
  </font>
guid: https://forum.linuxo.org/2003/11/30/linux-konzola/
id: 396
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linux konzola
url: /linux-konzola/
---
<font face="helvetica,arial">Ovaj dokument treba da pruži osnovna<br /> znanja za koriš?enje konzole u shell modu. Nije neohodno da ?italac ima<br /> bilo kakvo prethodno znanje o tome kako linux funkcioniše, ali u tom<br /> slu?aju treba da pro?ita ovaj tekst od po?etka. Spisak komandi služi da<br /> se upoznamo sa osnovnim Linux komandama: Komande su prikazane po tipu<br /> posla koji obavljaju. Završni deo teksta se bavi nekim naprednim<br /> mogu?nostima koje mogu da pokažu kako da iskoristite mo?an sistem kakav<br /> je Linux.<br /> </font><!--break-->

## <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Struktura Linux-a</font></font>

### <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Korisnici:</font></font>

<font face="helvetica,arial">Da bi koristili Linux mašinu morate da<br /> kreirate nalog na toj mašini. Informacija o nalogu sadrži vaše<br /> korisni?ko ime i lozinku koji zajedno kontrolišu vaš pristup na toj<br /> mašini. TakoÄ‘e postoji i jedinstveni broj koji je pridružen vašem<br /> korisni?kom nalogu i zove se user ID ili UID.</p> 

<p>
  </font>
</p>

<h3>
  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Grupe:</font></font>
</h3>

<p>
  <font face="helvetica,arial">KOrisnici koji recimo rade u istom delu<br /> jedne firme ili rade na istom projektu mogu se nalazi u odreÄ‘enoj grupi<br /> . Ovo je jednostavan metod za organizaciju korisnika. Kao i sa<br /> individualnim korisnicima, postoji i group id ili GID koji se<br /> dodeljuje svakoj grupi. </p> 
  
  <p>
    </font>
  </p>
  
  <h3>
    <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Fajlovi (datoteke):</font></font>
  </h3>
  
  <p>
    <font face="helvetica,arial">Sve informacije koje se smeštaju na Linux<br /> mašini se smeštaju u fajlove. Kao dodatak podacima koji se u njemu<br /> nalaze fajl sadrži i informaciju o tome koji korisnik je vlasnik fajla,<br /> koji korisnici mogu da mu pristupe, kada je preiran, kada poslednji put<br /> izmenjen i naravno kolika mu je veli?ina..</p> 
    
    <p>
      </font>
    </p>
    
    <h3>
      <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Direktorijumi:</font></font>
    </h3>
    
    <p>
      <font face="helvetica,arial">Direktorijumi su sli?ni folderima. Oni<br /> mogu da sadže fajlove kao i druge direktorijume (koje mi obi?no<br /> nazivamo podirektorijumima), i daju strukturu fajl sistema. Pod Linuxom<br /> postoji samo jedno stablo sa direktorijumima a njegov koren je <b>/</b>.<br /> Kao i fajlovi, direktorijum sadrži informacije o svojoj veli?ini,<br /> podatke o tome koji korisnici i/ili grupe mogu da mu pristupe, itd&#8230; </p> 
      
      <p>
        </font>
      </p>
      
      <h3>
        <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Putanje:</font></font>
      </h3>
      
      <p>
        <font face="helvetica,arial">Putanja je string niz direktorijuma koji<br /> završava sa imenom fajla. Direktorijum i imena fajlova se odvajaju<br /> sa <b>/</b> (front slash) karakterima. Na primer:<br /> <i>/dir1/dir2/fajl</i>1 je putanja do fajla <i>fajl1</i> koji se<br /> nalazi u <i>dir2</i>,<br /> a opet on se nalazi u direktorijumu <i>dir1</i>, koji se nalazi opet u<br /> osnovnom ili root<br /> direktorijumu, <i>/</i>.</p> 
        
        <p>
          </font>
        </p>
        
        <h3>
          <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Ovlaš?enja:</font></font>
        </h3>
        
        <p>
          <font face="helvetica,arial">Ovlaš?enja su veoma važna funkcija u<br /> Linuxu. Ona obezbeÄ‘uju sigurnost ograni?avaju?i akcije koje korisnik<br /> može da izvede na odreÄ‘enom fajlu ili direktorijumu. Ovlaš?enja<br /> kontrolišu prava ?itanja, zapisivanja ili pokretanja fajlova za<br /> vlasnika fajova, grupe i ostale korisnike. Ukoliko pokušate da recimo<br /> izmenite fajl za koji nemate ovlaš?enja dobi?ete poruku o grešci.</p> 
          
          <p>
            </font>
          </p>
          
          <h3>
            <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Procesi:</font></font>
          </h3>
          
          <p>
            <font face="helvetica,arial">Kada korisnik pokrene komandu kreira se<br /> proces koji sadrži instrukcije (kod) te komande. Proces takoÄ‘e sadrži<br /> kontrolne informacije kao što je UID korisnika koji je pokrenuo komandu<br /> i jedinstveni porcess id ili PID. Svo upravljanje procesa se obavalja<br /> koriš?enjem ovog broja<br /> PID. </p> 
            
            <p>
              </font>
            </p>
            
            <h3>
              <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Å koljka (The Shell) :</font></font>
            </h3>
            
            <p>
              <font face="helvetica,arial">U konzolnom modu korisnik obavlja<br /> interakciju sa mašinom preko shell-a. Shell je program koji služi za<br /> pokretanje drugih programa. Shell se konfigurišepodešavanjem njegovih<br /> promenljivih . Kada se prijavite (ulogujete) na Linux mašinu ona ?e<br /> automatski kreirati shellproces za vas, i podesiti promenljive<br /> okruženja na default<br /> vrednosti. U ovom tesktu se podrazumeva da koristite <span
 style="font-weight: bold;">bash</span> (the Bourne Again SHell), koji<br /> je postao standard za ve?inu popularnih Linux<br /> distribucija.<br /> </font>
            </p>
            
            <p>
              <font face="helvetica,arial"><br /> </font>
            </p>
            
            <h2>
              <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Pokretanje komandi <br /> </font></font>
            </h2>
            
            <h3>
              <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Zadavanje (unošenje) komandi:</font></font>
            </h3>
            
            <p>
              <font face="helvetica,arial">Da bi zadali komadu jednostavno treba da<br /> ukucate njeno ime iza shell prompta i pritisnete taster enter. Shell<br /> prompt obi?no ima slede?u formu: <i>[user@host<br /> directory]$</i>,<br /> ali se može i menjati, i može se razilkovati od mašine do<br /> mašine.<br /> Ve?ina komadi prihvata nekoliko argumenata ili opcija (ponekada se<br /> nazivau i zastavice ili flags). Obi?no se argumenti ispisuju sa jednim<br /> ili dva znaka za minus tj. &#8211; ili &#8212; .<br /> Ukoliko komanda zahteva argumente a vi ih niste napisali ob?no komanda<br /> prikaže kratku poruku sa opsim mogu?ih argumenata. Tipi?na komanda sa<br /> argumetima može da izgleda ovako:</p> 
              
              <p>
                <i>komanda -a1 -a2 </i><br /> <i>komanda &#8211;puno_ime_argumenta</i><br /> </font>
              </p>
              
              <h3>
                <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Putanja (PATH):</font></font>
              </h3>
              
              <p>
                <font face="helvetica,arial">PATH je shell promenljiva koja odreÄ‘uje u<br /> kojem direktorijumu Linux treba da pronaÄ‘e zadatu naredbu ukoliko niste<br /> ispisali poptnunu pputanju do fajla naredbe.PATH promenljiva sadrži<br /> stringove ili linije sa imenima direktorijuma koja su odvojena sa<br /> dvota?kom : . Ve?ina ako ne i sve komande prikazane u ovom tekstu se<br /> ve? nalaze u promenljivoj PATH i mogu se pokretati jednostavno<br /> samo unošenjem imena naredbe. Iz sigurnosnih razloga trenutni<br /> direktorijum se ne nalazi u PATH<br /> pa tako da bi pokrenuli program koji se nalazi u trenutnom<br /> direktorijumu morate pre imena maredbe dodati prefiks ./ (ta?ka i sleš<br /> linija) :</p> 
                
                <p>
                  <i>./komanda</i>
                </p>
                
                <p>
                  </font>
                </p>
                
                <p>
                  <font face="helvetica,arial"><br /> </font>
                </p>
                
                <h2>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Spisak komandi</font></font>
                </h2>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Kako do pomo?i:</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Ve?ina Linux konyolnih konakdi<br /> sadrži male rutine koje prikazuju korisne informacije im date<br /> argumente<br /> <i>-h</i> ili <i>&#8211;help</i> . Kao dodatak, ve?ina Linux mašina ima<br /> bukvalno na hiljade stranica dokumentacije o samim naredbama. Jedan od<br /> najboljih na?ina da doÄ‘ete do dokumentacije jeste man page syitem. Ono<br /> što treba da uradite jeste da pokrenete <b>man</b> program<br /> sa imenom komande kao argumentom i dobi?ete ispisano upustvo za datu<br /> komandu .<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b><i>komanda</i> -h:</b> prikazuje<br /> kratko upustvo o datoj komandi<i>.</i><br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b><i>komanda</i> &#8211;help:</b><br /> prikazuje kratko upustvo o datoj komandi<i>.</i><br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>man <i>komanda</i>:</b><br /> prikazuje kompletno upustvo o datoj komandi. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Prikazivanje fajlova (listing):</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Jedna od najosnovnijih operacija koju<br /> možete izvesti jeste da izlistate fajlove koji se nalaze u odreÄ‘enom<br /> direktorijumu sa komandom <b>ls</b>. Ovo vam omogu?ava da<br /> pregledate sadržaj direktorijuma i pronaÄ‘ete fajlove na kojima želite<br /> da radite. Ukoliko je spisak fajlova preduga?ak i ne može da stane na<br /> jedan ekran onda ?ete možda poželeti da povežete prikaz <b>ls </b>komande<br /> u neki program za pregled teksta kao što je less .<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>ls:</b> lista sadržaj trenutnog<br /> direktorijuma. <br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ls -a:</b> lista sve fajlove<br /> uklju?uju?i i skrivene fajlove.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ls -l:</b> koristi long listing<br /> format (prikazuje i ovlaš?enja, ime vlasnika, veli?inu, datum, itd&#8230;).<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ls | less:</b> povezuje listing<br /> direktorijuma u <b>less</b> radi lakšeg pregleda. <br /> </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Promena<br /> direktorijuma:</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Kada se prijavite na Linux mašinu<br /> automatski se nalazite u vašem /home direktorijumu.<br /> Da bi prešli u neki drugi direktorijum možete koristiti <b>cd</b><br /> komandu. <b>cd</b><br /> prihvata punu putanju do direktorijuma, relativnu putanju do trenutnog<br /> direktorujuma ili ili jedan od ve?eg broja slecijalnih argumenata koji<br /> su prikazani dole.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>cd <i>putanja</i>:</b> prelazi u<br /> direktorujum odreÄ‘en putanjom npr. <span
 style="font-style: italic; font-weight: bold;">cd /usr/bin</span><br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>cd ~ :</b> prelazi u vaš home<br /> direktorijum.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>cd &#8211; :</b> prelazi u predhodni<br /> direktorijum.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>cd .. :</b> prelazi u osnovni<br /> direktorijum teku?eg direktorijuma.<br /> </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Upravljanje sa fajlovima i<br /> direktorijumima</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial"><b>cp</b> komanda je korisna za kreiranje<br /> backup kopija fajlova ili direktorijuma. <b>mkdir</b> komanda kreira<br /> nove, prazne direktorijume na od vas odreÄ‘enoj lokaciji. <b>mv</b><br /> se može koristiti za premeštanje fajlova iz jednog u drugi<br /> direktorijum, ili za promenu njihovih imena kada ih premeštate u isti<br /> direktorijum ali sa drugim imenom. <b>rm</b> vam omog?ava da obrišete<br /> stare fajlove da oslobodili prostor na disku. MOžete da koristite <b>rm<br /> <i>-R</i></b><br /> da bi izbrisali sadržaj direktorijuma, a onda izbrisali i sam<br /> direktorijum. <b>rmdir</b><br /> ?e izbrisati direktorijum, ali samo ako je ve? otvoren.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>cp <i>source_path</i> <i>destination_path</i>:</b><br /> kopira fajlove iz izvora na nvu destinaciju.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>cp -R <i>source_path</i> <i>destination_path</i>:</b><br /> rekurzivno kopiranje. <br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>mkdir <i>directory</i>:</b><br /> kreira novi direktorijumy. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>mv <i>source_path</i> <i>destination_path</i>:</b><br /> premešta ili menja ime fajlu. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>rm <i>files</i>:</b> briše<br /> falove. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>rm -R <i>directory</i>:</b><br /> rekurzivno brisanje. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>rmdir <i>directory</i>:</b><br /> briše prazan direktorijum. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>touch <i>file</i>:</b> kreira<br /> prazan fajl. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Pronalaženje fajlova</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Kada se vaši fajlovi nalaze rašireni u<br /> mnogim razli?itim direktorijumima, ili tražite odreÄ‘eni sistemski fajl,<br /> naredbe <b>find</b> i <b>locate</b> vam mogu uštedeti mnogo vremena.<br /> <b>find</b> ?e se pokrenuti iz odreÄ‘enog direktrijuma i pretražiti i<br /> sve poddirektorijume u njemu. <b>locate</b>, sa druge strane,<br /> održava bazu podataka svih fajlova na sistemu. On jednostavno pretraži<br /> bazu podataka i traži da li ijedan fajl u bazi odgovara zadatom imenu<br /> fajla.<br /> <b>locate</b> je mnogo brži od <b>find</b>, aoli se baza ažurira samo<br /> jednom dnevno (na nekim sistemima i reÄ‘e) pa se možet desiti da ne može<br /> da pronaÄ‘e skoro kreirane fajlove.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>find <i>path</i> -name <i>filename</i>:</b><br /> pronalazi fajl sa imenom <i>filename</i> a pretragu po?inje od putanje<i>path</i>.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>locate <i>filename</i></b><br /> pronalazi fajove u bazi podataka sa imenima koja sadrže <i>filename</i>.<br /> </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Rad sa tekstulanim fajlovima</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">da bi videli sadržaj kratkog tekstualnog<br /> fajla možete da koristite naredbu <b>cat</b> i prikazali sadržaj na<br /> ekranu . <b>less</b> vam omogu?ava da skrolujete kroz tekst sa<br /> strelicama na tastaturi kao i sa page up i page down<br /> tasteriam. <b>grep</b> je alatka za pretraživanje tekstualnih fajlova<br /> kada su u pitanu odreÄ‘ene re?i ili stringovi. Kada grep pronaÄ‘e ono što<br /> traži on ?e prikazati celu liniju. <b>sort</b>, kao što mu i<br /> samo ime kaže sortira tekstualni fajl i rezultat prikazuje na ekranu.<br /> Na kraju, postoji mali milion tekstualnih editora, kao pšto je na<br /> primer <b>pico</b> sa ugraÄ‘enim pretraživa?em i alatom za<br /> proveru sintakse.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>cat <i>filename</i>:</b><br /> prikazuje sadržaj tekstulanog fajla <i>filename</i> na ekran. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>grep <i>string filename</i>:</b><br /> Taži i prikazuje linije iz <i>filename</i> koje sadrže dati <i>string</i>.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>less <i>filename</i>:</b><br /> Skrolovanje kroz sadržaj tekstualnog fajla. Pritisnite q za izlaz. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>pico <i>filename</i></b>: Otvara<br /> fajl <i>filename</i><br /> u jednostavnom tekst editoru. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>sort <i>filename</i>:</b><br /> Sortira linije u fajlu <i>filename</i> po abecedi. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Dekompresija arhiva</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Kada skidamo fajlove sa Interneta oni su<br /> obi?no kompresovani na neki na?in da bi smanjili njihovu veli?inu.<br /> Naj?eš?e se ve?i broj fajlova smešta u jedan kompresovani fajl radi<br /> lakšeg download-a.<br /> Da bi došli do fajlova koji se nalaze u arhivi morate da odredite kako<br /> je arhiva kreirana. Obi?no je dovoljna ektenzija fajla koja ukazuje na<br /> program sa kojim je arhiva napravljena.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>bunzip2 <i>filename.bz2</i>:</b><br /> dekompresuje bzip2 fajl (*.bz2). Obi?no se koristi za velike<br /> fajlove. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>gunzip <i>filename.gz</i>:</b><br /> dekompresuje (.gz) arhivu </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>unzip <i>filename.zip</i>:</b><br /> dekompresuje PkZip ili WinZip fajl (*.zip) </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>tar -xvf <i>filename.tar</i>:</b><br /> untar-uje (.tar) arhivu (tarball). </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>tar -xvzf <i>filename.tar.gz</i>:</b><br /> dekompresuje i untar-uje kompresovanu tar arhivu (*.tar.gz ili *.tgz). </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Koriš?enje mre-nih servisa</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Mre-ni servisi nam dozvoljavaju pristup<br /> resursima na drugim mašinama (serverima) na mreži sa vaše mašine. <b>ftp</b><br /> program nam omogu?ava da se konektujemo na FTP (file transfer<br /> protocol) server. FTP server ?e vam omogu?iti da postavljate i skidate<br /> fajlove sa njega. FTP nije sigurnosni protokol i sve naredne se šalju<br /> kao obi?an tekst, uklju?uju?i i lozinke. Komanda <b>ping</b> ?e<br /> pokrenuti zahev za pingom sa odreÄ‘enog servera. Ve?ina mašina ?e<br /> odgovoriti na ping zahtev ukoliko su povezane na mrežu i pravilno<br /> podešene.Program <b>ssh</b> ?e vam omogu?iti da se povežete na<br /> server pokre?u?i Secure Shell protokol. Koriste?i <b>ssh</b> možete se<br /> prijaviti na drugu mašinu i koristiti njen konzolni mod sa svoje<br /> mašine. SSH je sigurnosni protokol pa se sva komunikacija sa<br /> udaljenim serverom kriptuje <b>telnet</b> služi istoj svrski kao i <b>ssh</b>,<br /> ali je stariji, nesigurnosni protokol. Neke starije mašine mogu da<br /> pokre?u samo TELNET<br /> servere, ali kada kog je mogu?e treba koristiti <b>ssh</b>.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>ftp <i>server</i>:</b> povezuje<br /> se na FTP server. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ping <i>server</i>:</b> šalje<br /> zahtev za ping <i>serveru</i>. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ssh -l <i>user server</i>:</b><br /> povezuje se na udaljenu mašinu koriste?i Secure Shell protokol. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>telnet <i>server</i>:</b><br /> povezuje se na udaljenu mašinu koriste?i TELNET protokol. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Å tampanje</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Pristup štampa?u iz Linux konzole<br /> obezbeÄ‘uje Lpr (Line PRinter) set komandi.<br /> Koriste?i <b>lpr</b> komandu možete štampati tekstulani ili<br /> PostScript (.ps)<br /> dokument na bilo kom štampa?u. Da bi videli koji su štampa?i dostupni<br /> možete koristiti naredbu <b>lpstat</b>.<br /> Komanda <b>lpq</b> vam dozvoljava da pretražite sadržaj zadtaka koji<br /> su upu?eni štampa?u.<br /> Dobi?ete prikaz zadataja sa njihovim ID, vlasnikom, imenom fajla za<br /> svaki zadatak.<br /> Na kraju, komanda <b>lprm</b> ?e ukloniti svaki zatadak sa spiska<br /> preko njegovog IDa. Naravno, njih možete da uklonite ako ste ih pre<br /> toga poslati.<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>lpq -P<i>printer</i>: </b><br /> prikazuje zadatke koji su poslani štampa?u <i>printer</i>. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>lpr -P<i>printer</i> <i>document</i>:<br /> štampa </b> <i>document</i><br /> na štampa?u <i>printer</i>. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>lprm -P<i>printer</i> <i>n</i>: </b><br /> uklanja zadatak sa ID <i>n</i> sa štampa?a <i>printer</i>. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>lpstat -a: </b> Prikazuje status<br /> svih dostupnih štampa?a. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Kako do informacija o sistemu</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Slede?e komande prikazuju razne<br /> informacije o sistemu<br /> </font>
                </p>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>date: </b>prikazuje vreme i<br /> datum koji su podešeni u operativnom sistemu. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>df -h: </b>prikazuje zauze?e na<br /> disk particijama. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>free: </b>prikazuje zauze?e<br /> memorije. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>history: </b>prikazuje izvršene<br /> komande u trenutnom nalogu. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>hostname: </b>prikazuje ime<br /> lokalne mašine (host). </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>pwd: </b>prikazuje (trenutni)<br /> direktorijum. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>rwho -a: </b>prikazuje sve<br /> korisnike koji su prijavljeni na mrežu. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>uptime: </b>prikazuje vreme od<br /> poslednjeg restarta mašine. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>who: </b>prikazuje korisike koji<br /> su prijavljeni na mašini. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>whoami: </b>prikazuje vaše<br /> korisni?ko ime. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Kontrola procesa</font></font>
                </h3>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>ps: </b>prikazuje listu aktivnih<br /> procesa sa njihovim PID. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>ps -aux: </b>prikazuje sve<br /> aktivne procese, zajedn sa imenom njihovog vlasnika. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>top: </b>Prikazuje kontinuirano<br /> listu aktivnih procesa za zauze?em prcesora i memorije. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b><i>command</i> &: </b><br /> Pokre?e <i>command</i><br /> u pozadini. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>fg: </b>Vra?a zaustavljeni<br /> proces ili pozadinski proces. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>bg: </b>šalje proces u pozadinu.<br /> Isto se može posti?i i sa Ctrl-z. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>kill <i>pid</i>: </b> Primorava<br /> na gašenje procesa. Prvo odredite <i>pid</i> procesa pomo?u komande <b>ps</b>.<br /> </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>killall -9 <i>name</i>: </b><br /> ubija sve procese koji su odreÄ‘eni imenom <i>name</i>. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>nice <i>program level</i>:<br /> Pokre?e program sa </b>niceness <i>level</i>. OdreÄ‘uju?i visoki nice<br /> level ?e u?initi da se program pokre?e sa malim prioritetom. </font>
                  </li>
                </ul>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Promena ovlaš?enja na fajlu</font></font>
                </h3>
                
                <ul>
                  <li>
                    <font face="helvetica,arial"><b>chown <i>user.group filename</i>:</b><br /> menja korinsika koji poseduje <i>filename</i> u <i>user</i>, i<br /> grupu koja poseduje <i>filename</i> u <i>group</i>. Naravno, možete<br /> da menjate ovlaš?enja za one fajlove koji su vaše vlasništvo. </font>
                  </li>
                  <li>
                    <font face="helvetica,arial"><b>chmod <i>[augo][+-][rwx] filename</i>:</b><br /> menja prava pristupa za <i>filename</i> odobravaju?i ili<br /> onemogu?avaju?i (+-) ?itanje, pisanje ili izvršavanje (rwx) prava za<br /> sve, vlasnika,<br /> grupu ili druge korisnike (augo). Koristite ovu naredbu sa pažnjom.<br /> Možete sebi da onemogu?ite pristup sopstvenom fajlu pogrešnim<br /> podešavanjem ovlaš?enja. </font>
                  </li>
                </ul>
                
                <p>
                  <font face="helvetica,arial"><br /> </font>
                </p>
                
                <h2>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Napredne opcije</font></font>
                </h2>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Redirekcija:</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Shell daje svim programima pristup<br /> trima ta?kama koje se zovu standard input (STDIN), standard output<br /> (STDOUT), i standard<br /> error<br /> (STDERR) kada se program pokrene. Obi?no je STDIN povezan na tastaturu,<br /> dok su STDOUT i STDERR povezani na ekran. Ipak, redirekcija se može<br /> napraviti, kako za ulaz tako i za izlaz. Redirekcioni operatorr ><br /> vam omogu?ava da odredite ime dajla koji ?e primiti STDOUT (output)<br /> komande, dok operator < omogu?ava da STDIN povežete u fajl koji sadrži ulazne podatke. Evo nekih primera: <tt><i>command1 > output.txt</i></tt> šalje output tu output.txt<br /> <tt><i>command1 < input.txt </i></tt> odobavlja input izinput.txt<br /> </font>
                </p>
                
                <h3>
                  <font face="helvetica,arial"><font color="#213e59"
 face="lucida,helvetica,arial">Povezivanje (Piping):</font></font>
                </h3>
                
                <p>
                  <font face="helvetica,arial">Glavna svrha povezivanja jeste da<br /> refirektuje STDOUT iz jednog procesa u STDIN drugog procesa. Operator<br /> za povezivanje je | . Da bi povezali izlaz <i>command1</i> na<br /> ulaz <i>command2</i> treba da unesemo slede?e:</p> 
                  
                  <p>
                    <tt><i>command1</i> | <i>command2</i></tt><br /> </font>
                  </p>
                  
                  <p>
                    <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=396">Креирај тему форума везану за овај текст</a>
                  </p>