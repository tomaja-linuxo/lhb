---
author: tomaja
date: "2007-02-06T05:34:09Z"
excerpt: |
  Ovo je ujedno i poslednja verzija serije 1.4.x koja donosi novine i nove mogućnosti. Sledeća izdanja će biti samo ispravke određenih gre&scaron;aka sve do verzije 2.0 koja će pored ostalog biti i multiplatformska, jer će moći da se pokrene na Linux, Mac i MS Windows operativnim sistemima. Najnovije čedo koje pripada <a href="http://amarok.kde.org/content/view/10/66/" target="_blank">Amarok</a>  &quot;Fast forward&quot; seriji ima par novih stvarčica između kojih treba pomenuti i <img class=" alignright size-full wp-image-1561" src="https://linuxo.org/wp-content/uploads/2007/02/amarok.png" alt="Amarok" title="Amarok logo" hspace="4" width="128" height="128" align="right" /><ul><li>integrisani Shoutcast stream direktorijum.</li><li>podr&scaron;ku za proizvoljne oznake. Organizujte svoju muziku po sopstvenoj želji.</li><li>Menadžer za Magnatune redownload </li><li>Unapređen kvalitet zvuka pri kori&scaron;ćenju zvuka sa xine sound sistemom. </li></ul>Pored ovoga treba pomenuti mnogo drugih novih i unapređenih postojećih mogućnosti kao i veći broj isrpavljenih gre&scaron;aka iz prethodni verzija. Kompletnu listu isti možete pogledati u nastavku teksta a ja bih&nbsp; jo&scaron; ovde dodao i link ka <a href="http://amarok.kde.org/wiki/Scripts" target="_blank">skriptama</a> <a href="http://amarok.kde.org/wiki/Scripts"> i drugim dodacima</a>  koji vam jo&scaron; vi&scaron;e mogu olak&scaron;ati i ulep&scaron;ati kori&scaron;ćenje ovog odličnog audio plejera.
guid: https://forum.linuxo.org/2007/02/06/stigao-amarok-1-4-5/
id: 1562
image: /wp-content/uploads/2007/02/amarok.png
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1561";s:11:"_thumb_type";s:5:"thumb";}
- a:2:{s:9:"_thumb_id";s:4:"1561";s:11:"_thumb_type";s:5:"thumb";}
title: Stigao Amarok 1.4.5
url: /stigao-amarok-1-4-5/
---
Ovo je ujedno i poslednja verzija serije 1.4.x koja donosi novine i nove mogućnosti. Sledeća izdanja će biti samo ispravke određenih gre&scaron;aka sve do verzije 2.0 koja će pored ostalog biti i multiplatformska, jer će moći da se pokrene na Linux, Mac i MS Windows operativnim sistemima. Najnovije čedo koje pripada <a href="http://amarok.kde.org/content/view/10/66/" target="_blank">Amarok</a> "Fast forward" seriji ima par novih stvarčica između kojih treba pomenuti i<img class=" alignright size-full wp-image-1561" src="https://linuxo.org/wp-content/uploads/2007/02/amarok.png" alt="Amarok" title="Amarok logo" hspace="4" width="128" height="128" align="right" /> 

  * integrisani Shoutcast stream direktorijum.
  * podr&scaron;ku za proizvoljne oznake. Organizujte svoju muziku po sopstvenoj želji.
  * Menadžer za Magnatune redownload 
  * Unapređen kvalitet zvuka pri kori&scaron;ćenju zvuka sa xine sound sistemom. 

