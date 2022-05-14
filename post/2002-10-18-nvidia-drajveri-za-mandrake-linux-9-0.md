---
author: tomaja
date: "2002-10-18T14:30:42Z"
excerpt: |
  Ono što zanima ve?inu korisnika jeste kako da podese svoje GForce 2,3 itd , TNT, TNT2 kartice u novom Mandrake Linux-u
  Pošto Nvidia još uvek nije izbacila prekompajlirane drajvere ni za jednu novu Linux distribuciju dalje u tekstu možete na?i link ka drajverima, postupak kako da ih instalirate i poterate svoj sistem u pravom ubrzanom 2D/3D okruženju.
  Dakle, pri?a sledi...
guid: https://forum.linuxo.org/2002/10/18/nvidia-drajveri-za-mandrake-linux-9-0/
id: 226
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: NVidia drajveri za Mandrake Linux 9.0
url: /nvidia-drajveri-za-mandrake-linux-9-0/
---
Ono što zanima ve?inu korisnika jeste kako da podese svoje GForce 2,3 itd , TNT, TNT2 kartice u novom Mandrake Linux-u  
Pošto Nvidia još uvek nije izbacila prekompajlirane drajvere ni za jednu novu Linux distribuciju dalje u tekstu možete na?i link ka drajverima, postupak kako da ih instalirate i poterate svoj sistem u pravom ubrzanom 2D/3D okruženju.  
Dakle, pri?a sledi&#8230;<!--break-->

<font face="verdana, arial, helvetica" size="2">Potrebna su vam dva fajla<br /> sa <a href="http://www.nvidia.com/view.asp?IO=linux_display_1.0-3123">nVidia<br /> drajver sajta</a>: </p> 

<p>
  </font><font face="verdana, arial, helvetica" size="2"><b>NVIDIA_kernel-1.0-3123.tar.gz</b><br /> i<br /> <b>NVIDIA_GLX-1.0-3123.tar.gz</b></font><br /> <font face="verdana, arial, helvetica" size="2"><br /> Kada instalirate kernel source (ako ga ve? niste instalirali on se nalazi<br /> na Mandrake LInux 9.0 CD3)<br /> otvorite root konzolu i preÄ‘ite u direktorijum gde vam se nalaze gore pomenuti<br /> fajlovi i ukucajte slede?e:</p> 
  
  <p>
    $ tar xvzf NVIDIA_kernel.tar.gz<br /> $ tar xvzf NVIDIA_GLX.tar.gz<br /> $ cd NVIDIA_kernel<br /> $ make install<br /> $ cd ../NVIDIA_GLX<br /> $ make install
  </p>
  
  <p>
    Kada se sve završi, nadam se bez grešaka, u XF86Config-4 fajlu (možete u<br /> root konzloli ukucati kedit /etc/X11/XF86Config-4)<br /> zamenite slede?e:
  </p>
  
  <p>
    Driver &#8222;nv&#8220;<br /> u:<br /> Driver &#8222;nvidia&#8220;
  </p>
  
  <p>
    a u Module sekciji morate imati slede?i red:
  </p>
  
  <p>
    Load &#8222;glx&#8220;
  </p>
  
  <p>
    Ako postoje, uklonite slede?e redove:
  </p>
  
  <p>
    Load &#8222;dri&#8220;
  </p>
  
  <p>
    Load &#8222;GLcore&#8220;
  </p>
  
  <p>
    Snimite izmene u fajlu i restartujte X server i nakon toga bi trebali da<br /> vidite nVidia ekran.
  </p>
  
  <p>
    Ukoliko se X server ne pokrene automarski onda kao root traba da u konzoli ukucate slede?e:
  </p>
  
  <p>
    #cd /usr/X11R6/lib <br /> #ln -s /usr/lib/libGL.so libGL.so.1.2 && ln -s libGL.so.1.2 libGL.so <br /> #/sbin/ldconfig <br /> #reboot
  </p>
  
  <p>
    što ?e i restartovati X server i napokon namesti sve kako treba.
  </p>
  
  <p>
    <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=226">Креирај тему форума везану за овај текст</a>
  </p>