---
author: tomaja
date: "2019-06-20T14:04:26Z"
guid: /?p=89016
id: 89016
image: /wp-content/uploads/2019/06/arton47-e1561109686377.jpg
tinymce-comment-field_enabled:
- "1"
title: 'Нека нова времена: OpenMandriva 4.0'
url: /neka-nova-vremena-openmandriva-4-0/
---
И тако..после готово 3 године од последње финалне верзије, објављена је <a href="https://wiki.openmandriva.org/en/4.0/Release_Notes" target="_blank" rel="noopener noreferrer">OpenMandriva LX 4.0</a>.  Пре пар месеци сам [писао о њој](/stize-nova-openmandriva/) а сада имамо и могућност да видимо шта се од обећеног остварило.

**OpenMandriva** 4.0 је сада поприлично иновативна Линукс дистрибуција која рецимо користи <span class="caps">LLVM</span>/clang за комплајлирање уместо gcc-a за који се кратори надају да доноси боље перформансе, оптимизацију и стабилност. Такође, група системских алата који се &#8222;вуку&#8220; још из времена Mandrake/Mandrivе се замењују новим. Оно што се види на први поглед, а новина је, или унапређење од предгодне стабилне верије:

<ul class="spip">
  <li>
    <span class="caps">KDE</span> Plasma је ажурирана на 5.15.5 (са Frameworks-ом 5.58 и Applications 19.04.2, Qt 5.12.3);
  </li>
  <li>
    LibreOffice је сада употпуности упарен са Плазмом, и користи њене системске дијалоге, изглед и осећај при раду;
  </li>
  <li>
    Falkon, <span class="caps">KDE-ов претраживач веба који корисити исти мотор за рендеровање као и </span>Chromium, је сада подразумевани претраживач, смањујући оптерећење меморије уз стандадизовани кориснички интерфејс система;
  </li>
  <li>
    Како су проблематични патенти везани за <span class="caps">MP3</span> формат коначно истекли између Lx 3 и 4 издања, <span class="caps">MP3</span> декодери и енкодери су сада укључени у главну диструбуцију.Видео и аудио плејери су такође ажурирани.
  </li>
  <li>
    Апликације и алате које развија сама OpenMandriva:<br class="autobr" /><span class="caps">OM</span> Welcome је значајно унапређен а <span class="caps">OM</span> Control Center је укључен у главну дистрибуцију;<br class="autobr" /><span class="caps">OM</span> Control Center иначе мења већ времешне DrakX алате;<br class="autobr" /><span class="caps">OM</span> Repository Management Tool (om-repo-picker), уствари графички интерфејс за избор и рад са <span class="caps">DNF</span> репозиторијумима је такође доступан
  </li>
  <li>
    Нове могућности у Calamares-у :<br class="autobr" />Опција за једноставна замена партиција<br class="autobr" />Копирање лог фајла на успешно инсталиран систем<br class="autobr" />Аутоматско уклањање свих некоришћених језика на крају инсталације<br class="autobr" />Calamares сада провера да ли је систем инсталиран у VirtualBox или на стваран хардвер. На потоњем уклања све неупотребљене virtualbox unuseful пакете.
  </li>
</ul>

### Под хаубом

Много је измена које нису одмах видљиве корисницима али су важне за одржавање система, као и даља унапређена:

<ul class="spip">
  <li>
    <a class="spip_in" href="https://openmandriva.org/en/news/article/switching-to-rpmv4">Прелазак на <span class="caps">RPM</span> 4</a> као и <a class="spip_out" href="https://en.wikipedia.org/wiki/DNF_(software)" rel="external"><span class="caps">DNF</span></a> као менаџер софтверских пакета (уместо urpmi-ja);
  </li>
  <li>
    Алати за компајлирање су такође претрпели измене. Главни C/C++ алати су сада засновани на clang 8.0, glibc 2.29 и binutils 2.32. gcc 9.1 је такође доступан;
  </li>
  <li>
    Java је унапређена на OpenJDK 12 са међузависношћу пакета изграђеном око Java Modules-а.
  </li>
  <li>
    Python је ажуриран на 3.7.3, а уклоњене су зависности у односу на Python 2.x из главне диструбуције (за сада Python 2 остаје доступан у репоима за све оне који користе старије апликације);
  </li>
  <li>
    Perl, Rust и Go су ажурирани на тренутно најновије верзије;
  </li>
  <li>
    Све важније библиотеке су такође ажуриране (нпр. Boost 1.70, poppler 0.76);
  </li>
  <li>
    Линукс кернел је ажуриран ја верзију 5.1.9 са додатним унапређењима у погледу перформанси. Kernel 5.2-rc4 је такође доступан преко репоа за тестирање.
  </li>
