---
author: tomaja
date: "2018-11-12T21:17:17Z"
guid: /?p=88840
id: 88840
image: /wp-content/uploads/2018/11/http-quic.jpg
tinymce-comment-field_enabled:
- "1"
title: Нова верзија HTTP-а неће користити ТCP протокол
url: /nova-verzija-http-a-nece-koristiti-tcp-protokol/
---
Експериментални **_HTTP-over-QUIC_** <a href="https://www.zdnet.com/article/http-over-quic-to-be-renamed-http3/" target="_blank" rel="noopener">протокол ће бити преименован</a> у **_HTTP/3_** и очекује се да постане трећа званична верзија _HTTP_ протокола. Бар тако кажу званичници _Internet Engineering Task Force-а_ (IETF). Наиме, радне групе које раде на развоју HTTP-a и QUIC-a су то предложиле и изгледа да је предлог наилази на велику подршку. Самим тим ће ова у основу Google-ова експериментална технологија по други пут постати званично нова верија HTTP протокола. Пре овога, Google SPDY технологија је постала основа _HTTP/2_ протокола, који се данас користи.

_HTTP-over-QUIC_ је у основу поново написан _HTTP_ протокол који користи Google-ов _QUIC_ уместо _TCP_ (Transmission Control Protocol) као своју основну технологију. _**QUIC**_ је иначе скраћеница за &#8222;**<a href="https://www.chromium.org/quic" target="_blank" rel="noopener">Quick UDP Internet Connections</a>**&#8222;. То је Google-ов покушај да преуреди TCP протокол као унапређену технологију која комбинује HTTP/2, TCP, UDP, и TLS (за криптовање), између многих других ствари. <a href="https://blog.chromium.org/2015/04/a-quic-update-on-googles-experimental.html" target="_blank" rel="noopener">Google заправо жели</a> да QUIC постепено замени и TCP и UDP као нови протокол за пребацивае бинарних података преко Интернета, и због доброг разлога. Наиме, тестови су показали да је QUIC и бржи и сигурнији јер користи _encrypted-by-default_ имплементацију и то преко TLS 1.3 протокола.

<img class="size-medium wp-image-88844 aligncenter" src="/wp-content/uploads/2018/11/17656983818518293643-300x176.jpg" alt="" width="300" height="176" srcset="https://linuxo.org/wp-content/uploads/2018/11/17656983818518293643-300x176.jpg 300w, https://linuxo.org/wp-content/uploads/2018/11/17656983818518293643.jpg 462w" sizes="(max-width: 300px) 100vw, 300px" /> 

Ово је свакако важна вест, јер се тиче свих корисника WWW-a, тј. Интернета каквог га данас познајемо.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88840)