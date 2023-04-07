# 3D-Design
## Inhalt
1. ...
2. ...

### Einführung

Es gibt verschiedene Programme/Software, mit denen man digitale 3D-Modelle zeichnen bzw. modellieren kann. Diese 3D-Modelle können anschließend z.B. für 3D-Druck, Lasercutting oder CNC-Fräsen genutzt werden.

Je nach Anwendungszweck gibt es Programme mit unterschiedlichen Schwerpunkten und Funktionen. Zum Modellieren von Bauteilen für technische Produkte wird in der Regel CAD-Software benutzt (CAD = Computer Aided Design; engl. für „Computergestütztes Entwerfen“). Andererseits gibt es auch 3D-Grafikprogramme, die einen eher künstlerischen Schwerpunkt haben, z.B. für komplex geformte Figuren, die für 3D-Druck, Produktdesign, aber auch z.B. für 3D-Animationsfilme verwendet werden können.

> Bilder: Beispiel FreeCAD - Beispiel Blender

Zudem gibt es eine Vielzahl an Webseiten, von denen man fertige Modelle beziehen oder auf die man seine eigenen Kreationen hochladen und teilen kann.

Eine weitere Möglichkeit, ein 3D-Modell zu erstellen besteht im 3D-Scanning. Damit lassen sich Gegenstände, Ersatzteile oder auch Personen einscannen und als 3D-Modell am Rechner abbilden. Mit etwas Nachbearbeitung lassen sich diese Modelle auch 3D-drucken (mehr dazu im Basislernmodul zu 3D-Scanning).

## CAD-Software

CAD-Software wird in der Regel im technischen Bereich eingesetzt, z.B. im Maschinenbau, in der Architektur oder Elektrotechnik – bei Unternehmen für Produktentwicklung, technische Projektierung von Gebäuden und ähnlichen Bereichen. Aber auch für Hobby-Anwendungen, z.B. zum Designen von Objekten für 3D-Druck oder CNC-Fräsen haben sich CAD-Programme bewährt.

Soll ein in CAD entworfenes Modell mithilfe von CNC-Maschinen (fräsen oder drehen) gefertigt werden, muss es in einer CAM-Software (CAM = Computer Aided Manufacturing) bearbeitet werden, um z.B. Fräsdurchmesser, Drehzahlen, Arbeitsabläufe etc. zu definieren (mehr dazu im Basislernmodul zu CNC-Fräsen). Viele CAD-Programme haben ein integriertes CAM-Modul, man spricht dann von CAD/CAM-Software.

Beim Erstellen eines 3D-Modells – bei CAD spricht man von „modellieren“ oder „konstruieren“ – arbeitet man meistens mit sogenannter geometrischer und generativer Modellierung.

Dabei startet man üblicherweise mit dem Zeichnen einer 2D-Skizze, die aus Punkten, Linien, Kurven und geometrischen Formen wie Kreisen oder Sechsecken besteht. Als nächster Schritt wird diese 2D-Skizze zu einem 3D-Objekt mit festgelegter Dicke „aufgepolstert“. Aufbauend auf diesem Objekt können weitere Elemente hinzugefügt werden, etwa durch weitere 2D-Skizzen und Aufpolsterung (engl. „Pad“), durch Rotation der 2D-Skizze zur Erstellung eines Drehteils, durch Abziehen von Teilen (z.B. für Löcher oder Bohrungen) oder durch Vervielfältigung von Elementen.

> Bilder: FreeCAD Skizze zu Pad, Abzug/Bohrung, Rotation

Viele CAD-Programme enthalten auch Funktionen zum Erstellen von technischen Maßzeichnungen. Dabei wird das Bauteil zunächst in 3D modelliert und anschließend aus verschiedenen Blickrichtungen auf eine 2D-Zeichnung projiziert. Diese Ansichten können auf einem Blatt angeordnet, mit Bemaßungen sowie weiteren Informationen versehen und ausgedruckt werden. Dies ist hilfreich für Teile, die man nicht mit digitalen Fertigungsmethoden herstellen möchte, sondern mit konventionellen Werkzeugen, z.B. Zuschneiden und Bohren von Holzbrettern oder Aluminiumprofilen.

> Bild: FreeCAD Techdraw

