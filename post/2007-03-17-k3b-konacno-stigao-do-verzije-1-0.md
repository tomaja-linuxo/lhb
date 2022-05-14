---
author: tomaja
date: "2007-03-17T09:00:01Z"
excerpt: '<p><img class=" alignleft size-full wp-image-1639" src="https://linuxo.org/wp-content/uploads/2007/03/K3b-logo.jpg"
  alt="K3b" title="K3b" hspace="4" width="16" height="16" align="left" />Jedna od
  najkvalitetnijih GNU/GPL Linux aplikacija je konačno stigla do verzije 1.0. Značajan
  napredak koji traje već 9 godina je krunisan objavljivanjem praktično prve zvanične
  verzije ove sjajne aplikacije. Lista unapređenja i novina u odnosu na zadnju stabilnu
  verziju je velika i prikazana je u nastavku teksta. Treba napomenuti da je K3b optimizovan
  i za novi KDE 4.0 a u skladu sa tim je predstavljen i novi vizuelni identitet K3b-a.&nbsp;
  <span class="info">Novi KDE 4.0 biće objavljen 23.oktobra.2007.god. <a href="http://www.phoronix.com/?page=news_item&amp;px=NTM5Mg"
  target="_blank" title="Najava za KDE 4.0"><br />Vi&scaron;e informacija</a> ...</span></p><p>Za
  neupućene, K3b predstavlja aplikaciju za narezivanje i druge opreacije sa CD i DVD
  diskovima na Linux/KDE desktopu. Vi&scaron;e informacija na stranicama projekta:
  <a href="http://www.k3b.org" target="_blank" title="K3b home ">www.k3b.org</a> .
  Novu verziju o obliku izvornog koda možete preuzeti <a href="http://k3b.plainblack.com/download"
  target="_blank" title="K3b download stranica">ovde</a> .  </p>'
guid: https://forum.linuxo.org/2007/03/17/k3b-konacno-stigao-do-verzije-1-0/
id: 1640
image: /wp-content/uploads/2007/03/K3b-logo.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1639";s:11:"_thumb_type";s:5:"thumb";}
title: K3b konačno stigao do verzije 1.0
url: /k3b-konacno-stigao-do-verzije-1-0/
---
<img class=" alignleft size-full wp-image-1639" src="https://linuxo.org/wp-content/uploads/2007/03/K3b-logo.jpg" alt="K3b" title="K3b" hspace="4" width="16" height="16" align="left" />Jedna od najkvalitetnijih GNU/GPL Linux aplikacija je konačno stigla do verzije 1.0. Značajan napredak koji traje već 9 godina je krunisan objavljivanjem praktično prve zvanične verzije ove sjajne aplikacije. Lista unapređenja i novina u odnosu na zadnju stabilnu verziju je velika i prikazana je u nastavku teksta. Treba napomenuti da je K3b optimizovan i za novi KDE 4.0 a u skladu sa tim je predstavljen i novi vizuelni identitet K3b-a.&nbsp; <span class="info">Novi KDE 4.0 biće objavljen 23.oktobra.2007.god. <a href="http://www.phoronix.com/?page=news_item&px=NTM5Mg" target="_blank" title="Najava za KDE 4.0"><br />Vi&scaron;e informacija</a> &#8230;</span>

Za neupućene, K3b predstavlja aplikaciju za narezivanje i druge opreacije sa CD i DVD diskovima na Linux/KDE desktopu. Vi&scaron;e informacija na stranicama projekta: <a href="http://www.k3b.org" target="_blank" title="K3b home ">www.k3b.org</a> . Novu verziju o obliku izvornog koda možete preuzeti <a href="http://k3b.plainblack.com/download" target="_blank" title="K3b download stranica">ovde</a> . 

<!--break-->

