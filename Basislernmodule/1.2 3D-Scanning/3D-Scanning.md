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

Je nach eingesetztem 3D-Scanning-Verfahren entstehen entweder farblose bzw. einfarbige 3D-Modelle - d.h. es wird nur die Oberfläche des Objekts erfasst - oder farbige Modelle, die die Farben und Struktur des Objekts bzw. der Person miterfassen und als Textur über das 3D-Modell legen, womit ein relativ realisitisches Abbild des realen Objekts entsteht.

> Bilder

## Verfahren und Technologien

Es gibt unterschiedliche 3D-Scanning-Verfahren, wovon im Hobby-Bereich und in Fab Labs vor allem zwei hervorzuheben sind:
- Laserscanning
- Photogrammetrie

Zudem gibt es auch Geräte, die eine Kombination aus Laserscanning und Photgrammetrie oder noch weiteren Sensortypen einsetzen.

### Laserscanning

Beim Laserscanning werden die zu erfassenden Oberflächen zeilen- oder rasterartig mit einem Laserstrahl abgefahren. Die von der Oberfläche reflektierte Laserstrahlung trifft auf Sensoren, während aus den Messdaten die jeweilige Entfernung und Position der gescannten Punkte berechnet wird. Aus diesen Daten erzeugt eine Software ein dreidimensionales Modell der Oberfläche.

> Bild Laserscan

### Photogrammetrie

Bei der Photogrammetrie wird das zu erfassende Objekt zunächst aus vielen verschiedenen Winkeln fotografiert, entweder mit einer einzelnen Kamera oder mit vielen Kameras gleichzeitig.

Wird nur eine einzelne Kamera verwendet, muss man sie um das Objekt herumführen - von Hand oder maschinell mit einem Roboterarm - und möglichst viele Fotos aus vielen verschiedenen Perspektiven aufnehmen. Dabei sollte sich das Objekt bzw. die Person möglichst nicht bewegen. Möglich ist auch die Verwendung eines Drehtellers, auf dem das Objekt platziert und gedreht wird, sodass die Kamera nur noch in vertikaler Position verschoben werden muss.

Beim Einsatz mehrerer Kameras können diese in verschiedenen Winkeln um das Objekt bzw. die Person herum platziert werden. Die Kameras werden dann alle gleichzeitig ausgelöst.

Eine Software erkennt Unterschiede und Gemeinsamkeiten in den Bildern, findet die gleichen Punkte auf verschiedenen Bildern wieder und berechnet die jeweilige Position im dreidimensionalen Raum eines jeden Punktes. Aus diesen Positionsdaten wird ein 3D-Modell der Oberfläche generiert, zudem können die Farbpunkte (Pixel) der einzelnen Fotografien als Textur über das 3D-Modell gelegt werden.

> Bilder Photogrammetrie

### Gerätetypen

Geräte für 3D-Scanning gibt es in unterschiedlichen Ausführungen, z.B. als handgeführte Geräte, die man um das Objekt herumträgt, um es aus verschiedenen Winkeln zu erfassen. Es gibt auch Smartphone-Apps, mit denen man die Handykamera für Photogrammetrie-3D-Scanning nutzen kann. Die meisten guten Apps sind in der Regel kostenpflichtig oder nur im eingeschränkten Umfang kostenlos nutzbar.

Vor allem für 3D-Selfies von Personen oder Menschengruppen gibt es Kabinen, die mit einer großen Anzahl an Kameras ausgestattet sind, die die Personen aus allen Richtungen erfassen. Da alle Kameras gleichzeitig ausgelöst werden, geht diese Methode sehr schnell und die abgelichteten Personen müssen nur sehr kurz still halten. 

> Bilder Handheld-3D-Scanner, Kabine (Foto), Kabine (Schema/Skizze)


## Verarbeitung eines gescannten 3D-Modells

### Nachbearbeitung

Bei vielen 3D-Scanning-Methoden muss das 3D-Modell noch in einer Software nachbeartbeitet werden, bevor es z.B. für 3D-Druck verwendet werden kann.

Je nach Verfahren liegt das Modell zunächst entweder als Polygonnetz oder als Punktwolke vor und muss mit Software zu einem sauberen Modell zusammengefügt, bereinigt und geglättet werden.

> Bilder Polygonnetz und Punktwolke

### Software

Im Bereich 3D-Scanning gibt es u.a. folgende **Software**:

- [Meshroom](https://alicevision.org/#meshroom): Kostenlose Open-Source-Software für 3D-Rekonstruktion, basierend auf dem [AliceVision framework](https://alicevision.org/), einem Software-Paket für Photogrammetrie-Anwendungen.
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

Hat man ein 3D-gescanntes Modell bereinigt und in ein 3D-druckbares-Format überführt, z.B. STL (mehr dazu im Basislernmodul 3D-Druck), kann man es einfach mit einem FDM-3D-Drucker als einfarbiges Objekt ausdrucken. Bei Verwendung eines Mehrfarben-3D-Druckers kann auch eine mehrfarbige Figur gedruckt werden - mit einigen wenigen Farben und beschränkter Genauigkeit.

Möchte man eine sehr detaillierte 3D-Druck-Figur mit vielen Farben und hoher Genauigkeit der Oberflächenoptik erhalten, reicht ein einfacher FDM-3D-Drucker (verlinken) nicht aus. Kommerzielle Anbieter von 3D-Selfies nutzen meist eine andere 3D-Druck-Technologie: Binder Jetting, auch als Freistrahl-Bindemittelauftrag bezeichnet. Bei diesem 3D-Druck-Verfahren wird ein Pulver mit flüssigen Bindemittel aufgetragen und verbunden. Die entstehenden Figuren haben oft eine an Sandstein erinnernde Optik, zudem eine große Farbenvielfalt und Detailtreue.

> Bilder-Serie Binder Jetting Figur

Schließlich gibt es auch die Möglichkeit, eine einfarbig (möglichst weiß) gedruckte Figur aus dem FDM-3D-Drucker nachträglich zu bearbeiten und zu bemalen.

# Lizenzinformationen

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Bildnachweise

(Platzhalter)
