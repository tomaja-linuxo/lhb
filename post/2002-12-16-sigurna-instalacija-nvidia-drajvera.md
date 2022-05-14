---
author: tomaja
date: "2002-12-16T03:31:50Z"
excerpt: |
  Siguran i jednostavan na?in instalacije <i>nVIDIA</i> drajvera za video kartu, a da pri tome ne morate voditi ra?una o verziji kernela je da skinete drajvere u <b>.src.rpm</b> obliku.<br>
  Procedura instalacije je slede?a...
guid: https://forum.linuxo.org/2002/12/16/sigurna-instalacija-nvidia-drajvera/
id: 254
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Sigurna instalacija nVIDIA drajvera
url: /sigurna-instalacija-nvidia-drajvera/
---
Siguran i jednostavan na?in instalacije _nVIDIA_ drajvera za video kartu, a da pri tome ne morate voditi ra?una o verziji kernela je da skinete drajvere u **.src.rpm** obliku.  
Procedura instalacije je slede?a&#8230;<!--break-->

  * Skinite drajvere:  
    [NVIDIA_GLX-1.0-2960.src.rpm](http://download.nvidia.com/XFree86_40/1.0-2960/NVIDIA_GLX-1.0-2960.src.rpm)  
  
    [NVIDIA_kernel-1.0-2960.src.rpm](http://download.nvidia.com/XFree86_40/1.0-2960/NVIDIA_kernel-1.0-2960.src.rpm)  
    </p> 
      * Deinstalirati postoje?i drajver  
        **rpm -e NVIDIA_GLX  
        rpm -e NVIDIA_kernel**</p> 
          * Uraditi rebuild modula  
            **rpm &#8211;rebuild NVIDIA_GLX-1.0-2960.src.rpm  
            rpm &#8211;rebuild NVIDIA_kernel-1.0-2960.src.rpm**</p> 
              * Instalirati kernel i GLX module  
                **rpm -ivh /usr/src/RPM/RPMS/i586/NVIDIA_kernel-1.0-2960.i586.rpm  
                rpm -ivh /usr/src/RPM/RPMS/i586/NVIDIA_GLX-1.0-2960.i586.rpm**</p> 
                  * Otvoriti /etc/X11/XF86Config-4  
                    Prona?i sekciju &#8222;Device&#8220; i promeniti red u kome piše **Driver &#8222;nv&#8220;**, sa **Driver &#8222;nvidia&#8220;**</p> 
                      * Prona?i sekciju &#8222;Module&#8220; i dodati liniju **Load &#8222;glx&#8220;**, ako ona ve? ne postoji 
                          * Snimiti ovaj fajl i iza?i 
                              * Restartovati sistem komandom: reboot </ul> 
                                Kraj.
                                
                                [Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=254)