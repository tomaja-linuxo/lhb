---
author: tomaja
date: "2006-08-12T07:16:47Z"
excerpt: <table border="0"><tbody><tr><td><img class=" size-full wp-image-1248" src="https://linuxo.org/wp-content/uploads/2006/08/icon-gentoo.png"
  alt="Gentoo Linux " title="Gentoo Linux " width="106" height="108" /> <br /></td><td>Emerge
  je frontend aplikacija za Portage na Gentoo Linux-u. Portage predstavlja kolekciju
  programa koje možete da instalirate, sa liste ponuđenih, na svoj sistem. Dakle,
  Emerge koristite da bi instalirali pakete sa Portage. Sam tutorijal ćete naći u
  nstavku teksta a ja ću ovde još napomenuti za je poslednja verzija Portage-a 2.1.1
  (<a href="http://sources.gentoo.org/viewcvs.py/portage/main/trunk/RELEASE-NOTES?view=markup"
  title="Release Notes - Portage 2.1.1">release notes</a> )</td></tr></tbody></table>
guid: https://forum.linuxo.org/2006/08/12/kratko-upustvo-za-emerge-portage/
id: 1249
image: /wp-content/uploads/2006/08/icon-gentoo.png
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1246";s:11:"_thumb_type";s:5:"thumb";}
title: Kratko upustvo za Emerge/Portage
url: /kratko-upustvo-za-emerge-portage/
---
<table border="0">
  <tr>
    <td>
      <img class=" size-full wp-image-1248" src="https://linuxo.org/wp-content/uploads/2006/08/icon-gentoo.png" alt="Gentoo Linux " title="Gentoo Linux " width="106" height="108" />
    </td>
    
    <td>
      Emerge je frontend aplikacija za Portage na Gentoo Linux-u. Portage predstavlja kolekciju programa koje možete da instalirate, sa liste ponuđenih, na svoj sistem. Dakle, Emerge koristite da bi instalirali pakete sa Portage. Sam tutorijal ćete naći u nstavku teksta a ja ću ovde još napomenuti za je poslednja verzija Portage-a 2.1.1 (<a href="http://sources.gentoo.org/viewcvs.py/portage/main/trunk/RELEASE-NOTES?view=markup" title="Release Notes - Portage 2.1.1">release notes</a> )
    </td>
  </tr>
</table>

<!--break-->

Da bi pronašli pakete sa&nbsp; emerge-om, ukucajte 

**emerge &#8211;search ključna_reč**

Ovo bi trebalo da vam prikaže sve podudarne pakete koji odgovaraju vašoj ključnoj reči. Instalacija paketa je jednostavna , dovoljno je da ukucate

**emerge ime_paketa**

Emerge se može koristiti i za ažuriranje (update) vašeg sistema. Da bi prekomajlirali sistem sa novim&nbsp; USE flegovima i novim opcijama kompajlera pokrenite

**emerge -e system**

Da bi update-ovali i pakete koje ste naknadno instarali pokrenite sličnu naredbu:

**emerge -e world**

Ukoliko ne želite da rekompajlirate sve, već samo pakete i njihove međuzavisnosti pokrenite

**emerge &#8211;update &#8211;deep world  
** 

A sa vremena na vreme treba da pokrente i 

**emerge &#8211;update &#8211;deep system**  
da bi osigurali da je vaš sistem ažuriran .

Uklanjanje paketa je takođe veoma jednostavno.&nbsp; &#8211;unmerge parameter je sve što treba da dodate.

**emerge &#8211;unmerge ime_paketa**

Nakon što uklonili pakete, verovatno ćete želeti da uklonite i zaostale međuzavisnosti između paketa. Zato pokrenite

**emerge &#8211;depclean**

Naravno, nakon pokretanja neredbe&nbsp; emerge &#8211;depclean treba da pokrenete i&nbsp; 

**runrevdep-rebuild**

da bi bili sigurni da niste uklonili nešto što niste trebali. Revdep-rebuild je deo&nbsp; gentoolkit paketa. A njega možete instlairati pomoću naredbe: 

**emerge gentoolkit**

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1249)