&nbsp;K3b 1.0 ChangeLog (eng.):

  * K3b now includes a VideoDVD kio slave. It can be used in Konqueror through the protocol videodvd:/ to copy the files from a VideoDVD with on-the-fly decryption if libdvdcss is installed. (Be aware that in some countries it is not permitted to use libdvdcss.)
  * New Device menu containing all the actions possible for a device (like eject, unmount, &#8230;). This includes the possibility of assigning shortcuts to these kind of actions.
  * K3b now warns if user parameters for external programs have been specified. This has been introduced because there were some bug report that were caused by faulty user parameters.
  * New option in the data project to not cache the inodes. That means it is possible to have multiple actual copies of the same file on one CD/DVD. This is now the new default.
  * K3b now properly unmounts media before using them.
  * New Audio Track source editor dialog to cut audio track sources at the beginning and the end.
  * Splitted "read retries" and "ignore read errors" for data and audio sectors in cd copy and set new defaults for audio sectors which make more sense: 5 retires and skip unreadable sectors.
  * New Mediamanager which makes K3b always know which device contains which medium. This makes medium handling more smooth and the user now selects a medium instead of a device. Other advantages include: 
      * No waiting time anymore when asking for information on media (including for example Audio CD ripping).
      * Nice default image filenames.
      * CD Copy: Enable/disable options based on the source medium.
      * Automatically select newly inserted media as burning medium
  * DCOP call directBurn() now returns a boolean value stating if the process could be started.
  * New DCOP calls cddaRip(), videocdrip(), and videodvdrip() with media:/ url support.
  * K3b can now handle media:/ urls from the command line to specify devices
  * Better Lame settings dialog. Easier to use for the novice user and better defaults.
  * Nicer Ogg Vorbis encoder settings dialog.
  * K3b now shows the DVD Medium ID in the disk information view.
  * K3b now displays a rough estimate on the remaining time for the current job.
  * New automatic media size mode for the projects. This means K3b uses the size from an inserted medium for the project maximum size.
  * Make a suggestion for the filename when saving a project based on the Volume ID (data projects) or the CD-Text title (Audio CD)
  * The Audio encoder plugins are now able to provide (very simplistic) user feedback in case of an error.
  * New settings "Swap byte order" and "Write Wave header" in the audio encoding plugin using external apps. This makes way for the usage of such programs as mppenc to encode Musepack files. In fact, mppenc is set up as a default along with flac if installed.
  * New DCOP interface: K3bJobInterface which provides DCOP signals for the currently running job. It may, for example, be used to provide information to a Karamba module.
  * New KFile plugin for K3b projects. For now it only shows the type of the project (Data DVD or Audio CD or &#8230;) but may be extended to show arbitrary information.
  * K3b now chooses default image names based on the project name or the volumeid/cdtext title in case of CD/DVD copy.
  * The K3b Project DCOP Interface now uses the QString type for url parameters instead of KURL.
  * Save/load audio cd track sources in audio projects
  * Display a beautified volume id. For example: THE_TRANSPORTER -> The Transporter
  * Check if the image directory exists before starting to create a project image
  * Possibility to hide the OSD temporarily for one process.
  * Completely rewritten Video DVD ripping and transcoding support: 
      * Simple on-the-fly transcoding of Video DVD titles
      * Interface similar to Audio CD ripping
      * Preview images in the ripping window
      * Automatic clipping
      * Simple resizing with automatic aspect ratio handling
  * File System presets for all data projects including all the advanced options.
  * Completely rewritten data project verification: 
      * K3b now compares the written image instead of the single files. This may be less informative but at least it works.
      * Verification of Video DVD projects
  * Little GUI changes: 
      * Changed the dialog layout in the action dialogs.
      * Simplified the layout of the burn dialogs for data projects (more advanced settings hidden).
      * Improved theme support (transparent themes)
  * Device buffer status display for DVD burning with growisofs >= 7.0
  * Support for Audio CD ripping with libcdio instead of libcdparanoia
  * Support for Cdrkit, the Debian fork of cdrtools.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1640)