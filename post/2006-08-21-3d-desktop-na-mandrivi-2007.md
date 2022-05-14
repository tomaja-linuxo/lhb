---
author: tomaja
date: "2006-08-21T11:27:52Z"
excerpt: <table border="0"><tbody><tr><td><img class=" size-full wp-image-1260" src="https://linuxo.org/wp-content/uploads/2006/08/mandriva_star.jpg"
  alt="Mandriva Linux" title="Mandriva Linux " width="64" height="64" /> <br /></td><td>Mandriva
  2007 će podržavati 3D desktop efekte kroz XGL/AIGLX. Izbor će biti napravljen automatski
  na osnovu mogućnosti drajvera za vašu grafičku karticu. Ukoliko neko želi da ovo
  isproba na test verziji Mandrive 2007 treba da uradite sledeće:</td></tr></tbody></table><br
  />
guid: https://forum.linuxo.org/2006/08/21/3d-desktop-na-mandrivi-2007/
id: 1261
image: /wp-content/uploads/2006/08/mandriva_star.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1260";s:11:"_thumb_type";s:5:"thumb";}
- a:2:{s:9:"_thumb_id";s:4:"1260";s:11:"_thumb_type";s:5:"thumb";}
title: 3D desktop na Mandrivi 2007
url: /3d-desktop-na-mandrivi-2007/
---
<table border="0">
  <tr>
    <td>
      <img class=" size-full wp-image-1260" src="https://linuxo.org/wp-content/uploads/2006/08/mandriva_star.jpg" alt="Mandriva Linux" title="Mandriva Linux " width="64" height="64" />
    </td>
    
    <td>
      Mandriva 2007 će podržavati 3D desktop efekte kroz XGL/AIGLX. Izbor će biti napravljen automatski na osnovu mogućnosti drajvera za vašu grafičku karticu. Ukoliko neko želi da ovo isproba na test verziji Mandrive 2007 treba da uradite sledeće:
    </td>
  </tr>
</table>

<!--break-->

  * Instalirajte potrebne pakete I ( compiz, , x11-server-xgl, mesa-demos ) :  
    <em class="commande">urpmi compiz x11-server-xgl mesa-demos</em>  
    &nbsp; Postoji metapackage koji će instalirati sve potrebne pakete: **task-3ddesktop**
  * Aktivirajte Composite ekstenziju u Xorg-u. To možete uraditi i sa **drakx11** ( cf "Options" sekcija) ili ručnim editovanjem&nbsp; /etc/X11/xorg.conf fajla dodavanjem sledeće sekcije :  
     <span class="code">Section "Extensions"<br /> &nbsp;&nbsp;&nbsp;Option "Composite"<br /> EndSection </span>
  * Restartujte&nbsp; X server i jednosgtavno se ponovo ulogujte. XGL ili AIGLX će biti aktivirani automatski, naravno ako imate 3D drajvere za svoju grafičku karticu. Deakvitiranje Compiz-a ili XGL-a se može uraditi odvojeno editovanjem&nbsp; **/etc/sysconfig/compiz** i&nbsp; **/etc/sysconfig/xgl**. 

&nbsp;

**Napomena:** Da bi deaktivirali AIGLX potrebno je samo da deaktivirate compiz editovanjem&nbsp; **/etc/sysconfig/compiz** fajla.  
**Napomena&nbsp; 2 :** Da bi podesili Compiz plugin-ove treba da instalirate paket **gset-compiz**. Paketi compiz-quinnstorm i cgwd su takođe dostupni za one koji hoće da idu do kraja :). Ne zaboravite da još uvek ima dosta bagova u Compiz/AIGLX/XGL. 

&nbsp;

Za više informacija :  
&#8211; Gustavo Boiko ( dev Xorg de Mandriva ) par reči o budućnosti Linux/Mandriva desktopa : <a href="http://people.mandriva.com/%7Eboiko/desktop_thoughts/" target="_new" title="http://people.mandriva.com/~boiko/desktop_thoughts/">http://people.mandriva.com/~boiko/desktop_thoughts/</a>  
&#8211; XGL demo pod Mandrivom 2007 : <a href="http://www.linux-wizard.net/index.php?id_blog=83" target="_new" title="http://www.dailymotion.com/video/xb7sz_mandriva-linux-2007-3d-desktop">http://www.dailymotion.com/video/xb7sz_mandriva-linux-2007-3d-desktop</a>  
&#8211; Dokumentacija o Compiz-u i njegovim plugin-ovima : <a href="http://en.opensuse.org/Compiz" target="_new" title="http://en.opensuse.org/Compiz">http://en.opensuse.org/Compiz</a>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1261)