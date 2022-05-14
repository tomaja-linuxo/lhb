---
author: tomaja
date: "2004-11-07T08:16:58Z"
excerpt: |
  NVIDIA sre?om nastavlja da redovno izbacuje nove verzije Linux drajvera
  za svoje grafi?ke kartice. U pitanju je verzija <br>
  1.0-6629 koja je izba?ena za x86 i AMD64 procesore. Spisak novosti i
  poboljšanja sledi u nastavku teksta a link za download  možete
  prona?i u našoj <a
  href="http://www.linuxo.org/modules.php?name=Downloads&amp;d_op=viewdownload&amp;cid=12">download
  sekciji</a>. Još da napomenem da drajver treba da funkcioniše i na
  2.6.9 kernelu dok se sada podrška za recimo 2.6.8 seriju podrazumeva a
  uba?ena je podrška za još nekoliko modela Nvidia graf.kartica. Dakle,
guid: https://forum.linuxo.org/2004/11/07/novi-nvidia-graf-drajveri-za-x86-i-amd64/
id: 604
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Novi NVIDIA graf.drajveri  za x86 i AMD64
url: /novi-nvidia-graf-drajveri-za-x86-i-amd64/
---
NVIDIA sre?om nastavlja da redovno izbacuje nove verzije Linux drajvera  
za svoje grafi?ke kartice. U pitanju je verzija  
1.0-6629 koja je izba?ena za x86 i AMD64 procesore. Spisak novosti i  
poboljšanja sledi u nastavku teksta a link za download možete  
prona?i u našoj [download  
sekciji](http://www.linuxo.org/modules.php?name=Downloads&d_op=viewdownload&cid=12). Još da napomenem da drajver treba da funkcioniše i na  
2.6.9 kernelu dok se sada podrška za recimo 2.6.8 seriju podrazumeva a  
uba?ena je podrška za još nekoliko modela Nvidia graf.kartica. Dakle, <!--break-->

  * Dodana podrška za GeForce 6600 i GeForce 6600 GT.
  * Dodana je podrška za Quadro FX 4000 SDI
  * Dodana je podrška za 512 MB framebuffere.
  * UnapreÄ‘ena podrška za GLSL (OpenGL Shading Language).
  * UnapreÄ‘ena podrška za VBO (OpenGL Vertex Buffer Objects).
  * UnapreÄ‘ena podrška za Linux 2.6 kernele.
  * UnapreÄ‘ena podrška za PCI Express. 
  * Smanjen je prostor koji se zauzima za virtuelnu adresu u OpenGL  
    aplikacijama.
  * Ažurirana je dokumentacija. Pro?itajte faj [README](ftp://download.nvidia.com/XFree86/Linux-x86/1.0-6629/README.txt).  
    (app-s) APPENDIX  
    S: POWER MANAGEMENT SUPPORT  
    (app-t) APPENDIX  
    T: DISPLAY DEVICE NAMES  
    (app-u) APPENDIX  
    U: THE COMPOSITE X EXTENSION
  * UnapreÄ‘ena podrška za EM64T Linux/x86-64 sisteme
  * UnapreÄ‘ena podrška za RenderAccel
  * UnapreÄ‘ene performanse za Java2D.

Za korisnike SuSE Linuxa preporu?ujemo da pro?itaju [SuSE  
NVIDIA Installer HOWTO](ftp://ftp.suse.com/pub/suse/i386/supplementary/X/XFree86/nvidia-installer-HOWTO) pre nego što downloaduju drajver 

A kada to u?inite za instalaciju drajvera je dovoljno da pokrenete  
komandu:

&#8222;sh NVIDIA-Linux-x86-1.0-6629-pkg1.run&#8220; i naravno da podesite X  
config fajl ukoliko je to potrebno (uvek pro?itajte INSTALL i README  
fajlove koje dobijate uz sam drajver).

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=604)