> Zurück zur [Übersicht Basislernmodule](../../README.md)

# 3D-Design
## Inhalt

1. [Einführung](#einf%C3%BChrung)
2. [CAD-Software](#cad-software)
   - [Dateiformate für CAD-Modelle](#dateiformate-f%C3%BCr-cad-modelle)
   - [Beispiele für CAD-Software](#beispiele-f%C3%BCr-cad-software)
     - [FreeCAD](#freecad)
     - [Autodesk Fusion 360](#autodesk-fusion-360)
3. [3D-Grafik- und Modellierungsprogramme](#3d-grafik--und-modellierungsprogramme)
   - [Beispiele für 3D-Grafik- und 3D-Modellierungsprogramme](#beispiele-f%C3%BCr-3d-grafik--und-3d-modellierungsprogramme)
     - [Blender](#blender)
     - [Tinkercad](#tinkercad) 

[Lizenzinformationen](#lizenzinformationen)

[Bildnachweise](#bildnachweise)


## Einführung

Es gibt verschiedene Software, mit denen man digitale 3D-Modelle zeichnen bzw. modellieren kann. Diese 3D-Modelle können anschließend z.B. für 3D-Druck, Lasercutting oder CNC-Fräsen genutzt werden.

Je nach Anwendungszweck gibt es Programme mit unterschiedlichen Schwerpunkten und Funktionen. Zum Modellieren von Bauteilen für technische Produkte wird in der Regel CAD-Software benutzt (CAD = Computer Aided Design; engl. für „Computergestütztes Entwerfen“). Andererseits gibt es auch 3D-Grafikprogramme, die einen eher künstlerischen Schwerpunkt haben, z.B. für komplex geformte Figuren, die für 3D-Druck, Produktdesign, aber auch z.B. für 3D-Animationsfilme verwendet werden können.

<p align="center">									
<img height="300" src="https://user-images.githubusercontent.com/123781559/230741949-fb767a24-7d64-41e1-ac21-6c8ee098d404.png">									
<img height="300" src="https://user-images.githubusercontent.com/123781559/230742006-6dc72ee1-34d6-4eee-affc-183329d7f9eb.png">																	
</p>									
									
<p align="center">									
<a href="#s1">[1]</a> <i> Baugruppe in der Software FreeCAD - </i>									
<a href="#s2">[2]</a> <i> 3D-Modell in der 3D-Modellierungssoftware Blender </i>																	
</p>									

Statt eigene 3D-Modelle zu erstellen, kann man auch fertige Modelle aus dem Internet herunterladen, ggf. nachbearbeiten und anschließend z.B. mit einem 3D-Drucker ausdrucken (mehr dazu im [Basislernmodul 3D-Druck](../2_1_3D_printing/3D-Druck.md)). Es gibt eine Vielzahl an Webseiten, von denen man 3D-Modelle beziehen oder auf die man seine eigenen Kreationen hochladen und sie mit anderen teilen kann (mehr dazu im [Basislernmodul zum Thema Download von 3D-Modellen](../1_3_Using_3D_models_from_the_internet/Verwendung_von_3D_Modellen_aus_dem_Internet.md)).

Eine weitere Möglichkeit, ein 3D-Modell zu erstellen, besteht im 3D-Scanning. Damit lassen sich Gegenstände, Ersatzteile oder auch Personen einscannen und als 3D-Modell am Rechner abbilden. Mit etwas Nachbearbeitung lassen sich diese Modelle auch 3D-drucken (mehr dazu im [Basislernmodul zu 3D-Scanning](../1_2_3D_scanning/3D-Scanning.md)).

## CAD-Software

CAD-Software wird in der Regel im technischen Bereich eingesetzt, z.B. im Maschinenbau, in der Architektur oder Elektrotechnik – bei Unternehmen für Produktentwicklung, Planung von Gebäuden und ähnlichen Bereichen. Aber auch für Hobby-Anwendungen, z.B. zum Designen von Objekten für 3D-Druck oder CNC-Fräsen, haben sich CAD-Programme bewährt.

Soll ein in CAD entworfenes Modell mithilfe von CNC-Maschinen (fräsen oder drehen) gefertigt werden, muss es in einer CAM-Software (CAM = Computer Aided Manufacturing) bearbeitet werden, um Fräsdurchmesser, Drehzahlen, Arbeitsabläufe etc. zu definieren (mehr dazu im [Basislernmodul zu CNC-Fräsen](../2_3_CNC_milling/CNC-Fraesen.md)). Viele CAD-Programme haben ein integriertes CAM-Modul, man spricht dann von CAD/CAM-Software.

Beim Erstellen eines 3D-Modells – bei CAD spricht man von „modellieren“ oder „konstruieren“ – arbeitet man meistens mit sogenannter geometrischer und generativer Modellierung.

Dabei startet man üblicherweise mit dem Zeichnen einer 2D-Skizze, die aus Punkten, Linien, Kurven und geometrischen Formen wie Kreisen oder Sechsecken besteht. Mit Bemaßungen kann man die Skizzenelemente exakt definieren, z.B. Länge von Linien oder Kreisdurchmesser millimetergenau festlegen. Durch sogenannte Abhängigkeiten kann man beispielsweise festlegen, dass zwei Linien parallel oder gleich lang sein sollen. Als nächster Schritt wird diese 2D-Skizze zu einem 3D-Objekt mit festgelegter Dicke „aufgepolstert“ (engl. "Pad") oder um eine Achse rotiert wird, um einen Drehkörper (engl. "Revolution") zu erstellen. Aufbauend auf diesem Objekt können weitere Elemente hinzugefügt werden, etwa durch weitere 2D-Skizzen und Aufpolsterung/Drehung, durch Abziehen von Teilen (z.B. für Löcher, Bohrungen oder Taschen (engl. "Pocket")), durch Vervielfältigung von Elementen oder Abrundung von Kanten.

<p align="center">
[3] <img height="130" src="https://user-images.githubusercontent.com/123781559/230787254-ebd619b0-d32e-4870-903f-1376d1a02625.png"> <br>
[4] <img height="130" src="https://user-images.githubusercontent.com/123781559/230787339-42671cf1-cdf9-4c2b-b961-447bfd418588.png"> <br>
[5] <img height="130" src="https://user-images.githubusercontent.com/123781559/230787386-b8406c93-b49e-456c-8611-8e90f8bf9391.png">
</p>

<p align="center">
<a href="#s3">[3]</a> <i> 3D-Aufpolsterung (Pad) aus einer 2D-Skizze - </i>
<a href="#s4">[4]</a> <i> 3D-Drehkörper (Revolution) aus 2D-Skizze - </i>
<a href="#s5">[5]</a> <i> Tasche (Pocket) aus 2D-Skizze </i>
</p>


<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230790441-ef7c1deb-014a-4441-9c7d-ffd4dde279f8.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230790464-0a6f5112-d468-457e-9855-ff1a709c298a.png">
</p>

<p align="center">
<a href="#s6">[6]</a> <i> Konstruktionsskizze in FreeCAD - </i>
<a href="#s7">[7]</a> <i> Ein mit geometrischer Modellierung erstelltes Bauteil in FreeCAD </i>
</p>


Viele CAD-Programme enthalten auch Funktionen zum Erstellen von technischen Maßzeichnungen. Dabei wird das Bauteil zunächst in 3D modelliert und anschließend aus verschiedenen Blickrichtungen auf eine 2D-Zeichnung projiziert. Diese Ansichten können auf einem Blatt angeordnet, mit Bemaßungen sowie weiteren Informationen versehen und ausgedruckt werden. Dies ist hilfreich für Teile, die man nicht mit digitalen Fertigungsmethoden herstellen möchte, sondern mit konventionellen Werkzeugen, z.B. Zuschneiden und Bohren von Holzbrettern oder Aluminiumprofilen.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/230791093-6e675d05-3405-4e3e-82ef-5ad42a848693.png">
</p>

<p align="center">
<a href="#s8">[8]</a> <i> Technische (Maß)zeichnung in FreeCAD </i>
</p>

Einige CAD-Programme verfügen über Funktionen für „parametrisches Design“. Dabei werden Bauteile nicht mit exakten Zahlenwerten bemaßt (z.B. 10 mm), sondern mit Parametern (z.B. mit „Länge“ oder „Durchmesser“). Mit einem parametrischen Modell können dann viele unterschiedliche Varianten des Bauteils generiert werden, so muss etwa eine Schraube nicht in jeder beliebigen Variante neu modelliert werden, sondern nur einmal als parametrisches Modell, wobei man z.B. die Parameter „Länge“ und „Durchmesser“ variiert und das jeweils erzeugte Schraubenmodell als Variante abspeichert. Parameter können auch mithilfe von Formeln verknüpft werden (z.B. „Länge = 2 x Durchmesser + 10 mm“).

Auf Videoportalen wie YouTube finden sich viele Video-Tutorials für das Erlernen von CAD-Modellierung. Manche Fab Labs bieten auch Workshops an. Grundlagen für einfache Modelle lassen sich relativ schnell erlernen, für komplexere CAD-Projekte und erweiterte Funktionen braucht es jedoch viel Einarbeitung und Übung.


### Dateiformate für CAD-Modelle

Jede Software hat ihr eigenes Dateiformat für Projektdateien, z.B. haben Dateien in der Software "FreeCAD" die Dateiendung *.FCStd und Dateien in "Autodesk Fusion 360" die Endung *.f3d.
Es gibt im CAD-Bereich aber zahlreiche unterschiedliche Dateiformate, die von unterschiedlichen CAD-Programmen erstellt und geöffnet werden können.

Besonders hervorzuheben ist das STEP-Dateiformat (*.ste, *.step oder *.stp). STEP steht für „STandard for the Exchange of Product model data” und ist in einer weltweit anerkannten ISO-Norm standardisiert. STEP-Dateien eignen sich daher gut als Austauschformat zwischen unterschiedlichen CAD-Programmen. Möchte man seine CAD-Datei mit jemandem teilen, der eine andere CAD-Software benutzt, ist das Exportieren im STEP-Format also oft eine gute Lösung, auch wenn nicht alle Informationen und Editierfunktionen erhalten bleiben, aber zumindest kann die Datei in der anderen Software geöffnet, betrachtet und analysiert werden.

Plant man sein Produkt als Open Source Hardware zu veröffentlichen, ist es empfehlenswert, eine CAD-Software zu verwenden, die kostenfrei ist und auf Open Source Software basiert (z.B. FreeCAD oder Blender, mehr dazu siehe unten), damit möglichst viele Menschen die Dateien öffnen, bearbeiten und als verbesserte Variante zum Projekt beitragen können.

Ein weiteres wichtiges Dateiformat ist STL, vor allem für 3D-Druck. Praktisch jede bekannte CAD- oder 3D-Grafiksoftware kann 3D-Modelle im STL-Format exportieren, sodass man sie anschließend 3D-drucken kann (mehr dazu im [Basislernmodul 3D-Druck](../2_1_3D_printing/3D-Druck.md)).


### Beispiele für CAD-Software

Hier eine Auswahl einiger beliebter CAD-Programme, die weitestgehend kostenlos nutzbar sind:

#### FreeCAD

FreeCAD ist, wie der Name schon sagt, eine sogenannte „Free and open-source software“, d.h. die Software ist uneingeschränkt kostenlos, also auch für kommerzielle Anwendungen, und ihr Quellcode ist offen. Dies macht FreeCAD zu einer beliebten Softwarelösung in Open-Source-Communities, da garantiert ist, dass mit FreeCAD erstellte Projekte auch langfristig von jedem kostenlos geöffnet und bearbeitet werden können (als Open Source Hardware). Zudem kann FreeCAD von jedem modifiziert oder durch Erweiterungen ergänzt und verbessert werden (Open Source Software), wodurch es schon zahlreiche, von der Nutzer:innen-Community programmierte Bugfixes, Zusatzfunktionen, Workbenches und Makros gibt.

FreeCAD enthält viele unterschiedliche Programm-Module (sogenannte „Workbenches“) und Funktionen für 3D-Modellierung, 3D-Druck, CAM und CNC-Fräsen, Lasercutting, Bewegungssimulationen, Architektur und vieles mehr. Eine besondere Stärke von FreeCAD ist auch das parametrische Designen, wobei mit der „Spreadsheet“-Workbench Kalkulationstabellen erstellt werden können, mit denen man Parameter des CAD-Modells steuern kann. FreeCAD ist nicht cloud-basiert, sondern läuft rein lokal auf dem Rechner (Windows, Mac oder Linux).

**Download:** https://www.freecad.org/

**FreeCAD-Wiki:** https://wiki.freecad.org/ - In deutscher Sprache (teilweise unvollständig): https://wiki.freecad.org/Main_Page/de

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230791448-53b14b55-1f3d-4dbe-b351-d9323aa8fb55.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230791596-5868e09f-cb26-4cc5-9ead-c20ae9d21017.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i> FreeCAD-Benutzeroberfläche - </i>
<a href="#s10">[10]</a> <i> Baugruppe mit Skizzen in FreeCAD </i>
</p>


#### Autodesk Fusion 360

Fusion 360 ist eine von Autodesk entwickelte Software-Suite für CAD, CAM und weitere technische Anwendungen. Grundsätzlich ist Fusion 360 ein kostenpflichtiges Programm, es lässt sich jedoch unter bestimmten Bedingungen und mit eingeschränkter Funktionalität auch kostenlos nutzen. So muss man bei der Registrierung angeben, dass man Privatanwender:in ist („personal use“). Diese kostenlose „Hobby-Lizenz“ muss regelmäßig erneuert werden. Sobald man Projekte kommerziell nutzen möchte, ist man verpflichtet, eine Lizenz zu kaufen. Zudem stehen unter der kostenlosen Lizenz nicht alle Funktionen zur Verfügung. Die Bedingungen und Funktionen für kostenlose Nutzung können sich noch öfters ändern, die aktuellen Infos hierzu findet man auf der [Fusion-360-Webseite](https://www.autodesk.de/products/fusion-360/).

Fusion 360 ist cloud-basiert, d.h. man benötigt eine Verbindung zum Internet und muss sich bei erster Benutzung mit seinen Kontodaten anmelden. Projektdateien werden online in einer Cloud von Autodesk gespeichert, können jedoch auch lokal heruntergeladen werden (z.B. als f3d-Datei). Falls keine Internetverbindung besteht, kann auch zeitweilig offline gearbeitet werden, die Dateien werden bei nächster Verbindung mit dem Internet synchronisiert. Die erstmalige Anmeldung muss jedoch online erfolgen.

Aufgrund seiner klaren und verständlichen Bedienbarkeit gilt Fusion 360 als vergleichsweise leicht erlernbare CAD-Software, was sie zu einem viel genutzten und beliebten Programm in Maker-Communities macht.

**Registrierung und Download für Privatanwender:innen:** https://www.autodesk.de/products/fusion-360/personal

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230791930-d1f61b09-237b-4588-8795-999f708b8deb.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/230791949-6f1ebd53-2d95-4a97-b80d-a833959c66ae.png">
</p>

<p align="center">
<a href="#s11">[11]</a> <i> </i>
<a href="#s12">[12]</a> <i> Autodesk Fusion 360: Benutzeroberfläche</i>
</p>



## 3D-Grafik- und Modellierungsprogramme

Im Gegensatz zu CAD-Programmen, die eher für technische Produktentwicklung genutzt werden, richten sich 3D-Grafikprogramme eher an künstlerische oder Design-bezogene Anwendungen, z.B. zum Gestalten von Figuren, Vasen, Gefäßen oder sonstigen, komplex gestalteten Formen.

Dabei kommen oft sogenannte Sculpting-Werkzeuge zum Einsatz, womit sich 3D-Objekte präzise verformen lassen, ähnlich wie beim Töpfern mit Ton. Die millimetergenaue Bemaßung sowie Konstruktion von eher eckigen Teilen, wie bei technischen Bauteilen in CAD-Programmen, steht damit weniger im Vordergrund als die Freiheit in der Form- und Ausgestaltung des 3D-Objekts.

Weitere Funktionen von 3D-Grafikprogrammen sind z.B. die Texturierung, Animation (für Animationsfilme oder Videospiele) und Rendering, z.B. zur Inszenierung eines Objekts oder Produkts in einer bestimmten Umgebung und Belichtung in einer sogenannten Szene. Viele 3D-Grafikprogramme können die Modelle als STL-Datei exportieren, womit sie sich 3D-drucken lassen.

<p align="center">
<img height="250" src="https://user-images.githubusercontent.com/123781559/231005150-ca68ab7e-513b-40cb-82b2-33b35e3654b9.png">
<img height="250" src="https://user-images.githubusercontent.com/123781559/231005186-7ccdc655-0b44-4dec-8165-c06afcf1d2dd.png">
</p>

<p align="center">
<a href="#s13">[13]</a> <i> Scultping in der Software Blender - </i>
<a href="#s14">[14]</a> <i> Rendering von Kochtöpfen in Blender </i>
</p>



### Beispiele für 3D-Grafik- und 3D-Modellierungsprogramme

Hier eine Auswahl einiger beliebter 3D-Grafik- und 3D-Modellierungsprogramme, die kostenlos nutzbar sind:

#### Blender

Blender ist eine 3D-Grafiksuite, die als „Free and open-source software“, also kostenlos verfügbar und mit offenem Quellcode veröffentlich ist. Die Software-Suite umfasst Funktionen zum modellieren, texturieren und animieren. Blender ist ein im professionellen wie auch im Hobby-Bereich sehr beliebtes Programm, gilt als besonders ausgereifte Open-Source-Software und die Grundlagen lassen sich verhältnismäßig leicht erlernen.

**Download:** https://www.blender.org/

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231006876-84ec1b88-3213-4acb-aa66-78d41b9b0e7c.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231006928-30bffb9e-e718-43ac-859c-dd5a61bf99b8.png">
</p>

<p align="center">
<a href="#s15">[15]</a> <i> Blender-Benutzeroberfläche - </i>
<a href="#s16">[16]</a> <i> Sculpting in Blender </i>
</p>



#### Tinkercad

Tinkercad ist eine kostenlose, im Browser ausgeführte Web-App, die man für 3D-Design, aber auch für Elektronik und Programmierung einsetzen kann. Sie ist relativ einfach in der Bedienung und richtet sich in erster Linie an Kinder, Jugendliche und den Einsatz im Schulunterricht. Aber auch für Erwachsene, die sich nicht die Mühe machen wollen, ein komplexes CAD- oder 3D-Grafikdesignprogramm zu erlernen, ist Tinkercad interessant.

Auch wenn scheinbar "CAD" im Namen "Tinkercad" steckt, wäre es etwas unpassend, Tinkercad als CAD-Programm zu bezeichnen. Tinkercad eignet sich zwar gut für die Erstellung von einfachen 3D-Modellen, das System stößt jedoch schnell an seine Grenzen, sobald man etwas komplexere technische Produkte oder 3D-Figuren entwickeln möchte. Die Software ist eher auf einfache Bedienung als auf Funktionalität ausgerichtet, daher unterscheidet sich der Ablauf im Modellieren auch grundsätzlich von gängigen CAD-Programmen. STL-Export für 3D-Druck ist mit Tinkercad möglich.

Tinkercad gehört, so wie auch Fusion 360, zu dem Unternehmen Autodesk und setzt die Registrierung eines (kostenlosen) Benutzer:innen-Kontos voraus. Es muss jedoch keine Software heruntergeladen oder installiert werden, die Anwendung läuft direkt im Browser.

**Registrierung und Anwendung:** https://www.tinkercad.com/

<p align="center">
<img height="250" src="https://user-images.githubusercontent.com/123781559/231008608-c820e2b9-f7bf-4537-8ea6-02873cda1bb3.png">
<img height="250" src="https://user-images.githubusercontent.com/123781559/231008650-cef97389-a24c-4b71-ac55-2ee98d7ae5d4.png">
</p>

<p align="center">
<a href="#s17">[17]</a> <i> Tinkercad-Benutzeroberfläche (im Browser) - </i>
<a href="#s18">[18]</a> <i> 3D-Design eines Messschiebers in Tinkercad </i>
</p>

# Lizenzinformationen

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.


# Bildnachweise

<a name="s1"></a>
**[1]** Gsuter.png (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Gsuter.png

<a name="s2"></a>
**[2]** 3D Viewport, a Blender 2.93.4.png (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:3D_Viewport,_a_Blender_2.93.4.png

<a name="s3"></a>
**[3]** PartDesign Pad example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Pad_example.svg

<a name="s4"></a>
**[4]** PartDesign Revolution example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Revolution_example.svg

<a name="s5"></a>
**[5]** PartDesign Pocket example (adapted) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:PartDesign_Pocket_example.svg

<a name="s6"></a>
**[6]** GGTuto1 4 - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:GGTuto1_4.PNG

<a name="s7"></a>
**[7]** FreeCAD-20.1 (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:FreeCAD-20.1.png

<a name="s8"></a>
**[8]** TechDraw Workbench Example - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:TechDraw_Workbench_Example.png

<a name="s9"></a>
**[9]** Asm3 1 relnotes 0.20 - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Asm3_1_relnotes_0.20.jpg

<a name="s10"></a>
**[10]** screenshot-07.jpg (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://www.freecad.org/ (home page) [License info for freecad.org](https://wiki.freecad.org/Licence)

<a name="s11"></a>
**[11]** CAM Fusion 360 - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:CAM_Fusion_360.png

<a name="s12"></a>
**[12]** 3D Design by fusion 360 - **Image license:** [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) - **Source:** https://www.flickr.com/photos/kenming_wang/32276624594

<a name="s13"></a>
**[13]** sculpt01.jpg - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) - **Source:** https://www.blender.org/features/sculpting/ (Attribution: Blender Foundation – www.blender.org - [License info for blender.org](https://www.blender.org/about/website/) )

<a name="s14"></a>
**[14]** Kochtöpfe erstellt und gerendert in Blender-Cycles - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.de) - **Source:** https://de.wikipedia.org/wiki/Datei:Kocht%C3%B6pfe_in_Blender-Cycles_gerendert.png

<a name="s15"></a>
**[15]** Sculpting Mode Example - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://docs.blender.org/manual/en/latest/sculpt_paint/sculpting/introduction/general.html#id

<a name="s16"></a>
**[16]** sculpt-paint_sculpt_multires_example.png (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://docs.blender.org/manual/en/latest/sculpt_paint/sculpting/introduction/adaptive.html#multiresolution

<a name="s17"></a>
**[17]** Practice 3 D printing - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Windmill_3_D_printing.png

<a name="s18"></a>
**[18]** Caliper, drawn with Tinkercad - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://en.wikipedia.org/wiki/File:Schuifmaat_bottom_mechaniek.png
