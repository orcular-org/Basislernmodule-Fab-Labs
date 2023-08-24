**Translation note:**

This article is still being translated into **English**.

To do:
- Edit file
- Replace text by English translation
- Commit changes
- When done, remove this note

> Back to [basic learning modules overview](../../translations/EN_Readme.md)

# Laser cutting

## Contents

1. [Introduction](#introduction)
2. [Basics](#basics)
   - [Materials](#materials)
   - [Components of a laser cutter](#components-of-a-laser-cutter)
   - [Parameters: Power and speed](#parameters-power-and-speed)
   - [Kerf](#kerf)
   - [Vector graphic](#vector-graphic)
   - [Software](#software)
   - [Differences to other digital manufacturing methods](#differences-to-other-digital-manufacturing-methods)
3. [Design tips](#design-tips)
   - [Push-fit systems](#push-fit-systems)
   - [3D CAD and projection](#3d-cad-and-projection)
   - [Living hinge](#living-hinge)
   - [Downloading templates](#downloading-templates)
   - [Common mistakes](#common-mistakes)
4. [Preparation and process of a laser cutting](#preparation-and-process-of-a-laser-cutting)
   - [Safety](#safety)
   - [Laser cut file](#laser-cut-file)
   - [Preparation](#preparation)
   - [Laser cutting process](#laser-cutting-process)

[License information](#license-information)

[Image references](#image-references)


## Introduction

Lasercutting is a process in which a laser beam heats a material, melting or burning it in the process and thus separating it. The corresponding machines are called laser cutters. In addition to cutting, laser cutters are also capable of engraving, which means that the material is not cut through completely, but only processed on the surface, so that, for example, lettering or images can be added to the workpiece.

Workpieces to be cut must not be too thick, usually plates a few millimeters thick are used. Engravings can also be lasered on thicker objects as long as they fit within the height limits of the machine. For example, furniture, kitchen boards or pens with wooden handles can be engraved.

<p align="center">
<img height="350" src="images/1_Laser_cutting_wood.png">
<img height="350" src="images/2_Laser_engraving_wood.png">
</p>

<p align="center">
<a href="#s1">[1]</a> <i> A laser cutter cuts shapes from a wooden sheet (MDF) - </i>
<a href="#s2">[2]</a> <i> Laser engraving in a wooden sheet </i>
</p>


There are a variety of different laser cutters, which differ mainly in size and laser power.

Laser cutters typically found in a fab lab usually have a processing space of about 30 x 20 cm to 70 x 40 cm. For comparison, a DIN A3 (ISO 216) format (typical size of a wood panel for laser cutting) measures approx. 42 x 30 cm, so it fits well in most laser cutters. The power of the laser is usually between 30 and 60 watts. Such laser cutters can be used to cut and engrave, for example, thin sheets of wood, plastic, transparent acrylic, textile, leather or cardboard. For cutting metals (e.g. aluminum or steel), the power of these mid-range devices is usually not enough, but engravings on metal can still be realized with them.

<p align="center">
<img height="350" src="images/3_Fabulaser_Open_Source_Hardware_Laser_cutter.png">
<img height="350" src="images/4_Laser_cutter_fab_lab.png">
</p>

<p align="center">
<a href="#s3">[3]</a> <i> Fabulaser Mini - an open source hardware laser cutter - </i>
<a href="#s4">[4]</a> <i> Laser cutter in a fab lab </i>
</p>


There are also powerful industrial machines capable of cutting metals. However, since these machines are very expensive, you will hardly find them in Fab Labs, but rather in larger companies.

A laser cutter usually requires a digital graphic file as input, which contains all cutting lines and images to be engraved. Cutting lines must be available as vector graphics (more on this below).

Lasercutting can be used, for example, to produce nameplates, pictures, display stands, decorative items or jewelry (e.g. made of wood or plastic). Multi-part products such as storage boxes, small drawers, donation or savings boxes, toys, board games, puzzles or housings for electronic products can also be realized with lasercutting. The particular strength of laser engraving lies in the production of personalized or individual products, e.g. with names, portraits or logos.

<p align="center">
<img height="400" src="images/5_Laser_cut_and_engraved_objects.png">
</p>

<p align="center">
<a href="#s5">[5]</a> <i> Various laser cut and engraved objects </i>
</p>


## Basics

### Materials

Basically, it is very important to clarify before laser cutting whether the material may be processed, as there are substances that can produce life-threatening fumes during laser cutting. More info can be found in the material list below and in the [safety section](#safety).

Here is an overview of some popular and well-suited materials for laser cutting and engraving:

- **Plywood sheet:** Plywood is a cheap and very easy to laser-cut material and well suited for beginners. Panels with thicknesses around 4 millimeters are good to use. When engraving, the inner structure of the wood becomes visible, which often leads to an interesting look. Craft plywood is also popular for sawing and can be purchased at many hardware stores or online. Disadvantages are: It is very light and therefore not very stable and breaks quickly. In addition, the boards are often somewhat uneven. In projects where precision is important (e.g. [push-fit systems](#push-fit-systems)), this can lead to problems - in which case it is advisable to switch to MDF.
- **MDF:** MDF stands for "medium-density fiberboard". MDF consists of fine wood fibers (usually about 80%) plus glue, water and other additives; this mixture is pressed into dense boards. Due to this manufacturing method, MDF boards are heavier and more stable than plywood boards, and they are also very flat and have a uniform thickness. MDF sheets with a thickness of 2 to 5 millimeters can be laser cut and engraved very well. MDF is available in online stores, for example, and is a bit more expensive than plywood.
- **Acrylic glass:** Acrylic glass is a transparent plastic that can be laser cut very well. There are both colorless (fully transparent) and colored (semi-transparent) acrylic glass. This makes it very suitable for viewing windows, decoration, lamps, LED-lit displays and the like. In terms of sustainability, it can be noted that acrylic glass is not well recyclable - unlike some other plastics.
- **Cardboard:** Not all cardboard can be processed equally well with the laser cutter, so you should look for material that is well suited for lasercutting when buying it. Since cardboard is very light and unstable, it is more suitable for decorative products. In addition, cardboard is highly flammable, which is why you should ensure a good ventilation system in the laser cutter, supervise the laser cutting process particularly well and stop it if flames form.
- **Textiles** 
- **Leather** 
- **Cork**
- **Plastics:** Special care is required with plastics, as there are many types of plastic that can generate health- and life-threatening fumes during laser cutting, e.g. PVC. However, there are plastics that can be cut and engraved relatively safely, e.g. polypropylene (PP). But here, too, care should be taken and the project should be discussed with the fab lab or the owner of the machine. Some plastics, e.g. HDPE, tend to melt back together quickly after cutting - so laser cutting of plastic is challenging, but not impossible.
- **Metals:** In industrial and craft companies there are machines that can laser cut metal sheets. Since laser cutters of this type are very expensive, they are rarely found in fab labs. However, a typical fab lab laser cutter can quite possibly engrave metal (e.g. aluminum or steel).

<p align="center">
<img height="350" src="images/6_Laser_cut_and_engraved_acrylic_and_wood.png">
<img height="350" src="images/7_Laser_cut_and_engraved_plywood.png">
</p>

<p align="center">
<a href="#s6">[6]</a> <i> Laser cutting and engraving of acrylic glass and MDF wood sheet - </i>
<a href="#s7">[7]</a> <i> Laser engraving in plywood sheet; different engraving depths make the inner wood structure visible </i>
</p>

<p align="center">
<img height="400" src="images/8_Laser_cutting_metal.png">
</p>

<p align="center">
<a href="#s8">[8]</a> <i> Laser cutting of sheet metal - typical mid-range laser cutters in fab labs can often only engrave metals, but cutting metals requires expensive industrial laser cutters. </i>
</p>




### Components of a laser cutter
Good laser cutters have a closed housing and an ventilation system. There are also inexpensive laser cutters or laser engravers with an open structure. However, special care must be taken with these, as accidents can easily occur. In fab labs, closed laser cutters with an exhaust air system are usually found.

The upper, hinged cover is usually transparent so that you can observe the laser cutting process. Inside is the grid-shaped work surface, on which you place the plate to be cut. The working surface can be adjusted in height, which is very important for the so-called focusing of the laser (setting the focal point). The laser is calibrated so that it must be at a very specific distance from the workpiece in order to cut ideally. Each time you insert a sheet that is a different thickness than the previous sheet, you should refocus the laser cutter. Some laser cutters can do this automatically via an auto-focus function, others require you to use a supplied or built-in focusing aid as a distance gauge to manually adjust the laser cutter.

The laser beam itself is often generated inside the device, redirected via several mirrors and focused via lenses, similar to glasses. The laser exit is built in such a way that it can move in two axes: in the X direction (to the left and right) and in the Y direction (to the front and back).

Some laser cutters have a compressor-driven system that blows air onto the laser cutting point. This reduces the risk of flame formation.

During laser cutting, a ventilation system extracts air from the working area of the unit and leads the exhaust air outside via a filter system and a hose. This prevents unpleasant odors, and filters and discharges harmful vapors.

### Parameters: Power and speed
In laser cutting, there are two parameters in particular that are crucial to the process and must be set correctly before each operation:

- **Power (in watts or %):** In simple terms, power represents the energy or strength of the laser beam.
- **Speed (in millimeters per second):** Indicates how fast the laser moves over the workpiece.

If the laser moves slowly, it has more time to affect the material - it thus cuts deeper into the plate. If it moves quickly, it may only burn off the surface of the workpiece. At the same time, of course, this also depends on the power of the laser. The interaction of power and speed can therefore produce different results.

Depending on what and how you want to laser, you have to set these two parameters differently. So the first thing to do is to clarify the conditions:
- **Material:** Materials such as cardboard require less laser power than wood or plastics, for example.
- **Plate Thickness:** Thicker plates need more laser power to be cut, thinner plates need less power.
- **Cutting vs. engraving and engraving depth**: At high power or low speed, the laser beam passes through the entire material, i.e., it is cut. At low power and high speed, only the surface is processed, resulting in engraving. The depth (and thus visibility or clarity) of the engraving can also be varied via the parameter setting. A kind of grayscale effect can be achieved by deeper and shallower engraving areas.

Often you will find preset profiles in the laser cutter software where you only have to select which material and plate thickness you are using and whether you want to cut or engrave - the ideal values for power and speed are stored in the profiles and are set correctly when selected. In some workshops or operating manuals you can also find tables with recommended values for power and speed.

However, if you want to deviate from this or try out a previously untried material (for which no profile has yet been created), you usually have to carry out several tests, varying the values of power and speed, and thus approaching the ideal result.

Test cards developed for such material tests can also be found on the internet. The laser cutter tests different settings in a single run. The finished lasered test card can then be used to examine the result and read off the ideal values.

<p align="center">
<img height="350" src="images/9_Laser_cutting_test_card.png">
<img height="350" src="images/10_Laser_engraving_test_card.png">
</p>

<p align="center">
<a href="#s9">[9]</a> <i>  - </i>
<a href="#s10">[10]</a> <i> Test cards for determining the correct parameter values for power and speed - for laser cutting and engraving </i>
</p>


### Kerf

When cutting by laser, a small amount of material is burned, vaporized or melted along the cutting line. As a result, cut lines are not "infinitely thin" but have a certain width - the so-called kerf. A cut line can therefore be thought of more like a cutting channel - there is a tiny gap between the two parts.

Even though the cutting width is hardly visible to the naked eye - it is often only a fraction of a millimeter wide - it is important to keep it in mind for some applications. This applies, for example, to push-fit systems (more on this below in the [push-fit systems section](#push-fit-systems)), where a good fit of the pushed-in parts is important.  

To get an idea of the cutting width (kerf), you can measure a laser-cut part or hole with a caliper and compare the measured value with the value in the vector graphic - you will notice that there are slight deviations. Using the difference between the drawn length and the measured length, you can determine the width of the cut (kerf). This value can then be taken into account as the cutting line offset when drawing the vector graphic.

<p align="center">
<img height="300" src="images/11_Laser_cut_designed_vs_measured_length.png">
</p>

<p align="center">
<a href="#s11">[11]</a> <i> In this example, a laser-cut part that was drawn 40 mm wide measures only 39.75 mm - the difference of 0.25 mm results from the cutting width (kerf). Per cut edge it is therefore 0.25 mm : 2 = 0.125 mm here </i>
</p>


### Vector graphic
Für Lasercutting ist es wichtig, sich mit dem Konzept von Vektorgrafiken vertraut zu machen.

Eine Vektorgrafik ist eine Computergrafik, die aus Grundformen wie Linien, Kreisen, Polygonen (mehreckige Formen) und Kurven (Splines) aufgebaut ist. Die digitale Datei einer Vektorgrafik enthält dabei alle notwendigen Informationen, um die Grafik eindeutig darzustellen, z.B. Position und Länge von Linien oder Durchmesser von Kreisen. Zudem können u.a. Strichstärke und Farbe von Linien oder Füllfarbe von Formen gespeichert werden.
Damit unterscheiden sich Vektorgrafiken grundsätzlich von sogenannten Rastergrafiken, die über rasterartig angeordnete, farbige Bildpunkte (Pixel) aufgebaut sind.

Raster- und Vektorgrafiken lassen sich vor allem über zwei Methoden leicht unterscheiden:
- **Qualitätsverlust beim Skalieren (zoomen):**
  - Eine **Rastergrafik** wird beim Vergrößern (hineinzoomen) immer undeutlicher, irgendwann erkennt man einzelne Pixel
  - Eine **Vektorgrafik** hingegen bleibt beim Vergrößern stets scharf, da die Linien und Flächen nicht als Pixel, sondern über das oben beschriebene Verfahren definiert sind
- **Dateiformat:**
  - **Rastergrafiken** haben Dateiformate wie JPG/JPEG, PNG, GIF oder TIFF.
  - **Vektorgrafiken** haben Dateiformate wie SVG, DXF, AI oder unter gewissen Bedingungen auch PDF.

<p align="center">
<img height="300" src="images/12_Vektorgrafik_vs_Rastergrafik.png">
</p>

<p align="center">
<a href="#s12">[12]</a> <i> Vektorgrafiken lassen sich ohne Qualitätsverlust beliebig skalieren - Rastergrafiken hingegen werden beim Skalieren undeutlich und verpixelt. </i>
</p>


Um eine Grafikdatei für Lasercutting verwenden zu können, muss diese in einem Vektorformat vorliegen. Hintergrund ist, dass die Linien und Kurven einer Vektorgrafik über eine Software in Steuersignale für den Lasercutter umgewandelt werden, wobei der Laser jede Linie und Kurve abfährt und laserschneidet. Der Laser "kennt" damit Anfangs- und Endpunkt einer jeden Linie und Kurve und fährt sie in einem Durchlauf ab. Mit pixelbasierten Rastergrafiken wäre dies nicht möglich, da die Software nicht erkennen kann, welche Pixel zu einer Linie gehören.

Für Gravuren hingegen können auch Rastergrafiken verwendet werden. Der Laser fährt dann die Grafik - sozusagen zeilenweise - von oben nach unten ab; jede Zeile von links nach rechts. Dunklere Pixel werden tiefer eingraviert, helle Pixel weniger tief und leere bzw. weiße Pixel werden ausgelassen, also nicht graviert. Es können auch farbige Grafiken verwendet werden, wobei sie von der Software automatisch in Graustufen umgewandelt werden.

Dateiformate wie SVG können auch eine Kombination aus Vektorgrafik und Rastergrafik enthalten, wobei Vektorlinien geschnitten und Rastergrafiken graviert werden - sofern man nicht etwas anderes einstellt.

<p align="center">
<img height="350" src="images/13_Example_svg_file_vector_graphics_for_laser_cutting_and_engraving.png">
<img height="350" src="images/14_Laser_cut_and_engraved_plywood.png">
</p>

<p align="center">
<a href="#s13">[13]</a> <i> Beispiel für eine SVG-Grafikdatei - die schwarzen Konturlinien sind Vektorlinien und werden vom Laser geschnitten, das Katzenbild ist eine PNG-Rastergrafik und wird graviert - </i>
<a href="#s14">[14]</a> <i> Fertiges Ergebnis - erstellt mit Lasercutting und -gravur aus 4 mm dicken Sperrholzplatten </i>
</p>


In manchen Programmen ist es auch möglich, die Reihenfolge der Laserschnitte festzulegen, indem man den Vektorlinien unterschiedliche Farben gibt oder sie auf verschiedene Ebenen legt. Dies kann sinnvoll sein, wenn man z.B. erreichen möchte, dass zuerst die Inneren und zum Schluss die äußersten Linien geschnitten werden. Würde man mit dem äußersten Umriss anfangen, könnte die Platte nach dem Ausschneiden leicht kippen. Die später geschnittenen inneren Linien und Formen könnten dann verzerrt geschnitten werden oder der Laser schneidet gar nicht erst durch die gesamte Platte. Daher empfiehlt es sich, Schnittlinien stets in der Reihenfolge von innen nach außen zu schneiden.

<a name="abb15"></a>

<p align="center">
<img height="400" src="images/15_Example_svg_file_vector_graphics_for_laser_cutting.png">
</p>

<p align="center">
<a href="#s15">[15]</a> <i> In dieser SVG-Vektorgrafik wurden die Schnittlinien in unterschiedlichen Farben erstellt, damit die Schnitte in einer bestimmten Reihenfolge - von innen nach außen - ausgeführt werden können. Die hier vorgesehene Reihenfolge ist: zuerst rote Linien schneiden, dann blaue, schwarze und zuletzt grüne. </i>
</p>


### Software
Zum Zeichnen von Vektorgrafiken gibt es viele unterschiedliche Programme. Meistens wird derartige Software im professionellen Bereich eingesetzt, was die Softwarelizenzen relativ teuer macht. Es gibt aber auch gute kostenlose Alternativen:

Eine beliebte und kostenlose Open-Source-Software für **Vektorgrafikbearbeitung** ist **Inkscape**.

- **Inkscape:** https://inkscape.org

Für das Zeichnen und Erstellen von **Rastergrafiken** gibt es ebenfalls viele, teilweise teure Programme.
Als kostenlose und Open-Source-basierte Alternativen gibt es:

- **Krita:** https://krita.org
- **GIMP:** https://www.gimp.org

Je nach Lasercutter-Hersteller und -Modell benötigt man oft noch eine spezielle Software, die die Vektor- und Rastergrafiken in Steuersignale umwandelt und an den Lasercutter sendet. Diese Software wird üblicherweise mit dem Lasercutter mitgeliefert.

Viele Lasercutter nutzen die kostenlose Open-Source-Software Visicut (https://visicut.org). Beliebt, wenn auch nicht kostenlos, ist auch die Software Lightburn (https://lightburnsoftware.com/). Mit Lightburn können Vektorgrafiken gezeichnet und auch direkt aus der Software heraus an den Lasercutter gesendet werden, zudem verfügt das Programm über zahlreiche Komfortfunktionen speziell für Lasercutting und -gravieren.

### Differences to other digital manufacturing methods
Der wichtigste Unterschied zwischen **Lasercutting und 3D-Druck** ist, dass Lasercutting in der Regel deutlich schneller abläuft als 3D-Druck. 3D-Drucke können oft mehrere Stunden dauern, während Lasercut-Teile oft in wenigen Minuten fertig sind. Je nach Form und Komplexität kann sich dies im Einzelfall aber natürlich auch ganz anders verhalten. Bevor man also ein Teil 3D-druckt, lohnt es sich, zu überlegen, ob man es auch mit Lasercutting realisieren kann, sofern Form und Material dies zulassen (mehr zum Thema im [Basislernmodul 3D-Druck](../2_1_3D_printing/3D-Druck.md)).

<p align="center">
<img height="400" src="images/16_3D_printing_and_laser_cutting_orcuCar_Orcular.png">
</p>

<p align="center">
<a href="#s16">[16]</a> <i> Beispiel für Unterschiede in der Geschwindigkeit bei 3D-Druck vs. Lasercutting: Das 3D-Drucken der Teile (obere zwei Bilder) hat insgesamt ca. 2,5 Stunden gedauert - das Lasercutting (Bild unten links) nur ca. 12 Minuten. </i>
</p>


Auch zwischen **Lasercutting und CNC-Fräsen** gibt es typische Unterschiede. Während beim Lasercutten nur flache Teile in gleichmäßiger Dicke herstellbar sind (sozusagen "2D-Teile"), können mit CNC-Fräsen auch dreidimensionale Formen gefertigt werden. Zudem können Lasercutter nur begrenzt dicke Platten schneiden - je nach Material nur einige Millimeter bis ca. 1-2 Zentimeter Dicke - während mit CNC-Fräsen deutlich dickere Platten durchtrennt werden können. Außerdem können viele CNC-Fräsen auch Aluminium oder ähnlich harte Materialien bearbeiten, was mit Lasercuttern oft nicht möglich ist (mehr zum Thema im [Basislernmodul CNC-Fräsen](../2_3_CNC_milling/CNC-Fraesen.md)).

## Design tips

### Push-fit systems
Eine beliebte Anwendung von Lasercutting besteht in Stecksystemen - vor allem für Holzplatten. Dabei werden mehrere Teile so geformt, dass sie rechtwinklig zueinander gesteckt werden können. Eine Möglichkeit besteht darin, einen Zapfen in ein eckiges Loch zu stecken. Eine andere Methode ist der Einsatz von zinnenartigen Rändern, womit sich ganze Boxen oder ähnliche Strukturen zusammenstecken lassen.

<p align="center">
<img height="300" src="images/17_Laser_cut_box_push-fit_system.png">
<img height="300" src="images/18_Vector_graphics_for_laser_cut_box_push-fit_system.png">
</p>

<p align="center">
<a href="#s17">[17]</a> <i> Beispiel für eine Box mit Schubladen als Stecksystem aus 3 mm dicken, lasergeschnittenen Holzplatten - </i>
<a href="#s18">[18]</a> <i> Eine dazugehörige Vektorgrafik </i>
</p>


Dabei muss sichergestellt werden, dass die Zapfen nicht zu locker stecken, sondern einen festen Sitz haben. Andererseits darf die Lücke auch nicht zu eng sein, da man den Zapfen sonst nicht hineingedrückt bekommt. Hierbei muss auch die Schnittbreite (kerf) berücksichtigt werden.

Eine oft gut funktionierende Daumenregel lautet, dass Lücke und Zapfen in gleichen Dimensionen gezeichnet werden - also die gleiche Breite für Lücke und Zapfen. Die Höhe des Zapfens hingegen ergibt sich durch die Plattendicke, demnach wird die Höhe der Lücke gleich der Plattendicke gezeichnet. Bedingt durch die Schnittbreite (kerf) des Lasers werden Lücken ohnehin etwas weiter und Zapfen etwas schmaler ausfallen als in der Zeichnung, womit der Sitz oft relativ gut ist, manchmal aber etwas zu locker. Man kann die Verbindung auch etwas enger gestalten und die Steckverbindungen vorsichtig mit einem Gummihammer einschlagen. Steckverbindungen können in der Regel auch mehrmals gelöst und wieder zusammengesteckt werden, dabei nutzt sich das Material jedoch jedesmal etwas ab, sodass die Verbindung evtl. nicht mehr fest sitzt. Auch die Verwendung von Klebstoff oder Leim ist möglich.

Bevor man sich die Mühe macht und eine steckbare Box aufwendig selbst zeichnet, empfiehlt es sich, auf bestehende **Software-Hilfsmittel** zurückzugreifen:

- Für Inkscape gibt es die kostenlose Erweiterung [Lasercut tabbed box](https://inkscape.org/de/~Neon22/%E2%98%85lasercut-tabbed-box). Damit lassen sich Länge, Breite und Höhe sowie Zapfenlänge und Schnittbreiten-Versatz (kerf) für verschiedene boxartige Produkte als Vektorgrafik generieren. Diese Vektorgrafik kann auch nachträglich in Inkscape bearbeitet werden.
- Ein weiteres Tool heißt "Boxes.py" (https://www.festi.info/boxes.py/). Hierfür ist keine Softwareinstallation notwendig, die Anwendung läuft im Browser. Dieses Open-Source-Projekt bietet eine Vielzahl von verschiedenen steckbaren Lasercut-Bausätzen, z.B. Kisten, Schubladen, Fächer oder Truhen mit Deckeln. Es können Parameter wie Länge, Breite, Höhe und Schnittbreitenversatz eingegeben werden, abschließend wird eine downloadbare SVG-Vektorgrafik erzeugt, die man direkt für Lasercutting verwenden oder vorher noch bearbeiten kann. Einige Bausätze enthalten auch "living hinges", mehr dazu [unten](#living-hinge).

### 3D CAD and projection
Statt Lasercut-Projekte in 2D zu zeichnen, kann man auch eine 3D-CAD-Software verwenden (mehr dazu im [Basislernmodul 3D-Design und CAD](../1_1_3D_design/3D-Design.md)). Auf diese Weise kann man ein aus mehreren Lasercut-Teilen bestehendes Produkt entwerfen und in 3D darstellen. Vorteil an dieser Methode ist, dass man direkt sehen kann, wie das fertige, zusammengesteckte Produkt aussehen wird - beim Design in 2D sieht man die einzelnen Teile nur nebeneinander und benötigt etwas Vorstellungskraft, um sich ein Bild vom fertigen 3D-Produkt zu machen.

Zudem lassen sich auf diese Weise Produkte entwerfen, die nicht nur Lasercut-Teile, sondern beispielsweise auch 3D-gedruckte oder CNC-gefräste Teile, Schrauben oder andere Elemente enthalten.

Viele CAD-Programme (z.B. FreeCAD) verfügen über Tools, mit denen man die 3D-modellierten Teile für das Lasercutting auf eine 2D-Ebene projizieren und als Vektorgrafik exportieren kann, die man dann für Lasercutting verwenden kann.

<p align="center">
<img height="400" src="images/19_3D_CAD_designed_product_laser_cutting_3D_printing_FreeCAD_orcuCar_Orcular.png">
</p>

<p align="center">
<a href="#s19">[19]</a> <i> In einer 3D-CAD-Software (FreeCAD) modelliertes Spielzeugauto mit 3D-Druck- und Lasercut-Teilen. Letztere können in eine 2D-Vektorgrafik projiziert werden (siehe <a href="#abb15">Abbildung 15</a> oben). </i>
</p>


### Living hinge
Eine beliebte Technik im Lasercut-Design nennt sich "living hinge" (engl. für "Biegescharnier"). Gewöhnliche Scharniere bestehen aus mehreren Bauteilen, Biegescharniere hingegen aus nur einem einzigen Teil, welches an einer oder an mehreren Stellen dünnwandig ausgestaltet oder eng geschnitten ist. Biegescharniere finden sich z.B. bei Eierpappkartons oder bei Brotdosen aus Kunststoff.

Ein living hinge lässt sich mit Lasercutting herstellen, indem viele, sehr eng aneinander liegende und leicht versetzte Schnittlinien in die Platte geschnitten werden. Die Platte wird dadurch sehr flexibel und lässt sich an der Stelle leicht biegen. Dies geht vor allem mit dünnen Holzplatten gut. Man kann es für Scharnierfunktionen, z.B. für Deckel von Truhen, verwenden oder man nutzt es, um abgerundete Kanten zu erzeugen.

<p align="center">
<img height="350" src="images/20_Laser_cut_box_living_hinge.png">
<img height="350" src="images/21_Laser_cut_wood_living_hinge.png">
</p>

<p align="center">
<a href="#s20">[20]</a> <i> Eine zusammengesteckte Box aus lasergeschnittenen Holzteilen mit living hinge. - </i>
<a href="#s21">[21]</a> <i> Durch bestimmte Schnittmuster entsteht ein flexibles living hinge. </i>
</p>


### Downloading templates
Statt eigene Lasercut-Zeichnungen zu entwerfen, kann man auch fertige Vorlagen aus dem Internet verwenden. Viele Portale, die eigentlich eher für 3D-Druck-Dateien gedacht sind, enthalten auch Projekte für Lasercutting. Man findet sie, indem man einfach "laser cut" oder "lasercutting" in die Suchleiste eingibt. Mehr zu dem Thema im [Basislernmodul Verwendung von 3D-Modellen aus dem Internet](../1_3_Using_3D_models_from_the_internet/Verwendung_von_3D_Modellen_aus_dem_Internet.md).

### Common mistakes
Ein häufiger Anfängerfehler beim Erstellen von Lasercut-Vektorgrafiken ist, die Schnittlinien nicht richtig zu formatieren, sodass die Linien graviert und nicht geschnitten werden. Je nach Lasercutter und Software gibt es bestimmte Dinge, die beachtet werden müssen, damit die Software eine Linie als Schnittline erkennt und sie nicht graviert. Es lohnt sich also, vor Start des Lasercuttings die Einstellungen nochmals genau zu prüfen. 

Gelegentlich passiert auch ein Fehler, bei dem der Lasercutter jede Linie zweimal schneidet. Dies liegt meistens daran, dass man doppelte Linien in der Vektorgrafik hat. Da sie jedoch übereinanderliegen, erkennt man es am Bildschirm nicht. Hier sollte man die Tools der Software nutzen, um zu prüfen, ob doppelte Linien vorhanden sind (z.B. Ebenen nacheinander ausblenden oder Linien probeweise löschen, anschließend ggf. rückgängig machen).

Schließlich passiert es auch oft, dass ein fertig geschnittenes Bauteil nicht die gewünschte Größe hat, z.B. nur halb so groß ist, wie gewünscht. Man sollte also die Maße der Vektorgrafik genau prüfen und auch nachschauen, ob die richtigen Einheiten eingestellt sind (z.B. Millimeter und nicht Zoll).

## Preparation and process of a laser cutting

### Safety
Ein Lasercutter ist eine potenziell gefährliche Maschine und sollte niemals ohne Einweisung oder Befugnis benutzt werden. Fab Labs bieten in der Regel Einweisungen in die Sicherheit und Benutzung an, die man absolviert haben muss, bevor man das Gerät benutzen darf.

Bei ordnungsgemäßem Betrieb entsteht keine unmittelbare Gefahr für den Menschen. Falls der Betrieb jedoch nicht ordnungsgemäß verläuft, z.B. wegen Beschädigung des Gehäuses, bei Umbau und Umgehung der Sicherheitstechnik oder durch unübliche Reflexion und Streuung des Laserlichts, kann die Laserstrahlung vor allem für die Augen, aber auch für die Haut sehr gefährlich werden. Die Laserstrahlung eines Lasercutters ist unsichtbar, was die Gefahr noch vergrößert. Bei Unsicherheiten ist besondere Vorsicht geboten. Bei Defekten oder unüblichem Verhalten sollte eine Maschine nicht benutzt und das Fab-Lab-Personal verständigt werden.

Während des Lasercuttings entsteht oft ein hell leuchtender Punkt auf der bearbeiteten Platte. Man sollte es möglichst vermeiden, direkt in dieses helle Licht zu blicken, da es die Augen schädigen kann.

Neben der Gefahr durch Laserstrahlung selbst besteht auch eine Brandgefahr. Es ist wichtig, darauf zu achten, dass während des Laserns die Belüftung eingeschaltet ist und der Filter regelmäßig gewechselt wird, vor allem bei unüblicher Geruchs- oder Rauchbildung.

Ein Lasercutter sollte während des Betriebs nie unbeaufsichtigt gelassen werden. Man sollte stets in der Nähe bleiben und im Blick behalten, ob sich unübliche Flammen bilden. Im Zweifel sollte der Betrieb gestoppt werden. Man sollte wissen, wo sich der Notausschalter des Geräts befindet. Viele Lasercutter sind auch so konstruiert, dass sie beim Öffnen der oberen Abdeckung automatisch den Betrieb stoppen.

Für den unwahrscheinlichen Fall, dass ein Brand entsteht, sollte stets ein CO2-Feuerlöscher verwendet werden. Man sollte den Aufenthaltsort des CO2-Feuerlöschers kennen und sich mit seiner Bedienung vertraut machen.

Schließlich ist es wichtig zu wissen, welche Materialien man lasern darf und welche nicht. Dies ist stets mit dem Personal zu klären. Einige Kunststoffe, z.B. PVC, dürfen auf keinen Fall gelasert werden, da sie dabei gesundheitsgefährdende bis lebensgefährliche Dämpfe erzeugen.

### Laser cut file
Wie in den oberen Abschnitten beschrieben, benötigt man für das Lasercutting eine Grafikdatei - Schnittlinien als Vektorgrafik, Gravuren als Rastergrafik. Wie die Daten an den Lasercutter übertragen werden, ist bei jedem Lasercutter anders. Oft wird eine spezielle Software benötigt. Viele Programme bieten eine Funktion an, die eine Schätzung der Betriebsdauer - aufgeschlüsselt nach Schneiden und Gravieren - berechnet. Bevor man den Betrieb startet, empfiehlt es sich, anhand der Werte zu prüfen, ob der Auftrag wie gewünscht durchgeführt wird. Ist etwa die berechnete Zeitdauer für Gravur unüblich hoch und die Dauer für das Schneiden gleich null, so wurde die Vektorgrafik evtl. nicht erkannt.  

### Preparation
Die wichtigsten Schritte, an die man beim Start eines Lasercutting-Auftrags denken sollte, sind:
- Platte in den Lasercutter legen
- Ggf. Höhe verstellen und fokussieren (oder, falls vorhanden, Autofokus einschalten)
- Laser an die richtige Position fahren
- Richtiges Profil einstellen (Material und Plattendicke - daraus abgeleitet die Leistung und Geschwindigkeit)
- Grafikdatei übertragen
- Zeit berechnen lassen und auf Plausibilität prüfen
- Ggf. prüfen, ob Belüftung eingeschaltet ist
- Laserbetrieb starten
- Aufmerksam sein und in der Nähe bleiben, gelegentlich den Prozess beobachten

Je nach Lasercutter-Modell können manche Schritte von der obigen Liste abweichen.

### Laser cutting process
Üblicherweise beginnt ein Lasercutter zunächst mit den Gravuren. Der Grund liegt darin, dass ein einmal ausgeschnittenes Teil unter Umständen leicht kippen kann - nachträgliche Gravuren würden somit auf eine schräge Oberfläche treffen und nicht korrekt ausgeführt werden.

Anschließend werden die Schnittlinien ausgeführt. Das Schneiden geht für gewöhnlich deutlich schneller als das Gravieren.

Nach abgeschlossenem Lasercutting empfiehlt es sich, noch kurz zu warten, damit die Belüftungsanlage Rauch und Dämpfe absaugen kann. Danach kann die Klappe geöffnet und die Teile können entnommen werden.
Falls ein Schnitt nicht richtig durchgegangen ist, liegt dies entweder an einem falsch eingestellten Profil (falsche Parametereinstellungen), an einer Unebenheit der Platte oder an anderen Ursachen. Oft kann es helfen, einen Lasercut-Auftrag einfach ein zweites Mal auszuführen, sodass die halbfertigen Schnitte beim erneuten Durchgang ganz durchgeschnitten werden. Dabei muss die Platte exakt an die gleiche Position gelegt werden (möglichst mit Hilfe des Anschlags am Rand) oder gleich liegen gelassen werden. Es ist auch möglich, direkt am Computer einzustellen, dass der Laser zwei Durchgänge schneiden soll.

# License information

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Image references

<a name="s1"></a>
**[1]** CC BY-SA 3.0Laser cutting: Epilog Legend 36EXT cutting 2.5mm wood fibreboard - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Laser_cutting_snowflakes.jpg

<a name="s2"></a>
**[2]** (no title) - **Image license:** [Unsplash Lizenz](https://unsplash.com/de/lizenz) - **Source:** https://unsplash.com/de/fotos/k3CN3UUrCxE

<a name="s3"></a>
**[3]** mini_banner.jpg (cropped) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://github.com/fab-machines/Fabulaser-Mini

<a name="s4"></a>
**[4]** Lasercutter in einem Fab Lab - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s5"></a>
**[5]** Verschiedene lasergeschnittene und -gravierte Objekte - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s6"></a>
**[6]** Laser cut letter - Acrylic and MDF (cropped) - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) - **Source:** https://www.flickr.com/photos/creative_tools/6981296223

<a name="s7"></a>
**[7]** Lasergravur in Sperrholzplatte - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s8"></a>
**[8]** Laser cutting machine - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Laser_cutting_machine.jpg

<a name="s9"></a>
**[9]** CO2 Laser Test Cut and Engraving Template (cropped) - **Image license:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - **Source:** https://www.thingiverse.com/thing:4575909

<a name="s10"></a>
**[10]** CO2 Laser Test Cut and Engraving Template (cropped) - **Image license:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - **Source:** https://www.thingiverse.com/thing:4575909

<a name="s11"></a>
**[11]** (no title) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - [License info for fabacademy.org](https://fabacademy.org/terms-of-service.html)  - **Source:** https://fabacademy.org/2018/labs/fablabamsterdam/lasercut/group3.html

<a name="s12"></a>
**[12]** Vektorgrafik vs. Rastergrafik - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org) **Adapted/Remixed from:** 1.) https://de.wikipedia.org/wiki/Vektorgrafik 2.) https://de.wikipedia.org/wiki/Datei:Zeichen_224_-_Haltestelle,_StVO_2017.svg , 3.) https://de.wikipedia.org/wiki/Datei:Zeichen_224_20px.png **Licenses:** 1.) [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) , 2.) [Public domain](https://creativecommons.org/publicdomain/zero/1.0/) , 3.) [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.en)

<a name="s13"></a>
**[13]** Cats (Tipu & Dr. Scott) Lasercutting SVG-Datei - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s14"></a>
**[14]** Cats (Tipu & Dr. Scott) Lasercutting Aufsteller - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s15"></a>
**[15]** orcuCar Lasercut SVG file - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s16"></a>
**[16]** orcuCar - 3D-Druck vs. Lasercutting - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s17"></a>
**[17]** PartBox 3mm wood - **Image license:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - **Source:** https://www.thingiverse.com/thing:1279926

<a name="s18"></a>
**[18]** PartBox 3mm wood - **Image license:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - **Source:** https://www.thingiverse.com/thing:1279926

<a name="s19"></a>
**[19]** orcuCar CAD (FreeCAD) + 3D printing + laser cutting - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s20"></a>
**[20]** KERF PURSE - **Image license:** [CC BY-NC-ND 2.0](https://creativecommons.org/licenses/by-nc-nd/2.0/) - **Source:** https://www.flickr.com/photos/augustlang/27519342320/

<a name="s21"></a>
**[21]** Parametric Flexible Wood Cut (cropped) - **Image license:** [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) - **Source:** https://www.thingiverse.com/thing:461749

