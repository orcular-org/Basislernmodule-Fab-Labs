> Zurück zur [Übersicht Basislernmodule](../../README.md)

# 3D-Scanning

## Inhalt

1. [Einführung](#einführung)
2. [Verfahren und Technologien](#verfahren-und-technologien)
   - [Laserscanning](#laserscanning)
   - [Photogrammetrie](#photogrammetrie)
   - [Gerätetypen](#gerätetypen)
3. [Verarbeitung eines gescannten 3D-Modells](#verarbeitung-eines-gescannten-3d-modells)
   - [Nachbearbeitung](#nachbearbeitung)
   - [Software](#software)
   - [Hardware](#hardware)
   - [3D-Druck von 3D-gescannten Modellen](#3d-druck-von-3d-gescannten-modellen)

[Lizenzinformationen](#lizenzinformationen)

[Bildnachweise](#bildnachweise)

## Einführung

3D-Scanning bezeichnet verschiedene Verfahren, bei denen die Oberflächen von real vorhandenen Objekten, Personen oder Umgebungen mit speziellen Geräten derart erfasst werden, dass ein digitales 3D-Modell davon entsteht. 3D-Scanning wird in vielen Bereichen eingesetzt, z.B. in der Filmindustrie, in der Gelände- und Gebäudevermessung oder in Form von Reverse Engineering, d.h. Reproduktion von vorhandenen technischen Bauteilen.

Im Kontext von Fab Labs und Maker-Communities werden 3D-Scanning-Methoden vor allem zum Erstellen von dreidimensionalen Personenmodellen (sogenannte "3D-Selfies"), zum Nachbilden von Figuren, Spielzeugen u.ä. sowie zur Reproduktion von Ersatzteilen eingesetzt. Aus den 3D-gescannten Modellen lassen sich in Fab Labs wieder reale Objekte fertigen, beispielsweise mit 3D-Druckern.

Je nach eingesetztem 3D-Scanning-Verfahren entstehen entweder farblose bzw. einfarbige 3D-Modelle - d.h. es wird nur die Oberfläche des Objekts erfasst - oder farbige Modelle, die die Farben und Struktur des Objekts bzw. der Person miterfassen und als Textur über das 3D-Modell legen, womit ein relativ realistisches Abbild des realen Objekts entsteht.

<p align="center">
<img height="300" src="images/1_3D_selfie.png">
<img height="300" src="images/2_3D_scanning_MeshLab_example.png">
</p>

<p align="center">
<a href="#s1">[1]</a> <i> 3D-Selfie: Personenmodell, erstellt über 3D-Scanning und 3D-Druck - </i>
<a href="#s2">[2]</a> <i> 3D-gescanntes Modell einer Statue, dargestellt in der Software MeshLab </i>
</p>

<p align="center">
<img height="300" src="images/3_Photogrammetry_with_camera.png">
</p>

<p align="center">
<a href="#s3">[3]</a> <i> Photogrammetrie: Eine 3D-Scanning-Methode unter Verwendung einer Fotokamera </i>
</p>




## Verfahren und Technologien

Es gibt unterschiedliche 3D-Scanning-Verfahren, wovon im Hobby-Bereich und in Fab Labs vor allem zwei hervorzuheben sind:
- Laserscanning
- Photogrammetrie

Zudem gibt es auch Geräte, die eine Kombination aus Laserscanning und Photogrammetrie oder noch weiteren Methoden einsetzen.

### Laserscanning

Beim Laserscanning werden die zu erfassenden Oberflächen zeilen- oder rasterartig mit einem Laserstrahl abgefahren. Die von der Oberfläche reflektierte Laserstrahlung trifft auf Sensoren, woraufhin aus den so gewonnenen Messdaten die jeweilige Entfernung und Position der gescannten Punkte berechnet wird. Aus diesen Daten erzeugt eine Software ein dreidimensionales Modell der Oberfläche.

### Photogrammetrie

Bei der Photogrammetrie wird das zu erfassende Objekt zunächst aus vielen verschiedenen Winkeln fotografiert, entweder mit einer einzelnen Kamera oder mit vielen Kameras gleichzeitig.

Wird nur eine einzelne Kamera verwendet, muss man sie um das Objekt herumführen - von Hand oder maschinell mit einem Roboterarm - und möglichst viele Fotos aus vielen verschiedenen Perspektiven aufnehmen. Dabei sollte sich das Objekt bzw. die Person möglichst nicht bewegen. Möglich ist auch die Verwendung eines Drehtellers, auf dem das Objekt platziert und gedreht wird, sodass die Kamera nur noch in vertikaler Position verschoben werden muss.

Beim Einsatz mehrerer Kameras können diese in verschiedenen Winkeln um das Objekt bzw. die Person herum platziert werden. Die Kameras werden dann alle gleichzeitig ausgelöst.

Eine Software erkennt Unterschiede und Gemeinsamkeiten in den Bildern, findet die gleichen Punkte auf verschiedenen Bildern wieder und berechnet die jeweilige Position eines jeden Punktes im dreidimensionalen Raum. Aus diesen Positionsdaten wird ein 3D-Modell der Oberfläche generiert, zudem können die Farbpunkte (Pixel) der einzelnen Fotografien als Textur über das 3D-Modell gelegt werden.

<p align="center">
<img height="300" src="images/4_Photogrammetry_Meshroom.png">
<img height="300" src="images/5_Photogrammetry_Meshroom2Blender.png">
</p>

<p align="center">
<a href="#s4">[4]</a> <i> Photogrammetrie mit der Software Meshroom - </i>
<a href="#s5">[5]</a> <i> Meshroom2Blender - eine Erweiterung für die 3D-Grafiksoftware Blender </i>
</p>


### Gerätetypen

Geräte für 3D-Scanning gibt es in unterschiedlichen Ausführungen, z.B. als handgeführte Geräte, die man um das Objekt herumträgt, um es aus verschiedenen Winkeln zu erfassen. Es gibt auch Smartphone-Apps, mit denen man die Handykamera für Photogrammetrie-3D-Scanning nutzen kann. Die meisten guten Apps sind in der Regel kostenpflichtig oder nur in eingeschränktem Umfang kostenlos nutzbar.

Vor allem für 3D-Selfies von Personen oder Menschengruppen gibt es Kabinen, die mit einer großen Anzahl an Kameras ausgestattet sind, die die Personen aus allen Richtungen erfassen. Da alle Kameras gleichzeitig ausgelöst werden, geht diese Methode sehr schnell und die abgelichteten Personen müssen nur sehr kurz still halten. 

<p align="center">
<img height="400" src="images/6_Handheld_3D_Scanner.png">
<img height="400" src="images/7_3D_selfie_cabin.png">
</p>

<p align="center">
<a href="#s6">[6]</a> <i> Handgeführter 3D-Scanner mit Laserscanner und integrierter Kamera für Texturierung - </i>
<a href="#s7">[7]</a> <i> 3D-Selfie-Kabine: In der Wand befinden sich viele Kameras, die alle gleichzeitig ausgelöst werden und damit die Person in der Mitte aus verschiedenen Winkeln fotografieren. 
 </i>
</p>



## Verarbeitung eines gescannten 3D-Modells

### Nachbearbeitung

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

### 3D-Druck von 3D-gescannten Modellen

Hat man ein 3D-gescanntes Modell bereinigt und in ein 3D-druckbares Format überführt, z.B. STL (mehr dazu im [Basislernmodul 3D-Druck](../2_1_3D_printing/3D-Druck.md)), kann man es einfach mit einem FDM-3D-Drucker als einfarbiges Objekt ausdrucken. Bei Verwendung eines Mehrfarben-3D-Druckers kann auch eine mehrfarbige Figur gedruckt werden - mit einigen wenigen Farben und beschränkter Genauigkeit.

Möchte man eine sehr detaillierte 3D-Druck-Figur mit vielen Farben und hoher Genauigkeit der Oberflächenoptik erhalten, reicht ein einfacher FDM-3D-Drucker (FDM = Fused Deposition Modeling, mehr dazu [hier](../2_1_3D_printing/3D-Druck.md)) nicht aus. Kommerzielle Anbieter von 3D-Selfies nutzen meist eine andere 3D-Druck-Technologie: Binder Jetting, auch als Freistrahl-Bindemittelauftrag bezeichnet. Bei diesem 3D-Druck-Verfahren wird ein Pulver mit flüssigem Bindemittel aufgetragen und verbunden. Die entstehenden Figuren haben oft eine an Sandstein erinnernde Optik, zudem eine große Farbenvielfalt und Detailtreue.

<p align="center">
<img height="300" src="images/10_3D_printed_3D_selfie.png">
</p>

<p align="center">
<a href="#s10">[10]</a> <i> 3D-gedrucktes Modell eines 3D-Selfies </i>
</p>


Schließlich gibt es auch die Möglichkeit, eine einfarbig (möglichst weiß) gedruckte Figur aus dem FDM-3D-Drucker nachträglich zu bearbeiten und zu bemalen.

# Lizenzinformationen

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Bildnachweise

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

