> Zurück zur [Übersicht Basislernmodule](../../README.md)

# 3D-Druck

## Inhalt

1. [Einführung](#einführung)
2. [Grundlagen](#grundlagen)
   - [Filament](#filament)
   - [Komponenten eines 3D-Druckers](#komponenten-eines-3d-druckers)
   - [Kalibrierung](#kalibrierung)
3. [Vorbereitung eines 3D-Drucks](#vorbereitung-eines-3d-drucks)
   - [Digitales 3D-Modell](#digitales-3d-modell)
   - [Slicer-Software](#slicer-software)
   - [Slicing, Prüfung und Export](#slicing-prüfung-und-export)
   - [G-Code](#g-code)
   - [Stützmaterial und Brücken](#stützmaterial-und-brücken)
   - [Infill](#infill)
4. [Ablauf eines 3D-Drucks](#ablauf-eines-3d-drucks)
   - [Vor dem Drucken](#vor-dem-drucken)
   - [Leveling, Schürze und Rand](#leveling-schürze-und-rand)
   - [Die erste Schicht](#die-erste-schicht)
   - [Weitere Schichten](#weitere-schichten)
   - [Nach dem Druck](#nach-dem-druck)

[Lizenzinformationen](#lizenzinformationen)

[Bildnachweise](#bildnachweise)

## Einführung

Mit 3D-Druck bezeichnet man viele unterschiedliche Verfahren, bei denen ein Gerät (3D-Drucker) materielle, dreidimensionale Objekte erschafft. Dabei werden die Objekte meistens zunächst in einer Software als 3D-Modell entworfen und anschließend an den 3D-Drucker gesendet.

Es gibt kleine, relativ günstige 3D-Drucker für zu Hause oder für Fab Labs, die meistens aus Kunststoff drucken, aber auch größere Drucker bis hin zu großen Anlagen, die ganze Gebäude, zumindest die Grundstruktur aus Wänden, aus Beton drucken können. Manche 3D-Drucker können auch Metall oder Lebensmittel wie Schokolade drucken – die Bandbreite an 3D-Druckverfahren ist sehr groß.


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

FDM steht für "Fused Deposition Modeling". Das bedeutet, ein Stoff, meistens ein Kunststoff/Plastik, wird von dem 3D-Drucker erhitzt, dabei geschmolzen und anschließend schichtweise aufgetragen. Die Schichten kühlen kurz darauf ab, wodurch sie sich zu einem festen Objekt zusammenfügen. Mit FDM gedruckte Objekte lassen sich gut an den typischen Schichten erkennen, die meist nur einen Bruchteil eines Millimeters dick sind.
  


<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228348704-86426b52-4b1d-4f8c-a432-14c66ffa2119.png">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228352600-c652c874-372b-4f5d-9970-316e3557aa9b.png">
</p>

<p align="center">
       <a href="#s5">[5]</a> <i> 3D-Druck - </i>
       <a href="#s6">[6]</a> <i> 3D-gedrucktes Objekt mit sichtbaren Schichten </i>
</p>


Daher zählt man 3D-Druck auch zu den sogenannten "additiven Verfahren", da Objekte entstehen, indem neues Material hinzugefügt ("addiert") wird. Im Gegensatz dazu gibt es auch "subtraktive Verfahren", d.h. Fertigungsverfahren, bei denen ein bestehendes Material getrennt wird bzw. etwas "weggenommen" wird, z.B. durch [Lasercutting](../2.2%20Lasercutting/Lasercutting.md) oder [CNC-Fräsen](../2.3%20CNC-Fr%C3%A4sen/CNC-Fr%C3%A4sen.md).

Mit FDM-3D-Druckern können z.B. dekorative Objekte wie Figuren oder Vasen, kleine Spielzeuge, personalisierte Namensschilder und Schlüsselanhänger, Modelle für Demonstrationszwecke (z.B. von Maschinen oder Gebäuden), Ersatzteile für bestehende Produkte (z.B. Schubladengriffe oder drehbare Knöpfe für Musikanlagen), Alltagshelfer wie Handtuchhaken oder Funktionsteile wie Gehäuse für Elektronikgeräte, Flaschenöffner oder sogar Bauteile für 3D-Drucker gedruckt werden.

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228950513-8ab76058-957e-4ce9-8508-2e45329b62c0.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228950645-b1502905-6c1c-4f3a-8d73-a67f2cd63270.png">
</p>

<p align="center">
<a href="#s7">[7]</a> <i> 3D-gedrucktes Lautsprechergehäuse - </i>
<a href="#s8">[8]</a> <i> 3D-gedrucktes Modell einer Turbine</i>
</p>

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228954408-7558e95f-a85c-470c-960a-92e0bbfa1bd8.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/228954649-96d65f57-c056-4b25-830b-e36800b428ae.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i> 3D-gedruckte Schale - </i>
<a href="#s10">[10]</a> <i> Verschiedene 3D-gedruckte Objekte</i>
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
Das gängigste 3D-Druck-Material ist PLA. Es ist günstig, einfach zu drucken, ist für die allermeisten Anwendungen und damit auch für Einsteiger:innen gut geeignet.

PLA ist eine Kunststoff- bzw. Plastiksorte und steht für "polylactic acid" (englisch für "Polylactide").

Hier eine Kurzübersicht der gängigsten Materialien für FDM-3D-Drucker und die wichtigsten Vor- und Nachteile:

- **PLA:** Günstig, einfach zu drucken, gut für Einsteiger:innen, ideal für dekorative Objekte oder Bauteile mit niedrigen Belastungen; gut recyclebar
- **PETG / PET-G:** Robuster als PLA, gut für Funktionsbauteile, die hohe Kräfte/Belastungen aushalten sollen; leichter zu drucken als ABS; etwas fester als ABS
- **PET:** Eher selten als 3D-Druck-Filament zu finden, weniger geeignet als PET-G; sehr gut recyclebar; lässt sich z.B. aus PET-Flaschen herstellen
- **ABS:** Ähnlich gut belastbar wie PETG, höhere Hitzebeständigkeit als PETG; dünstet beim Drucken ungesunde Dämpfe aus, gut belüfteter Raum notwendig; schwierig zu drucken, Gehäuse und hohe Heizbetttemperatur empfehlenswert
- **ASA:** Gilt als „Nachfolger“ von ABS; verzieht weniger und dünstet weniger aus als ABS
- **Nylon:** Besonders hohe mechanische und thermische Beständigkeit; schwierig zu drucken, eher für Fortgeschrittene; teurer als andere Filamentsorten; anfällig für Feuchte
- **TPU:** Flexibles, „gummiartiges“ Material; lässt sich nach dem Druck leicht verformen; ideal für kleine Reifen, Stempel u.ä.; relativ schwierig zu drucken; teurer als andere Filamentsorten

Da jedes Material eine andere Schmelztemperatur hat, ist es wichtig, diese im Druckprozess korrekt einzustellen. Der 3D-Drucker erhitzt im sogenannten Extruder das Filament auf eine Temperatur, mit der es sich gut verflüssigen und drucken lässt, während das Heizbett auf eine Temperatur eingestellt wird, die sicherstellt, dass das Filament gut darauf haftet. So verwendet man z.B. für PLA üblicherweise eine Extrudertemperatur von 200-230 °C und eine Heizbetttemperatur von 60 °C. Diese Temperaturempfehlungen können aber je nach Hersteller auch abweichen. Am besten prüft man die Angaben auf der Filamentrolle bzw. in beigelegten Datenblättern und gleicht sie mit den Einstellungen in der Slicer-Software ab (mehr [zum Thema Slicing später](#slicer-software)).

Filamente werden meistens in den Durchmesser-Varianten 1,75 mm und 2,85 mm verkauft, wobei 1,75 mm die deutlich verbreitete Variante ist. Für größere 3D-Drucker bzw. für solche, bei denen die Düse entsprechend getauscht wurde, wird das dickere 2,85-mm-Filament verwendet.

Gewöhnliche 3D-Drucker können nur mit einem Filament zurzeit drucken, d.h. wenn man in einer anderen Farbe oder mit einem anderen Material drucken möchte, muss man die Filamentrolle wechseln. Es gibt aber auch 3D-Drucker, die mit zwei oder mehr Filamenten auf einmal drucken können. So können mehrfarbige Objekte oder auch Objekte aus verschiedenen Materialien gedruckt werden, z.B. indem das Stützmaterial (mehr dazu siehe unten, Abschnitt [Stützmaterial](#stützmaterial-und-brücken)) aus einem leicht entfernbaren Material und das eigentliche Objekt aus einem stabilen Material gedruckt wird.

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
       <a href="#s17">[17]</a> <i> Die wichtigsten Komponenten eines 3D-Druckers </i>
</p>

Die wichtigste Komponente ist der Extruder, den man sich ähnlich wie einen "Druckkopf" bei Tintenstrahldruckern vorstellen kann.

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231214463-7300d3b7-f7c8-4ef1-835b-832cdd675ac4.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231214586-2137f3f7-d4fa-4cc6-8046-e9be2a258ec0.png">
</p>

<p align="center">
<a href="#s18">[18]</a> <i> Vereinfachte Schnittdarstellung eines Extruders mit: (1) Filament - (2) Extruder mit Zahnrädern für den Filamentvorschub - (3) Beheizte Düse (Nozzle) - </i>
<a href="#s19">[19]</a> <i> Foto eines Extruders </i>
</p>



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
       <a href="#s20">[20]</a> <i> X-, Y- und Z-Achse eines 3D-Druckers - </i>
       <a href="#s21">[21]</a> <i> Draufsicht eines 3D-Druckers mit X- und Y-Achse </i>
</p>

<br>

Die Z-Achse hingegen bezieht sich auf die vertikale (senkrechte) Bewegung:
- Z-Achse: "oben und unten"

<br>

<p align="center">
       <img height="400" src="https://user-images.githubusercontent.com/123781559/228372746-eb115280-5621-4a70-bccf-280dc9de1353.png">
</p>

<p align="center">
       <a href="#s22">[22]</a> <i> Frontansicht eines 3D-Druckers mit X- und Z-Achse </i>
</p>

Der Extruder sitzt oft auf einer Stange, auf der er sich nach links und rechts (also in X-Richtung) bewegen kann. Angesteuert wird dies über einen Motor und einen Riemen.

Für Bewegungen in der Y-Achse wird oft gar nicht der Extruder bewegt, sondern das Heizbett – auch hier durch einen Motor und ein Riemen.

Für die Z-Achse wiederum gibt es meist motorgesteuerte Spindeln, die die gesamte X-Achsen-Stange nach oben und unten verschiebt. Bei manchen 3D-Druckern wird nicht der Extruder (bzw. die x-Achse), sondern das Heizbett nach oben bzw. unten bewegt.

Den Druckablauf kann man sich nun so vorstellen, dass ein 3D-Drucker zunächst wie ein „2D-Drucker“ funktioniert. Geschmolzenes Filament wird durch die Düse/Nozzle des Extruders gedrückt, während sich gleichzeitig die X- und Y-Achsen bewegen. Somit „zeichnet“ der Drucker die erste, unterste Schicht auf das Heizbett, sozusagen „in 2D“. Sobald die erste Schicht fertig ist, fährt der Extruder ein kleines Stück weit (oft nur einen Bruchteil eines Millimeters) in z-Richtung hoch und „zeichnet“ darauf dann die zweite Schicht. So wird fortgefahren, bis die oberste Schicht und damit das ganze dreidimensionale Objekt fertig ist.

### Kalibrierung

Ein neu gekaufter oder neu zusammengebauter 3D-Drucker muss zunächst kalibriert werden. Die meisten 3D-Drucker haben dafür ein Programm, das man über die Einstellungen starten kann. Beim Kalibrieren fährt der Extruder verschiedene Punkte an, fährt die x-, y- und z-Achse jeweils einmal in gesamter Länge ab und „tastet“ das Heizbett ab. Die Messwerte und Koordinaten werden gespeichert und es wird sichergestellt, dass der 3D-Drucker korrekt ausgerichtet ist.

Manchmal kann es notwendig sein, einen 3D-Drucker erneut zu kalibrieren, z.B. nachdem man ihn transportiert hat oder wenn Fehler in den Druckergebnissen auffallen.


## Vorbereitung eines 3D-Drucks
### Digitales 3D-Modell

Zunächst braucht man ein digitales 3D-Modell des Objekts, das man drucken möchte. Solche 3D-Modelle kann man entweder selbst modellieren/designen (z.B. mit einer CAD-Software) oder man lädt sich ein fertiges Modell aus dem Internet. Die meisten Modelldateien sind auch klein genug, um z.B. per E-Mail verschickt zu werden. Eine weitere Möglichkeit, ein 3D-Modell zu erstellen, besteht im 3D-Scannen eines realen Objekts oder einer Person.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231223723-82e3d49e-2547-459c-ad68-068bcb5e983a.png">
</p>

<p align="center">
<a href="#s23">[23]</a> <i> 3D-Modell eines Bauteils, erstellt in FreeCAD </i>
</p>



Mit den Themen [3D-CAD-Modellierung](../1.1%203D-Design/3D-Design.md) (CAD = Computer Aided Design), [3D-Scanning](../1.2%203D-Scanning/3D-Scanning.md) und [Modell-Download von Webseiten](../1.3%20Verwendung%20von%203D%20Modellen%20aus%20dem%20Internet/Verwendung%20von%203D%20Modellen%20aus%20dem%20Internet.md) befassen sich andere Basislernmodule.

Für die meisten 3D-Drucker benötigt man Dateien im STL-Format (oder manchmal auch OBJ-Format) - also mit der Dateiendung „.stl“ oder „.obj“. STL ist aber das üblichere Dateiformat. Fast jede CAD-Software ist in der Lage, 3D-Modelle im STL-Format zu exportieren. Bei heruntergeladenen Dateien aus dem Internet sollte man zunächst prüfen, ob es im STL-Format vorliegt.

Bevor man die STL-Datei drucken kann, muss man sie noch in einer sogenannten Slicer-Software bearbeiten. Kurz gesagt, erzeugt die Slicer-Software auf Basis des 3D-Modells viele kleine, übereinanderliegende Schichten oder Scheiben und berechnet die Steuerbefehle für den 3D-Drucker, der das Modell dann Schicht für Schicht aufeinander druckt (eine genauere [Beschreibung des Slicings weiter unten](#slicing-prüfung-und-export)).

### Slicer-Software

Es gibt viele verschiedene Slicer-Programme. Viele große und bekannte Hersteller von 3D-Druckern haben ihre eigene Slicer-Software und bieten diese über ihre Website in der Regel kostenlos zum Download an. Zwei Beispiele (mit Download-Links):

- PrusaSlicer		https://www.prusa3d.com/de/page/prusaslicer_424/ 
- UltiMaker Cura 	https://ultimaker.com/de/software/ultimaker-cura 

Viele Slicer-Programme basieren auf Open-Source-Software, z.B. wurde der PrusaSlicer auf Basis der Open-Source-Software „Slic3r“ entwickelt und der PrusaSlicer selbst ist damit auch Open Source.

Manche kleinere Hersteller von 3D-Druckern nutzen auch Slicer-Programme der größeren Hersteller und liefern dazu nur eine Konfigurationsdatei, die die Slicer-Software auf den 3D-Drucker anpasst.

In der Slicer-Software sieht man eine Vorschau des Heizbetts sowie der importierten 3D-Objekte. Mit der Software lassen sich die zu druckenden 3D-Objekte vervielfältigen (um ein Objekt gleich mehrmals zu drucken), virtuell im Raum bewegen, drehen, skalieren (vergrößern/verkleinern), und in gewünschte Positionen auf dem Heizbett platzieren.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231225892-91ae9e6e-60d9-4985-a746-0d75631386c3.png">
</p>

<p align="center">
<a href="#s24">[24]</a> <i> Vorbereitung mehrerer Objekte für den 3D-Druck in einer Slicer-Software (PrusaSlicer) </i>
</p>



### Slicing, Prüfung und Export

Es gibt zahlreiche Einstellungen im Slicer, wobei in diesem Basislernmodul nicht auf alle Einstellungen im Detail eingegangen wird. Für einen ersten, einfachen 3D-Druck reichen meistens die Standard-Einstellungen aus.

Die wichtigste Einstellung ist das Material. Möchte man z.B. mit PLA drucken, wählt man in der Materialeinstellung „PLA“ aus oder gibt die empfohlenen Temperaturen des Filamentherstellers an.

Nachdem man die STL-Datei(en) im Slicer importiert, korrekt gedreht, ausgerichtet und die [Stützmaterialien](#stützmaterial-und-brücken) eingestellt hat, muss man das Slicing starten.

Slicing (von englisch „slice“ = Scheibe) ist ein Ablauf in der Software, der das 3D-Objekt in viele dünne Scheiben (slices) unterteilt, die übereinander geschichtet sind. Die Scheiben haben dabei genau die Höhe bzw. Dicke, die man eingestellt hat, z.B. 0,15 mm (dieser Parameter wird meistens als „Schichthöhe“ oder englisch „layer height“ bezeichnet). Eine Schicht ist also quasi nur „2D“, während die aufeinandergestapelten Schichten zusammen ein 3D-Objekt ergeben.
  
<p align="center">
<img height="340" src="https://user-images.githubusercontent.com/123781559/231289616-610e09a9-8198-4fc3-82aa-3d009fdc7b99.png">
<img height="340" src="https://user-images.githubusercontent.com/123781559/231227964-e6d9f173-5828-4e47-8245-025ed0141fdc.png">
</p>

<p align="center">
<a href="#s25">[25]</a> <i> Slicing eines 3D-Objekts für den 3D-Druck (Software: PrusaSlicer) - </i>
<a href="#s26">[26]</a> <i> Schichten (slices) in Seitenansicht </i>
   <br> <i> (Bilder anklicken zum Vergrößern) </i>
</p>

Die Slicer-Software macht an der Stelle aber noch viel mehr als nur das eigentliche Slicing. Sie generiert auch den genauen Verlaufsweg des Extruders, also auch den Weg, den der Extruder in jeder Schicht in x- und y-Richtung und anschließend auch in Höhenrichtung (z) nimmt.
Außerdem werden beim Slicing auch Stützmaterialien generiert, sofern man welche eingestellt hat (mehr dazu siehe unten, Abschnitt „Stützmaterial“).

Nach ausgeführtem Slicing empfiehlt es sich, den Druckablauf zu prüfen. Die meisten Slicer bieten eine Vorschau- bzw. Simulationsfunktion an. Damit kann man sich die verschiedenen Schichten (von der ersten, untersten Schicht bis zur letzten ganz oben) einzeln ansehen und auch den Verlaufsweg des Extruders innerhalb einer jeden Schicht anzeigen lassen.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231230669-11a2e5bb-27ca-406f-80df-aaeadde64d8b.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231230687-ba466471-1fb5-4a9d-9184-15513a43e678.png">
</p>

<p align="center">
<a href="#s27">[27]</a> <i>  - </i>
<a href="#s28">[28]</a> <i> Simulation des 3D-Druckablaufs mit sichtbarer Infill-Struktur (Software: PrusaSlicer) </i>
</p>


Hat man das Slicing überprüft, kann man die Datei als sogenannte „G-Code“-Datei exportieren.

### G-Code

G-Code ist ein standardisiertes Dateiformat, das nicht nur im 3D-Druck, sondern auch in anderen Fertigungsverfahren (z.B. [CNC-Fräsen](../2.3%20CNC-Fr%C3%A4sen/CNC-Fr%C3%A4sen.md) oder [Lasercutting](../2.2%20Lasercutting/Lasercutting.md)) verwendet wird. Grundsätzlich ist der G-Code dafür da, der Maschine „mitzuteilen“, was sie machen soll, und zwar ganz genau in vielen kleinen Einzelschritten und Werten. Beispielsweise steht im G-Code, dass das Hotend sowie das Heizbett auf eine bestimmte Temperatur aufheizen sollen, dass der Extruder des 3D-Druckers an eine bestimmte Position fahren soll (angegeben in X-, Y-, und Z-Koordinaten) und wann das Filament, angetrieben durch die Zahnräder, vorgeschoben und aus der Nozzle gedrückt werden soll.

Der von der Slicer-Software generierte G-Code muss an den 3D-Drucker übertragen werden, wobei es je nach 3D-Drucker-Modell verschiedene Möglichkeiten gibt. Viele 3D-Drucker verfügen über einen SD-Karten-Slot oder USB-Eingang. Der G-Code muss dann auf eine SD-Karte oder einen USB-Stick kopiert werden, anschließend wird das Speichermedium in den 3D-Drucker gesteckt. Es gibt aber auch 3D-Drucker, die per Kabel direkt mit dem PC verbunden werden können. Der Druckvorgang wird dann direkt vom PC aus gestartet.

### Stützmaterial und Brücken
Da beim 3D-Druck stets Material aufeinandergeschichtet werden muss, kann es Probleme geben, wenn ein Objekt sogenannte Überhänge hat. Ein 3D-Drucker kann nicht „in der Luft“ drucken. Eine zu druckende Wand muss daher idealerweise im 90°-Winkel nach oben ragen, wobei je nach Material auch Schrägen möglich sind (meistens in Winkeln von mindestens 45°). Die Ränder der Schichten überlappen sich dann ein wenig.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231237520-44af31e4-83dc-4b5d-8b13-a84a15cea35e.png">
</p>

<p align="center">
<a href="#s29">[29]</a> <i> Der Schichtwinkel sollte mindestens 45° betragen </i>
</p>

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231262464-72dd29d8-2bf0-4287-aeb1-8fb7f66ad6d3.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231262498-2cadc795-e7a6-4308-b73d-f9e4768bcd7c.png">
</p>

<p align="center">
<a href="#s30">[30]</a> <i>  - </i>
<a href="#s31">[31]</a> <i> Objekt mit 45°-Schräge im PrusaSlicer </i>
</p>



Größere Überhänge sind jedoch nicht möglich. Oft lässt sich dieses Problem lösen, indem man das Objekt in der Slicer-Software in eine günstigere Position dreht. Viele Slicer verfügen über eine Funktion, bei der man nur eine Oberfläche des Objekts anklicken muss, auf die es „gelegt“ werden soll.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231267207-d3abbc50-cd72-4855-b2fa-4f09f9d2fde3.png">
</p>

<p align="center">
<a href="#s32">[32]</a> <i> Oben: Nur die Beine des Tisches lassen sich drucken, die Tischplatte hingegen müsste "in der Luft gedruckt" werden (funktioniert nicht). <br> Unten: Einfache Lösung: Den Tisch so umdrehen, dass er frei von Überhängen ist und sich gut drucken lässt. </i>
</p>


Bei komplexer geformten Objekten kann es sein, dass es keine überhangfreie Drehposition gibt. In dem Fall kann man in der Slicer-Software automatisch sogenanntes Stützmaterial generieren lassen. Dieses Stützmaterial ist größtenteils hohl und lässt sich nach dem 3D-Druck meistens relativ leicht entfernen, z.B. mit den Fingern oder mit einer Zange.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231269120-b3aa2e5a-f668-4734-a817-5a4bc9b2ce56.png">
</p>

<p align="center">
<a href="#s33">[33]</a> <i> 3D-gedrucktes Objekt mit (entfernbarem) Stützmaterial: <br> Diese Dino-Figur ist ein gutes Beispiel für ein Modell, das sich nicht überhangfrei drucken lässt, egal wie man es dreht - daher ist Stützmaterial notwendig. </i>
</p>


Zudem können manche 3D-Drucker und Slicer auch sogenannte Brücken drucken, wenn die Voraussetzungen stimmen. Bei einer Brücke spannt der Extruder Fäden von einer Seite eines Sockels zur anderen. Eine nur einseitig befestigte und am anderen Ende frei in der Luft hängende "Brücke" ist nicht möglich. Zudem darf eine Brücke nicht zu lang bzw. der Abstand zwischen den Sockeln nicht zu groß sein, da der Faden beim Drucken sonst zu wenig Spannung hat und herunterhängt. Für kurze Distanzen sind Brücken aber eine sehr gute Möglichkeit, um ohne Stützmaterial „in der Luft“ zu drucken.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231270536-47aa3b98-7e93-41ae-9f14-c63984b7f1ac.png">
</p>

<p align="center">
<a href="#s34">[34]</a> <i> Brücke in einer Slicer-Software (PrusaSlicer) </i>
</p>



### Infill
Meistens ist es gar nicht notwendig, ein komplett massives Kunststoffteil zu drucken. Nur die äußere Hülle des 3D-gedruckten Objekts ist massiv, innen ist das Objekt jedoch zum Teil hohl und zum Teil mit einer Art Gitterstruktur gefüllt. Wie viel Prozent des Inneren eines Objekts mit Material gefüllt ist, lässt sich in Slicern über den Parameter „Infill“ einstellen.

Ein Infill von z.B. 15 % (üblicher Standardwert) bedeutet, dass das Objekt zu 15% mit Material gefüllt ist, während die restlichen 85 % hohl bzw. mit Luft gefüllt sind. Für die meisten 3D-Druck-Vorhaben reicht das vollkommen aus. Somit wiegt das Objekt weniger, es wird in kürzerer Zeit gedruckt und es wird weniger Material verbraucht als bei einem massiven Objekt (Infill 100%). Je nach Bedarf kann ein niedriger oder auch ein höherer Infill-Wert eingestellt werden, z.B. wenn das Objekt starke Belastungen aushalten soll.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231274669-ce1fc5f2-1b33-4dd6-a743-5b1384c512b8.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/231274846-3f1a59d6-1904-4776-84f2-ac12ee6be783.png">
</p>

<p align="center">
<a href="#s35">[35]</a> <i> Sichtbares Infill (gelb) in unterschiedlich eingestellten Füllraten (Slicer-Software: UltiMaker Cura) - </i> <br>
<a href="#s36">[36]</a> <i> Halbfertig ausgedruckte Figur mit sichtbarer Infill-Struktur </i>
</p>


## Ablauf eines 3D-Drucks
### Vor dem Drucken

Vor Beginn eines 3D-Drucks sollte man überprüfen, ob das richtige Filament eingesetzt und ob genügend Filament auf der Rolle vorhanden ist. Zudem empfiehlt es sich, das Heizbett zu reinigen, z.B. mit Isopropanol oder Glasreiniger. Damit werden unsichtbare Fettreste entfernt, die z.B. durch Berühren des Druckbetts mit den Fingern entstehen können. Fettreste können dazu führen, dass das Filament nicht richtig auf dem Druckbett haftet.

Hat man den fertigen G-Code an den 3D-Drucker übertragen und den 3D-Druck gestartet, sollte man den Beginn des Drucks eine Weile beobachten und bei Problemen den 3D-Druck pausieren oder abbrechen. 


### Leveling, Schürze und Rand
Beim Start eines 3D-Druck-Auftrags wird der 3D-Drucker üblicherweise zunächst das Heizbett an verschiedenen Stellen abtasten, um nochmals die Z-Positionen zu kalibrieren (sogenanntes „Leveling“).

Danach wird eine wenige Zentimeter lange Linie am Rand des Heizbetts gedruckt, die sogenannte „intro line“ oder „purge line“ (engl. purge = reinigen). Dieser Vorgang dient der „Spülung“ der Düse und stellt sicher, dass die Düse voll mit zähflüssigem Filament gefüllt, gut durchflutet und bereit zum Drucken ist. Würde der 3D-Drucker die purge line weglassen und direkt mit dem Druck des Objekts beginnen, könnte es sein, dass zu Beginn noch kein Filament herauskommt oder dass es nur sehr ungleichmäßig heraustritt.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231279149-0d816436-0c5a-4ce7-841a-6cb67fe9a45a.png">
</p>

<p align="center">
<a href="#s37">[37]</a> <i> Purge line am Rand des Heizbetts: Diese Linie wird vor Beginn des eigentlichen 3D-Drucks gezogen, um die Düse zu spülen und für einen gleichmäßigen Filamentfluss zu sorgen. </i>
</p>



Anschließend wird meist, falls so eingestellt, eine Außenlinie um die Fläche herum gedruckt, wo die Objekte entstehen sollen. Diese sogenannte „Schürze“ (engl. „skirt“) vermittelt gleich zu Beginn des Drucks einen Eindruck von der Größe der zu druckenden Objekte. Zudem kann man an der Schürze bereits früh erkennen, ob das Material gut haftet und ob keine Probleme in der Qualität erkennbar sind, um den Druck an der Stelle im Zweifel noch abbrechen zu können.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/231280914-673540b8-6d43-4d43-ac21-7403f314c2bd.png">
</p>

<p align="center">
<a href="#s38">[38]</a> <i> Schürze (skirt) am Rand eines 3D-gedruckten Objekts: Die Schürze dient dazu, vor Beginn des eigentlichen Drucks den Umriss zu erkennen, zudem wird der Durchfluss in der Düse stabilisiert. </i>
</p>



Bei manchen Materialien kann es hilfreich sein, zusätzlich einen Rand (engl. „brim“) zu drucken, um das Objekt während des Drucks zu stabilisieren. Die Rand-Funktion kann bei Bedarf in den Einstellungen des Slicers aktiviert und eingestellt werden.

### Die erste Schicht

Nach dem Drucken von Schürze und Rand wird die erste Schicht des Objekts gedruckt. Diese sollte man genau beobachten. Stellt man fest, dass die erste Schicht unsauber ausgeführt ist, z.B. wenn das Filament an einigen Stellen nicht richtig haftet (zu erkennen an kleinen Erhebungen in der Schicht), sollte man den Druck an dieser Stelle abbrechen, das bereits gedruckte Material entfernen, das Heizbett reinigen bzw. die Z-Achse neu kalibrieren und den Druck neu starten.

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231281848-0418b2c1-a7d3-4319-855d-fcf984df0e4c.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/231281880-e13b9e86-3d65-4556-96aa-e4b1b79bf8a1.png">
</p>

<p align="center">
<a href="#s39">[39]</a> <i>  - </i>
<a href="#s40">[40]</a> <i> Gelungene erste Schicht eines 3D-Drucks: Der Druck der ersten Schicht sollte stets genau beobachtet und bei Qualitätsmängeln ggf. neu gestartet werden. </i>
</p>

Eine misslungene erste Schicht kann sonst dazu führen, dass das gesamte Objekt im späteren Verlauf unsauber wird oder gänzlich misslingt. Da ein 3D-Druck mehrere Minuten oder oft sogar Stunden dauern kann, lohnt es sich, eine gute erste Schicht sicherzustellen, bevor man viel Zeit und Material verschwendet.

### Weitere Schichten

Im Laufe des 3D-Drucks kann man beobachten, wie die weiteren Schichten aufgetragen werden. Dabei wird man auch das Innere des Objekts mit der Infill-Gitterstruktur erkennen.

Wenn die erste Schicht gut gelungen ist, kann man den 3D-Drucker problemlos unbeobachtet lassen. Ob man auch den Raum verlassen oder gar über Nacht drucken darf, muss man im Zweifel mit dem/der Besitzer:in des Druckers bzw. mit dem Fab Lab absprechen.

### Nach dem Druck

Sobald der 3D-Druck fertig ist, fährt der Extruder in eine Position, wo er nicht stört, sodass man das Objekt entnehmen kann. Viele 3D-Drucker haben eine entnehmbare Platte (z.B. aus Federstahlblech) auf dem Druckbett. Dies erleichtert die Entnahme der Objekte, da man erst die Platte als Ganzes entnehmen, danach leicht biegen und die Objekte einfach von der Platte lösen kann.

Abschließend muss man ggf. vorhandenes Stützmaterial entfernen. Zudem kann man das Objekt auf verschiedene Arten nachbearbeiten, z.B. schleifen oder mit Epoxidharz behandeln, um die Oberflächenoptik zu verschönern.

# Lizenzinformationen

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.


# Bildnachweise

<a name="s1"></a>
**[1]** DIY-3D-Drucker mit Open-Hardware-Lizenz [(Repository)](https://gitlab.fabcity.hamburg/hardware/interfacer-osh-build-workshops/3-d-printer-hypercuboid) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s2"></a>
**[2]** Prusa i3 metal frame - **Image license:** [GNU Free Documentation License, Version 1.2](https://commons.wikimedia.org/wiki/Commons:GNU_Free_Documentation_License,_version_1.2) - **Source:** https://commons.wikimedia.org/wiki/File:Prusa_i3_metal_frame.jpg

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
**[10]** Verschiedene 3D-gedruckte Objekte - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s11"></a>
**[11]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s12"></a>
**[12]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s13"></a>
**[13]** 3D-gedrucktes Objekt - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s14"></a>
**[14]** Makerbot Store, Manhattan (NY, USA) - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Makerbot_Store,_Manhattan_(NY,_USA)_(8764959982).jpg

<a name="s15"></a>
**[15]** ABS filament spool - **Image license:** [GNU Free Documentation License, Version 1.2](https://commons.wikimedia.org/wiki/Commons:GNU_Free_Documentation_License,_version_1.2) - **Source:** https://commons.wikimedia.org/wiki/File:ABS_filament_spool.jpg

<a name="s16"></a>
**[16]** 3DBenchy created using color mixing on an FDM printer - **Image license:** [GNU Free Documentation License, Version 1.2](https://commons.wikimedia.org/wiki/Commons:GNU_Free_Documentation_License,_version_1.2) - **Source:** https://commons.wikimedia.org/wiki/File:3DBenchy_created_using_color_mixing_on_an_FDM_printer.jpg

<a name="s17"></a>
**[17]** Die wichtigsten Komponenten eines 3D-Druckers (3D-Modell erstellt in FreeCAD) - [3DBenchy attribution](https://www.3dbenchy.com/license/) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s18"></a>
**[18]** Filament Driver diagram of a 3D printer (FDM). 1 Filament. 2 Filament Driver (Extruder). 3 Heated Nozzle. 4 Print. 5 Build Platform. (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://en.wikibooks.org/wiki/File:Filament_Driver_diagram.svg

<a name="s19"></a>
**[19]** Taz 5 3D Printer (16721682637).jpg - https://www.sparkfun.com/products/retired/13300 - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Taz_5_3D_Printer_%2816721682637%29.jpg

<a name="s20"></a>
**[20]** X-, Y- und Z-Achse eines 3D-Druckers - [3DBenchy attribution](https://www.3dbenchy.com/license/) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s21"></a>
**[21]** Draufsicht eines 3D-Druckers mit X- und Y-Achse - [3DBenchy attribution](https://www.3dbenchy.com/license/) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s22"></a>
**[22]** Frontansicht eines 3D-Druckers mit X- und Z-Achse - [3DBenchy attribution](https://www.3dbenchy.com/license/) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s23"></a>
**[23]** 3D-Modell eines Bauteils, erstellt in FreeCAD - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s24"></a>
**[24]** Vorbereitung mehrerer Objekte für den 3D-Druck in einer Slicer-Software (PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s25"></a>
**[25]** Slicing eines 3D-Objekts für den 3D-Druck (Software: PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s26"></a>
**[26]** Schichten (slices) in Seitenansicht (Software: PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s27"></a>
**[27]** Simulation des 3D-Druckablaufs mit sichtbarer Infill-Struktur (Software: PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s28"></a>
**[28]** Simulation des 3D-Druckablaufs mit sichtbarer Infill-Struktur (Software: PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s29"></a>
**[29]** Schichtwinkel beim 3D-Druck mindestens 45° - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org) - **Adapted from:** An illustration demonstrating the effect of using a part-cooling fan 3D printing on a filament-based 3D printer. - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:3D_printing_calibration_part-cooling_fan_airflow.svg

<a name="s30"></a>
**[30]** Objekt mit 45°-Schräge im PrusaSlicer - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s31"></a>
**[31]** Objekt mit 45°-Schräge im PrusaSlicer - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s32"></a>
**[32]** Objekt nicht 3D-druckbar, gedrehtes Objekt druckbar - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s33"></a>
**[33]** Kunststoffdino mit Stützstruktur Rapid Prototyping /Kunststoff schichtweise aufgetragen - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Rapid-dino.jpg

<a name="s34"></a>
**[34]** Brücke in einer Slicer-Software (PrusaSlicer) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s35"></a>
**[35]** Different levels of infill denisity, as generated by Cura software (cropped, rearranged)- **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Infill_density.jpg

<a name="s36"></a>
**[36]** 3D printed HULK (40% only power) (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:HULK_(40%25).jpg

<a name="s37"></a>
**[37]** Purge line 3D-Druck - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s38"></a>
**[38]** Schürze (skirt) im 3D-Druck - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s39"></a>
**[39]** Erste Schicht 3D-Druck - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s40"></a>
**[40]** Erste Schicht 3D-Druck - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)
