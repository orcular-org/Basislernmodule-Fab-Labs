**Translation note:**

This article is still being translated into **English**.

To do:
- Edit file
- Replace text by English translation
- Commit changes
- When done, remove this note

> Back to [basic learning modules overview](../../translations/EN_Readme.md)

# 3D scanning

## Contents

1. [Introduction](#introduction)
2. [Processes and technologies](#processes-and-technologies)
   - [Laser scanning](#laser-scanning)
   - [Photogrammetry](#photogrammetry)
   - [Device types](#device-types)
3. [Processing of a scanned 3D model](#processing-of-a-scanned-3d-model)
   - [Post processing](#post-processing)
   - [Software](#software)
   - [Hardware](#hardware)
   - [3D printing from 3D scanned models](#3d-printing-from-3d-scanned-models)

[License information](#license-information)

[Image references](#image-references)

## Introduction

3D scanning refers to various processes in which the surfaces of real objects, people or environments are recorded with special devices in such a way that a digital 3D model is created. 3D scanning is used in many areas, e.g. in the film industry, in terrain and building surveying or in the form of reverse engineering, i.e. the reproduction of existing technical components.

In the context of fab labs and maker communities, 3D scanning methods are primarily used to create three-dimensional human models (so-called "3D selfies"), to replicate figures, toys, and the like, as well as for the reproduction of spare parts. Real objects can be produced from the 3D scanned models in fab labs, for example with 3D printers.

Depending on the 3D scanning method used, either colorless (monochrome) 3D models are created - i.e. only the surface of the object is captured - or colored models that capture the colors and structure of the object or person and overlay them as a texture on the 3D model, creating a relatively realistic image of the real object.

<p align="center">
<img height="300" src="images/1_3D_selfie.png">
<img height="300" src="images/2_3D_scanning_MeshLab_example.png">
</p>

<p align="center">
<a href="#s1">[1]</a> <i> 3D selfie: Person model created via 3D scanning and 3D printing - </i>
<a href="#s2">[2]</a> <i> 3D scanned model of a statue rendered in MeshLab software </i>
</p>

<p align="center">
<img height="300" src="images/3_Photogrammetry_with_camera.png">
</p>

<p align="center">
<a href="#s3">[3]</a> <i> Photogrammetry: A 3D scanning method using a photo camera </i>
</p>




## Processes and technologies

There are different 3D scanning methods, of which two in particular stand out in the hobby sector and in fab labs:
- Laser scanning
- Photogrammetry

There are also devices that use a combination of laser scanning and photogrammetry or other methods.

### Laser scanning

With laser scanning, the surfaces to be recorded are scanned in a line or grid pattern with a laser beam. The laser radiation reflected from the surface hits sensors, whereupon the respective distance and position of the scanned points is calculated from the measurement data obtained in this way. Software uses this data to create a three-dimensional model of the surface.

### Photogrammetry

In photogrammetry, the object to be captured is first photographed from many different angles, either with a single camera or with many cameras simultaneously.

If only a single camera is used, you have to move it around the object - by hand or mechanically with a robotic arm - and take as many photos as possible from many different perspectives. The object or person should not move if possible. It is also possible to use a turntable on which the object is placed and rotated so that the camera only has to be moved in the vertical position.

When using multiple cameras, they can be placed at different angles around the object or person. The cameras are then all triggered at the same time.

Software recognizes differences and similarities in the images, finds the same points on different images and calculates the respective position of each point in three-dimensional space. A 3D model of the surface is generated from this position data. In addition, the color points (pixels) of the individual photographs can be laid over the 3D model as a texture.

<p align="center">
<img height="300" src="images/4_Photogrammetry_Meshroom.png">
<img height="300" src="images/5_Photogrammetry_Meshroom2Blender.png">
</p>

<p align="center">
<a href="#s4">[4]</a> <i> Photogrammetry with the software Meshroom - </i>
<a href="#s5">[5]</a> <i> Meshroom2Blender - an extension for the 3D graphics software Blender </i>
</p>


### Device types

Devices for 3D scanning come in different forms, e.g. as handheld devices that you carry around the object to capture it from different angles. There are also smartphone apps that allow you to use your phone camera for photogrammetry 3D scanning. Most good apps are usually paid or only available for free to a limited extent.

Especially for 3D selfies of people or groups of people, there are booths that are equipped with a large number of cameras that capture people from all directions. Since all cameras are triggered at the same time, this method is very quick and the people photographed only have to stay still for a very short time. 

<p align="center">
<img height="400" src="images/6_Handheld_3D_Scanner.png">
<img height="400" src="images/7_3D_selfie_cabin.png">
</p>

<p align="center">
<a href="#s6">[6]</a> <i> Handheld 3D scanner with laser scanner and integrated camera for texturing - </i>
<a href="#s7">[7]</a> <i> 3D photo booth: There are many cameras in the wall that all fire at the same time, taking pictures of the person in the center from different angles. 
 </i>
</p>



## Processing of a scanned 3D model

### Post processing

Bei vielen 3D-Scanning-Methoden muss das 3D-Modell noch in einer Software nachbearbeitet werden, bevor es z.B. für 3D-Druck verwendet werden kann.

Je nach Verfahren liegt das Modell zunächst entweder als Polygonnetz oder als Punktwolke vor und muss mit Software zu einem sauberen Modell zusammengefügt, bereinigt und geglättet werden.

<p align="center">
<img height="250" src="images/8_Polygon_Mesh_Dolphin_example.png">
<img height="250" src="images/9_Point_Cloud_Tux_example.png">
</p>

<p align="center">
<a href="#s8">[8]</a> <i> Beispiel für ein Polygonnetz - </i>
<a href="#s9">[9]</a> <i> Beispiel für eine Punktwolke (erstellt per Photogrammetrie) </i>
</p>


### Software

Im Bereich 3D-Scanning gibt es u.a. folgende **Software**:

- [Meshroom](https://alicevision.org/#meshroom): Kostenlose Open-Source-Software für 3D-Rekonstruktion, basierend auf dem [AliceVision Framework](https://alicevision.org/), einem Software-Paket für Photogrammetrie-Anwendungen.
- [MeshLab](https://www.meshlab.net/): Kostenlose Open-Source-Software zum Bearbeiten, Bereinigen, Rendering, Texturieren und Konvertieren von 3D-gescannten Polygonnetz-3D-Modellen.
- [3DF Zephyr](https://www.3dflow.net): Ein Programm mit einer [kostenlosen](https://www.3dflow.net/3df-zephyr-free/) und mehreren kostenpflichtigen Versionen für Photogrammetrie, also für die Generierung von 3D-Modellen aus mehreren 2D-Einzelbildern.
- [ReconstructMe](https://www.reconstructme.net): Software zum Erstellen von 3D-Selfies mit eigener Kamera - verfügbar sind sowohl eine kostenlose als auch eine kostenpflichtige Version.

### Hardware

Für Fab Labs und Maker gibt es u.a. folgende **Geräte und Hardware-Projekte** (teilweise Open-Source-Hardware):
- [OpenScan](https://www.openscan.eu/) - ([GitHub-Seite](https://openscan-org.github.io/OpenScan-Doc/))
- [FabScan](https://fabscan.org)
- [MakerScanner](http://www.makerscanner.com/)

Zudem gibt es auch professionelle Geräte, die jedoch sehr teuer sind und in der Regel nur von Unternehmen genutzt werden, doch auch manche Fab Labs verfügen über solche Geräte.

### 3D printing from 3D scanned models

Hat man ein 3D-gescanntes Modell bereinigt und in ein 3D-druckbares Format überführt, z.B. STL (mehr dazu im [Basislernmodul 3D-Druck](../2_1_3D_printing/3D-Druck.md)), kann man es einfach mit einem FDM-3D-Drucker als einfarbiges Objekt ausdrucken. Bei Verwendung eines Mehrfarben-3D-Druckers kann auch eine mehrfarbige Figur gedruckt werden - mit einigen wenigen Farben und beschränkter Genauigkeit.

Möchte man eine sehr detaillierte 3D-Druck-Figur mit vielen Farben und hoher Genauigkeit der Oberflächenoptik erhalten, reicht ein einfacher FDM-3D-Drucker (FDM = Fused Deposition Modeling, mehr dazu [hier](../2_1_3D_printing/3D-Druck.md)) nicht aus. Kommerzielle Anbieter von 3D-Selfies nutzen meist eine andere 3D-Druck-Technologie: Binder Jetting, auch als Freistrahl-Bindemittelauftrag bezeichnet. Bei diesem 3D-Druck-Verfahren wird ein Pulver mit flüssigem Bindemittel aufgetragen und verbunden. Die entstehenden Figuren haben oft eine an Sandstein erinnernde Optik, zudem eine große Farbenvielfalt und Detailtreue.

<p align="center">
<img height="300" src="images/10_3D_printed_3D_selfie.png">
</p>

<p align="center">
<a href="#s10">[10]</a> <i> 3D-gedrucktes Modell eines 3D-Selfies </i>
</p>


Schließlich gibt es auch die Möglichkeit, eine einfarbig (möglichst weiß) gedruckte Figur aus dem FDM-3D-Drucker nachträglich zu bearbeiten und zu bemalen.

# License information

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Image references

<a name="s1"></a>
**[1]** 3D selfie in 1-20 scale as received from Shapeways, the printer company for Madurodam's Fantasitron IMG 4557 FRD.jpg - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:3D_selfie_in_1-20_scale_as_received_from_Shapeways,_the_printer_company_for_Madurodam%27s_Fantasitron_IMG_4557_FRD.jpg

<a name="s2"></a>
**[2]** MeshLabv121 david.png - **Image license:** [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.html.en) - **Source:** https://commons.wikimedia.org/wiki/File:MeshLabv121_david.png

<a name="s3"></a>
**[3]** Balkan Heritage Field School (photogrammetry course) at Stobi, Republic of Macedonia (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Balkan_Heritage_Field_School-5.jpg

<a name="s4"></a>
**[4]** buddha_dataset.png - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://alicevision.org (home page)

<a name="s5"></a>
**[5]** meshroom2blender.jpg - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://alicevision.org (home page)

<a name="s6"></a>
**[6]** VIUscan handheld 3D scanner in use.jpg - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:VIUscan_handheld_3D_scanner_in_use.jpg

<a name="s7"></a>
**[7]** 3D-scanning photo booth for 3D selfies at the Doob NY SOHO store. - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Doob_NY_SOHO_3D_selfie_photo_booth_IMG_4939_FRD.jpg

<a name="s8"></a>
**[8]** An example of a polygon mesh. - **Image license:** [Public domain](https://en.wikipedia.org/wiki/Public_domain) - **Source:** https://commons.wikimedia.org/wiki/File:Dolphin_triangle_mesh.svg

<a name="s9"></a>
**[9]** TuxaufRasen-Photogrammetriepunktwolke.png - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:TuxaufRasen-Photogrammetriepunktwolke.png

<a name="s10"></a>
**[10]** Madurodam Shapeways 3D selfie in 1 20 scale after a second spray of varnish FRD.jpg - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Madurodam_Shapeways_3D_selfie_in_1_20_scale_after_a_second_spray_of_varnish_FRD.jpg

