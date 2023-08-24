**Translation note:**

This article is still being translated into **English**.

To do:
- Edit file
- Replace text by English translation
- Commit changes
- When done, remove this note

> Back to [basic learning modules overview](../../translations/EN_Readme.md)

# CNC milling

## Contents

1. [Introduction](#introduction)
2. [Basics](#basics)
   - [Materials](#materials)
   - [Types of CNC milling machines](#types-of-cnc-milling-machines)
   - [Components of a CNC milling machine](#components-of-a-CNC-milling-machine)
   - [CAM](#cam)
3. [Parameters and settings](#parameters-and-settings)
   - [Milling tool shapes](#milling-tool-shapes)
   - [Main parameters](#main-parameters)
   - [Milling tool diameter](#milling-tool-diameter)
   - [Determination of spindle speed, feed rate and cutting depth](#determination-of-spindle-speed-feed-rate-and-cutting-depth)
   - [Safety height](#safety-height)
   - [Operation types](#operation-types)
   - [Holding tags](#holding-tags)
4. [Preparation and procedure of a CNC milling job](#preparation-and-procedure-of-a-cnc-milling-job)
   - [Safety](#safety)
   - [CAM, simulation, G-code file](#cam-simulation-g-code-file)
   - [Workpiece](#workpiece)
   - [Set zero point](#set-zero-point)
   - [CNC milling process](#cnc-milling-process)
   - [Post-processing](#post-processing)

[License information](#license-information)

[Image references](#image-references)

## Introduction

Milling is a manufacturing process in which a rapidly rotating milling tool (also called a milling cutter) moves through a workpiece - e.g. a wooden board or a metal block - and removes material in the form of swarf (or chips). In this way, different shapes and components can be manufactured.

<p align="center">
<img height="350" src="images/1_Milling_cutter.png">
<img height="350" src="images/2_CNC_milling.png">
</p>


<p align="center">
<a href="#s1">[1]</a> <i> Milling tools - </i>
<a href="#s2">[2]</a> <i> A milling machine in use - chips removed can be seen on the right of the picture </i>
</p>

<p align="center">
<img height="350" src="images/3_CNC_milling_aluminium.png">
</p>


<p align="center">
<a href="#s3">[3]</a> <i> CNC milling of aluminum </i>
</p>



The classic application is with milling machines, where the axis of rotation of the milling tool is rotated by an electric motor, while the movement of the cutter in space is performed by manual control with cranks or electrically controlled at the touch of buttons.

When a milling machine is combined with a CNC (Computerized Numerical Control, sometimes just called "NC"), it is called a CNC milling machine - or often simply a "CNC mill" or CNC router. In this process, CNC code is first generated on the computer, either through human-written code or with the help of 3D CAD models and CAD/CAM software (more on this below). This NC code is then transferred to the machine, which executes all movements fully automatically according to the instructions in the program and produces the part.

<p align="center">
<img height="250" src="images/4_CNC_milling_machine.png">
<img height="250" src="images/5_Open_Source_Hardware_CNC_milling_machine.png">
<img height="250" src="images/6_CNC_milling_machine_fab_lab.png">
</p>

<p align="center">
<a href="#s4">[4]</a> <i> CNC milling machine (open-source hardware) - </i>
<a href="#s5">[5]</a> <i> Small desktop CNC milling machine (open-source hardware) - </i>
<a href="#s6">[6]</a> <i> CNC milling machine in a fab lab (click images to enlarge)</i>
</p>


In addition to CNC mills, there are also other CNC machines, e.g. CNC lathes (for CNC turning). In these basic learning modules, however, the focus is on machines that are typically used in fab labs, these include CNC milling machines in particular.

Compared to other typical digital manufacturing methods in fab labs, such as 3D printing or laser cutting, CNC milling is significantly more demanding and challenging. This is primarily due to the fact that a lot of preparation is required, especially on the software side, since a complex CAM program (more on this [below](#cam)) must first be modeled, in which all CNC operations and steps are defined individually. This requires some prior knowledge and is usually a bit more time-consuming than the preparation of 3D printing or laser cutting. In addition, you have to define parameters such as spindle speed and feed rate, for this you have to be familiar with materials and milling tools and often you have to calculate something. There is a lot to learn about CNC milling. In this basic learning module, however, only the most important basics are dealt with, which are important for the beginning in the hobby and fab lab area.

The advantage of CNC milling over 3D printing and lasercutting is that you can also machine metals, such as aluminum or, depending on the machine, even steel. In addition, significantly thicker wood boards can be machined than with lasercutting. In contrast to lasercutting, not only flat, plate-shaped objects are possible, but also three-dimensional shapes.

## Basics

### Materials

CNC milling machines in fab labs are mainly used to machine wood. Depending on the machine, aluminum or steel are also possible. Plastics offer another possibility, e.g. sheets of recycled plastic.

<p align="center">
<img height="350" src="images/7_CNC_milled_wood_parts_box.png">
<img height="350" src="images/8_CNC_milling_metal.png">
</p>


<p align="center">
<a href="#s7">[7]</a> <i> Wood can be well processed with CNC milling, for example, for parts of boxes or furniture. - </i>
<a href="#s8">[8]</a> <i> Some CNC milling machines can also machine aluminum or even steel. </i>
</p>

<p align="center">
<img height="300" src="images/9_CNC_milling_recycled_plastic_Precious_Plastic.png">
<img height="300" src="images/10_CNC_milling_recycled_plastic_Precious_Plastic.png">
</p>


<p align="center">
<a href="#s9">[9]</a> <i>  - </i>
<a href="#s10">[10]</a> <i> Many plastics can be CNC milled - here, for example, a "Precious Plastic" sheet made from recycled HDPE </i>
</p>



### Types of CNC milling machines

The most common CNC milling machine variant in fab labs is the 3-axis portal milling machine. In portal milling machines, the milling head is guided on a crossbeam between two uprights. The workpiece, e.g. a plate, lies on a horizontal surface and is screwed or clamped there. The milling tool always points vertically downwards and can be moved in three spatial axes: X-, Y- and Z-axis - hence the name "3-axis milling machine". The Z-axis usually refers to the vertical axis, i.e. the movement up and down.

CNC milling machines were originally developed for industry and craft businesses and are relatively expensive. Some fab labs nevertheless have such expensive industrial machines, while others tend to use inexpensive hobby machines, of which there are now also many. There are also kits and instructions for building your own CNC milling machines. This often involves using a hand-held router and adding moving axes and a CNC control.

In addition to 3-axis milling machines, there are also 4- and 5-axis milling machines. In addition to the three linear movement axes, one or two rotary axes are added. This is realized either by allowing the milling tool to rotate around the workpiece or by rotating the clamped workpiece - depending on the design of the machine. In this way, the milling machine can also work from the side or at an angle into the workpiece - making significantly more complex shapes possible. However, 4- and 5-axis milling machines of this type are more likely to be found in industry than in fab labs.

<p align="center">
<img height="400" src="images/11_5-axis_CNC_machine.png">
</p>


<p align="center">
<a href="#s11">[11]</a> <i> A 5-axis CNC milling machine - The milling tool can move in three linear axes and additionally rotate around two axes - thus it is also possible to mill from the side and at an angle into the workpiece, making it possible to produce much more complex shapes than with 3-axis machines. </i>
</p>


A special project in the area of fab lab and maker communities is the Maslow CNC milling machine. The Maslow CNC is a project based on open-source hardware and software. Its unique feature is its design: The plate to be machined is not flat and horizontal, but almost vertical, slightly angled. This makes the machine particularly space-saving. A manually operated router is used as the centerpiece. This sits in a housing that hangs on two chains that are lengthened and shortened under motor control, allowing the router to move left, right, up and down across the slab. In addition, the Z-direction of the router is controlled, i.e. the vertical plunge into the slab.

<p align="center">
<img height="350" src="images/12_Maslow_CNC_machine.png">
<img height="350" src="images/13_CNC_milling_recycled_plastic_Precious_Plastic_Maslow_CNC.png">
</p>


<p align="center">
<a href="#s12">[12]</a> <i> The Maslow CNC machine stands slightly inclined, almost vertically, which makes it very space-saving. A router, which can actually be used for manual operation, hangs on two chains that are lengthened and shortened via motors - this controls the movement of the router. - </i>
<a href="#s13">[13]</a> <i> In addition to wood, it is also possible to process plastic, for example (here: a "Precious Plastic" recycled plastic sheet). </i>
</p>




### Components of a CNC milling machine

The most important components are the milling tool with motor-driven spindle, the guided and motor-controlled axes and the CNC control, whose functions have already been explained above.

A so-called sacrificial plate made of wood or plastic is often attached as a base on the milling table for CNC milling. The reason is that the milling cutter often has to mill a little deeper than the lower edge of the workpiece in order to mill the part out of the workpiece block. In doing so, the tool mills a little bit into the sacrificial plate. The sacrificial plate has to be replaced after some time, since the workpieces eventually no longer lie completely flat but crooked due to the many grooves and can therefore no longer be machined accurately.

Some CNC milling machines have an extraction system. Here, the chips are extracted directly at the workpiece and transported via a hose into a container. If such an extraction system is missing, the work surface must be regularly cleaned of chips, e.g. with a vacuum cleaner.

More professional CNC milling machines have a device that sprays lubricant and coolant onto the milling tool. This is especially important when milling metals.

<p align="center">
<img height="400" src="images/14_Cutting_fluid_CNC_milling.png">
</p>


<p align="center">
<a href="#s14">[14]</a> <i> Supply of cooling lubricant during milling through a ball joint hose  </i>
</p>


### CAM

Before the actual CNC milling, a digital control code must first be created that "tells" the machine what to do.
The beginning of this takes place in CAD/CAM software. CAD stands for Computer Aided Design. CAD software can therefore be used to design 3D models of components or objects (more on this in the [3D design and CAD basic learning module](../1_1_3D_design/EN_3D_design.md)).

Next, CAM is carried out on the basis of a 3D CAD model. CAM stands for "Computer Aided Manufacturing". CAM software exists as stand-alone programs, but is often integrated as a module in a CAD program - this is then referred to as CAD/CAM software.

In CAM, various CNC operations are defined on the basis of a CAD model, e.g. pockets, profiles or bores (drilled holes). In addition, important parameters such as spindle speed and feed rate are entered. Details on all these terms can be found in the next sections.

In the [3D design and CAD basic learning module](../1_1_3D_design/EN_3D_design.md), the two software solutions FreeCAD and Autodesk Fusion 360 are presented - both programs are CAD/CAM software, so they can be used both to model parts and to prepare CNC milling of these parts.

<p align="center">
<img height="400" src="images/15_CAM_in_FreeCAD_Path_workbench.png">
</p>


<p align="center">
<a href="#s15">[15]</a> <i> CAM in FreeCAD software: The red and green lines show the paths that the milling tool is to take - this is how the component shown here is created from a solid block of material. </i>
</p>




## Parameters and settings


### Milling tool shapes
Milling tools come in many different shapes, for different applications. The most common form, and the one most often used in the fab lab sector, is the end mill. The shank is the part of the tool that has no cutting edges and is clamped into the machine.

<p align="center">
<img height="400" src="images/16_Milling_cutter.png">
</p>


<p align="center">
<a href="#s16">[16]</a> <i> Different milling tools: On the bottom right, a radius end mill with rounding at the tip. The top view on the left clearly shows the number of teeth or cutting edges: a double-edged milling tool at the top and a four-edged milling tool at the bottom. </i>
</p>


### Main parameters

The most important characteristic values and parameters in CNC milling are:

- **Milling diameter (in millimeters, mm):** the diameter of the milling tool.
- **Speed (in revolutions per minute, rpm):** the speed at which the milling tool rotates (spindle speed).
- **Feed rate (in millimeters per minute, mm/min):** the speed at which the milling tool moves in the horizontal direction.
- **Depth of cut (in millimeters, mm):** As a rule, this describes the depth to which the milling tool plunges into the material per pass.

There are many other adjustable parameters, but these four are the most important and decisive ones. The individual parameters will be discussed in more detail in the following sections.

<p align="center">
<img height="400" src="images/17_EN_CNC_milling_parameters.png">
</p>


<p align="center">
<a href="#s17">[17]</a> <i> The most important parameters in milling. </i>
</p>

<p align="center">
<img height="250" src="images/18_CAM_in_FreeCAD_Path_workbench.png">
<img height="250" src="images/19_CAM_in_FreeCAD_Path_workbench.png">
</p>


<p align="center">
<a href="#s18">[18]</a> <i> Path (green) for milling a pocket in the FreeCAD CAD/CAM software. - </i>
<a href="#s19">[19]</a> <i> The same model in side view: Based on the green path lines, you can see the depth of cut - here it is 0.3 mm, the depth of the pocket is 2 mm. </i>
</p>



### Milling tool diameter
Milling tools come in different diameters - usually between three and ten millimeters for fab lab machines. For each milling project, one must either decide on a milling diameter or divide the CNC project into several sections with different diameters. In this case, the milling tool must be changed during the process, usually by hand. Some professional machines can also change tools autonomously without the need for a person to intervene.

The larger the milling diameter, the more material is removed per time, thus the faster the production runs. At the same time, a milling diameter cannot be larger than the smallest pocket (a depression in the material) to be milled. It is therefore necessary to select the milling cutter as large as possible, but as small as necessary.

### Determination of spindle speed, feed rate and cutting depth

The parameter settings are very important, as too high or too low speeds or feed rates can lead to unclean results or, in the worst case, damage to the machine.

Once you have selected your milling diameter and know the material of the workpiece to be milled, you can calculate the other parameters. Tables and formulas can be found in reference books and on the Internet (for example [here](https://www.sorotec.de/webshop/Datenblaetter/fraeser/schnittwerte.pdf) - only available in German), and they are also usually found on site in the workshop or fab lab. The calculated values for speed and feed can be entered into the CAM program. To a certain extent, it is also possible to deviate from the values, i.e. the calculated values are only used as a guide value, but you should be well versed in this.

For the cutting depth, it is often assumed as a guideline that it should be no more than the milling diameter. To be on the safe side, cutting depths smaller than the milling diameter are recommended, e.g. half the diameter. This is especially important when milling metals. The reason for this is that the milling tool cuts more material per time at a greater plunge depth, which puts a lot of stress on the tool and workpiece and can lead to unclean results or damage. In addition, milling tools are optimized by their shape for milling, i.e. cutting across the tool axis. They can also drill a bit, meaning they can work in the direction of the axis, but their shape makes them less suitable for this. Therefore, plunging should rather be done in small steps and the entire surface to be removed should be milled first after each plunge.


### Safety height

Es gibt bestimmte Bereiche, in denen das Fräswerkzeug mit einer anderen Geschwindigkeit fährt als in anderen. Oberhalb der Sicherheitshöhe fährt der Fräser relativ schnell, sobald er an der zu fräsenden Stelle am Werkstück angekommen ist, senkt er sich langsam ab und fährt ab da nur noch mit verringerter Geschwindigkeit. Während des Fräsens im Werkstück bewegt er sich mit der Vorschubgeschwindigkeit. Hintergrund ist, dass ein Fräswerkzeug, dass mit sehr hoher Geschwindigkeit in das Material taucht, beschädigt werden oder sogar abbrechen kann, daher müssen die Bewegungen unterhalb der Sicherheitshöhe deutlich langsamer ablaufen als darüber.

Ab welcher Höhe die Sicherheitshöhe beginnt und mit welcher Geschwindigkeit sich der Fräser oberhalb dieser Höhe bewegen soll, kann in der CAM-Software eingestellt werden.

<p align="center">
<img height="400" src="images/20_FreeCAD_Path_workbench_Visual_reference_for_Depth_properties.png">
</p>


<p align="center">
<a href="#s20">[20]</a> <i> Sicherheitshöhe und einige weitere Parameter, wie sie in der CAD/CAM-Software FreeCAD verwendet werden. Oberhalb der Sicherheitshöhe bewegt sich das Fräswerkzeug ("tool" im Bild) mit erhöhter Geschwindigkeit. Mit "step down" ist hier die Schnitttiefe bezeichnet (mehr zu CAM in FreeCAD: https://wiki.freecad.org/Path_Workbench ). </i>
</p>



### Operation types

Es gibt viele unterschiedliche Bearbeitungsarten, die man in CAM-Systemen als eine sogenannte Operation anlegen kann. Die wichtigsten sind:

- **Profil:** Das Fräswerkzeug fährt die äußere Kontur des zu fertigenden Teils ab, beginnend auf der Oberfläche des Werkstücks. Danach geht es schrittweise - jeweils um die Schnitttiefe - in das Material hinein und fährt das Profil erneut ab. Am Ende ist das Teil nahezu vollständig vom Werkstückblock getrennt und kann entnommen werden. Wichtig ist hier, Haltestege mit einzuplanen - mehr dazu im nächsten Abschnitt.
- **Tasche:** Eine Tasche stellt eine Vertiefung im Material dar. Ähnlich wie beim Profilfräsen beginnt der Fräsvorgang an der Oberfläche und geht dann schrittweise herunter, je Durchgang um die Schnitttiefe.
- **Bohrung:** Bohrungen, also kreisrunde Löcher, können mit Bohr- oder Fräswerkzeugen gefertigt werden. Spannt man ein Bohrwerkzeug ein und stellt die CAM-Operation entsprechend als Bohrung ein, wird der Bohrvorgang senkrecht ausgeführt, wie bei einer Bohrmaschine. Verwendet man hingegen ein Fräswerkzeug, ist es wichtig, dass der Fräsdurchmesser kleiner als der Bohrdurchmesser ist und das Fräswerkzeug nicht in einem Durchgang vollständig in das Material geht - ein Fräser sollte nicht zum Bohren verwendet werden. Stattdessen empfiehlt es sich, eine Helixform als Pfad zu verwenden. Alternativ kann eine Operation vom Typ "Tasche" erstellt werden,  sodass stufenweise Kreisflächen gefräst werden - je Stufe um eine Zuschnitttiefe weiter - und somit praktisch eine Bohrung gefräst wird.

Operationen werden in der CAD/CAM-Software als Pfade (engl. "Path") angelegt und sichtbar gemacht. Anhand der visualisierten Pfade kann man bereits erkennen, welchen Weg das Fräswerkzeug nehmen wird.

<p align="center">
<img height="350" src="images/21_FreeCAD_Path_workbench_Profile_operation.png">
<img height="350" src="images/22_FreeCAD_Path_workbench_Pocket_operation.png">
</p>


<p align="center">
<a href="#s21">[21]</a> <i> CAM-Operation "Profil": entlang des grünen Pfades wird die äußere Kontur des Bauteils gefräst. - </i>
<a href="#s22">[22]</a> <i> CAM-Operation "Tasche": Eine Vertiefung im Material, dessen Hohlraum durch den Fräser vollständig entfernt wird, bis der Boden der Tasche (grün) erreicht wird. </i>
</p>

<p align="center">
<img height="350" src="images/23_FreeCAD_Path_workbench_with_holding_tags.png">
<img height="350" src="images/24_FreeCAD_Path_workbench_Helix_operation.png">
</p>


<p align="center">
<a href="#s23">[23]</a> <i> Bauteil in der Software FreeCAD mit mehreren CAM-Operationen (grüne und rote Pfade): Außenkontur und innere Kreiskontur als "Profil" mit Haltestegen, die vier kleinen Bohrungen als "Taschen". - </i>
<a href="#s24">[24]</a> <i> Nahansicht einer Bohrung des Bauteils: Die Bohrung wird hier nicht als Bohr-Operation, sondern als gefräste Tasche ausgeführt. Der Pfad hat eine Helixform, um das Material langsam und damit schonend für das Fräswerkzeug zu bearbeiten. (Bilder anklicken zum Vergrößern) </i>
</p>



### Holding tags

Wird ein Teil vollständig vom Werkstück getrennt, also ein Profil oder eine äußere Kontur gefräst, sollte man sogenannte Haltestege mit einplanen. Andernfalls könnte sich das gefertigte Teil im letzten Fräsvorgang verdrehen, kippen und mit dem Fräswerkzeug verkeilen. Die Folgen wären, dass das Teil nicht richtig gefertigt wird, im schlimmsten Fall droht ein Schaden an der Maschine.

Haltestege lassen sich im CAM-System einstellen. Im Endergebnis befinden sich die Haltestege am untersten Ende des Werkstücks und sind relativ schmal und flach, sodass sie sich leicht durchtrennen lassen.

<p align="center">
<img height="400" src="images/25_FreeCAD_Path_workbench_simulation_with_holding_tags.png">
<img height="400" src="images/26_FreeCAD_Path_workbench_simulation_with_holding_tags.png">
</p>


<p align="center">
<a href="#s25">[25]</a> <i>  - </i>
<a href="#s26">[26]</a> <i> Haltestege (gelb) in der CAM-Simulationsansicht von FreeCAD </i>
</p>

<p align="center">
<img height="350" src="images/27_Holding_tags_CNC_milled_aluminium.png">
<img height="350" src="images/28_Holding_tags_CNC_milled_wood.png">
</p>


<p align="center">
<a href="#s27">[27]</a> <i> Haltestege in einem CNC-gefrästen Aluminium-Teil. Im linken Bereich ist ein Haltesteg gut sichtbar; rechts sind einige Spanreste, da der Fräser im letzten Schritt nicht tief genug gegangen ist. - </i>
<a href="#s28">[28]</a> <i> Haltestege in einem Holzbrett, gefräst mit einer Maslow-CNC. (Bilder anklicken zum Vergrößern)</i>
</p>



Das Fräswerkzeug nimmt im untersten Bereich des zu fräsenden Profils einen Pfad, bei dem es vor den Stellen, wo die Haltestege vorgesehen sind, ein Stück hochfährt und diesen Teil ausspart, womit die Haltestege übrig bleiben.

Größe und Anzahl der Haltestege sollten so gewählt werden, dass sie das Teil sicher halten können, ansonsten sollten sie so klein wie möglich entworfen werden, damit man sie leicht durchtrennen kann.

Nach abgeschlossenem Fräsvorgang können die Haltestege je nach Material mit unterschiedlichen Methoden durchtrennt werden. Bei Holz kann beispielsweise eine Säge verwendet werden, bei Aluminium funktioniert es mit einer Metallsäge oder auch mit Hammer und Meißel gut. Nach dem Trennen sollten die Säge- oder Bruchstellen mit einer Feile nachbearbeitet werden.



## Preparation and procedure of a CNC milling job

### Safety

CNC-Maschinen sind potenziell gefährliche Maschinen und sollten nie ohne Einweisung und Freigabe benutzt werden. Fab Labs bieten in der Regel eine verpflichtende Sicherheitseinweisung an. Die Einzelheiten hierzu sind bei jeder Maschine anders, daher erfolgt in diesem Basislernmodul keine genauere Beschreibung.

### CAM, simulation, G-code file

Ein relativ großer Aufwand beim CNC-Fräsen steckt in der Vorbereitung mit der CAM-Software. Hat man alle Operationen und CAM-Pfade definiert, sollte eine Simulation durchgeführt werden. Die meisten CAM-Programme verfügen über eine Simulationsfunktion, bei der der vollständige Fräsvorgang dargestellt wird, ähnlich wie bei einem Video, wobei man während der Simulation die 3D-Ansicht frei drehen kann.

<p align="center">
<img height="350" src="images/29_FreeCAD_Path_workbench_CAM_simulation.png">
</p>


<p align="center">
<a href="#s29">[29]</a> <i> CAM-Simulationsmodus in FreeCAD: Die grünen und roten Pfade zeigen den Verlaufsweg des Fräswerkzeugs (grau). Zu Beginn der Simulation ist ein massiver, dunkelroter Block zu sehen; während der Simulation kann man beobachten, wie der Fräser (grau) Material entfernt, wodurch die gelben Flächen entstehen. In dieser Momentaufnahme ist das äußere Profil bereits fertig, die Tasche ist gerade mitten in der Bearbeitung. </i>
</p>


Die Simulation kann auch in erhöhter Geschwindigkeit abgespielt werden. Während der Simulation wird sichtbar, wann an welcher Stelle Material abgetragen wird und wie das fertige Teil am Ende aussieht. Fallen noch Fehler auf, kann das CAM-Programm noch nachbearbeitet werden und man spart sich teure Fehler in der Fertigung.

Abschließend muss das CAM-Programm mithilfe eines Post-Prozessors (üblicherweise in der Software eingebaut) als eine G-Code-Datei exportiert werden. G-Codes beim CNC-Fräsen basieren auf dem gleichen Prinzip wie G-Codes beim 3D-Druck - mehr dazu in dem [Basislernmodul zu 3D-Druck](../2_1_3D_printing/3D-Druck.md), im Abschnitt [G-Code](../2_1_3D_printing/3D-Druck.md#g-code).

### Workpiece

Das Werkstück, beispielsweise eine Holzplatte oder ein Metallblock, muss sicher am Frästisch befestigt werden. In den meisten Fällen kann das Werkstück mit einigen Schrauben einfach an die Opferplatte geschraubt werden, vorzugsweise mit Senkkopfschrauben, um die Gefahr von Kollisionen mit dem Fräswerkzeug zu verringern. Dennoch sollte man stets aufpassen, dass die Maschine nicht in die Schraube hineinfräst.

Eine weitere Möglichkeit besteht darin, das Werkstück einzuspannen, sofern die CNC-Fräsmaschine über eine Spannvorrichtung verfügt.

### Set zero point

CNC-Maschinen können über Pfeiltasten - je nach Modell am Gerät selbst oder über die Tastatur eines angeschlossenen Computers - gesteuert werden. Dies kann man beispielsweise zum Anfahren des Nullpunkts nutzen.

Der Maschine muss mitgeteilt werden, wo sie mit dem Fräsauftrag beginnen soll, man muss also den sogenannten Nullpunkt definieren. Hierfür gibt es unterschiedliche Methoden, z.B. durch das Anfahren des Nullpunkts an der Werkstückoberfläche bei drehender Spindel (sogenanntes "Ankratzen"). An dieser Stelle wird über die Bedienung der CNC-Fräse der Nullpunkt gesetzt. Die Maschine speichert also die X-, Y- und Z-Koordinaten dieses Punktes ab und wird das CNC-Programm an diesem Punkt starten.

### CNC milling process

Ist der Nullpunkt gesetzt, muss zu Beginn eines CNC-Auftrags die G-Code-Datei über eine Steuersoftware an die CNC-Steuerung der Maschine übergeben und der Betrieb gestartet werden. Während des Fräsens sollte man stets in der Nähe bleiben und bei ungewöhnlichem Verhalten oder drohenden Schäden den Fräsvorgang stoppen - über die Steuersoftware oder über den Notausschalter.

### Post-processing

Nach abgeschlossener Fertigung kann das Werkstück bzw. das gefertigte Teil entnommen werden. Vor allem bei Metallteilen sollte man vorsichtig sein, da wegen der scharfen Kanten Verletzungsgefahr besteht. Die Kanten sollten entgratet und gefeilt werden, zudem können Oberflächen geschliffen werden.

# License information

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Image references

<a name="s1"></a>
**[1]** fräser-schaftfräser-fräsen-3203969 (cropped) - **Image license:** [Pixabay Inhaltslizenz](https://pixabay.com/de/service/terms/) - **Source:** https://pixabay.com/de/photos/fr%C3%A4ser-schaftfr%C3%A4ser-fr%C3%A4sen-3203969/

<a name="s2"></a>
**[2]** Milling Cutter Engaged (cropped) - **Image license:** [CC0 Public Domain](https://creativecommons.org/publicdomain/zero/1.0/) - **Source:** https://www.publicdomainpictures.net/en/view-image.php?image=146351&picture=milling-cutter-engaged

<a name="s3"></a>
**[3]** CNC-Fräsen von Aluminium - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s4"></a>
**[4]** Open Source CNC Milling machine - Large version - Open Lab Starter Kit - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://github.com/Open-Lab-Starter-Kit/OLSK-Large-CNC

<a name="s5"></a>
**[5]** Open Source CNC Milling machine - Small version - Open Lab Starter Kit - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://github.com/Open-Lab-Starter-Kit/OLSK-Small-CNC

<a name="s6"></a>
**[6]** CNC-Fräsmaschine in einem Fab Lab - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s7"></a>
**[7]** Plywood CNC Box (cropped) - **Image license:** [CC BY-NC-SA 2.0](https://creativecommons.org/licenses/by-nc-sa/2.0/) - **Source:** https://www.flickr.com/photos/phidauex/4480597010

<a name="s8"></a>
**[8]** CNC Machining aluminum billet with Tormach (cropped) - **Image license:** [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) - **Source:** https://www.flickr.com/photos/zombieite/10339203625

<a name="s9"></a>
**[9]** CNC milling Precious Plastic (recycled HDPE) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s10"></a>
**[10]** CNC milling Precious Plastic (recycled HDPE) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s11"></a>
**[11]**  5 Achs Bearbeitung (Attribution: HELLER) - **Image license:** [CC BY-SA 3.0 DE](https://creativecommons.org/licenses/by-sa/3.0/de/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:Machining_5-axis.jpg

<a name="s12"></a>
**[12]** Bar and Maslow CNC - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:Bar_and_Maslow_CNC.jpg

<a name="s13"></a>
**[13]** Maslow CNC + Precious Plastic sheet - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s14"></a>
**[14]** Kühlschmiermittel beim Fräsen - **Image license:** [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/deed.de) - **Source:** https://commons.wikimedia.org/wiki/File:Makino-S33-MachiningCenter-example.jpg?uselang=de

<a name="s15"></a>
**[15]** Pathwb.png - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Pathwb.png

<a name="s16"></a>
**[16]** MillingCutterSlotEndMillBallnose.jpg (cropped) - **Image license:** [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/deed.en) - **Source:** https://commons.wikimedia.org/wiki/File:MillingCutterSlotEndMillBallnose.jpg

<a name="s17"></a>
**[17]** Die wichtigsten Parameter beim Fräsen (modelliert in FreeCAD, Bildbearbeitung mit Krita) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s18"></a>
**[18]** CNC milling pocket in FreeCAD Path Workbench - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s19"></a>
**[19]** CNC milling pocket in FreeCAD Path Workbench - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s20"></a>
**[20]** Path-DepthsAndHeights.gif - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Path-DepthsAndHeights.gif

<a name="s21"></a>
**[21]** Path profile example.jpg (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Path_profile_example.jpg

<a name="s22"></a>
**[22]** Path Pocket Shape example.png (cropped) - **Image license:** [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) - **Source:** https://wiki.freecad.org/File:Path_Pocket_Shape_example.png

<a name="s23"></a>
**[23]** CNC milling in FreeCAD (profiles, holding tags, pockets in helix shape) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s24"></a>
**[24]** CNC milling in FreeCAD (pocket in helix shape) - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s25"></a>
**[25]** Haltestege (gelb) in der CAM-Simulationsansicht von FreeCAD - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s26"></a>
**[26]** Haltestege (gelb) in der CAM-Simulationsansicht von FreeCAD - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s27"></a>
**[27]** Haltestege CNC-gefrästes Aluminiumteil - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s28"></a>
**[28]** Haltestege CNC-gefrästes Holzbrett - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Author:** Oskar Lidtke, [github.com/orcular-org](https://github.com/orcular-org)

<a name="s29"></a>
**[29]** G-Code path simulation on FreeCAD's Path workbench - **Image license:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) - **Source:** https://commons.wikimedia.org/wiki/File:FreeCAD-path-simulation.png


