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

Die klassische Anwendung erfolgt mit Fräsmaschinen, wobei die Drehachse des Fräswerkzeugs über einen Elektromotor gedreht wird, während die Bewegung des Fräsers im Raum per Handbedienung mit Kurbeln oder elektrisch gesteuert per Tastendruck erfolgt.

Kombiniert man eine Fräsmaschine mit einer CNC-Steuerung (CNC = Computerized Numerical Control - engl. für "rechnergestützte numerische Steuerung", manchmal auch nur "NC" genannt), so handelt es sich um eine CNC-Fräsmaschine (oder umgangssprachlich oft einfach "CNC-Fräse" genannt). Dabei wird zunächst am Computer ein CNC-Programm generiert, entweder durch vom Menschen geschriebenen Code oder mithilfe von 3D-CAD-Modellen und CAD/CAM-Software (mehr dazu unten). Dieser NC-Code wird dann an die Maschine übertragen, die gemäß den Anweisungen im Programm vollautomatisiert alle Bewegungen ausführt und das Teil fertigt.

> Bild CNC-Fräse

Neben den CNC-Fräsen gibt es auch andere CNC-Maschinen, z.B. CNC-Drehmaschinen. In diesen Basislernmodulen liegt der Fokus jedoch auf Maschinen, die typischerweise in Fab Labs genutzt werden, dazu zählen eben typscherweise CNC-Fräsen.

Im Vergleich zu anderen typischen digitalen Fertigungsmethoden in Fab Labs, etwa 3D-Druck oder Lasercutting, ist CNC-Fräsen deutlich anspruchsvoller. Dies liegt vor allem daran, dass vor allem softwareseitig viel Vorbereitung notwendig ist, da erst ein aufwendiges CAM-Programm modelliert werden muss, bei dem man alle CNC-Arbeitsschritte einzeln definiert. Dies erfordert einiges an Vorwissen und ist meist etwas aufwendiger als die Vorbereitung von 3D-Drucken oder Lasercuttings. Zudem muss man Parameter wie Drehzahl und Vorschub definieren, hierfür muss man sich mit Materialien und Fräswerkzeugen auskennen und oft auch etwas berechnen. Zum Thema CNC-Fräsen gibt es sehr viel zu lernen. In diesem Basislernmodul wird jedoch nur auf die wichtigsten Grundlagen eingegangen, die für den Anfang im Hobby- und Fab-Lab-Bereich wichtig sind.

Der Vorteil von CNC-Fräsen gegenüber 3D-Druck und Lasercutting ist, dass man auch Metalle bearbeiten kann (z.B. Aluminium oder je nach Maschine auch Stahl). Zudem sind deutlich dickere Holzplatten als beim Lasercutting bearbeitbar. Im Gegensatz zu Lasercutting sind zudem nicht nur flache, plattenförmige Objekte, sondern auch dreidimensionale Formen möglich.

## Grundlagen

### Materialien

Mit CNC-Fräsen in Fab Labs wird vor allem Holz bearbeitet. Je nach Maschine sind auch Aluminium oder Stahl möglich. Eine weitere Möglichkeit bieten Kunststoffe, z.B. Platten aus Recyclingplastik.

### Arten von CNC-Fräsmaschinen

Die häufigste CNC-Fräsmaschinen-Variante in Fab Labs ist die 3-Achs-Portalfräse. Bei Portalfräsen wird der Fräskopf an einem Querbalken zwischen zwei Ständern geführt. Das Werkstück, z.B. eine Platte, liegt auf einer waagerechten Oberfläche und ist dort festgeschraubt oder eingespannt. Das Fräswerkzeug zeigt stets senkrecht nach unten und kann in drei Raumachsen bewegt werden: X-, Y- und Z-Achse. Daher kommt die Bezeichnung "3-Achs-Fräsmaschine". Die Z-Achse bezeichnet in der Regel die senkrechte Achse, also die Bewegung nach oben und unten.