Einige CAD-Programme verfügen über Funktionen für „parametrisches Design“. Dabei werden Bauteile nicht mit exakten Zahlenwerten bemaßt (z.B. 10 mm), sondern mit Parametern (z.B. mit („Länge“ oder „Durchmesser“). Mit einem parametrischen Modell können dann viele unterschiedliche Varianten des Bauteils generiert werden, z.B. wird eine Schraube nicht in jeder beliebigen Variante neu modelliert, sondern nur einmal als parametrisches Modell, wobei z.B. die Parameter „Länge“ und „Durchmesser“ variiert und das jeweils erzeugte Schraubenmodell als Variante abgespeichert wird. Parameter können auch mithilfe von Formeln verknüpft werden (z.B. „Länge = 2 x Durchmesser + 10 mm“).

> Bild: FreeCAD parametrisches Design

Auf Videoportalen wie YouTube finden sich viele Video-Tutorials für das Erlernen von CAD-Modellierung. Grundlagen für einfache Modelle lassen sich relativ schnell erlernen, für komplexere CAD-Projekte und erweiterte Funktionen braucht es jedoch viel Einarbeitung und Übung.


### Dateiformate für CAD-Modelle

Jede Software hat ihr eigenes Dateiformat für Projektdateien, z.B. haben FreeCAD-Dateien die Dateiendung *.FCStd und Autodesk-Fusion-360-Dateien die Endung *.f3d.
Es gibt im CAD-Bereich aber zahlreiche unterschiedliche Dateiformate, die teilweise von unterschiedlichen CAD-Programmen erstellt und geöffnet werden können.

Besonders hervorzuheben ist das STEP-Dateiformat (*.ste, *.step oder *.stp). STEP steht für „STandard for the Exchange of Product model data” und ist in einer weltweit anerkannten ISO-Norm standardisiert. STEP-Dateien eignen sich daher gut als Austauschformat zwischen unterschiedlichen CAD-Programmen. Möchte man seine CAD-Datei mit jemandem teilen, der eine andere CAD-Software benutzt, ist das Exportieren im STEP-Format also oft eine gute Lösung, auch wenn nicht alle Informationen und Editierfunktionen erhalten bleiben, aber zumindest kann die Datei in der anderen Software geöffnet, betrachtet und analysiert werden.

Plant man sein Produkt als Open Source Hardware zu veröffentlichen, ist es empfehlenswert, eine CAD-Software zu verwenden, die kostenfrei ist und auf Open Source Software basiert (z.B. FreeCAD oder Blender, mehr dazu siehe unten), damit möglichst viele Menschen die Dateien öffnen, bearbeiten und als verbesserte Variante zum Projekt beitragen können.

Ein weiteres wichtiges Dateiformat ist STL, vor allem für 3D-Druck. Praktisch jede bekannte CAD- oder 3D-Grafiksoftware kann 3D-Modelle im STL-Format exportieren, sodass man sie anschließend 3D-drucken kann (mehr dazu im Basislernmodul 3D-Druck).


### Beispiele für CAD-Software

Hier eine Auswahl einiger beliebter und empfohlener CAD-Programme, die weitestgehend kostenlos nutzbar sind:

#### FreeCAD

FreeCAD ist, wie der Name schon sagt, eine sogenannte „Free and open-source software“, d.h. die Software ist uneingeschränkt kostenlos, also auch für kommerzielle Anwendungen, und ihr Quellcode ist offen. Dies macht FreeCAD zu einer beliebten Softwarelösung in Open-Source-Communities, da garantiert ist, dass mit FreeCAD erstellte Projekte auch langfristig von jedem kostenlos geöffnet und bearbeitet werden können (als Open Source Hardware). Zudem kann FreeCAD von jedem modifiziert oder durch Erweiterungen ergänzt und verbessert werden (Open Source Software), wodurch schon zahlreiche, von der Nutzer:innen-Community programmierte Zusatzfunktionen, Workbenches, Makros und Bugfixes gibt.

FreeCAD enthält viele unterschiedliche Programm-Module (sogenannte „Workbenches“) und Funktionen für 3D-Modellierung, 3D-Druck, CAM und CNC-Fräsen, Lasercutting, Bewegungssimulationen, Architektur und vieles mehr. Eine besondere Stärke von FreeCAD ist auch das parametrische Designen, wobei mit der „Spreadsheet“-Workbench Kalkulationstabellen erstellt werden können, mit denen man Parameter des CAD-Modells steuern kann.

**Download:** https://www.freecad.org/

**FreeCAD-Wiki:** https://wiki.freecad.org/

> Bilder

#### Autodesk Fusion 360

Fusion 360 ist eine von Autodesk entwickelte Software-Suite für CAD, CAM und weitere technische Anwendungen. Grundsätzlich ist Fusion 360 ein kostenpflichtiges Programm, es lässt sich jedoch unter bestimmten Bedingungen und mit eingeschränkter Funktionalität auch kostenlos nutzen. So muss man bei der Registrierung angeben, dass man Privatanwender:in ist („personal use“). Diese kostenlose „Hobby-Lizenz“ muss regelmäßig erneuert werden. Sobald man Projekte kommerziell nutzen möchte, ist man verpflichtet, eine Lizenz zu kaufen. Zudem stehen unter der kostenlosen Lizenz nicht alle Funktionen zur Verfügung. Die Bedingungen und Funktionen für kostenlose Nutzung können sich noch öfters ändern, die aktuellen Infos hierzu findet man auf der [Fusion-360-Webseite](https://www.autodesk.de/products/fusion-360/).

Fusion 360 ist cloud-basiert, d.h. man benötigt eine Verbindung zum Internet und muss sich bei erster Benutzung mit seinen Kontodaten anmelden. Projektdateien werden online in einer Cloud von Autodesk gespeichert, können jedoch auch lokal heruntergeladen werden (z.B. als f3d-Datei). Falls keine Internetverbindung besteht, kann auch zeitweilig offline gearbeitet werden, die Dateien werden bei nächster Verbindung mit dem Internet synchronisiert. Die erstmalige Anmeldung muss jedoch online erfolgen.

Aufgrund seiner klaren und verständlichen Bedienbarkeit gilt Fusion 360 als vergleichsweise leicht erlernbare CAD-Software, was es zu einem viel genutzten und beliebten Programm in Maker-Communities macht.

**Registrierung und Download für Privatanwender:innen:** https://www.autodesk.de/products/fusion-360/personal

> Bilder

## 3D-Grafik- und Modellierungsprogramme

Im Gegensatz zu CAD-Programmen, die eher für technische Produktentwicklung genutzt werden, richten sich 3D-Grafikprogramme eher an künstlerische oder Design-bezogene Anwendungen, z.B. zum Gestalten von Figuren, Vasen, Gefäßen oder sonstige, komplex gestaltete Formen.

Dabei kommen oft sogenannte Sculpting-Werkzeuge zum Einsatz, womit sich 3D-Objekte präzise verformen lassen, ähnlich wie beim Töpfern mit Ton. Die millimetergenaue Bemaßung sowie Konstruktion von eher eckigen Teilen, wie bei technischen Bauteilen in CAD-Programmen, steht damit weniger im Vordergrund als die Freiheit in der Form- und Ausgestaltung des 3D-Objekts.

Weitere Funktionen von 3D-Grafikprogrammen sind z.B. die Texturierung, Animation (für Animationsfilme oder Videospiele) und Rendering (z.B. zur Inszenierung eines Objekts oder Produkts in einer bestimmten Umgebung und Belichtung in einer sogenannten Szene). Viele 3D-Grafikprogramme können die Modelle als STL-Datei exportieren, womit sie sich 3D-drucken lassen.

### Beispiele für 3D-Grafik- und 3D-Modellierungsprogramme

Hier eine Auswahl einiger beliebter und empfohlener 3D-Grafik- und 3D-Modellierungsprogramme, die kostenlos nutzbar sind:

#### Blender

Blender ist eine 3D-Grafiksuite, die als „Free and open-source software“, also kostenlos verfügbar und mit offenem Quellcode veröffentlich ist. Die Software-Suite umfasst Funktionen zum modellieren, texturieren und animieren. Blender ist ein im professionellen wie auch im Hobby-Bereich sehr beliebtes Programm, gilt als besonders ausgereifte Open-Source-Software und die Grundlagen lassen sich verhältnismäßig leicht erlernen.

**Download:** https://www.blender.org/

> Bilder

#### Tinkercad

Tinkercad ist eine kostenlose, im Browser ausgeführte Web-App, die man für 3D-Design, aber auch für Elektronik und Programmierung einsetzen kann. Sie ist relativ einfach in der Bedienung und richtet sich in erster Linie an Kinder, Jugendliche und den Einsatz im Schulunterricht. Aber auch für Erwachsene, die sich nicht die Mühe machen wollen, ein komplexes CAD- oder 3D-Grafikdesignprogramm zu erlernen, ist Tinkercad interessant.

Auch wenn scheinbar "CAD" im Namen "Tinkercad" steckt, wäre es etwas unpassend, Tinkercad als CAD-Programm zu bezeichnen. Tinkercad eignet sich zwar gut für die Erstellung von einfachen 3D-Modellen, das System stößt jedoch schnell an seine Grenzen, sobald man etwas komplexere technische Produkte oder 3D-Figuren entwickeln möchte. Die Software ist eher auf einfache Bedienung als auf Funktionalität ausgerichtet, daher unterscheidet sich der Ablauf im Modellieren auch grundsätzlich von gängigen CAD-Programmen. STL-Export für 3D-Druck ist mit Tinkercad möglich.

Tinkercad gehört, so wie auch Fusion 360, zu dem Unternehmen Autodesk und setzt die Registrierung eines (kostenlosen) Benutzer:innen-Kontos voraus. Es muss jedoch keine Software heruntergeladen oder installiert werden, die Anwendung läuft direkt im Browser.

**Registrierung und Anwendung:** https://www.tinkercad.com/

> Bilder

## Download fertiger 3D-Modelle

Statt eigene 3D-Modelle zu erstellen, kann man auch fertige Modelle aus dem Internet herunterladen, ggf. nachbearbeiten und anschließend z.B. für 3D-Druck benutzen. Mehr dazu im Basislernmodul „Verwendung von 3D Modellen aus dem Internet“.