</ul>

Подршка за хардвер је значајно унапређена у ОpenMandriva 4.0. Поред уобичајеног ажурирања на нове верзије драјвера (укључујући Mesa 19.1.0 графички пакет), OMLx 4.0 сада има комплетиране портове тј. верзије система за aarch64 и armv7hnl платформе. <span class="caps">RISC</span>-V порт је и даље у ради, и још увек није спреман за објављивање. Припремљена је и посебна верзија са нове <span class="caps">AMD</span> процесоре (Ryzen, ThreadRipper, <span class="caps">EPYC</span>) која ради боље од генеричке верзије корићењем нових могућности у тим процесорима.

<img class="size-full wp-image-89020 aligncenter" src="/wp-content/uploads/2019/06/open-mandriva-lx-40.png" alt="open-mandriva-lx-40" width="700" height="80" srcset="https://linuxo.org/wp-content/uploads/2019/06/open-mandriva-lx-40.png 700w, https://linuxo.org/wp-content/uploads/2019/06/open-mandriva-lx-40-300x34.png 300w" sizes="(max-width: 700px) 100vw, 700px" /> 

У припреми је и нови модел по којем ће се убудуће објављивати нове верзије OpenMandrive. У основи, корисници ће имати више опција, а сам модел ће бити најављен нешто касније.

### Основи системски пакети:

Kernel 5.1.9<br class="autobr" /><span class="caps">KDE</span> Plasma: 5.15.5<br class="autobr" /><span class="caps">KDE</span> Frameworks: 5.58.0<br class="autobr" /><span class="caps">KDE</span> Applications: 19.04.2<br class="autobr" />Qt Framework 5.12.3<br class="autobr" />Systemd 242<br class="autobr" /><span class="caps">LLVM</span>/clang 8.0.1<br class="autobr" />Java 12

### Главни софтверски пакети:

LibreOffice 6.2.4<br class="autobr" />Firefox Quantum 66.0.5<br class="autobr" />Krita 4.2.1<br class="autobr" />DigiKam 6.0<br class="autobr" />Xorg 1.20.4, Mesa 19.1.0<br class="autobr" />Calamares 3.2.7

Ту су и потпуно нове апликације које су убачене на листу <span class="caps">ISO</span> пакета, од којих смо већину већ поменули:<br class="autobr" />Dnfdragora &#8211; графчки интерфејс за менаџер пакета, замена за стари rpmdrake<br class="autobr" />Kuser &#8211; алат за рад са кориснима и групама, замена за стари userdrake<br class="autobr" />KBackup &#8211; алаз за прављење резервне копије фолдера и фајлова, замена за стари draksnapshot<br class="autobr" />OpenMandriva Control Center<br class="autobr" />OpenMandriva Repository Management Tool

Препоручује се да направи резервна копија података и да се потом уради чиста инсталација уместо ажурирања система, да би се избегли могући конфликти са постојећим подешавањима система. До сада уочене проблеме са новом OpenMandriva-ом можете потражити на <a class="spip_out" href="https://wiki.openmandriva.org/en/4.0/Errata" rel="external">Errata</a> страницама.

<a href="https://www.openmandriva.org/en/documentation/openmandriva-lx/download" target="_blank" rel="noopener noreferrer"><strong>Преузимање</strong></a> (ISO фајлови):  
<a href="https://sourceforge.net/projects/openmandriva/files/release/4.0/" target="_blank" rel="noopener noreferrer">https://sourceforge.net/projects/openmandriva/files/release/4.0/</a>

или (torrent фајлови)

<a href="http://downloads.openmandriva.org/torrents/" target="_blank" rel="noopener noreferrer">http://downloads.openmandriva.org/torrents/</a>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=89016)