CNC-Fräsmaschinen wurden ursprünglich für die Industrie und und Handwerksbetriebe entwickelt und sind relativ teuer. Manche Fab Labs verfügen dennoch über solche teuren Industriemaschinen, andere greifen eher auf kostengünstige Hobbygeräte zurück, von denen es mittlerweile auch viele gibt. Zudem gibt es Bausätze und Bauanleitungen zum Bau von eigenen CNC-Fräsmaschinen. Dabei wird oft eine handbetriebene Oberfräse eingesetzt und um bewegliche Achsen und eine CNC-Steuerung ergänzt.

Es gibt auch 4- und 5-Achs-Fräsmaschinen. Dabei kommen zusätzlich zu den drei linearen Bewegungsachsen noch eine bis zwei Drehachsen hinzu. Dies wird realisiert, indem sich  entweder das Fräswerkzeug um das Werkstück drehen kann oder indem das eingespannte Werkstück gedreht wird - je nach Bauart der Maschine. Auf diese Weise kann die Fräse auch seitlich oder schräg in das Werkstück hineinarbeiten - damit sind deutlich komplexere Formen möglich. Derartige 4- und 5-Achs-Fräsen finden sich jedoch eher in der Industrie als in Fab Labs.

> Bild 5-Achs-Fräse



Eine Besonderheit im Bereich Fab-Lab- und Maker-Communities stellt die Maslow-CNC-Fräse dar. Die Maslow-CNC ist ein auf Open-Source-Hardware und -Software basierendes Projekt. Ihre Besonderheit ist der Aufbau: die zu bearbeitende Platte liegt nicht flach und waagerecht, sondern fast senkrecht, leicht angewinkelt. Dadurch ist die Maschine besonders platzsparend. Als Herzstück setzt man eine handbetriebene Oberfräse ein. Diese sitzt in einem Gehäuse, welches auf zwei Ketten hängt, die motorgesteuert verlängert und verkürzt werden, sodass sich die Fräse nach links, rechts, oben und unten über die Platte bewegen kann. Zudem wird die Z-Richtung der Fräse angesteuert, also das senkrechte Eintauchen in die Platte.

> Bilder Maslow-CNC



### Komponenten einer CNC-Fräsmaschine

Die wichtigsten Komponenten sind das Fräswerkzeug mit motorbetriebener Spindel, die geführten und motorgesteuerten Achsen und die CNC-Steuerung, deren Funktionen bereits oben erläutert wurden.

Als Unterlage auf dem Frästisch wird bei CNC-Fräsen oft eine sogenannte Opferplatte aus Holz oder Kunststoff befestigt. Der Grund liegt darin, dass der Fräser oft auch etwas tiefer als die Unterkante des Werkstücks fräsen muss, um das Teil aus dem Werkstückblock herauszufräsen. Dabei fräst das Werkzeug ein klein wenig in die Opferplatte hinein. Die Opferplatte muss nach einiger Zeit ausgetauscht werden, da die Werkstücke wegen der vielen Rillen irgendwann nicht mehr ganz eben, sondern schief aufliegen und damit nicht mehr genau bearbeitet werden können.

Manche CNC-Fräsmaschinen verfügen über eine Absaugung. Hierbei werden die Späne direkt am Werkstück abgesaugt und über einen Schlauch in einen Behälter transportiert. Fehlt so eine Absaugung, muss die Arbeitsfläche regelmäßig von Spänen bereinigt werden, z.B. mit einem Staubsauger.

Professionellere CNC-Fräsmaschinen verfügen über eine Vorrichtung, die Schmier- und Kühlmittel auf das Fräswerkzeug spritzt. Dies ist vor allem beim Fräsen von Metallen wichtig.

### CAM