Pored ovoga treba pomenuti mnogo drugih novih i unapređenih postojećih mogućnosti kao i veći broj isrpavljenih gre&scaron;aka iz prethodni verzija. Kompletnu listu isti možete pogledati u nastavku teksta a ja bih&nbsp; jo&scaron; ovde dodao i link ka <a href="http://amarok.kde.org/wiki/Scripts" target="_blank">skriptama</a>  [i drugim dodacima](http://amarok.kde.org/wiki/Scripts) koji vam jo&scaron; vi&scaron;e mogu olak&scaron;ati i ulep&scaron;ati kori&scaron;ćenje ovog odličnog audio plejera.  
<!--break-->

&nbsp;

Sledi kompletni ChangeLog (eng.)

### Version 1.4.5

#### Features

  * Added support for custom song labels. Labels can be managed through the GUI or using new DCOP functions. ([BR 89314](http://bugs.kde.org/show_bug.cgi?id=89314)) 
  * New DCOP functions to make it easier for scripts to use Amarok's Dynamic Collection feature. 
  * Download songs from Shared Music (DAAP) directly into the collection. 
  * Fadeout for Helix engine when pressing Stop. 
  * Guided editing of the collection/playlist/devices filters. Patch by Giovanni Venturi. ([BR 139292](http://bugs.kde.org/show_bug.cgi?id=139292)) 
  * Added GUI options for fadeout and fadeout on exit. Both are now enabled by default. 
  * Support for Speex (.spx), WavPack (.wv) and TrueAudio (.tta) files in the collection thanks to taglib plugins by Luk&aacute;� Lalinsk&yacute; . 
  * Search inside of lyrics, by using "/" on Context Browser. Patch by Carles Pina i Estany. ([BR 139210](http://bugs.kde.org/show_bug.cgi?id=139210)) 
  * "Automatically show context browser" feature makes a return, as per popular request. It is however disabled by default. 
  * Improved keyboard navigation: Space key is now a shortcut for Play/Pause, and cursor left/right seeks forward/backward. 
  * Cover images are shown in collection browser. Patch by Trever Fischer . ([BR 91044](http://bugs.kde.org/show_bug.cgi?id=91044)) 
  * Send cover art to MTP media devices if they support it. 
  * Elapsed time can be shown in OSD. Patch by Christian Engels . ([BR 120051](http://bugs.kde.org/show_bug.cgi?id=120051)) 
  * New redownload manager for the Magnatune.com store. Allows re-download of any previous purchase free of charge (in any format). 
  * New items in the playlist are colorized, as a visual cue. 
  * Show rating as stars in flat collection view. Patch by Daniel Faust . ([BR 133797](http://bugs.kde.org/show_bug.cgi?id=133797)) 
  * Synchronize play count, last played time and date of modification to iPods. Patch by Michael. ([BR 136759](http://bugs.kde.org/show_bug.cgi?id=136759)) 
  * Propose list of composers in collection when editing the composer tag from the playlist. ([BR 137775](http://bugs.kde.org/show_bug.cgi?id=137775)) 
  * Greatly improved sound quality for the xine equalizer. Patch by Tobias Knieper. ([BR 127307](http://bugs.kde.org/show_bug.cgi?id=127307)) 
  * Fancy graphical volume slider for the OSD. Patch by Alexander Bechikov . . 
  * Support for %composer and %genre when guessing tags from filenames. 
  * Cached lyrics are now AFT-enabled, and will follow your files around as you move and rename them. 

#### Changes

  * Added configure option to build without DAAP support. 
  * Album covers are now downloaded and added to album directory when purchasing from the Magnatune.com store. ([BR 136680](http://bugs.kde.org/show_bug.cgi?id=136680)) 
  * Update context browser when a change in the collection has been detected. ([BR 140588](http://bugs.kde.org/show_bug.cgi?id=140588)) 
  * Ignore leading 'The ' when sorting playlist by artist. ([BR 139829](http://bugs.kde.org/show_bug.cgi?id=139829)) 
  * Smart Playlists now have 'does not start with' and 'does not end with' options, as well as a dropdown for mount points. ([BR 139552](http://bugs.kde.org/show_bug.cgi?id=139552)) 
  * Support for cue files not matching audio files' name. Patch by Dawid Wr&oacute;bel. ([BR 128046](http://bugs.kde.org/show_bug.cgi?id=128046)) 
  * Script Manager now remembers if categories were open or closed. 
  * Restart collection scanner as long as not more than 5 % of the files make it crash. ([BR 106474](http://bugs.kde.org/show_bug.cgi?id=106474)) 
  * Ensure the first selected item in the Collection Browser stays visible when the search field is cleared using the clear button. 
  * Duplicate filenames are now allowed on MTP media devices if the files are in different folders. 
  * Save media device transfer queue when adding items or after transfers. ([BR 138885](http://bugs.kde.org/show_bug.cgi?id=138885)) 
  * Upgraded internal SQLite to 3.3.12. 
  * MTP media devices are not automatically connected on start-up. This should solve slow loading times for those with large collections on an MTP media device. Contributed by Mikko Sepp&auml;l&auml;. ([BR 138409](http://bugs.kde.org/show_bug.cgi?id=138409)) 
  * Internationalize unknown artist/album/genre strings. Contributed by Mikko Sepp&auml;l&auml;. ([BR 138409](http://bugs.kde.org/show_bug.cgi?id=138409)) 
  * Don't assume that a device returning 0 tracks is invalid. It could just have no tracks on. Contributed by Mikko Sepp&auml;l&auml;. ([BR 138409](http://bugs.kde.org/show_bug.cgi?id=138409)) 
  * Magnatune store look now matches rest of Amarok much better. 
  * Album art is displayed on the Magnatune purchase dialog. 
  * Generic media device now has an option to force VFAT-safe filenames even on non-VFAT filesystems. 
  * Double-clicked items in sidebar and urls passed on the command line are treated equally: append them to playlist if not yet there and start playing the first if nothing is playing. 
  * "Scan Changes" button was replaced with "Update Collection" menu entry. 
  * Consistent double-click behavior in sidebar. ([BR 138125](http://bugs.kde.org/show_bug.cgi?id=138125)) 
  * Propose name of currently loaded playlist when saving current one. 
  * Remove support for older libmtp versions. We now require 0.0.15 or newer. 
  * Deleting a playlist item on an MTP media device now results in it being removed from the playlist. 
  * Magnatune store is lazy loaded to improve startup times. 
  * Dynamic mode logic has been rethought to provide a faster and better user experience. 
  * When checking for duplicate files on a Rio Karma media device, use track number in addition to artist, album & title. ([BR 137152](http://bugs.kde.org/show_bug.cgi?id=137152)) 
  * The XMMS visualization interface has been removed. LibVisual supersedes this feature. 
  * It is now possible to select the time unit for length-based smart playlists. ([BR 136841](http://bugs.kde.org/show_bug.cgi?id=136841)) 
  * Show shadowed cover images in the system tray tooltip. ([BR 136589](http://bugs.kde.org/show_bug.cgi?id=136589)) 
  * Amarok won't crossfade if it was paused, and user started another track. Patch by Tuomas Nurmi. ([BR 136428](http://bugs.kde.org/show_bug.cgi?id=136428)) 
  * Amarok now saves playlists with relative paths by default. 

#### Bugfixes

  * Disable seeking in streams. ([BR 140364](http://bugs.kde.org/show_bug.cgi?id=140364)) 
  * With the default theme, the playlist browser info pane would not show the horizontal scrollbar if necessary. ([BR 134221](http://bugs.kde.org/show_bug.cgi?id=134221)) 
  * Some .rm files would make Amarok crash. ([BR 137695](http://bugs.kde.org/show_bug.cgi?id=137695)) 
  * Remember 'User Cover Art for Folder Icons' when organizing files. ([BR 138582](http://bugs.kde.org/show_bug.cgi?id=138582)) 
  * "Listening since&#8230;" has been changed to the more clear "First Played&#8230;" Patch by Andrew Ash. ([BR 131727](http://bugs.kde.org/show_bug.cgi?id=131727)) 
  * Fixed regression: the DEL key no longer worked in the playlist after opening the File Browser context menu. ([BR 140197](http://bugs.kde.org/show_bug.cgi?id=140197)) 
  * Smart playlists now work correctly with "is not" filters containing numbers. Patch by Felix Rotthowe. 
  * Context browser would not display updated covers correctly. ([BR 130518](http://bugs.kde.org/show_bug.cgi?id=130518)) 
  * The select custom cover dialog no longer starts in the wrong directory for compilations. ([BR 131776](http://bugs.kde.org/show_bug.cgi?id=131776)) 
  * Amarok's xine engine would cut off approximately the last second of an audio file. ([BR 135190](http://bugs.kde.org/show_bug.cgi?id=135190)) 
  * Cue sheet would remain enabled when switching to a stream. Patch by Ted Percival. ([BR 127683](http://bugs.kde.org/show_bug.cgi?id=127683)) 
  * Length of tracks wouldn't be shown correctly for some cue files. Patch by Dawid Wr&oacute;bel ([BR 139707](http://bugs.kde.org/show_bug.cgi?id=139707)) 
  * Assume that all dots but the last in script executable files belong to the script name. ([BR 139460](http://bugs.kde.org/show_bug.cgi?id=139460)) 
  * Don't crash when quitting while initially loading the playlist. ([BR 136353](http://bugs.kde.org/show_bug.cgi?id=136353)) 
  * The same track could be queued multiple times for transferring to a media device. ([BR 129136](http://bugs.kde.org/show_bug.cgi?id=129136)) 
  * Migrate statistics for files moved from outside to the collection. ([BR 127776](http://bugs.kde.org/show_bug.cgi?id=127776)) 
  * Select All/Copy action would not copy from context browser. ([BR 138635](http://bugs.kde.org/show_bug.cgi?id=138635)) 
  * Xine-engine: When a track was fading out (after pressing Stop), and you started another track, Amarok could become unresponsive. 
  * Improved seeking with xine-engine. No longer jumps to 0 when you seek too quickly. Patch by Alexander Bechikov. ([BR 99808](http://bugs.kde.org/show_bug.cgi?id=99808)) 
  * Improved cover images handling for Various Artists. Patch by Tobias Knieper. ([BR 136833](http://bugs.kde.org/show_bug.cgi?id=136833)) 
  * Don't enable a mount point for devices that can't support them (mtp, njb). 
  * With SQLite, the search in the collection browser was case-sensitive with UTF-8. Patch by Stanislav Nikolov. ([BR 138482](http://bugs.kde.org/show_bug.cgi?id=138482)) 
  * (Don't) Show Under Various Artists would not work when multiple albums are selected. Patch by Tobias Knieper. ([BR 112422](http://bugs.kde.org/show_bug.cgi?id=112422)) 
  * Changed temp download location for Magnatune purchases. ([BR 137912](http://bugs.kde.org/show_bug.cgi?id=137912)) 
  * Fixed potential double payment issues in the Magnatune store. 
  * Only synchronize already set values to media devices. ([BR 138150](http://bugs.kde.org/show_bug.cgi?id=138150)) 
  * Correctly update total playlist play time when removing last.fm streams. Patch by Modestas Vainius. ([BR 134333](http://bugs.kde.org/show_bug.cgi?id=134333)) 
  * File organization jobs could not be canceled. Patch by Wenli Liu . ([BR 136527](http://bugs.kde.org/show_bug.cgi?id=136527)) 
  * Sending filenames to MTP media devices as UTF-8 caused problems, use Latin-1 instead. 
  * It's now possible to delete a file from an MTP media device and re-upload it without having to reconnect the device. 
  * Wikipedia links to edit sections are no longer shown. 
  * Metadata is read from Rio Karma media devices as UTF-8. 
  * Last.fm streams could be paused with DCOP or global shortcuts. ([BR 133013](http://bugs.kde.org/show_bug.cgi?id=133013)) 
  * Dynamic mode can still be used after a collection rescan. ([BR 133269](http://bugs.kde.org/show_bug.cgi?id=133269)) 
  * Dynamic mode will repopulate from all available sources. ([BR 137212](http://bugs.kde.org/show_bug.cgi?id=137212)) 
  * Dynamic mode no longer repeats songs often. ([BR 107693](http://bugs.kde.org/show_bug.cgi?id=107693)) 
  * When transferring files to a Generic media device, having certain characters (such as '#') in a tag field could cause a directory based on that field to not be created. 
  * Editing lyrics from within the context browser no longer removes all linebreaks. 
  * Read metadata from MTP media devices as UTF-8. 
  * Some shoutcast streams would show an empty title. ([BR 127741](http://bugs.kde.org/show_bug.cgi?id=127741)) 
  * Pause would act as Play/Pause. ([BR 116101](http://bugs.kde.org/show_bug.cgi?id=116101)) 
  * The same track would sometimes be shown twice in suggested songs. ([BR 129395](http://bugs.kde.org/show_bug.cgi?id=129395)) 
  * Detect VFAT partitioned devices on FreeBSD. Patch by Daniel O'Connor. 
  * Favorite Tracks wouldn't be shown on Context Browser, and Statistics Panel would be empty for SQLite users. ([BR 136791](http://bugs.kde.org/show_bug.cgi?id=136791)) 
  * Volume slider in the player window would not react correctly to the mouse wheel. ([BR 136714](http://bugs.kde.org/show_bug.cgi?id=136714)) 
  * When using a proxy set by script, context browser wouldn't work properly, and the application would crash when closing. ([BR 112437](http://bugs.kde.org/show_bug.cgi?id=112437)) 
  * Proxy settings wouldn't be respected when downloading podcast episodes. ([BR 134028](http://bugs.kde.org/show_bug.cgi?id=134028)) 
  * Xine engine could hang when skipping through tracks quickly with crossfade on. 
  * Fix crash when an MTP media device returned a playlist with an invalid track ID. ([BR 136552](http://bugs.kde.org/show_bug.cgi?id=136552)) 
  * The Install MP3 support script would be run regardless of what the user answered to the shown dialog. ([BR 136294](http://bugs.kde.org/show_bug.cgi?id=136294)) 
  * OSD wouldn't always show up-to-date ratings. Patch by Tuomas Nurmi . ([BR 125612](http://bugs.kde.org/show_bug.cgi?id=125612)) 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1562)