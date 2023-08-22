**Translation note:**

This article is still being translated into **English**.

To do:
- Edit file
- Replace text by English translation
- Commit changes
- When done, remove this note

> Back to [basic learning modules overview](../../translations/EN_Readme.md)

# 3D printing

## Contents

1. [Introduction](#introduction)
2. [Basics](#basics)
   - [Filament](#filament)
   - [3D printer components](#3D-printer-components)
   - [Calibration](#calibration)
3. [Preparing a 3D print](#preparing-a-3D-print)
   - [Digital 3D model](#digital-3D-model)
   - [Slicer software](#slicer-software)
   - [Slicing, testing and export](#slicing-testing-and-export)
   - [G-code](#g-code)
   - [Support material and bridges](#support-material-and-bridges)
   - [Infill](#infill)
4. [3D printing process](#3D-printing-process)
   - [Before printing](#before-printing)
   - [Leveling, skirt and brim](#leveling-skirt-and-brim)
   - [The first layer](#the-first-layer)
   - [More layers](#more-layers)
   - [After printing](#after-printing)

[License information](#license-information)

[Image references](#image-references)

## Introduction

3D printing refers to many different processes in which a device (3D printer) creates material, three-dimensional objects. In most cases, the objects are first designed in software as a 3D model and then sent to the 3D printer.

There are small, relatively inexpensive 3D printers for the home or for fab labs that print mostly from plastic, but also larger printers up to large systems that can print entire buildings, at least the basic structure of walls, from concrete. Some 3D printers can also print metal or food like chocolate - the range of 3D printing processes is very wide.


<p align="center">
       <img height="400" src="images/1_3D_Printer_Open_Source_Hardware.png">
       <img height="400" src="images/2_Prusa_3D_Printer.png">
</p>

<p align="center">
       <a href="#s1">[1]</a> <i> DIY 3D printer with open hardware license - </i>
       <a href="#s2">[2]</a> <i> Prusa 3D Printer </i>
</p>


<p align="center">
       <img height="300" src="images/3_BigFDM_3D_Printer.png">
       <img height="300" src="images/4_3D_printing_buildings.png">
</p>

<p align="center">
       <a href="#s3">[3]</a> <i> BigFDM 3D printer for large models up to 80 x 80 x 90 cm - </i>
       <a href="#s4">[4]</a> <i> 3D printing houses </i>
</p>

The most widespread and popular 3D printers are those that work according to the so-called FDM process. This basic learning module will therefore initially only deal with FDM printers.

The second most common type of 3D printers in fab labs besides the FDM process are probably the SLA printers. However, these are more difficult to use and therefore less suitable for beginners than FDM printers, so it is recommended to start with FDM first.

FDM stands for "fused deposition modeling". This means that a material, usually plastic, is heated by the 3D printer, melted in the process, and then applied in layers. The layers cool shortly thereafter, causing them to bond together to form a solid object. Objects printed with FDM can be easily recognized by the typical layers, which are usually only a fraction of a millimeter thick.
  


<p align="center">
       <img height="400" src="images/5_3D_printing.png">
       <img height="400" src="images/6_Visible_layers_on_3D_printed_object.png">
</p>

<p align="center">
       <a href="#s5">[5]</a> <i> 3D printing - </i>
       <a href="#s6">[6]</a> <i> 3D printed object with visible layers </i>
</p>


This is why 3D printing is also classified as "additive manufacturing", since objects are created by adding new material. In contrast, there is also "subtractive manufacturing", i.e. manufacturing processes in which an existing material is separated or something is "taken away", e.g. by [laser cutting](../2_2_Laser_cutting/EN_Laser_cutting.md) or [CNC milling](../2_3_CNC_milling/EN_CNC_milling.md).

FDM 3D printers can be used, for example, to print decorative objects such as figurines or vases, small toys, personalized name tags and key chains, models for demonstration purposes (e.g. of machines or buildings), spare parts for existing products (e.g. drawer handles or rotating knobs for music systems), everyday helpers such as towel hooks or functional parts such as housings for electronic devices, bottle openers or even components for 3D printers.

<p align="center">
<img height="300" src="images/7_3D_printed_speaker_casing.png">
<img height="300" src="images/8_3D_printed_jet_engine_turbine_model.png">
</p>

<p align="center">
<a href="#s7">[7]</a> <i> 3D printed speaker housing - </i>
<a href="#s8">[8]</a> <i> 3D printed model of a turbine</i>
</p>

<p align="center">
<img height="300" src="images/9_3D_printing_a_yarn_bowl.png">
<img height="300" src="images/10_3D_printed_objects.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i> 3D printed bowl - </i>
<a href="#s10">[10]</a> <i> Various 3D printed objects</i>
</p>

<p align="center">
<img height="230" src="images/11_3D_printed_object.png">
<img height="230" src="images/12_3D_printed_object.png">
<img height="230" src="images/13_3D_printed_object.png">
</p>

<p align="center">
<a href="#s11">[11]</a> <i>  - </i>
<a href="#s12">[12]</a> <i>  - </i>
<a href="#s13">[13]</a> <i> Various 3D printed objects</i>
</p>




## Basics
### Filament

The basic material needed for an FDM 3D printer is called filament. A filament is a thin plastic wire wound on a spool.

<p align="center">
<img height="300" src="images/14_Filament_for_3D_printing.png">
<img height="300" src="images/15_Filament_for_3D_printing.png">
</p>

<p align="center">
<a href="#s14">[14]</a> <i> Different spools of filament - </i>
<a href="#s15">[15]</a> <i> Filament spool</i>
</p>

Filaments come in a wide variety of colors and materials.
The most common 3D printing material is PLA. It is cheap, easy to print, suitable for most applications and therefore also for beginners.

PLA is a type of plastic and stands for "polylactic acid".

Here is a brief overview of the most common materials for FDM 3D printers and the main advantages and disadvantages:

- **PLA:** Inexpensive, easy to print, good for beginners, ideal for decorative objects or components with low loads; good recyclability. 
- **PETG / PET-G:** More robust than PLA, good for functional components that need to withstand high forces/loads; easier to print than ABS; slightly stronger than ABS. 
- **PET:** Rather rarely found as 3D printing filament, less suitable than PET-G; very well recyclable; can be produced from PET bottles, for example. 
- **ABS:** Similar to PETG in load capacity, higher heat resistance than PETG; emits unhealthy fumes during printing, well ventilated room required; difficult to print, enclosure and high heating bed temperature recommended.
- **ASA:** Considered the "successor" to ABS; less warping and evaporates less than ABS. 
- **Nylon:** Particularly high mechanical and thermal resistance; difficult to print, more for advanced users; more expensive than other filament types; susceptible to moisture 
- **TPU:** Flexible, "rubbery" material; can be easily deformed after printing; ideal for small tires, stamps, etc.; relatively difficult to print; more expensive than other types of filaments. 

Since every material has a different melting temperature, it is important to set this correctly in the printing process. The 3D printer heats the filament in the so-called extruder to a temperature at which it can be liquefied and printed well, while the heating bed is set to a temperature that ensures that the filament adheres well to it. For example, for PLA, it is common to use an extruder temperature of 200-230 °C and a heating bed temperature of 60 °C. However, these temperature recommendations can also differ depending on the manufacturer. It is best to check the specifications on the filament spool or in the enclosed data sheets and compare them with the settings in the slicer software (more [about slicing later](#slicer-software)).

Filaments are mostly sold in 1.75 mm and 2.85 mm diameter variants, with 1.75 mm being the significantly more common variant. For larger 3D printers or those where the nozzle has been changed accordingly, the thicker 2.85 mm filament is used.

Ordinary 3D printers can only print with one filament at a time, so if you want to print in a different color or with a different material, you have to change the filament spool. However, there are 3D printers that can print with two or more filaments at once. In this way, multicolored objects or objects made of different materials can be printed, e.g. by printing the support material (see more below, section [support material](#support-material-and-bridges)) from an easily removable material and the actual object from a stable material.

<p align="center">
<img height="400" src="images/16_3D_printing_color_mixing.png">
</p>

<p align="center">
<a href="#s16">[16]</a> <i> Multicolor 3D Printing</i>
</p>

### 3D printer components

First of all, you should familiarize yourself with the basic structure of an FDM 3D printer. A typical FDM 3D printer is described here as an example. Most FDM printers are built in this or a similar way. Depending on the manufacturer and model, this setup may also differ, but the basic principles remain the same.

<p align="center">
       <img height="500" src="images/17_Die_wichtigsten_Komponenten_eines_3D-Druckers.png">
</p>

<p align="center">
       <a href="#s17">[17]</a> <i> The main components of a 3D printer </i>
</p>

The most important component is the extruder, which can be thought of as similar to a "print head" in inkjet printers.

<p align="center">
<img height="300" src="images/18_Extruder.png">
<img height="300" src="images/19_Extruder.png">
</p>

<p align="center">
<a href="#s18">[18]</a> <i> Simplified sectional view of an extruder with: (1) Filament - (2) Extruder with gears for filament feed - (3) Heated nozzle - </i>
<a href="#s19">[19]</a> <i> Photo of an extruder </i>
</p>



At the top of the extruder is an opening into which the filament wire is inserted. Inside the extruder, the filament is pulled in or pushed on down by two gears that control the "feed" of the filament.

After that, the filament goes through a cooling section. A fan blows air against the cooling fins to cool the filament in this area. This prevents the filament from conducting heat upwards and melting in the area of the gears. Liquid filament could then no longer be pushed forward by the gear wheels. In the course of a 3D printing process, the fan may sometimes start and sometimes stop again.

After the cooling section of the extruder, the filament moves further down through the so-called "hot end". There, the filament is heated, melted and liquefied to some extent. Finally, the viscous filament is pressed through a nozzle. The filament, which is e.g. 1.75 mm thick, is pressed through the nozzle to a much smaller diameter (usually approx. 0.4 mm). The emerging filament can now be used for layer-by-layer deposition, i.e. 3D printing.

In order for the extruder to create objects in three-dimensional space, it must be able to move in all directions. This is why 3D printers have three motor-controlled axes: the X, Y and Z axes.

The X and Y axes usually refer to movements in the horizontal base:
- X-axis: "left and right"
- Y-axis: "front and back"

<p align="center">
       <img height="400" src="images/20_X-_Y-_and_Z-axis_3D_printer.png">
       <img height="400" src="images/21_Top_view_3D_printer_with_X-_and_Y-axis.png">
</p>

<p align="center">
       <a href="#s20">[20]</a> <i> X, Y and Z axis of a 3D printer - </i>
       <a href="#s21">[21]</a> <i> Top view of 3D printer with X and Y axis </i>
</p>

<br>

The Z axis, on the other hand, refers to vertical movement:
- Z-axis: "top and bottom"

<br>

<p align="center">
       <img height="400" src="images/22_Front_view_3D_printer_with_X-_and_Z-axis.png">
</p>

<p align="center">
       <a href="#s22">[22]</a> <i> Front view of a 3D printer with X- and Z-axis </i>
</p>

The extruder often sits on a rod on which it can move to the left and right (i.e. in the X direction). This is controlled by a motor and a belt.

For movements in the Y-axis, it is often not the extruder that is moved at all, but the heating bed - again by a motor and a belt.

For the Z-axis, on the other hand, there are usually motor-controlled spindles that move the entire X-axis bar up and down. In some 3D printers, it is not the extruder (or the x-axis) that is moved up or down, but the heating bed.

The printing process can now be imagined in such a way that a 3D printer initially functions like a "2D printer". Molten filament is pushed through the extruder's nozzle while the X and Y axes move at the same time. Thus, the printer "draws" the first, bottom layer onto the heated bed, "in 2D" so to speak. As soon as the first layer is ready, the extruder moves up a small distance (often only a fraction of a millimeter) in the z-direction and then "draws" the second layer on top of it. This continues until the top layer and thus the entire three-dimensional object is finished.

### Calibration

A newly purchased or newly assembled 3D printer must first be calibrated. Most 3D printers have a program for this that can be started via the settings. During calibration, the extruder moves to various points, moves along the x-, y- and z-axis once in their entire length and "scans" the heating bed. The measured values and coordinates are saved and it is ensured that the 3D printer is correctly aligned.

Sometimes it may be necessary to recalibrate a 3D printer, e.g. after you have transported it or if you notice errors in the print results.


## Preparing a 3D print
### Digital 3D model

First, you need a digital 3D model of the object you want to print. Such 3D models can either be modeled/designed by yourself (e.g. with CAD software) or you can download a ready-made model from the internet. Most model files are also small enough to be sent by e-mail, for example. Another way to create a 3D model is to 3D scan a real object or person.

<p align="center">
<img height="400" src="images/23_3D_CAD_model_part_FreeCAD.png">
</p>

<p align="center">
<a href="#s23">[23]</a> <i> 3D model of a component created in FreeCAD </i>
</p>



Other basic learning modules deal with the topics of [3D CAD modelling](../1_1_3D_design/EN_3D_design.md) (CAD = Computer Aided Design), [3D scanning](../1_2_3D_scanning/EN_3D_scanning.md) and [downloading models from websites.](../1_3_Using_3D_models_from_the_internet/EN_Using_3D_models_from_the_internet.md).

Für die meisten 3D-Drucker benötigt man Dateien im STL-Format (oder manchmal auch OBJ-Format) - also mit der Dateiendung „.stl“ oder „.obj“. STL ist aber das üblichere Dateiformat. Fast jede CAD-Software ist in der Lage, 3D-Modelle im STL-Format zu exportieren. Bei heruntergeladenen Dateien aus dem Internet sollte man zunächst prüfen, ob es im STL-Format vorliegt.

Bevor man die STL-Datei drucken kann, muss man sie noch in einer sogenannten Slicer-Software bearbeiten. Kurz gesagt, erzeugt die Slicer-Software auf Basis des 3D-Modells viele kleine, übereinanderliegende Schichten oder Scheiben und berechnet die Steuerbefehle für den 3D-Drucker, der das Modell dann Schicht für Schicht aufeinander druckt (eine genauere [Beschreibung des Slicings weiter unten](#slicing-prüfung-und-export)).

### Slicer software

Es gibt viele verschiedene Slicer-Programme. Viele große und bekannte Hersteller von 3D-Druckern haben ihre eigene Slicer-Software und bieten diese über ihre Website in der Regel kostenlos zum Download an. Zwei Beispiele (mit Download-Links):

- PrusaSlicer		https://www.prusa3d.com/de/page/prusaslicer_424/ 
- UltiMaker Cura 	https://ultimaker.com/de/software/ultimaker-cura 

Viele Slicer-Programme basieren auf Open-Source-Software, z.B. wurde der PrusaSlicer auf Basis der Open-Source-Software „Slic3r“ entwickelt und der PrusaSlicer selbst ist damit auch Open Source.

Manche kleinere Hersteller von 3D-Druckern nutzen auch Slicer-Programme der größeren Hersteller und liefern dazu nur eine Konfigurationsdatei, die die Slicer-Software auf den 3D-Drucker anpasst.

In der Slicer-Software sieht man eine Vorschau des Heizbetts sowie der importierten 3D-Objekte. Mit der Software lassen sich die zu druckenden 3D-Objekte vervielfältigen (um ein Objekt gleich mehrmals zu drucken), virtuell im Raum bewegen, drehen, skalieren (vergrößern/verkleinern), und in gewünschte Positionen auf dem Heizbett platzieren.

<p align="center">
<img height="400" src="images/24_Slicing_in_PrusaSlicer.png">
</p>

<p align="center">
<a href="#s24">[24]</a> <i> Vorbereitung mehrerer Objekte für den 3D-Druck in einer Slicer-Software (PrusaSlicer) </i>
</p>



### Slicing, testing and export

Es gibt zahlreiche Einstellungen im Slicer, wobei in diesem Basislernmodul nicht auf alle Einstellungen im Detail eingegangen wird. Für einen ersten, einfachen 3D-Druck reichen meistens die Standard-Einstellungen aus.

Die wichtigste Einstellung ist das Material. Möchte man z.B. mit PLA drucken, wählt man in der Materialeinstellung „PLA“ aus oder gibt die empfohlenen Temperaturen des Filamentherstellers an.

Nachdem man die STL-Datei(en) im Slicer importiert, korrekt gedreht, ausgerichtet und die [Stützmaterialien](#stützmaterial-und-brücken) eingestellt hat, muss man das Slicing starten.

Slicing (von englisch „slice“ = Scheibe) ist ein Ablauf in der Software, der das 3D-Objekt in viele dünne Scheiben (slices) unterteilt, die übereinander geschichtet sind. Die Scheiben haben dabei genau die Höhe bzw. Dicke, die man eingestellt hat, z.B. 0,15 mm (dieser Parameter wird meistens als „Schichthöhe“ oder englisch „layer height“ bezeichnet). Eine Schicht ist also quasi nur „2D“, während die aufeinandergestapelten Schichten zusammen ein 3D-Objekt ergeben.
  
<p align="center">
<img height="340" src="images/25_Slicing_in_PrusaSlicer.png">
<img height="340" src="images/26_Slicing_in_PrusaSlicer_visible_layers.png">
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
<img height="350" src="images/27_Slicing_simulation_infill_in_PrusaSlicer.png">
<img height="350" src="images/28_Slicing_simulation_infill_in_PrusaSlicer.png">
</p>

<p align="center">
<a href="#s27">[27]</a> <i>  - </i>
<a href="#s28">[28]</a> <i> Simulation des 3D-Druckablaufs mit sichtbarer Infill-Struktur (Software: PrusaSlicer) </i>
</p>


Hat man das Slicing überprüft, kann man die Datei als sogenannte „G-Code“-Datei exportieren.

### G-code

G-Code ist ein standardisiertes Dateiformat, das nicht nur im 3D-Druck, sondern auch in anderen Fertigungsverfahren (z.B. [CNC-Fräsen](../2_3_CNC_milling/CNC-Fraesen.md) oder [Lasercutting](../2_2_Laser_cutting/Lasercutting.md)) verwendet wird. Grundsätzlich ist der G-Code dafür da, der Maschine „mitzuteilen“, was sie machen soll, und zwar ganz genau in vielen kleinen Einzelschritten und Werten. Beispielsweise steht im G-Code, dass das Hotend sowie das Heizbett auf eine bestimmte Temperatur aufheizen sollen, dass der Extruder des 3D-Druckers an eine bestimmte Position fahren soll (angegeben in X-, Y-, und Z-Koordinaten) und wann das Filament, angetrieben durch die Zahnräder, vorgeschoben und aus der Nozzle gedrückt werden soll.

Der von der Slicer-Software generierte G-Code muss an den 3D-Drucker übertragen werden, wobei es je nach 3D-Drucker-Modell verschiedene Möglichkeiten gibt. Viele 3D-Drucker verfügen über einen SD-Karten-Slot oder USB-Eingang. Der G-Code muss dann auf eine SD-Karte oder einen USB-Stick kopiert werden, anschließend wird das Speichermedium in den 3D-Drucker gesteckt. Es gibt aber auch 3D-Drucker, die per Kabel direkt mit dem PC verbunden werden können. Der Druckvorgang wird dann direkt vom PC aus gestartet.

### Support material and bridges
Da beim 3D-Druck stets Material aufeinandergeschichtet werden muss, kann es Probleme geben, wenn ein Objekt sogenannte Überhänge hat. Ein 3D-Drucker kann nicht „in der Luft“ drucken. Eine zu druckende Wand muss daher idealerweise im 90°-Winkel nach oben ragen, wobei je nach Material auch Schrägen möglich sind (meistens in Winkeln von mindestens 45°). Die Ränder der Schichten überlappen sich dann ein wenig.

<p align="center">
<img height="400" src="images/29_Layer_angle_minimum_45_degrees_3D_printing.png">
</p>

<p align="center">
<a href="#s29">[29]</a> <i> Der Schichtwinkel sollte mindestens 45° betragen </i>
</p>

<p align="center">
<img height="350" src="images/30_3D_printing_object_45_degree_angle_PrusaSlicer.png">
<img height="350" src="images/31_3D_printing_object_45_degree_angle_PrusaSlicer.png">
</p>

<p align="center">
<a href="#s30">[30]</a> <i>  - </i>
<a href="#s31">[31]</a> <i> Objekt mit 45°-Schräge im PrusaSlicer </i>
</p>



Größere Überhänge sind jedoch nicht möglich. Oft lässt sich dieses Problem lösen, indem man das Objekt in der Slicer-Software in eine günstigere Position dreht. Viele Slicer verfügen über eine Funktion, bei der man nur eine Oberfläche des Objekts anklicken muss, auf die es „gelegt“ werden soll.

<p align="center">
<img height="400" src="images/32_Flipping_object_in_PrusaSlicer_for_better_3D_printing.png">
</p>

<p align="center">
<a href="#s32">[32]</a> <i> Oben: Nur die Beine des Tisches lassen sich drucken, die Tischplatte hingegen müsste "in der Luft gedruckt" werden (funktioniert nicht). <br> Unten: Einfache Lösung: Den Tisch so umdrehen, dass er frei von Überhängen ist und sich gut drucken lässt. </i>
</p>


Bei komplexer geformten Objekten kann es sein, dass es keine überhangfreie Drehposition gibt. In dem Fall kann man in der Slicer-Software automatisch sogenanntes Stützmaterial generieren lassen. Dieses Stützmaterial ist größtenteils hohl und lässt sich nach dem 3D-Druck meistens relativ leicht entfernen, z.B. mit den Fingern oder mit einer Zange.

<p align="center">
<img height="400" src="images/33_Support_material_3D_printing.png">
</p>

<p align="center">
<a href="#s33">[33]</a> <i> 3D-gedrucktes Objekt mit (entfernbarem) Stützmaterial: <br> Diese Dino-Figur ist ein gutes Beispiel für ein Modell, das sich nicht überhangfrei drucken lässt, egal wie man es dreht - daher ist Stützmaterial notwendig. </i>
</p>


Zudem können manche 3D-Drucker und Slicer auch sogenannte Brücken drucken, wenn die Voraussetzungen stimmen. Bei einer Brücke spannt der Extruder Fäden von einer Seite eines Sockels zur anderen. Eine nur einseitig befestigte und am anderen Ende frei in der Luft hängende "Brücke" ist nicht möglich. Zudem darf eine Brücke nicht zu lang bzw. der Abstand zwischen den Sockeln nicht zu groß sein, da der Faden beim Drucken sonst zu wenig Spannung hat und herunterhängt. Für kurze Distanzen sind Brücken aber eine sehr gute Möglichkeit, um ohne Stützmaterial „in der Luft“ zu drucken.

<p align="center">
<img height="400" src="images/34_Bridging_3D_printing_PrusaSlicer.png">
</p>

<p align="center">
<a href="#s34">[34]</a> <i> Brücke in einer Slicer-Software (PrusaSlicer) </i>
</p>



### Infill
Meistens ist es gar nicht notwendig, ein komplett massives Kunststoffteil zu drucken. Nur die äußere Hülle des 3D-gedruckten Objekts ist massiv, innen ist das Objekt jedoch zum Teil hohl und zum Teil mit einer Art Gitterstruktur gefüllt. Wie viel Prozent des Inneren eines Objekts mit Material gefüllt ist, lässt sich in Slicern über den Parameter „Infill“ einstellen.

Ein Infill von z.B. 15 % (üblicher Standardwert) bedeutet, dass das Objekt zu 15% mit Material gefüllt ist, während die restlichen 85 % hohl bzw. mit Luft gefüllt sind. Für die meisten 3D-Druck-Vorhaben reicht das vollkommen aus. Somit wiegt das Objekt weniger, es wird in kürzerer Zeit gedruckt und es wird weniger Material verbraucht als bei einem massiven Objekt (Infill 100%). Je nach Bedarf kann ein niedriger oder auch ein höherer Infill-Wert eingestellt werden, z.B. wenn das Objekt starke Belastungen aushalten soll.

<p align="center">
<img height="350" src="images/35_Infill_3D_printing_UltiMaker_Cura_slicer.png">
<img height="350" src="images/36_Infill_3D_printing.png">
</p>

<p align="center">
<a href="#s35">[35]</a> <i> Sichtbares Infill (gelb) in unterschiedlich eingestellten Füllraten (Slicer-Software: UltiMaker Cura) - </i> <br>
<a href="#s36">[36]</a> <i> Halbfertig ausgedruckte Figur mit sichtbarer Infill-Struktur </i>
</p>


## 3D printing process
### Before printing

Vor Beginn eines 3D-Drucks sollte man überprüfen, ob das richtige Filament eingesetzt und ob genügend Filament auf der Rolle vorhanden ist. Zudem empfiehlt es sich, das Heizbett zu reinigen, z.B. mit Isopropanol oder Glasreiniger. Damit werden unsichtbare Fettreste entfernt, die z.B. durch Berühren des Druckbetts mit den Fingern entstehen können. Fettreste können dazu führen, dass das Filament nicht richtig auf dem Druckbett haftet.

Hat man den fertigen G-Code an den 3D-Drucker übertragen und den 3D-Druck gestartet, sollte man den Beginn des Drucks eine Weile beobachten und bei Problemen den 3D-Druck pausieren oder abbrechen. 


### Leveling, skirt and brim
Beim Start eines 3D-Druck-Auftrags wird der 3D-Drucker üblicherweise zunächst das Heizbett an verschiedenen Stellen abtasten, um nochmals die Z-Positionen zu kalibrieren (sogenanntes „Leveling“).

Danach wird eine wenige Zentimeter lange Linie am Rand des Heizbetts gedruckt, die sogenannte „intro line“ oder „purge line“ (engl. purge = reinigen). Dieser Vorgang dient der „Spülung“ der Düse und stellt sicher, dass die Düse voll mit zähflüssigem Filament gefüllt, gut durchflutet und bereit zum Drucken ist. Würde der 3D-Drucker die purge line weglassen und direkt mit dem Druck des Objekts beginnen, könnte es sein, dass zu Beginn noch kein Filament herauskommt oder dass es nur sehr ungleichmäßig heraustritt.

<p align="center">
<img height="400" src="images/37_Purge_line_3D_printing.png">
</p>

<p align="center">
<a href="#s37">[37]</a> <i> Purge line am Rand des Heizbetts: Diese Linie wird vor Beginn des eigentlichen 3D-Drucks gezogen, um die Düse zu spülen und für einen gleichmäßigen Filamentfluss zu sorgen. </i>
</p>



Anschließend wird meist, falls so eingestellt, eine Außenlinie um die Fläche herum gedruckt, wo die Objekte entstehen sollen. Diese sogenannte „Schürze“ (engl. „skirt“) vermittelt gleich zu Beginn des Drucks einen Eindruck von der Größe der zu druckenden Objekte. Zudem kann man an der Schürze bereits früh erkennen, ob das Material gut haftet und ob keine Probleme in der Qualität erkennbar sind, um den Druck an der Stelle im Zweifel noch abbrechen zu können.

<p align="center">
<img height="400" src="images/38_Skirt_3D_printing.png">
</p>

<p align="center">
<a href="#s38">[38]</a> <i> Schürze (skirt) am Rand eines 3D-gedruckten Objekts: Die Schürze dient dazu, vor Beginn des eigentlichen Drucks den Umriss zu erkennen, zudem wird der Durchfluss in der Düse stabilisiert. </i>
</p>



Bei manchen Materialien kann es hilfreich sein, zusätzlich einen Rand (engl. „brim“) zu drucken, um das Objekt während des Drucks zu stabilisieren. Die Rand-Funktion kann bei Bedarf in den Einstellungen des Slicers aktiviert und eingestellt werden.

### The first layer

Nach dem Drucken von Schürze und Rand wird die erste Schicht des Objekts gedruckt. Diese sollte man genau beobachten. Stellt man fest, dass die erste Schicht unsauber ausgeführt ist, z.B. wenn das Filament an einigen Stellen nicht richtig haftet (zu erkennen an kleinen Erhebungen in der Schicht), sollte man den Druck an dieser Stelle abbrechen, das bereits gedruckte Material entfernen, das Heizbett reinigen bzw. die Z-Achse neu kalibrieren und den Druck neu starten.

<p align="center">
<img height="300" src="images/39_First_layer_3D_printing.png">
<img height="300" src="images/40_First_layer_3D_printing.png">
</p>

<p align="center">
<a href="#s39">[39]</a> <i>  - </i>
<a href="#s40">[40]</a> <i> Gelungene erste Schicht eines 3D-Drucks: Der Druck der ersten Schicht sollte stets genau beobachtet und bei Qualitätsmängeln ggf. neu gestartet werden. </i>
</p>

Eine misslungene erste Schicht kann sonst dazu führen, dass das gesamte Objekt im späteren Verlauf unsauber wird oder gänzlich misslingt. Da ein 3D-Druck mehrere Minuten oder oft sogar Stunden dauern kann, lohnt es sich, eine gute erste Schicht sicherzustellen, bevor man viel Zeit und Material verschwendet.

### More layers

Im Laufe des 3D-Drucks kann man beobachten, wie die weiteren Schichten aufgetragen werden. Dabei wird man auch das Innere des Objekts mit der Infill-Gitterstruktur erkennen.

Wenn die erste Schicht gut gelungen ist, kann man den 3D-Drucker problemlos unbeobachtet lassen. Ob man auch den Raum verlassen oder gar über Nacht drucken darf, muss man im Zweifel mit dem/der Besitzer:in des Druckers bzw. mit dem Fab Lab absprechen.

### After printing

Sobald der 3D-Druck fertig ist, fährt der Extruder in eine Position, wo er nicht stört, sodass man das Objekt entnehmen kann. Viele 3D-Drucker haben eine entnehmbare Platte (z.B. aus Federstahlblech) auf dem Druckbett. Dies erleichtert die Entnahme der Objekte, da man erst die Platte als Ganzes entnehmen, danach leicht biegen und die Objekte einfach von der Platte lösen kann.

Abschließend muss man ggf. vorhandenes Stützmaterial entfernen. Zudem kann man das Objekt auf verschiedene Arten nachbearbeiten, z.B. schleifen oder mit Epoxidharz behandeln, um die Oberflächenoptik zu verschönern.

# License information

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.


# Image references

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
