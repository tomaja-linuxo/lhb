---
author: tomaja
date: "2007-05-04T11:02:39Z"
excerpt: |
  <p><img class=" alignright size-full wp-image-1708" src="https://linuxo.org/wp-content/uploads/2007/05/php.gif" alt="PHP " title="PHP" hspace="4" width="95" height="51" align="right" />PHP razvojni tim&nbsp; je objavio nove stabilne verzije ovog popularnog programskog jezika i to <a href="http://www.php.net/downloads.php#v5">PHP 5.2.2</a> i <a href="http://www.php.net/downloads.php#v4">PHP 4.4.7</a>. Ovo su veća stabilnosna i sigurnosna unapređenja u 5.x i 4.4.x razvojnim granama, pa se stoga preporučuje ažuriranje &scaron;to je pre moguće. Detalji slede... <br /> </p>
guid: https://forum.linuxo.org/2007/05/04/azurirajte-svoj-php/
id: 1709
image: /wp-content/uploads/2007/05/php.gif
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1708";s:11:"_thumb_type";s:5:"thumb";}
title: Ažurirajte svoj PHP
url: /azurirajte-svoj-php/
---
<img class=" alignright size-full wp-image-1708" src="https://linuxo.org/wp-content/uploads/2007/05/php.gif" alt="PHP " title="PHP" hspace="4" width="95" height="51" align="right" />PHP razvojni tim&nbsp; je objavio nove stabilne verzije ovog popularnog programskog jezika i to [PHP 5.2.2](http://www.php.net/downloads.php#v5) i [PHP 4.4.7](http://www.php.net/downloads.php#v4). Ovo su veća stabilnosna i sigurnosna unapređenja u 5.x i 4.4.x razvojnim granama, pa se stoga preporučuje ažuriranje &scaron;to je pre moguće. Detalji slede&#8230; 

<!--break-->

Sigurnosna unapređenja i ispravke u PHP 5.2.2 i PHP 4.4.7 (en):

* Fixed CVE-2007-1001, GD wbmp used with invalid image size (by Ivan Fratric)  
* Fixed asciiz byte truncation inside mail() (MOPB-33 by Stefan Esser)  
* Fixed a bug in mb\_parse\_str() that can be used to activate register_globals (MOPB-26 by Stefan Esser)  
* Fixed unallocated memory access/double free in in array\_user\_key_compare() (MOPB-24 by Stefan Esser)  
* Fixed a double free inside session\_regenerate\_id() (MOPB-22 by Stefan Esser)  
* Added missing open\_basedir & safe\_mode checks to zip:// and bzip:// wrappers. (MOPB-21 by Stefan Esser).  
* Limit nesting level of input variables with max\_input\_nesting_level as fix for (MOPB-03 by Stefan Esser)  
* Fixed CRLF injection inside ftp_putcmd(). (by loveshell[at]Bug.Center.Team)  
* Fixed a possible super-global overwrite inside import\_request\_variables(). (by Stefano Di Paola, Stefan Esser)  
* Fixed a remotely trigger-able buffer overflow inside bundled libxmlrpc library. (by Stanislav Malyshev)

Security Enhancements and Fixes in PHP 5.2.2 only:

* Fixed a header injection via Subject and To parameters to the mail() function (MOPB-34 by Stefan Esser)  
* Fixed wrong length calculation in unserialize S type (MOPB-29 by Stefan Esser)  
* Fixed substr\_compare and substr\_count information leak (MOPB-14 by Stefan Esser) (Stas, Ilia)  
* Fixed a remotely trigger-able buffer overflow inside make\_http\_soap_request(). (by Ilia Alshanetsky)  
* Fixed a buffer overflow inside user\_filter\_factory_create(). (by Ilia Alshanetsky)

Security Enhancements and Fixes in PHP 4.4.7 only:

* XSS in phpinfo() (MOPB-8 by Stefan Esser)

[http://www.php.net/](http://www.php.net/ "http://www.php.net/")



[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1709)