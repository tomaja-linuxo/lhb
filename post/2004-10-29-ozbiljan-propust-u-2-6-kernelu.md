---
author: tomaja
date: "2004-10-29T04:14:35Z"
excerpt: |
  Distributer popularne Linux distribucije SuSE je upozorio na veoma
  ozbiljan sigurnosni propust u verziji 2.6 Linux kernela, koji bi mogao
  potencijalnim napada?ima omogu?iti da ugase sistem koji se pokre?e na
  2.6 kernelima.Ovo se odnosi na kernele koji su stariji od 2.6.8
  kernela.  Iako 2.6 kernel donosi mnogo poboljšanja i
  enterprise-friendly mogu?nosti u Linux, još uvek je u ranoj fazi
  prilagoÄ‘avanja komercijalnim i enterprise proizvodima.
  Najve?i proizvoÄ‘a?i Linux sistema kao što su MandrakeSoft SA, SuSE ili
  RedHat još uvek nisu kao default opciju ubacili 2.6 kernele u svoje
  komercijalne enterprise proizvode a problem leži u tome kako novi
  kernel upravlja logovanjem iptables firewall-a što može dovesti do
  upada i gašenja sistema. Ovo je bug sa brojem 9 od mogu?ih 10.
guid: https://forum.linuxo.org/2004/10/29/ozbiljan-propust-u-2-6-kernelu/
id: 588
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Ozbiljan propust u 2.6 kernelu
url: /ozbiljan-propust-u-2-6-kernelu/
---
Distributer popularne Linux distribucije SuSE je upozorio na veoma  
ozbiljan sigurnosni propust u verziji 2.6 Linux kernela, koji bi mogao  
potencijalnim napada?ima omogu?iti da ugase sistem koji se pokre?e na  
2.6 kernelima.Ovo se odnosi na kernele koji su stariji od 2.6.8  
kernela. Iako 2.6 kernel donosi mnogo poboljšanja i  
enterprise-friendly mogu?nosti u Linux, još uvek je u ranoj fazi  
prilagoÄ‘avanja komercijalnim i enterprise proizvodima.  
Najve?i proizvoÄ‘a?i Linux sistema kao što su MandrakeSoft SA, SuSE ili  
RedHat još uvek nisu kao default opciju ubacili 2.6 kernele u svoje  
komercijalne enterprise proizvode a problem leži u tome kako novi  
kernel upravlja logovanjem iptables firewall-a što može dovesti do  
upada i gašenja sistema. Ovo je bug sa brojem 9 od mogu?ih 10.<!--break-->Alternativa je da se upgrade-uje kernel ili da se isklju?i firewall

  
logging za IP i TCP opcije, što opet nije preporu?ljivo. Sistemi  
koji koriste 2.4 kernele nisu ugroženi.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=588)