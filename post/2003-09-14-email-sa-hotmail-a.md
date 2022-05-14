---
author: tomaja
date: "2003-09-14T05:00:06Z"
excerpt: |
  Preuzimanje poste sa Hotmail-a<br />
  Ko zeli da skida postu sa hotmaila uz pomoc programa za elektronsku postu to moze da izvede uz pomoc malog programa po imenu Hotwayd. Prozedura je sledeca:<br />
  Skinite fajl hotwayd-0.5.3-1.i586.rpm sa http://sourceforge.net/forum/forum.php?thread_id=930851&forum_id=80217<br />
  Sada editujte
guid: https://forum.linuxo.org/2003/09/14/email-sa-hotmail-a/
id: 372
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Email sa Hotmail-a
url: /email-sa-hotmail-a/
---
Preuzimanje poste sa Hotmail-a  
Ko zeli da skida postu sa hotmaila uz pomoc programa za elektronsku postu to moze da izvede uz pomoc malog programa po imenu Hotwayd. Prozedura je sledeca:  
Skinite fajl hotwayd-0.5.3-1.i586.rpm sa http://sourceforge.net/forum/forum.php?thread\_id=930851&forum\_id=80217  
Sada editujte<!--break-->xinetd.conf fajl (mdk 9.1 koristi xinetd) koji se nalazi u /etc/xinetd.conf. Dodajte sledece redove:

  
service hotwayd  
{  
disable = no  
type = unlisted  
socket_type = stream  
protocol = tcp  
wait = no  
user = nobody  
groups = yes  
server = /usr/sbin/hotwayd  
port = 110  
}

Zatim dajemo komandu xinetd da ponovo pokrene konfiguracioni fajl:  
killall -HUP xinetd  
Da bi bili sigurni da pop3 server nije blokiran editujemo /etc/host.allow file u kome dodajemo:  
hotwayd : 127.0.0.1  
U programu za el. postu(ja koristim Mozilla Mail) upisite:  
Server Name : 127.0.0.1  
User Name : ime @hotmail.com  
Server type je POP3 a SMTP je 127.0.0.1  
Za vise informacija posetite http://hotwayd.sourceforge.net/ .

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=372)