Vor dem eigentlichen CNC-Fräsen muss zunächst ein digitaler Steuercode erstellt werden, der der Maschine "mitteilt", was sie tun soll.
Der Beginn hierfür findet in einer CAD/CAM-Software statt. CAD steht für "Computer Aided Design" (engl. für „Computergestütztes Entwerfen“). Mit CAD-Software können also 3D-Modelle von Bauteilen oder Objekten konstruiert bzw. modelliert werden (mehr dazu im Basislernmodul 3D-Design und CAD).

Auf Basis eines 3D-CAD-Modells wird als nächstes das CAM durchgeführt. CAM steht für "Computer Aided Manufacturing" (engl. für "Computergestützte Fertigung"). Es gibt CAM-Software als eigenständiges Programme, oft sind sie jedoch als Modul in ein CAD-Programm integriert - man spricht dann von CAD/CAM-Software.

Im CAM werden auf Basis eines CAD-Modells verschiedene CNC-Arbeitsschritte definiert, z.B. Taschen, Profile oder Bohrungen. Zudem werden wichtige Parameter wie Drehzahl und Vorschub eingegeben. Details zu all diesen Begriffen finden sich in den nächsten Abschnitten.

Im Basislernmodul 3D-Design und CAD (verlinken) werden die beiden Softwarelösungen FreeCAD und Autdesk Fusion 360 vorgestellt - beide Programme sind CAD/CAM-Software, können also sowohl zum Modellieren von Bauteilen als auch zum Vorbereiten von CNC-Fräsen dieser Bauteile genutzt werden.

> Bild CAM



## Kenngrößen und Einstellungen


### Fräswerkzeug-Formen
Fräswerkzeuge gibt es in vielen verschiedenen Formen, für verschiedene Anwendungen. Die gängigste und im Fab-Lab-Bereich am häufigsten eingesetzte Form ist der Schaftfräser. Der Schaft ist der Teil des Werkzeugs, der über keine Schneiden verfügt und in die Maschine eingespannt wird.

> Bild Schaftfräser
> https://en.wikipedia.org/wiki/File:End_Mill_02_labels.png
> https://en.wikipedia.org/wiki/Milling_cutter

### Wichtigste Kenngrößen

Die wichtigsten Kenngrößen und Parameter beim CNC-Fräsen sind:

- **Fräsdurchmesser (in Millimeter, mm):** Der Durchmesser des Fräswerkzeugs.
- **Drehzahl (in Umdrehungen pro Minute, U/min):** Die Geschwindigkeit, mit der sich das Fräswerkzeug dreht.
- **Vorschubgeschwindigkeit (in Millimeter pro Minute, mm/min):** Die Geschwindigkeit, mit der sich das Fräswerkzeug in horizontaler Richtung bewegt.
- **Schnitttiefe (auch Zustelltiefe oder Eintauchtiefe genannt) (in Millimeter, mm):** In der Regel beschreibt dies die Tiefe, die das Fräswerkzeug pro Durchgang in das Material eintaucht.

Es gibt noch viele weitere einstellbare Parameter, diese vier sind jedoch die wichtigsten und maßgeblichen. Auf die einzelnen Parameter wird in den folgenden Abschnitten noch näher eingegangen.

> Bild Fräsparameter

### Fräsdurchmesser
Fräswerkzeuge gibt es in unterschiedlichen Durchmessern - bei Fab-Lab-Maschinen üblicherweise zwischen drei bis zehn Millimetern. Für jedes Fräsvorhaben muss man sich entweder für einen Fräsdurchmesser entscheiden oder das Projekt in mehrere Unteraufträge mit unterschiedlichen Durchmessern teilen. Dabei muss das Fräswerkzeug im Laufe des Prozesses gewechselt werden, in der Regel von Hand. Manche professionelle Maschinen können auch selbstständig Werkzeuge wechseln, ohne dass eine Person eingreifen muss.

Je größer der Fräsdurchmesser, desto mehr Material wird pro Zeit entfernt, d.h. desto schneller läuft die Fertigung ab. Gleichzeitig kann ein Fräsdurchmesser nicht größer als die kleinste zu fräsende Tasche sein. Es gilt also, den Fräser so groß wie möglich, aber so klein wie nötig auszuwählen.

