---
author: gandalf
date: "2005-11-21T23:06:51Z"
excerpt: |
  A simple question with a complex answer! It is complex because security
  issues arise from a variety of sources: your code, your server, the
  other things running on your server, the users, etc. While Mambo itself
  is relatively secure, you may still experience problems if the server
  is compromised or if a user gives up a password. The basic steps you
  should take however include:<br />
  <ul>
  <li>Do not unnecessarily leave directories open with CHMOD set at 777 (configuration.php in particular should be set to chmod 644)</li>
  <li>Delete your old installation directory (don't just rename it!).</li>
  <li>Implement HTTP access controls for your admin login.</li>
  <li>Make all your admin passwords at least 8 characters and containing symbols and numbers as well as letters.</li>
  </ul>
  There's more that you can do, but it is outside the scope of this FAQ.<br />
guid: https://forum.linuxo.org/2005/11/21/how-do-i-secure-my-mambo-site/
id: 153
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: How do I secure my Mambo site?
url: /how-do-i-secure-my-mambo-site/
---
A simple question with a complex answer! It is complex because security  
issues arise from a variety of sources: your code, your server, the  
other things running on your server, the users, etc. While Mambo itself  
is relatively secure, you may still experience problems if the server  
is compromised or if a user gives up a password. The basic steps you  
should take however include:

  * Do not unnecessarily leave directories open with CHMOD set at 777 (configuration.php in particular should be set to chmod 644)
  * Delete your old installation directory (don&#8217;t just rename it!).
  * Implement HTTP access controls for your admin login.
  * Make all your admin passwords at least 8 characters and containing symbols and numbers as well as letters.

There&#8217;s more that you can do, but it is outside the scope of this FAQ.  
<!--break-->

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=153)