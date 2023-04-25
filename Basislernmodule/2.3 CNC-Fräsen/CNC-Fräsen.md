> Zurück zur [Übersicht Basislernmodule](../../README.md)

# CNC-Fräsen

## Inhalt

1. [Einführung](#einführung)
2. [Grundlagen](#grundlagen)
   - [Materialien](#materialien)
   - [Arten von CNC-Fräsmaschinen](#arten-von-cnc-fräsmaschinen)
   - [Komponenten einer CNC-Fräsmaschine](#komponenten-einer-cnc-fräsmaschine)
   - [CAM](#cam)
3. [Kenngrößen und Einstellungen](#kenngrößen-und-einstellungen)
   - [Fräswerkzeug-Formen](#fräswerkzeug-formen)
   - [Wichtigste Kenngrößen](#wichtigste-kenngrößen)
   - [Fräsdurchmesser](#fräsdurchmesser)
   - [Ermittlung von Drehzahl, Vorschub und Schnitttiefe](#ermittlung-von-drehzahl-vorschub-und-schnitttiefe)
   - [Sicherheitshöhe](#sicherheitshöhe)
   - [Bearbeitungsarten](#bearbeitungsarten)
   - [Haltestege](#haltestege)
4. [Vorbereitung und Ablauf eines CNC-Fräs-Auftrags](#vorbereitung-und-ablauf-eines-cnc-fräs-auftrags)
   - [Sicherheit](#sicherheit)
   - [CAM, Simulation, G-Code-Datei](#cam-simulation-g-code-datei)
   - [Werkstück](#werkstück)
   - [Nullpunkt setzen](#nullpunkt-setzen)
   - [Ablauf des CNC-Fräsens](#ablauf-des-cnc-fräsens)
   - [Nachbearbeitung](#nachbearbeitung)

[Lizenzinformationen](#lizenzinformationen)

[Bildnachweise](#bildnachweise)

## Einführung

Fräsen ist ein Fertigungsverfahren, bei dem ein sich schnell drehendes Fräswerkzeug durch ein Werkstück - z.B. eine Holzplatte oder einen Metallblock - fährt und Material in Form von Spänen abträgt. Somit lassen sich unterschiedliche Formen und Bauteile fertigen.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233688153-23ca40a5-ca3b-4af9-b14d-aef2676d04a4.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233688354-45113abf-05a0-4c45-b5b8-ba5576b98737.png">
</p>


<p align="center">
<a href="#s1">[1]</a> <i> Fräswerkzeuge - </i>
<a href="#s2">[2]</a> <i> Eine Fräsmaschine im Einsatz - rechts im Bild sind abgetragene Späne zu sehen </i>
</p>

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233688512-95e1a20b-cb17-4477-9cdd-7350541f8b25.png">
</p>


<p align="center">
<a href="#s3">[3]</a> <i> CNC-Fräsen von Aluminium </i>
</p>



Die klassische Anwendung erfolgt mit Fräsmaschinen, wobei die Drehachse des Fräswerkzeugs über einen Elektromotor gedreht wird, während die Bewegung des Fräsers im Raum per Handbedienung mit Kurbeln oder elektrisch gesteuert per Tastendruck erfolgt.

Kombiniert man eine Fräsmaschine mit einer CNC-Steuerung (CNC = Computerized Numerical Control - engl. für "rechnergestützte numerische Steuerung", manchmal auch nur "NC" genannt), so handelt es sich um eine CNC-Fräsmaschine - oder umgangssprachlich oft einfach "CNC-Fräse" genannt. Dabei wird zunächst am Computer ein CNC-Code generiert, entweder durch vom Menschen geschriebenen Code oder mithilfe von 3D-CAD-Modellen und CAD/CAM-Software (mehr dazu unten). Dieser NC-Code wird dann an die Maschine übertragen, die gemäß den Anweisungen im Programm vollautomatisiert alle Bewegungen ausführt und das Teil fertigt.

<p align="center">
<img height="250" src="https://user-images.githubusercontent.com/123781559/233688656-3916c509-5212-49ef-a258-22c1556f3b5e.png">
<img height="250" src="https://user-images.githubusercontent.com/123781559/233688782-a2ea509f-5303-40a6-b407-ccf146b5a807.png">
<img height="250" src="https://user-images.githubusercontent.com/123781559/233688954-0a87a29a-f3d8-4f5f-945e-6d7a4592a390.png">
</p>

<p align="center">
<a href="#s4">[4]</a> <i> CNC-Fräsmaschine (Open Source Hardware) - </i>
<a href="#s5">[5]</a> <i> Kleine Tisch-CNC-Fräse (Open Source Hardware) - </i>
<a href="#s6">[6]</a> <i> CNC-Fräsmaschine in einem Fab Lab (Bilder anklicken zum Vergrößern)</i>
</p>


Neben den CNC-Fräsen gibt es auch andere CNC-Maschinen, z.B. CNC-Drehmaschinen. In diesen Basislernmodulen liegt der Fokus jedoch auf Maschinen, die typischerweise in Fab Labs genutzt werden, dazu zählen insbesondere CNC-Fräsen.

Im Vergleich zu anderen typischen digitalen Fertigungsmethoden in Fab Labs, etwa 3D-Druck oder Lasercutting, ist CNC-Fräsen deutlich anspruchsvoller. Dies liegt primär daran, dass vor allem softwareseitig viel Vorbereitung notwendig ist, da erst ein aufwendiges CAM-Programm (mehr dazu [unten](#cam)) modelliert werden muss, bei dem man alle CNC-Arbeitsschritte einzeln definiert. Dies erfordert einiges an Vorwissen und ist meist etwas aufwendiger als die Vorbereitung von 3D-Drucken oder Lasercuttings. Zudem muss man Parameter wie Drehzahl und Vorschub definieren, hierfür muss man sich mit Materialien und Fräswerkzeugen auskennen und oft auch etwas berechnen. Zum Thema CNC-Fräsen gibt es sehr viel zu lernen. In diesem Basislernmodul wird jedoch nur auf die wichtigsten Grundlagen eingegangen, die für den Anfang im Hobby- und Fab-Lab-Bereich wichtig sind.

Der Vorteil von CNC-Fräsen gegenüber 3D-Druck und Lasercutting ist, dass man auch Metalle bearbeiten kann, wie etwa Aluminium oder je nach Maschine auch Stahl. Zudem sind deutlich dickere Holzplatten als beim Lasercutting bearbeitbar. Im Gegensatz zu Lasercutting sind zudem nicht nur flache, plattenförmige Objekte, sondern auch dreidimensionale Formen möglich.

## Grundlagen

### Materialien

Mit CNC-Fräsen in Fab Labs wird vor allem Holz bearbeitet. Je nach Maschine sind auch Aluminium oder Stahl möglich. Eine weitere Möglichkeit bieten Kunststoffe, z.B. Platten aus Recyclingplastik.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233689223-7545b747-2e2d-4661-99ed-a013fdb3e714.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233689503-8b389fa5-884c-402a-bf16-872c34a3d751.png">
</p>


<p align="center">
<a href="#s7">[7]</a> <i> Holz lässt sich gut mit CNC-Fräsen verarbeiten, z.B. für Teile von Kisten oder Möbeln. - </i>
<a href="#s8">[8]</a> <i> Manche CNC-Fräsen können auch Aluminium oder sogar Stahl bearbeiten. </i>
</p>

<p align="center">
<img height="300" src="https://user-images.githubusercontent.com/123781559/233689738-cfa3be5f-7e59-4d97-bc4b-2d966b6f065d.png">
<img height="300" src="https://user-images.githubusercontent.com/123781559/233689802-b91418c4-3dbf-454a-bf31-163009ddf6fe.png">
</p>


<p align="center">
<a href="#s9">[9]</a> <i>  - </i>
<a href="#s10">[10]</a> <i> Viele Kunststoffe lassen sich CNC-fräsen - hier z.B. eine "Precious Plastic"-Platte aus recyceltem HDPE </i>
</p>



### Arten von CNC-Fräsmaschinen

Die häufigste CNC-Fräsmaschinen-Variante in Fab Labs ist die 3-Achs-Portalfräse. Bei Portalfräsen wird der Fräskopf an einem Querbalken zwischen zwei Ständern geführt. Das Werkstück, z.B. eine Platte, liegt auf einer waagerechten Oberfläche und ist dort festgeschraubt oder eingespannt. Das Fräswerkzeug zeigt stets senkrecht nach unten und kann in drei Raumachsen bewegt werden: X-, Y- und Z-Achse - daher kommt die Bezeichnung "3-Achs-Fräsmaschine". Die Z-Achse bezeichnet in der Regel die senkrechte Achse, also die Bewegung nach oben und unten.

CNC-Fräsmaschinen wurden ursprünglich für die Industrie und Handwerksbetriebe entwickelt und sind relativ teuer. Manche Fab Labs verfügen dennoch über solche teuren Industriemaschinen, andere greifen eher auf kostengünstige Hobbygeräte zurück, von denen es mittlerweile auch viele gibt. Zudem gibt es Bausätze und Anleitungen zum Bau von eigenen CNC-Fräsmaschinen. Dabei wird oft eine handbetriebene Oberfräse eingesetzt und um bewegliche Achsen und eine CNC-Steuerung ergänzt.

Neben 3-Achs-Fräsmaschinen gibt es auch 4- und 5-Achs-Fräsmaschinen. Dabei kommen zusätzlich zu den drei linearen Bewegungsachsen noch ein bis zwei Drehachsen hinzu. Dies wird realisiert, indem sich  entweder das Fräswerkzeug um das Werkstück drehen kann oder indem das eingespannte Werkstück gedreht wird - je nach Bauart der Maschine. Auf diese Weise kann die Fräse auch seitlich oder schräg in das Werkstück hineinarbeiten - damit sind deutlich komplexere Formen möglich. Derartige 4- und 5-Achs-Fräsen finden sich jedoch eher in der Industrie als in Fab Labs.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233690001-7e103765-c02f-4d8a-839a-21f6c6fe5a76.png">
</p>


<p align="center">
<a href="#s11">[11]</a> <i> Eine 5-Achs-CNC-Fräse - Das Fräswerkzeug kann sich in drei linearen Achsen bewegen und zusätzlich um zwei Achsen drehen - somit kann auch seitlich und schräg in das Werkstück gefräst werden, wodurch deutlich komplexere Formen als mit 3-Achs-Maschinen herstellbar sind. </i>
</p>


Eine Besonderheit im Bereich Fab-Lab- und Maker-Communities stellt die Maslow-CNC-Fräse dar. Die Maslow-CNC ist ein auf Open-Source-Hardware und -Software basierendes Projekt. Ihre Besonderheit ist der Aufbau: Die zu bearbeitende Platte liegt nicht flach und waagerecht, sondern fast senkrecht, leicht angewinkelt. Dadurch ist die Maschine besonders platzsparend. Als Herzstück wird eine handbetriebene Oberfräse eingesetzt. Diese sitzt in einem Gehäuse, welches auf zwei Ketten hängt, die motorgesteuert verlängert und verkürzt werden, sodass sich die Fräse nach links, rechts, oben und unten über die Platte bewegen kann. Zudem wird die Z-Richtung der Fräse angesteuert, also das senkrechte Eintauchen in die Platte.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233690136-bd7046d0-735f-4d69-a5cc-f01ec4536fd8.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233690221-f4449aae-83f4-4ede-a985-50ac0a8c819f.png">
</p>


<p align="center">
<a href="#s12">[12]</a> <i> Die Maslow-CNC-Maschine steht leicht angeschrägt, fast senkrecht, was sie sehr platzsparend macht. Eine eigentlich für den Handbetrieb nutzbare Oberfräse hängt an zwei Ketten, die über Motoren verlängert und verkürzt werden - darüber wird die Bewegung der Fräse gesteuert. - </i>
<a href="#s13">[13]</a> <i> Neben Holz ist auch die Bearbeitung von z.B. Kunststoff möglich (hier: eine "Precious Plastic"-Recyclingkunststoffplatte). </i>
</p>




### Komponenten einer CNC-Fräsmaschine

Die wichtigsten Komponenten sind das Fräswerkzeug mit motorbetriebener Spindel, die geführten und motorgesteuerten Achsen und die CNC-Steuerung, deren Funktionen bereits oben erläutert wurden.

Als Unterlage auf dem Frästisch wird bei CNC-Fräsen oft eine sogenannte Opferplatte aus Holz oder Kunststoff befestigt. Der Grund liegt darin, dass der Fräser oft auch etwas tiefer als bis zur Unterkante des Werkstücks fräsen muss, um das Teil aus dem Werkstückblock herauszufräsen. Dabei fräst das Werkzeug ein klein wenig in die Opferplatte hinein. Die Opferplatte muss nach einiger Zeit ausgetauscht werden, da die Werkstücke wegen der vielen Rillen irgendwann nicht mehr ganz eben, sondern schief aufliegen und damit nicht mehr genau bearbeitet werden können.

Manche CNC-Fräsmaschinen verfügen über eine Absaugung. Hierbei werden die Späne direkt am Werkstück abgesaugt und über einen Schlauch in einen Behälter transportiert. Fehlt so eine Absaugung, muss die Arbeitsfläche regelmäßig von Spänen bereinigt werden, z.B. mit einem Staubsauger.

Professionellere CNC-Fräsmaschinen verfügen über eine Vorrichtung, die Schmier- und Kühlmittel auf das Fräswerkzeug spritzt. Dies ist vor allem beim Fräsen von Metallen wichtig.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233690293-301bc88d-b00b-4f68-b6d5-3fffeb866583.png">
</p>


<p align="center">
<a href="#s14">[14]</a> <i> Zuführung von Kühlschmiermittel beim Fräsen durch einen Kugelgelenkschlauch  </i>
</p>


### CAM

Vor dem eigentlichen CNC-Fräsen muss zunächst ein digitaler Steuercode erstellt werden, der der Maschine "mitteilt", was sie tun soll.
Der Beginn hierfür findet in einer CAD/CAM-Software statt. CAD steht für "Computer Aided Design" (engl. für „Computergestütztes Entwerfen“). Mit CAD-Software können also 3D-Modelle von Bauteilen oder Objekten konstruiert bzw. modelliert werden (mehr dazu im [Basislernmodul 3D-Design und CAD](../1.1%203D-Design/3D-Design.md)).

Auf Basis eines 3D-CAD-Modells wird als nächstes das CAM durchgeführt. CAM steht für "Computer Aided Manufacturing" (engl. für "Computergestützte Fertigung"). Es gibt CAM-Software als eigenständige Programme, oft sind sie jedoch als Modul in ein CAD-Programm integriert - man spricht dann von CAD/CAM-Software.

Im CAM werden auf Basis eines CAD-Modells verschiedene CNC-Arbeitsschritte definiert, z.B. Taschen, Profile oder Bohrungen. Zudem werden wichtige Parameter wie Drehzahl und Vorschub eingegeben. Details zu all diesen Begriffen finden sich in den nächsten Abschnitten.

Im [Basislernmodul 3D-Design und CAD](../1.1%203D-Design/3D-Design.md) werden die beiden Softwarelösungen FreeCAD und Autodesk Fusion 360 vorgestellt - beide Programme sind CAD/CAM-Software, können also sowohl zum Modellieren von Bauteilen als auch zum Vorbereiten des CNC-Fräsens dieser Bauteile genutzt werden.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233690608-3465bd63-b85d-4fbf-ba00-8c5efbc7f838.png">
</p>


<p align="center">
<a href="#s15">[15]</a> <i> CAM in der Software FreeCAD: Die roten und grünen Linien zeigen die Pfade, die das Fräswerkzeug nehmen soll - so entsteht aus einem massiven Materialblock das hier dargestellte Bauteil. </i>
</p>




## Kenngrößen und Einstellungen


### Fräswerkzeug-Formen
Fräswerkzeuge gibt es in vielen verschiedenen Formen, für verschiedene Anwendungen. Die gängigste und im Fab-Lab-Bereich am häufigsten eingesetzte Form ist der Schaftfräser. Der Schaft ist der Teil des Werkzeugs, der über keine Schneiden verfügt und in die Maschine eingespannt wird.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233690716-901c354e-9593-41f6-97cc-9f32baaa4dd6.png">
</p>


<p align="center">
<a href="#s16">[16]</a> <i> Verschiedene Fräswerkzeuge: Rechts unten ein Radiusschaftfräser mit Rundung an der Spitze. In der Draufsicht links lässt sich gut die Zähnezahl bzw. Anzahl der Schneiden erkennen: oben ein zweischneidiges und unten vierschneidige Fräswerkzeuge. </i>
</p>


### Wichtigste Kenngrößen

Die wichtigsten Kenngrößen und Parameter beim CNC-Fräsen sind:

- **Fräsdurchmesser (in Millimeter, mm):** der Durchmesser des Fräswerkzeugs.
- **Drehzahl (in Umdrehungen pro Minute, U/min):** die Geschwindigkeit, mit der sich das Fräswerkzeug dreht.
- **Vorschubgeschwindigkeit (in Millimeter pro Minute, mm/min):** die Geschwindigkeit, mit der sich das Fräswerkzeug in horizontaler Richtung bewegt.
- **Schnitttiefe (auch Zustelltiefe oder Eintauchtiefe genannt) (in Millimeter, mm):** In der Regel beschreibt dies die Tiefe, die das Fräswerkzeug pro Durchgang in das Material eintaucht.

Es gibt noch viele weitere einstellbare Parameter, diese vier sind jedoch die wichtigsten und maßgeblichen. Auf die einzelnen Parameter wird in den folgenden Abschnitten noch näher eingegangen.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233690884-b4e131fe-7eca-4a92-8069-fc09ebdeb2d3.png">
</p>


<p align="center">
<a href="#s17">[17]</a> <i> Die wichtigsten Parameter beim Fräsen. </i>
</p>

<p align="center">
<img height="250" src="https://user-images.githubusercontent.com/123781559/233691010-4084b953-9e8c-4bba-a037-1707da09d480.png">
<img height="250" src="https://user-images.githubusercontent.com/123781559/233691063-9f2a06ed-5501-4581-9fb9-d77d06257d39.png">
</p>


<p align="center">
<a href="#s18">[18]</a> <i> Pfad (grün) zum Fräsen einer Tasche in der CAD/CAM-Software FreeCAD. - </i>
<a href="#s19">[19]</a> <i> Gleiches Modell in der Seitenansicht: Anhand der grünen Pfadlinien erkennt man die Schnitttiefe - hier beträgt sie 0,3 mm, die Tiefe der Tasche beträgt 2 mm. </i>
</p>



### Fräsdurchmesser
Fräswerkzeuge gibt es in unterschiedlichen Durchmessern - bei Fab-Lab-Maschinen üblicherweise zwischen drei und zehn Millimetern. Für jedes Fräsvorhaben muss man sich entweder für einen Fräsdurchmesser entscheiden oder das CNC-Vorhaben in mehrere Abschnitte mit unterschiedlichen Durchmessern unterteilen. Dabei muss das Fräswerkzeug im Laufe des Prozesses gewechselt werden, in der Regel von Hand. Manche professionelle Maschinen können auch selbstständig Werkzeuge wechseln, ohne dass eine Person eingreifen muss.

Je größer der Fräsdurchmesser, desto mehr Material wird pro Zeit entfernt, d.h. desto schneller läuft die Fertigung ab. Gleichzeitig kann ein Fräsdurchmesser nicht größer als die kleinste zu fräsende Tasche (Vertiefung im Material) sein. Es gilt also, den Fräser so groß wie möglich, aber so klein wie nötig auszuwählen.

### Ermittlung von Drehzahl, Vorschub und Schnitttiefe

Die Parameter-Einstellungen sind sehr wichtig, da zu hohe oder zu niedrige Drehzahlen oder Vorschubgeschwindigkeiten zu unsauberen Ergebnissen oder im schlimmsten Fall zur Beschädigung der Maschine führen können.

Hat man seinen Fräsdurchmesser gewählt und kennt das zu fräsende Material des Werkstücks, kann man daraus die anderen Parameter berechnen. In Fachbüchern und im Internet (beispielsweise [hier](https://www.sorotec.de/webshop/Datenblaetter/fraeser/schnittwerte.pdf)) finden sich Tabellen und Formeln, zudem finden sich diese üblicherweise vor Ort in der Werkstatt bzw. im Fab Lab. Die berechneten Werte für Drehzahl und Vorschub können in das CAM-Programm eingegeben werden. In gewissem Rahmen kann auch von den Werten abgewichen werden, d.h. man verwendet die berechneten Werte lediglich als Richtwert, dabei sollte man sich aber gut auskennen.

Für die Schnitttiefe wird oft als Richtwert angenommen, dass sie höchstens den Fräsdurchmesser betragen sollte. Um sicher zu gehen, empfehlen sich Schnitttiefen kleiner als der Fräsdurchmesser, z.B. der halbe Durchmesser. Dies ist vor allem beim Fräsen von Metallen wichtig. Hintergrund ist, dass das Fräswerkzeug bei größerer Eintauchtiefe mehr Material pro Zeit schneidet, was Werkzeug und Werkstück stark belastet und zu unsauberen Ergebnissen oder Schäden führen kann. Zudem sind Fräswerkzeuge durch ihre Form auf das Fräsen optimiert, also das Schneiden quer zur Werkzeugachse. Sie können auch ein stückweit bohren, also in Achsrichtung arbeiten, sind jedoch durch ihre Form weniger dafür geeignet. Daher sollte eher in kleinen Schritten eingetaucht und nach jedem Eintauchen zunächst die gesamte zu entfernende Fläche gefräst werden.


### Sicherheitshöhe

Es gibt bestimmte Bereiche, in denen das Fräswerkzeug mit einer anderen Geschwindigkeit fährt als in anderen. Oberhalb der Sicherheitshöhe fährt der Fräser relativ schnell, sobald er an der zu fräsenden Stelle am Werkstück angekommen ist, senkt er sich langsam ab und fährt ab da nur noch mit verringerter Geschwindigkeit. Während des Fräsens im Werkstück bewegt er sich mit der Vorschubgeschwindigkeit. Hintergrund ist, dass ein Fräswerkzeug, dass mit sehr hoher Geschwindigkeit in das Material taucht, beschädigt werden oder sogar abbrechen kann, daher müssen die Bewegungen unterhalb der Sicherheitshöhe deutlich langsamer ablaufen als darüber.

Ab welcher Höhe die Sicherheitshöhe beginnt und mit welcher Geschwindigkeit sich der Fräser oberhalb dieser Höhe bewegen soll, kann in der CAM-Software eingestellt werden.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233691132-4b9651e5-beb2-4071-8475-5cbf4eae72bd.png">
</p>


<p align="center">
<a href="#s20">[20]</a> <i> Sicherheitshöhe und einige weitere Parameter, wie sie in der CAD/CAM-Software FreeCAD verwendet werden. Oberhalb der Sicherheitshöhe bewegt sich das Fräswerkzeug ("tool" im Bild) mit erhöhter Geschwindigkeit. Mit "step down" ist hier die Schnitttiefe bezeichnet (mehr zu CAM in FreeCAD: https://wiki.freecad.org/Path_Workbench ). </i>
</p>



### Bearbeitungsarten

Es gibt viele unterschiedliche Bearbeitungsarten, die man in CAM-Systemen als eine sogenannte Operation anlegen kann. Die wichtigsten sind:

- **Profil:** Das Fräswerkzeug fährt die äußere Kontur des zu fertigenden Teils ab, beginnend auf der Oberfläche des Werkstücks. Danach geht es schrittweise - jeweils um die Schnitttiefe - in das Material hinein und fährt das Profil erneut ab. Am Ende ist das Teil nahezu vollständig vom Werkstückblock getrennt und kann entnommen werden. Wichtig ist hier, Haltestege mit einzuplanen - mehr dazu im nächsten Abschnitt.
- **Tasche:** Eine Tasche stellt eine Vertiefung im Material dar. Ähnlich wie beim Profilfräsen beginnt der Fräsvorgang an der Oberfläche und geht dann schrittweise herunter, je Durchgang um die Schnitttiefe.
- **Bohrung:** Bohrungen, also kreisrunde Löcher, können mit Bohr- oder Fräswerkzeugen gefertigt werden. Spannt man ein Bohrwerkzeug ein und stellt die CAM-Operation entsprechend als Bohrung ein, wird der Bohrvorgang senkrecht ausgeführt, wie bei einer Bohrmaschine. Verwendet man hingegen ein Fräswerkzeug, ist es wichtig, dass der Fräsdurchmesser kleiner als der Bohrdurchmesser ist und das Fräswerkzeug nicht in einem Durchgang vollständig in das Material geht - ein Fräser sollte nicht zum Bohren verwendet werden. Stattdessen empfiehlt es sich, eine Helixform als Pfad zu verwenden. Alternativ kann eine Operation vom Typ "Tasche" erstellt werden,  sodass stufenweise Kreisflächen gefräst werden - je Stufe um eine Zuschnitttiefe weiter - und somit praktisch eine Bohrung gefräst wird.

Operationen werden in der CAD/CAM-Software als Pfade (engl. "Path") angelegt und sichtbar gemacht. Anhand der visualisierten Pfade kann man bereits erkennen, welchen Weg das Fräswerkzeug nehmen wird.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691233-ffcd7bdb-982f-4f83-97f9-7e19545b5e62.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691332-96c767ad-e786-4668-a330-ffea015f7636.png">
</p>


<p align="center">
<a href="#s21">[21]</a> <i> CAM-Operation "Profil": entlang des grünen Pfades wird die äußere Kontur des Bauteils gefräst. - </i>
<a href="#s22">[22]</a> <i> CAM-Operation "Tasche": Eine Vertiefung im Material, dessen Hohlraum durch den Fräser vollständig entfernt wird, bis der Boden der Tasche (grün) erreicht wird. </i>
</p>

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691428-f2fa0dd5-54d3-489a-863b-40f37615784a.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691467-edc4197a-1843-42ab-8df7-a78c20f94bc1.png">
</p>


<p align="center">
<a href="#s23">[23]</a> <i> Bauteil in der Software FreeCAD mit mehreren CAM-Operationen (grüne und rote Pfade): Außenkontur und innere Kreiskontur als "Profil" mit Haltestegen, die vier kleinen Bohrungen als "Taschen". - </i>
<a href="#s24">[24]</a> <i> Nahansicht einer Bohrung des Bauteils: Die Bohrung wird hier nicht als Bohr-Operation, sondern als gefräste Tasche ausgeführt. Der Pfad hat eine Helixform, um das Material langsam und damit schonend für das Fräswerkzeug zu bearbeiten. (Bilder anklicken zum Vergrößern) </i>
</p>



### Haltestege

Wird ein Teil vollständig vom Werkstück getrennt, also ein Profil oder eine äußere Kontur gefräst, sollte man sogenannte Haltestege mit einplanen. Andernfalls könnte sich das gefertigte Teil im letzten Fräsvorgang verdrehen, kippen und mit dem Fräswerkzeug verkeilen. Die Folgen wären, dass das Teil nicht richtig gefertigt wird, im schlimmsten Fall droht ein Schaden an der Maschine.

Haltestege lassen sich im CAM-System einstellen. Im Endergebnis befinden sich die Haltestege am untersten Ende des Werkstücks und sind relativ schmal und flach, sodass sie sich leicht durchtrennen lassen.

<p align="center">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233691502-92ef4333-3a83-4c76-8fd9-594705c1a1c5.png">
<img height="400" src="https://user-images.githubusercontent.com/123781559/233691548-05b920a4-3c86-4c36-9861-23633f01910e.png">
</p>


<p align="center">
<a href="#s25">[25]</a> <i>  - </i>
<a href="#s26">[26]</a> <i> Haltestege (gelb) in der CAM-Simulationsansicht von FreeCAD </i>
</p>

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691645-35fdbcc8-f000-46a8-a162-1b9a8897606f.png">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691744-48c2a0af-bd04-4fd2-9251-9a49acbb94ab.png">
</p>


<p align="center">
<a href="#s27">[27]</a> <i> Haltestege in einem CNC-gefrästen Aluminium-Teil. Im linken Bereich ist ein Haltesteg gut sichtbar; rechts sind einige Spanreste, da der Fräser im letzten Schritt nicht tief genug gegangen ist. - </i>
<a href="#s28">[28]</a> <i> Haltestege in einem Holzbrett, gefräst mit einer Maslow-CNC. (Bilder anklicken zum Vergrößern)</i>
</p>



Das Fräswerkzeug nimmt im untersten Bereich des zu fräsenden Profils einen Pfad, bei dem es vor den Stellen, wo die Haltestege vorgesehen sind, ein Stück hochfährt und diesen Teil ausspart, womit die Haltestege übrig bleiben.

Größe und Anzahl der Haltestege sollten so gewählt werden, dass sie das Teil sicher halten können, ansonsten sollten sie so klein wie möglich entworfen werden, damit man sie leicht durchtrennen kann.

Nach abgeschlossenem Fräsvorgang können die Haltestege je nach Material mit unterschiedlichen Methoden durchtrennt werden. Bei Holz kann beispielsweise eine Säge verwendet werden, bei Aluminium funktioniert es mit einer Metallsäge oder auch mit Hammer und Meißel gut. Nach dem Trennen sollten die Säge- oder Bruchstellen mit einer Feile nachbearbeitet werden.



## Vorbereitung und Ablauf eines CNC-Fräs-Auftrags

### Sicherheit

CNC-Maschinen sind potenziell gefährliche Maschinen und sollten nie ohne Einweisung und Freigabe benutzt werden. Fab Labs bieten in der Regel eine verpflichtende Sicherheitseinweisung an. Die Einzelheiten hierzu sind bei jeder Maschine anders, daher erfolgt in diesem Basislernmodul keine genauere Beschreibung.

### CAM, Simulation, G-Code-Datei

Ein relativ großer Aufwand beim CNC-Fräsen steckt in der Vorbereitung mit der CAM-Software. Hat man alle Operationen und CAM-Pfade definiert, sollte eine Simulation durchgeführt werden. Die meisten CAM-Programme verfügen über eine Simulationsfunktion, bei der der vollständige Fräsvorgang dargestellt wird, ähnlich wie bei einem Video, wobei man während der Simulation die 3D-Ansicht frei drehen kann.

<p align="center">
<img height="350" src="https://user-images.githubusercontent.com/123781559/233691827-28757bab-7727-4dfc-970f-e3b94805c32b.png">
</p>


<p align="center">
<a href="#s29">[29]</a> <i> CAM-Simulationsmodus in FreeCAD: Die grünen und roten Pfade zeigen den Verlaufsweg des Fräswerkzeugs (grau). Zu Beginn der Simulation ist ein massiver, dunkelroter Block zu sehen; während der Simulation kann man beobachten, wie der Fräser (grau) Material entfernt, wodurch die gelben Flächen entstehen. In dieser Momentaufnahme ist das äußere Profil bereits fertig, die Tasche ist gerade mitten in der Bearbeitung. </i>
</p>


Die Simulation kann auch in erhöhter Geschwindigkeit abgespielt werden. Während der Simulation wird sichtbar, wann an welcher Stelle Material abgetragen wird und wie das fertige Teil am Ende aussieht. Fallen noch Fehler auf, kann das CAM-Programm noch nachbearbeitet werden und man spart sich teure Fehler in der Fertigung.

Abschließend muss das CAM-Programm mithilfe eines Post-Prozessors (üblicherweise in der Software eingebaut) als eine G-Code-Datei exportiert werden. G-Codes beim CNC-Fräsen basieren auf dem gleichen Prinzip wie G-Codes beim 3D-Druck - mehr dazu in dem [Basislernmodul zu 3D-Druck](../2.1%203D-Druck/3D-Druck.md), im Abschnitt [G-Code](../2.1%203D-Druck/3D-Druck.md#g-code).

### Werkstück

Das Werkstück, beispielsweise eine Holzplatte oder ein Metallblock, muss sicher am Frästisch befestigt werden. In den meisten Fällen kann das Werkstück mit einigen Schrauben einfach an die Opferplatte geschraubt werden, vorzugsweise mit Senkkopfschrauben, um die Gefahr von Kollisionen mit dem Fräswerkzeug zu verringern. Dennoch sollte man stets aufpassen, dass die Maschine nicht in die Schraube hineinfräst.

Eine weitere Möglichkeit besteht darin, das Werkstück einzuspannen, sofern die CNC-Fräsmaschine über eine Spannvorrichtung verfügt.

### Nullpunkt setzen

CNC-Maschinen können über Pfeiltasten - je nach Modell am Gerät selbst oder über die Tastatur eines angeschlossenen Computers - gesteuert werden. Dies kann man beispielsweise zum Anfahren des Nullpunkts nutzen.

Der Maschine muss mitgeteilt werden, wo sie mit dem Fräsauftrag beginnen soll, man muss also den sogenannten Nullpunkt definieren. Hierfür gibt es unterschiedliche Methoden, z.B. durch das Anfahren des Nullpunkts an der Werkstückoberfläche bei drehender Spindel (sogenanntes "Ankratzen"). An dieser Stelle wird über die Bedienung der CNC-Fräse der Nullpunkt gesetzt. Die Maschine speichert also die X-, Y- und Z-Koordinaten dieses Punktes ab und wird das CNC-Programm an diesem Punkt starten.

### Ablauf des CNC-Fräsens

Ist der Nullpunkt gesetzt, muss zu Beginn eines CNC-Auftrags die G-Code-Datei über eine Steuersoftware an die CNC-Steuerung der Maschine übergeben und der Betrieb gestartet werden. Während des Fräsens sollte man stets in der Nähe bleiben und bei ungewöhnlichem Verhalten oder drohenden Schäden den Fräsvorgang stoppen - über die Steuersoftware oder über den Notausschalter.

### Nachbearbeitung

Nach abgeschlossener Fertigung kann das Werkstück bzw. das gefertigte Teil entnommen werden. Vor allem bei Metallteilen sollte man vorsichtig sein, da wegen der scharfen Kanten Verletzungsgefahr besteht. Die Kanten sollten entgratet und gefeilt werden, zudem können Oberflächen geschliffen werden.

# Lizenzinformationen

**Author:** Oskar Lidtke, https://github.com/orcular-org/

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />Except where otherwise noted, this work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)</a>.

See best practices for [attribution](https://wiki.creativecommons.org/wiki/Best_practices_for_attribution) and [marking your own work](https://wiki.creativecommons.org/wiki/Marking_your_work_with_a_CC_license) with a CC license.

For attribution and licenses of the images used, see the section below.

# Bildnachweise

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


