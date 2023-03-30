Entwurf - Stand 28.03.2023
Oskar Lidtke
 
# 3D-Druck
## Inhalt

1. [Einführung](#einführung)
2. [Grundlagen](#grundlagen)
   - [Filament](#filament)
3. ...

### Einführung

Mit 3D-Druck bezeichnet man viele unterschiedliche Verfahren, bei denen ein Gerät (3D-Drucker) materielle, dreidimensionale Objekte erschafft. Dabei werden die Objekte meistens zunächst in einer Software als 3D-Modell entworfen und anschließend an den 3D-Drucker gesendet.

Es gibt kleine, relativ günstige 3D-Drucker für zu Hause oder für Fab Labs, die meistens aus Kunststoff drucken, aber auch größere Drucker bis hin zu großen Anlagen, die ganze Gebäude (zumindest die Grundstruktur aus Wänden) aus Beton drucken können. Manche 3D-Drucker können auch Metall oder Lebensmittel wie Schokolade drucken – die Bandbreite an 3D-Druckverfahren ist sehr groß.


<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/227555108-ebd86be8-9850-4ab8-94d8-15be34ee5be7.png">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/227562019-978eda65-88b7-49d7-b66e-72f8941ae146.png">
</p>

<p align="center">
       <a href="#s1">[1]</a> <i> DIY-3D-Drucker mit Open-Hardware-Lizenz - </i>
       <a href="#s2">[2]</a> <i> 3D-Drucker von Prusa </i>
</p>


<p align="center">
       <img height="300" src="https://user-images.githubusercontent.com/123781559/228344847-ec0f3dfa-57fd-4b9f-8b2a-cdafccb589ca.png">
       <img height="300" src="https://user-images.githubusercontent.com/123781559/228344985-73ceffa9-d48f-4804-a34a-712ae6ad6995.png">
</p>

<p align="center">
       <a href="#s3">[3]</a> <i> BigFDM-3D-Drucker für große Modelle bis zu 80 x 80 x 90 cm - </i>
       <a href="#s4">[4]</a> <i> 3D-Druck von Häusern </i>
</p>

Am weitesten verbreitet und am beliebtesten sind 3D-Drucker, die nach dem sogenannten FDM-Verfahren arbeiten. In diesem Basislernmodul wird es daher zunächst nur um FDM-Drucker gehen.

Die zweithäufigste Art von 3D-Druckern in Fab Labs neben dem FDM-Verfahren sind wohl die SLA-Drucker. Diese sind jedoch schwieriger in der Anwendung und damit weniger gut für Einsteiger:innen geeignet als FDM-Drucker, es empfiehlt sich also, zunächst mit FDM anzufangen.

FDM steht für "Fused Deposition Modeling". Das bedeutet, ein Stoff (meistens ein Kunststoff/Plastik) wird von dem 3D-Drucker erhitzt, dabei geschmolzen und anschließend schichtweise aufgetragen. Die Schichten kühlen kurz darauf ab, womit sie sich zu einem festen, zusammengefügten Objekt vereinigen. Mit FDM gedruckte Objekte lassen sich gut an den typischen Schichten erkennen, die meist nur ein Bruchteil eines Millimeters dick sind.
  


<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228348704-86426b52-4b1d-4f8c-a432-14c66ffa2119.png">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228352600-c652c874-372b-4f5d-9970-316e3557aa9b.png">
</p>

<p align="center">
       <a href="#s5">[5]</a> <i> 3D-Druck - </i>
       <a href="#s6">[6]</a> <i> 3D-gedrucktes Objekt mit sichtbaren Schichten </i>
</p>


Daher zählt man 3D-Druck auch zu den sogenannten "additiven Verfahren", da Objekte entstehen, indem neues Material hinzugefügt ("addiert") wird. Im Gegensatz dazu gibt es auch "subtraktive Verfahren", d.h. Fertigungsverfahren, wo ein bestehendes Material getrennt wird bzw. etwas "weggenommen" wird, z.B. durch Lasercutting oder CNC-Fräsen. (verlinken)

Mit FDM-3D-Druckern können z.B. dekorative Objekte wie Figuren oder Vasen, kleine Spielzeuge, personalisierte Namensschilder und Schlüsselanhänger, Modelle für Demonstrationszwecke (z.B. von Maschinen oder Gebäuden), Ersatzteile für bestehende Produkte (z.B. Schubladengriffe oder drehbare Knöpfe für Musikanlagen), Alltagshelfer wie Handtuchhaken oder Funktionsteile wie Gehäuse für Elektronik-Geräte, Flaschenöffner oder sogar Bauteile für 3D-Drucker gedruckt werden.

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228950513-8ab76058-957e-4ce9-8508-2e45329b62c0.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228950645-b1502905-6c1c-4f3a-8d73-a67f2cd63270.png">
</p>

<p align="center">
<a href="#s7">[7]</a> <i> 3D-gedruckter Lautsprecher - </i>
<a href="#s8">[8]</a> <i> 3D-gedrucktes Modell einer Turbine</i>
</p>

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228954408-7558e95f-a85c-470c-960a-92e0bbfa1bd8.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228954649-96d65f57-c056-4b25-830b-e36800b428ae.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i> 3D-gedruckte Schale - </i>
<a href="#s10">[10]</a> <i> Verschiedene Objekte</i>
</p>

<p align="center">
<img height="230" src="https://user-images.githubusercontent.com/123781559/228958699-f2e9ea4c-5c8e-4902-9ec7-268f865793ee.png">
<img height="230" src="https://user-images.githubusercontent.com/123781559/228958805-1750d640-9f1c-4cec-bde2-bc2d8b1c51ff.png">
<img height="230" src="https://user-images.githubusercontent.com/123781559/228958899-5732f5e3-24c7-4530-bb69-c3214c4cdb74.png">
</p>

<p align="center">
<a href="#s11">[11]</a> <i>  - </i>
<a href="#s12">[12]</a> <i>  - </i>
<a href="#s13">[13]</a> <i> Verschiedene 3D-gedruckte Objekte</i>
</p>




## Grundlagen
### Filament

Das Grundmaterial, das man für einen FDM-3D-Drucker benötigt, nennt sich Filament. Ein Filament ist ein dünner Kunststoffdraht, der auf eine Rolle gewickelt ist.

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228964087-d6a8c22b-640f-4da6-9847-7d67378b6798.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228964181-d73f73c3-8ba2-49a9-9cdd-4f701e3b1ab0.png">
</p>

<p align="center">
<a href="#s14">[14]</a> <i> Verschiedene Filamentrollen - </i>
<a href="#s15">[15]</a> <i> Filamentrolle</i>
</p>

Filamente gibt es in verschiedensten Farben und Materialien.
Das gängigste 3D-Druck-Material ist PLA. Es ist günstig, einfach zu drucken, reicht für die allermeisten Anwendungen völlig aus und ist damit gut für Einsteiger:innen geeignet.

PLA ist eine Kunststoff- bzw. Plastiksorte und steht für "polylactic acid" (englisch für "Polylactide").

Hier eine Kurzübersicht der gängigsten Materialien für FDM-3D-Drucker und die wichtigsten Vor- und Nachteile:

- **PLA:** Günstig, einfach zu drucken, gut für Einsteiger:innen, ideal für dekorative Objekte oder Bauteile mit niedrigen Belastungen; gut recyclebar
- **PETG / PET-G:** Robuster als PLA, gut für Funktionsbauteile, die hohe Kräfte/Belastungen aushalten sollen; leichter zu drucken als ABS; etwas fester als ABS
- **PET:** Eher selten als 3D-Druck-Filament zu finden, weniger geeignet als PET-G; sehr gut recyclebar; lässt sich z.B. aus PET-Flaschen herstellen
- **ABS:** Ähnlich gut belastbar wie PETG, höhere Hitzebeständigkeit als PETG; dünstet beim Drucken ungesunde Dämpfe aus, gut belüfteter Raum notwendig; schwierig zu drucken, Gehäuse und hohe Heizbetttemperatur empfehlenswert
- **ASA:** Gilt als „Nachfolger“ von ABS; verzieht weniger und dünstet weniger aus als ABS
- **Nylon:** Besonders hohe mechanische und thermische Beständigkeit; schwierig zu drucken, eher für Fortgeschrittene; teurer als andere Filamentsorten; anfällig für Feuchte
- **TPU:** Flexibles, „gummiartiges“ Material; lässt sich nach dem Druck leicht verformen; ideal für kleine Reifen, Stempel u.ä.; relativ schwierig zu drucken; teurer als andere Filamentsorten

Da jedes Material eine andere Schmelztemperatur hat, ist es wichtig, diese korrekt einzustellen. Der 3D-Drucker erhitzt im sogenannten Extruder das Filament auf eine Temperatur, mit der es sich gut verflüssigen und drucken lässt, während das Heizbett auf eine Temperatur eingestellt wird, die sicherstellt, dass das Filament gut darauf haftet. So verwendet man z.B. für PLA üblicherweise eine Extrudertemperatur von 200-230 °C und eine Heizbetttemperatur von 60 °C. Diese Temperaturempfehlungen können aber je nach Hersteller auch abweichen. Am besten prüft man die Angaben auf der Filamentrolle bzw. in beigelegten Datenblättern und gleicht sie mit den Einstellungen in der Slicer-Software ab (mehr [zum Thema Slicing später](#slicer-software)).

Filamente werden meistens in den Durchmesser-Varianten 1,75 mm und 2,85 mm verkauft, wobei 1,75 mm die deutlich verbreitete Variante ist. Für größere 3D-Drucker bzw. für solche, wo die Düse entsprechend getauscht wurde, wird das dickere 2,85-mm-Filament verwendet.

Gewöhnliche 3D-Drucker können nur mit einem Filament zur Zeit drucken, d.h. wenn man in einer anderen Farbe oder mit einem anderen Material drucken möchte, muss man die Filamentrolle wechseln. Es gibt aber auch 3D-Drucker, die mit zwei oder mehr Filamenten auf einmal drucken können. So können mehrfarbige Objekte oder auch Objekte aus verschiedenen Materialien gedruckt werden, z.B. indem das Stützmaterial aus einem leicht entfernbaren Material und das eigentliche Objekt aus einem stabilen Material gedruckt wird.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/228966443-6117228a-d488-49cc-9fb7-bca371345b53.png">
</p>

<p align="center">
<a href="#s16">[16]</a> <i> Mehrfarbiger 3D-Druck</i>
</p>

### Komponenten eines 3D-Druckers

Zunächst sollte man sich mit dem grundlegenden Aufbau eines FDM-3D-Druckers vertraut machen. Hier wird beispielhaft ein typischer FDM-3D-Drucker beschrieben. Die meisten FDM-Drucker sind auf diese oder ähnliche Weise aufgebaut. Je nach Hersteller und Modell kann dieser Aufbau auch abweichen, aber die Grundprinzipien bleiben die gleichen.

<p align="center">
       <img height="500" src="https://user-images.githubusercontent.com/123781559/228371509-65427cdb-5a2f-43db-bab9-18c349bc308e.png">
</p>

<p align="center">
       <a href="#s5">[x]</a> <i> Die wichtigsten Komponenten eines 3D-Druckers - </i>
</p>

Die wichtigste Komponente ist der Extruder, den man sich ähnlich wie einen "Druckkopf" bei Tintenstrahldruckern vorstellen kann.

  

(Beschriftete Bilder eines Extruders inkl. Schnittansicht)
(Skizze/Entwurf  überarbeiten und ergänzen)

Oben am Extruder befindet sich eine Öffnung, in die der Filamentdraht eingeführt wird. Im Inneren des Extuders wird das Filament von zwei Zahnrädern, die den "Vorschub" des Filaments steuern, eingezogen bzw. nach unten weitergeschoben.

Danach geht das Filament durch einen Kühlteil. Ein Ventilator bläst Luft gegen die Kühlrippen, um das Filament in diesem Bereich zu kühlen. Auf diese Weise verhindert man, dass das Filament Wärme nach oben leitet und bereits im Bereich der Zahnräder schmilzt. Flüssiges Filament ließe sich dann nicht mehr von den Zahnrädern vorschieben. Im Laufe eines 3D-Druck-Vorgangs kann es sein, dass der Ventilator mal anspringt und mal wieder ausgeht.

Nach dem Kühlteil des Extruders bewegt sich das Filament weiter nach unten durch das sogenannte "Hotend" (von engl. „hot end“ = „heißes Ende“). Dort wird das Filament erhitzt, geschmolzen und ein Stück weit verflüssigt. Abschließend wird das zähflüssige Filament durch eine Düse (sogenannte "Nozzle") gedrückt. Das z.B. 1,75 mm dicke Filament wird durch die Düse/Nozzle auf einen deutlich kleineren Durchmesser gepresst (meistens ca. 0,4 mm). Das austretende Filament kann nun zum schichtweisen Auftragen, also 3D-Drucken, verwendet werden.

Damit der Extruder Objekte im dreidimensionalen Raum erschaffen kann, muss er sich in alle Richtungen bewegen können. Dafür gibt es bei 3D-Druckern die drei motorgesteuerten Achsen: X-, Y- und Z-Achse.

Die X- und Y-Achse beziehen sich in der Regel auf Bewegungen in der horizontalen bzw. waagerechten Grundfläche:
- X-Achse: "links und rechts"
- Y-Achse: "vorne und hinten"

<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228372124-5b5fd75e-29c4-4cda-bc98-a285a9d389b2.png">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228372187-d8ed1539-0d39-43ea-b18e-60b2039fb0be.png">
</p>

<p align="center">
       <a href="#s5">[x]</a> <i> X-, Y- und Z-Achse eines 3D-Druckers - </i>
       <a href="#s6">[x]</a> <i> Draufsicht eines 3D-Druckers mit X- und Y-Achse </i>
</p>

<br>

Die Z-Achse hingegen bezieht sich auf die vertikale (senkrechte) Bewegung:
- Z-Achse: "oben und unten"

<br>

<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228372746-eb115280-5621-4a70-bccf-280dc9de1353.png">
</p>

<p align="center">
       <a href="#s5">[x]</a> <i> Frontansicht eines 3D-Druckers mit X- und Z-Achse - </i>
</p>

Der Extruder sitzt oft auf einer Stange, auf der er sich nach links und rechts (also in X-Richtung) bewegen kann. Angesteuert wird dies über einen Motor und einen Riemen.

[Abbildung]
(Bild der Stange, des Motors und des Riemens)

Für Bewegungen in der Y-Achse wird oft gar nicht der Extruder bewegt, sondern das Heizbett – auch hier durch einen Motor und ein Riemen.

[Abbildung]
(Bild Y-Achse Riemen)

Für die Z-Achse wiederum gibt es meist motorgesteuerte Spindeln, die die gesamte X-Achsen-Stange nach oben und unten verschiebt. Bei manchen 3D-Druckern wird nicht der Extruder (bzw. die x-Achse), sondern das Heizbett nach oben bzw. unten bewegt.

[Abbildung]
(Bild Spindeln und bewegliche x-Achse + Bild bewegliches Heizbett)

Den  Druckablauf kann man sich nun so vorstellen, dass ein 3D-Drucker zunächst wie ein „2D-Drucker“ funktioniert. Geschmolzenes Filament wird durch die Düse/Nozzle des Extruders gedrückt, während sich gleichzeitig die X- und Y-Achsen bewegen. Somit „zeichnet“ der Drucker die erste, unterste Schicht auf das Heizbett, sozusagen „in 2D“. Sobald die erste Schicht fertig ist, fährt der Extruder ein kleines Stück weit (oft nur ein Bruchteil eines Millimeters) in z-Richtung hoch und „zeichnet“ darauf dann die zweite Schicht. So wird fortgefahren, bis die oberste Schicht und damit das ganze dreidimensionale Objekt fertig ist.

### Kalibrierung

Ein neu gekaufter oder neu zusammengebauter 3D-Drucker muss zunächst kalibriert werden. Die meisten 3D-Drucker haben dafür ein Programm, das man über die Einstellungen starten kann. Beim Kalibrieren fährt der Extruder verschiedene Punkte an, fährt die x-, y- und z-Achse jeweils einmal in gesamter Länge ab und „tastet“ das Heizbett ab. Die Messwerte und Koordinaten werden gespeichert und es wird sichergestellt, dass der 3D-Drucker korrekt ausgerichtet ist.

Manchmal kann es notwendig sein, einen 3D-Drucker erneut zu kalibrieren, z.B. nachdem man ihn transportiert hat oder wenn Fehler in den Druckergebnissen auffallen.


## Vorbereitung eines 3D-Drucks
### Digitales 3D-Modell

Zunächst braucht man ein digitales 3D-Modell des Objekts, das man drucken möchte. Solche 3D-Modelle kann man entweder selbst modellieren/designen (z.B. mit einer CAD-Software) oder man lädt sich ein fertiges Modell aus dem Internet. Die meisten Modelldateien sind auch klein genug, um z.B. per E-Mail verschickt zu werden. Eine weitere Möglichkeit, ein 3D-Modell zu erstellen, besteht im 3D-Scannen eines realen Objekts oder einer Person.

  
(Bilder CAD-Modell und 3D-gescanntes und -gedrucktes Personenmodell)

Mit den Themen 3D-CAD-Modellierung (CAD = Computer Aided Design), 3D-Scanning und Modell-Download von Webseiten befasst sich ein anderes Basislernmodul. (verlinken)

Für die meisten 3D-Drucker benötigt man Dateien im STL-Format (oder manchmal auch OBJ-Format) - also mit der Dateiendung „.stl“ oder „.obj“. STL ist aber das üblichere Dateiformat. Fast jede CAD-Software ist in der Lage, 3D-Modelle im STL-Format zu exportieren. Bei heruntergeladenen Dateien aus dem Internet sollte man zunächst prüfen, ob es im STL-Format vorliegt.

Bevor man die STL-Datei drucken kann, muss man sie noch in einer sogenannten Slicer-Software bearbeiten. Kurz gesagt, erzeugt die Slicer-Software auf Basis des 3D-Modells viele kleine, übereinanderliegende Schichten oder Scheiben und berechnet die Steuerbefehle für den 3D-Drucker, der das Modell dann Schicht für Schicht aufeinanderdruckt (eine genauere [Beschreibung des Slicings weiter unten](#slicing-prüfung-und-export)).

### Slicer-Software

Es gibt viele verschiedene Slicer-Programme. Viele große und bekannte Hersteller von 3D-Druckern haben ihre eigene Slicer-Software und bieten diese über ihre Website in der Regel kostenlos zum Download an. Zwei Beispiele (mit Download-Links):

- PrusaSlicer		https://www.prusa3d.com/de/page/prusaslicer_424/ 
- UltiMaker Cura 	https://ultimaker.com/de/software/ultimaker-cura 

Viele Slicer-Programme basieren auf Open Source Software, z.B. wurde der PrusaSlicer auf Basis der Open-Source-Software „Slic3r“ entwickelt und der PrusaSlicer selbst ist damit auch Open Source.

Manche kleinere Hersteller von 3D-Druckern nutzen auch Slicer-Programme der größeren Hersteller und liefern dazu nur eine Konfigurationsdatei, die die Slicer-Software auf den 3D-Drucker anpasst.

In der Slicer-Software sieht man eine Vorschau des Heizbetts sowie der importierten 3D-Objekte. Mit der Software lassen sich die zu druckenden 3D-Objekte vervielfältigen (um ein Objekt gleich mehrmals zu drucken), virtuell im Raum bewegen, drehen, skalieren (vergrößern/verkleinern), und in gewünschte Positionen auf dem Heizbett platzieren.

 
(Bild Slicer mit mehreren Objekten)


### Slicing, Prüfung und Export

Es gibt zahlreiche Einstellungen im Slicer, wobei in diesem Basislernmodul nicht auf alle Einstellungen im Detail eingegangen wird. Für einen ersten, einfachen 3D-Druck reichen meistens die Standard-Einstellungen aus.

Die wichtigste Einstellung ist das Material. Möchte man z.B. mit PLA drucken, wählt man in der Materialeinstellung „PLA“ aus oder gibt die empfohlenen Temperaturen des Filamentherstellers an.

Nachdem man die STL-Datei(en) im Slicer importiert, korrekt gedreht, ausgerichtet und die Stützmaterialien eingestellt hat, muss man das Slicing starten.

Slicing (von englisch „slice“ = Scheibe) ist ein Ablauf in der Software, der das 3D-Objekt in viele dünne Scheiben (slices) unterteilt, die übereinander geschichtet sind. Die Scheiben haben dabei genau die Höhe bzw. Dicke, die man eingestellt hat, z.B. 0,15 mm (dieser Parameter wird meistens als „Schichthöhe“ oder englisch „layer height“ bezeichnet). Eine Schicht ist also quasi nur „2D“, während die aufeinandergestapelten Schichten zusammen ein 3D-Objekt ergeben.
  

(Bild von Slices in 2D und 3D, mit Beschriftung der Schichthöhe)

Die Slicer-Software tut an der Stelle aber noch viel mehr als nur das eigentliche Slicing. Sie generiert auch den genauen Verlaufsweg des Extruders, also auch den Weg, den der Extruder in jeder Schicht in x- und y-Richtung und anschließend auch in Höhenrichtung (z) nimmt.
Außerdem werden beim Slicing auch Stützmaterialien generiert, sofern man welche eingestellt hat (mehr dazu siehe unten, Abschnitt „Stützmaterial“).

Nach ausgeführtem Slicing empfiehlt es sich, den Druckablauf zu prüfen. Die meisten Slicer bieten eine Vorschau- bzw. Simulationsfunktion an. Damit kann man sich die verschiedenen Schichten (von der ersten, untersten Schicht bis zur letzten ganz oben) einzeln ansehen und auch den Verfahrensweg des Extruders innerhalb einer jeden Schicht anzeigen lassen.
  
(Bilder von Simulationen)

Hat man das Slicing überprüft, kann man die Datei als sogenannte „G-Code“-Datei exportieren.

### G-Code

G-Code ist ein standardisiertes Dateiformat, das nicht nur im 3D-Druck, sondern auch in anderen Fertigungsverfahren (z.B. CNC-Fräsen oder Lasercutting (verlinken)) verwendet wird. Grundsätzlich ist der G-Code dafür da, der Maschine „mitzuteilen“, was sie machen soll, und zwar ganz genau in vielen kleinen Einzelschritten und Werten. Z.B. steht im G-Code, dass das Hotend sowie das Heizbett auf eine bestimmte Temperatur aufheizen sollen, dass der Extruder des 3D-Druckers an eine bestimmte Position fahren soll (angegeben in X-, Y-, und Z-Koordinaten) und wann das Filament, angetrieben durch die Zahnräder, vorgeschoben und aus der Nozzle gedrückt werden soll.

Der von der Slicer-Software generierte G-Code muss an den 3D-Drucker übertragen werden, wobei es je nach 3D-Drucker-Modell verschiedene Möglichkeiten gibt. Viele 3D-Drucker verfügen über einen SD-Karten-Slot oder USB-Eingang. Der G-Code muss dann auf eine SD-Karte oder einen USB-Stick kopiert und anschließend in den 3D-Drucker gesteckt werden. Es gibt aber auch 3D-Drucker, die per Kabel direkt mit dem PC verbunden werden können. Der Druckvorgang wird dann direkt vom PC aus gestartet.

### Stützmaterial und Brücken
Da beim 3D-Druck stets Material aufeinandergeschichtet werden muss, kann es Probleme geben, wenn ein Objekt sogenannte Überhänge hat. Ein 3D-Drucker kann nicht „in der Luft“ drucken. Eine zu druckende Wand muss daher idealerweise im 90°-Winkel nach oben ragen, wobei je nach Material auch Schrägen möglich sind (meistens in Winkeln von max. 45°). Die Ränder der Schichten überlappen sich dann ein wenig.

 
  
(Bilder Schichtwinkel)
(Skizze/Entwurf  überarbeiten und ergänzen)

Größere Überhänge sind jedoch nicht möglich. Oft lässt sich dieses Problem lösen, indem man das Objekt in der Slicer-Software in eine günstigere Position dreht. Viele Slicer verfügen über eine Funktion, bei der man nur eine Oberfläche des Objekts anklicken muss, auf die es „gelegt“ werden soll.

   

   

(Bild mit Beispiel Tisch)
(Skizze/Entwurf  überarbeiten und ergänzen)

Bei komplexer geformten Objekten kann es sein, dass es keine überhangfreie Drehposition gibt. In dem Fall kann man in der Slicer-Software automatisch sogenanntes Stützmaterial generieren lassen. Dieses Stützmaterial ist größtenteils hohl und lässt sich nach dem 3D-Druck meistens relativ leicht entfernen, z.B. mit den Fingern oder mit einer Zange.

 

(Bild Stützmaterial)

Zudem können manche 3D-Drucker und Slicer auch sogenannte Brücken drucken, wenn die Voraussetzungen stimmen. Bei einer Brücke spannt der Extruder Fäden von einer Seite eines Sockels zur anderen. Ein einseitig frei hängender Überhang ist nicht möglich. Zudem darf eine Brücke nicht zu lang bzw. der Abstand zwischen den Sockeln nicht zu groß sein, da der Faden beim Drucken sonst zu wenig Spannung hat und herunterhängt. Für kurze Distanzen sind Brücken aber eine sehr gute Möglichkeit, um ohne Stützmaterial „in der Luft“ zu drucken.

 

(Bild Brücke)

### Infill
Meistens ist es gar nicht notwendig, ein komplett massives Kunststoffteil zu drucken. Nur die äußere Hülle des 3D-gedruckten Objekts ist massiv, innen drin ist das Objekt jedoch zum Teil hohl und zum Teil mit einer Art Gitterstruktur gefüllt. Wie viel Prozent des Inneren eines Objekts mit Material gefüllt ist, lässt sich in Slicern über den Parameter „Infill“ einstellen.

Ein Infill von z.B. 15 % (üblicher Standard-Wert) bedeutet, dass das Objekt zu 15% mit Material gefüllt ist, während die restlichen 85 % hohl bzw. mit Luft gefüllt sind. Für die meisten 3D-Druck-Vorhaben reicht das vollkommen aus. Somit wiegt das Objekt weniger, es wird in kürzerer Zeit gedruckt und es wird weniger Material verbraucht als bei einem massiven Objekt (Infill 100%). Je nach Bedarf kann ein niedriger oder auch ein höherer Infill-Wert eingestellt werden, z.B. wenn das Objekt starke Belastungen aushalten soll.

    

(Bild Infill im Slicer + im realen Objekt)

## Ablauf eines 3D-Drucks
### Vor dem Drucken

Vor Beginn eines 3D-Drucks sollte man überprüfen, ob das richtige Filament eingesetzt ist und ob genügend Filament auf der Rolle vorhanden ist. Zudem empfiehlt es sich, das Heizbett zu reinigen, z.B. mit Isopropanol oder Glasreiniger. Damit werden unsichtbare Fettreste entfernt (die z.B. durch berühren des Druckbetts mit den Fingern entstehen können). Fettreste können dazu führen, dass das Filament nicht richtig auf dem Druckbett haftet.

Hat man den fertigen G-Code an den 3D-Drucker übertragen und den 3D-Druck gestartet, sollte man den Beginn des Drucks eine Weile beobachten und bei Problemen eingreifen oder den 3D-Druck pausieren oder abbrechen. 


### Leveling, Schürze und Rand
Beim Start eines 3D-Druck-Auftrags wird der 3D-Drucker üblicherweise zunächst das Heizbett an verschiedenen Stellen abtasten, um nochmals die Z-Positionen zu kalibrieren (sogenanntes „Leveling“).

Danach wird eine paar Zentimeter lange Linie am Rand des Heizbetts gedruckt, die sogenannte „intro line“ oder „purge line“ (engl. purge = reinigen). Dieser Vorgang dient der „Spülung“ der Düse und stellt sicher, dass die Düse voll mit zähflüssigem Filament gefüllt, gut durchflutet und bereit zum Drucken ist. Würde der 3D-Drucker die purge line weglassen und direkt mit dem Druck des Objekts beginnen, könnte es sein, dass zu Beginn noch kein Filament herauskommt oder dass es nur sehr ungleichmäßig heraustritt.

 
(Bild purge line)

Anschließend wird meist (falls so eingestellt) eine Außenlinie um die Fläche herum gedruckt, wo die Objekte entstehen sollen. Diese sogenannte „Schürze“ (engl. „skirt“) vermittelt gleich zu Beginn des Drucks einen Eindruck von der Größe der zu druckenden Objekte. Zudem kann man an der Schürze bereits früh erkennen, ob das Material gut haftet und ob keine Probleme in der Qualität erkennbar sind, um den Druck an der Stelle im Zweifel noch abbrechen zu können.

 

(Bild Schürze)

Bei manchen Materialien kann es hilfreich sein, zusätzlich einen Rand (engl. „brim“) zu drucken, um das Objekt während des Drucks zu stabilisieren. Die Rand-Funktion kann bei Bedarf in den Einstellungen des Slicers aktiviert und eingestellt werden.

### Die erste Schicht

Nach dem Drucken von Schürze und Rand wird die erste Schicht des Objekts gedruckt. Diese sollte man genau beobachten. Stellt man fest, dass die erste Schicht unsauber ausgeführt ist, z.B. wenn das Filament an einigen Stellen nicht richtig haftet (zu erkennen an kleinen Erhebungen in der Schicht, siehe Bild), sollte man den Druck an dieser Stelle abbrechen, das bereits gedruckte Material entfernen, das Heizbett reinigen bzw. die Z-Achse neu kalibrieren und den Druck neu starten.


  
(Bild erste Schicht)

Eine misslungene erste Schicht kann sonst dazu führen, dass das gesamte Objekt im späteren Verlauf unsauber wird oder gänzlich misslingt. Da ein 3D-Druck mehrere Minuten oder oft sogar Stunden dauern kann, lohnt es sich, eine gute erste Schicht sicherzustellen, bevor man viel Zeit und Material verschwendet.

### Weitere Schichten

Im Laufe des 3D-Drucks kann man beobachten, wie die weiteren Schichten aufgetragen werden. Dabei wird man auch das Innere des Objekts mit der Infill-Gitterstruktur erkennen.

Wenn die erste Schicht gut gelungen ist, kann man den 3D-Drucker problemlos unbeobachtet lassen. Ob man auch den Raum verlassen oder gar über Nacht drucken darf, muss man im Zweifel mit dem/der Besitzer:in des Druckers bzw. mit dem Fab Lab absprechen.

### Nach dem Druck

Sobald der 3D-Druck fertig ist, fährt der Extruder in eine Position, wo er nicht stört, sodass man das Objekt entnehmen kann. Viele 3D-Drucker haben eine entnehmbare Platte (z.B. aus Federstahlblech). Dies erleichtert die Entnahme der Objekte, da man erst die Platte als ganzes entnehmen, danach leicht biegen und die Objekte einfach von der Platte lösen kann.

Abschließend muss man ggf. vorhandenes Stützmaterial entfernen, zudem kann man das Objekt auf verschiedene Arten nachbearbeiten, z.B. schleifen oder mit Epoxidharz behandeln, um die Oberflächenoptik zu verschönern.


# Bildnachweise

<a name="s1"></a>
**[1]** DIY-3D-Drucker mit Open-Hardware-Lizenz [(Repository)](https://gitlab.fabcity.hamburg/hardware/interfacer-osh-build-workshops/3-d-printer-hypercuboid) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Created by:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s2"></a>
**[2]** Prusa i3 metal frame - **Image license:** [GNU Free Documentation License, Version 1.2](https://en.wikipedia.org/wiki/GNU_Free_Documentation_License) - **Source:** https://commons.wikimedia.org/wiki/File:Prusa_i3_metal_frame.jpg

<a name="s3"></a>
**[3]** BigFDM 3D-Drucker [(Repository)](https://github.com/fab-machines/BigFDM) - **Image Source:** https://openlab-hamburg.de/

<a name="s4"></a>
**[4]** Eco-sustainable 3D printed house - **Image license:** [CC BY 2.5](https://creativecommons.org/licenses/by/2.5/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Eco-sustainable_3D_printed_house_%22Tecla%22.jpg

<a name="s5"></a>
**[5]** A photo of the printing head of a FELIX 3D Printer in action - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Felix_3D_Printer_-_Printing_Head_Cropped.JPG

<a name="s6"></a>
**[6]** 3DBenchy - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) - **Source:** https://flic.kr/p/rVrSsc

<a name="s7"></a>
**[7]** Lautsprecher aus 3D Drucker - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Mg_4327-20171101-3d-lautsprecher.jpg

<a name="s8"></a>
**[8]** A Jet Engine turbine printed from the Howard Community College Makerbot - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:HCC_3D_printed_turbine_view_1.jpg

<a name="s9"></a>
**[9]** 3D printing a yarn bowl - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) - **Source:** https://www.flickr.com/photos/ruthanddave/49896309407

<a name="s10"></a>
**[10]** Verschiedene 3D-gedruckte Objekte - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Created by:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s11"></a>
**[11]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Created by:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s12"></a>
**[12]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Created by:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s13"></a>
**[13]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Created by:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s14"></a>
**[14]** Makerbot Store, Manhattan (NY, USA) - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Makerbot_Store,_Manhattan_(NY,_USA)_(8764959982).jpg

<a name="s15"></a>
**[15]** ABS filament spool - **Image license:** [GNU Free Documentation License, Version 1.2](https://en.wikipedia.org/wiki/GNU_Free_Documentation_License) - **Source:** https://commons.wikimedia.org/wiki/File:ABS_filament_spool.jpg

<a name="s16"></a>
**[16]** 3DBenchy created using color mixing on an FDM printer - **Image license:** [GNU Free Documentation License, Version 1.2](https://en.wikipedia.org/wiki/GNU_Free_Documentation_License) - **Source:** https://commons.wikimedia.org/wiki/File:3DBenchy_created_using_color_mixing_on_an_FDM_printer.jpg


(Platzhalter)

(...)

(...)

(...)

(...)

(...)

(...)

(...)

(Platzhalter)
