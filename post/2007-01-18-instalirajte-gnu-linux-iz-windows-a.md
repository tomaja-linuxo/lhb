---
author: GoranSTX
date: "2007-01-18T05:30:09Z"
excerpt: U toku je rad na win-based *buntu instaleru koji za cilj ima da korisnicima
  Win platforme olak&scaron;a prelazak na linux. Korisnik neće morati da zna kako
  se reže .iso slika na CD, kako se pode&scaron;ava redosled butabilnih uređaja, kako
  se particioni&scaron;e disk ili name&scaron;ta dual-boot sistem. Trenutno postoji
  <a href="https://wiki.ubuntu.com/install.exe/Prototype">prototip instalera</a> ,
  a za dalji razvoj potrebni su <a href="http://www.ubuntuforums.org/showthread.php?t=338279">testeri
  i developeri</a>. Za one koje interesuju detaljnije informacije, a ne žele da klikaju
  na linkove, pročitajte nastavak teksta [ENG]
guid: https://forum.linuxo.org/2007/01/18/instalirajte-gnu-linux-iz-windows-a/
id: 1543
title: Instalirajte GNU/Linux iz Windows-a
url: /instalirajte-gnu-linux-iz-windows-a/
---
U toku je rad na win-based *buntu instaleru koji za cilj ima da korisnicima Win platforme olak&scaron;a prelazak na linux. Korisnik neće morati da zna kako se reže .iso slika na CD, kako se pode&scaron;ava redosled butabilnih uređaja, kako se particioni&scaron;e disk ili name&scaron;ta dual-boot sistem. Trenutno postoji [prototip instalera](https://wiki.ubuntu.com/install.exe/Prototype) , a za dalji razvoj potrebni su [testeri i developeri](http://www.ubuntuforums.org/showthread.php?t=338279). Za one koje interesuju detaljnije informacije, a ne žele da klikaju na linkove, pročitajte nastavak teksta [ENG]<!--break-->The aim of this installer is to provide an easier way for a Windows user to install Ubuntu without having to know how to burn a cd iso, set the bios to boot from cd, repartition the disks, set up a multiboot system, etc. It will not replace any of the current Ubuntu installation options, and will not require that windows is installed prior to the installation of Ubuntu.

The installer works by creating a disk image of a pre-installed ubuntu system on the hard disk (downloaded with a bittorrent downloader integrated into the installer, or a standard http download when we find mirrors), and then installing GRUB for windows, which can be chain loaded by the existing boot loader, and which then loads the linux kerner and initrd from the ntfs partition. The initrd is modified to support mounting the image file mentioned above as a root file system, and then continuing the boot process like a normal installation.

This does not use a virtual machine to run linux on, so the performance of the resulting system will be similar to the performance of any other linux installation. The system will use ext3 in the image file, so users will get all the benefits of a linux filesystem.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1543)