### Ermittlung von Drehzahl, Vorschub und Schnitttiefe

Die Parameter-Einstellungen sind sehr wichtig, da zu hohe oder zu niedrige Drehzahlen oder Vorschubgeschwindigkeiten zu unsauberen Ergebnissen oder im schlimmsten Fall zur Beschädigung der Maschine führen können.

Hat man seinen Fräsdurchmesser gewählt und kennt das zu fräsende Material des Werkstücks, kann man daraus die anderen Parameter berechnen. In Fachbüchern und im Internet (beispielsweise [hier](https://www.sorotec.de/webshop/Datenblaetter/fraeser/schnittwerte.pdf)) finden sich Tabellen und Formeln, zudem finden sich diese üblicherweise vor Ort in der Werkstatt bzw. im Fab Lab. Die berechneten Werte für Drehzahl und Vorschub können in das CAM-Programm eingegeben werden. Im gewissen Rahmen kann auch von den Werten abgewichen werden, d.h. man verwendet die berechneten Werte lediglich als Richtwert, dabei sollte man sich aber gut auskennen.

Für die Schnitttiefe wird oft als Richtwert angenommen, dass sie höchstens den Fräsdurchmesser betragen sollte. Um sicher zu gehen, empfehlen sich Schnitttiefen kleiner als der Fräsdurchmesser, z.B. der halbe Durchmesser. Dies ist vor allem beim Fräsen von Metallen wichtig.


### Sicherheitshöhe

Es gibt bestimmte Bereiche, in denen das Fräswerkzeug mit einer anderen Geschwindigkeit fährt als in anderen. Oberhalb der Sicherheitshöhe fährt der Fräser relativ schnell, sobald er an der zu fräsenden Stelle am Werkstück angekommen ist, senkt er sich langsam ab und fährt ab da nur noch mit verringerter Geschwindigkeit. Während des Fräsens im Werkstück bewegt er sich mit der Vorschubgeschwindigkeit.

Ab welcher Höhe die Sicherheitshöhe beginnt und mit welcher Geschwindigkeit sich der Fräser oberhalb dieser Höhe bewegen soll, kann in der CAM-Software eingestellt werden.

> Bild aus FreeCAD-Path-WB


### Bearbeitungsarten

Es gibt viele unterschiedliche Bearbeitungsarten, die man in CAM-Systemen erstellen kann. Die wichtigsten sind:

- **Profil:** Das Fräswerkzeug fährt die äußere Kontur des zu fertigenden Teils ab, beginnend auf der Oberfläche des Werkstücks. Danach geht es schrittweise - jeweils um die Schnitttiefe - in das Material hinein und fährt das Profil erneut ab. Am Ende ist das Teil nahezu vollständig vom Werkstückblock getrennt und kann entnommen werden. Wichtig ist hier, Haltestege mit einzuplanen - mehr dazu im nächsten Abschnitt.
- **Tasche:** Eine Tasche stellt eine Vertriefung im Material dar. Ähnlich wie beim Profilfräsen beginnt der Fräsvorgang an der Oberfläche und geht dann schrittweise herunter, je Schritt um die Schnitttiefe.
- **Bohrung:** Bohrungen, also kreisrunde Löcher, können mit Bohr- oder Fräswerkzeugen gefertigt werden. Spannt man ein Bohrwerkzeug ein und stellt den CAM-Bearbeitungstyp entsprechend als Bohrung ein, wird der Bohrvorgang senkrecht ausgeführt, wie bei einer Bohrmaschine. Verwendet man ein Fräswerkzeug, ist es wichtig, dass der Fräsdurchmesser kleiner als der Bohrdurchmesser ist und das Fräswerkzeug nicht in einem Durchgang in das Material geht - ein Fräser sollte nicht zum Bohren verwendet werden. Stattdessen empfiehlt sich eine Helix- bzw. Spiralform als Pfad oder es werden stufenweise Kreisflächen gefräst, je Stufe um eine Zuschnitttiefe weiter.

Bearbeitungsschritte werden in der CAD/CAM-Software als Pfade (engl. "Path") angelegt und sichtbar gemacht. Anhand der visualisierten Pfade kann man bereits erkennen, welchen Weg das Fräswerkzeug nehmen wird.

> Bilder Profil, Tasche, Bohrung, CAM-Pfade

### Haltestege

Wird ein Teil vollständig vom Werkstück getrennt, also ein Profil oder eine äußere Kontur gefräst, sollte man sogenannte Haltestege mit einplanen. Andernfalls könnte sich das gefertigte Teil im letzten Fräsvorgang verdrehen, kippen und mit dem Fräswerkzeug verkeilen. Die Folgen wären, dass das Teil nicht richtig gefertigt wird und im schlimmsten Fall droht ein Schaden an der Maschine.

Haltestege lassen sich im CAM-System einstellen. Im Endergebnis befinden sich die Haltestege am untersten Ende des Werkstücks und sind relativ schmal und flach, sodass sie sich leicht zu trennen sind.

> Bilder Haltestege, CAM-Pfad, Foto 

Das Fräswerkzeug nimmt im untersten Bereich des zu fräsenden Profils einen Pfad, bei dem es vor den Stellen, wo die Haltestege vorgesehen sind, ein Stück hoch fährt und diesen Teil ausspart, womit die Haltestege übrig bleiben.

Größe und Anzahl der Haltestege sollten so gewählt werden, dass sie das Teil sicher halten können, ansonsten sollten sie so klein wie möglich entworfen werden, damit man sie leicht durchtrennen kann.

Nach abgeschlossenem Fräsvorgang können die Haltestege je nach Material mit unterschiedlichen Methoden durchtrennt werden. Bei Holz kann beispielsweise eine Säge verwendet werden, bei Aluminium funktioniert es mit einer Metallsäge oder auch mit Hammer und Meißel gut. Nach dem Trennen sollten die Säge- oder Bruchstellen mit einer Feile nachbearbeitet werden.



## Vorbereitung und Ablauf eines CNC-Fräs-Auftrags

### Sicherheit

CNC-Maschinen sind potenziell gefährliche Maschinen und sollten nie ohne Einweisung und Freigabe benutzt werden. Fab Labs bieten in der Regel eine verpflichtende Sicherheitseinweisung an. Die Einzelheiten hierzu sind bei jeder Maschine anders, daher erfolgt in diesem Basislernmodul keine genauere Beschreibung.

### CAM, Simulation, G-Code-Datei

Ein relativ großer Aufwand beim CNC-Fräsen steckt in der Vorbereitung und der CAM-Software. Hat man alle Bearbeitungsschritte und CAM-Pfade definiert, sollte eine Simulation durchgeführt werden. Die meisten CAM-Programme verfügen über eine Simulationsfunktion, bei der der vollständige Fräsvorgang dargestellt wird, ähnlich wie bei einem Video, wobei man während der Simulation die 3D-Ansicht frei drehen kann.

Die Simulation kann auch in erhöhter Geschwindigkeit abgespielt werden. Während der Simulation wird sichtbar, wann an welcher Stelle Material abgetragen wird und wie das fertige Teil am Ende aussieht. Fallen noch Fehler auf, kann das CAM-Programm noch nachbearbeitet werden und man spart sich teure Fehler in der Fertigung.

Abschließend muss das CAM-Programm mithilfe eines Post-Prozessors (üblicherweise in der Software eingebaut) als eine G-Code-Datei exportiert werden. G-Codes beim CNC-Fräsen basieren auf dem gleichen Prinzip wie G-Codes beim 3D-Druck - mehr dazu in dem Basislernmodul zu 3D-Druck.

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

(Platzhalter)
