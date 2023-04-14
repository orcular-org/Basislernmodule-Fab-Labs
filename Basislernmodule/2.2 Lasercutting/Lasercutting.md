# Lasercutting
## Inhalt

1. [Einführung](#einführung)

2. [Grundlagen](#grundlagen)
   - [Materialien](#materialien)
   - [Komponenten eines Lasercutters](#komponenten-eines-lasercutters)
   - [Parameter: Leistung und Geschwindigkeit](#parameter-leistung-und-geschwindigkeit)
   - [Schnittbreite (kerf)](#schnittbreite-kerf)
   - [Vektorgrafik](#vektorgrafik)
   - [Software](#software)
   - [Unterschiede zu anderen digitalen Fertigungsmethoden](#unterschiede-zu-anderen-digitalen-fertigungsmethoden)

3. [Designtipps](#designtipps)
   - [Stecksysteme](#stecksysteme)
   - [3D-CAD und Projektion](#3d-cad-und-projektion)
   - [Living hinge](#living-hinge)
   - [Download von Vorlagen](#download-von-vorlagen)
   - [Häufige Fehler](#häufige-fehler)

4. [Vorbereitung und Ablauf eines Lasercuttings](#vorbereitung-und-ablauf-eines-lasercuttings)
   - [Sicherheit](#sicherheit)
   - [Lasercut-Datei](#lasercut-datei)
   - [Vorbereitung](#vorbereitung)
   - [Ablauf eines Lasercuttings](#ablauf-eines-lasercuttings)

[Lizenzinformationen](#lizenzinformationen)

[Bildnachweise](#bildnachweise)


## Einführung

Lasercutting (engl. für Laserschneiden) ist ein Prozess, bei dem ein Laserstrahl ein Material erhitzt, dieses dabei schmilzt oder verbrennt und somit trennt. Die entsprechenden Maschinen nennt man Lasercutter. Zusätzlich zum Schneiden sind Lasercutter auch in der Lage zu gravieren, d.h. das Material wird nicht vollständig durchtrennt, sondern nur an der Oberfläche bearbeitet, womit sich z.B. Schriftzüge oder Abbildungen in das Werkstück einbringen lassen.

Zu schneidende Werkstücke dürfen nicht zu dick sein, in der Regel verwendet man einige Millimeter dicke Platten. Gravuren können auch auf dickere Objekte gelasert werden, solange sie in die Höhenbegrenzung der Maschine passen. So lassen sich z.B. auch Möbel, Küchenbretter oder Stifte mit Holzgriff gravieren.

> Bilder: Lasercut, Gravur

Es gibt eine Vielzahl an unterschiedlichen Lasercuttern, die sich vor allem in ihrer Größe und Laserleistung unterscheiden.

Lasercutter, die man typischerweise in einem Fab Lab vorfindet, haben meistens einen Bearbeitungsraum von ca. 30 x 20 cm bis 70 x 40 cm. Zum Vergleich: ein DIN-A3-Format (typische Größe einer Holzplatte für Lasercutting) misst ca. 42 x 30 cm, passt also gut in die meisten Lasercutter. Die Leistung des Lasers liegt meistens zwischen 30 und 60 Watt. Mit derartigen Lasercuttern kann man z.B. dünne Platten aus Holz, Kunststoff, transparentem Acrylglas, Textil, Leder oder Pappe schneiden und gravieren. Zum Schneiden von Metallen (z.B. Aluminium oder Stahl) reicht die Leistung dieser Mittelklasse-Geräte in der Regel nicht aus, aber Gravuren auf Metall lassen sich damit durchaus realisieren.

> Bild: Lasercutter

Es gibt auch leistungsstarke Industriegeräte, die in der Lage sind, Metalle zu schneiden. Da diese Maschinen sehr teuer sind, wird man sie jedoch kaum in Fab Labs vorfinden, sondern eher in größeren Unternehmen.

Ein Lasercutter benötigt in der Regel eine digitale Grafikdatei als Eingabe, die alle Schnittlinien und zu gravierenden Abbildungen enthält. Schnittlinien müssen dabei als Vektorgrafik vorliegen (mehr dazu unten).

Mit Lasercutting lassen sich z.B. Namensschilder, Bilder, Aufsteller, Deko-Artikel oder Schmuck herstellen. Auch mehrteilige Produkte wie Aufbewahrungsboxen, kleine Schubladen, Spar- oder Spendendosen, Spielzeuge, Brettspiele, Puzzles oder Gehäuse für Elektronikprodukte lassen sich mit Lasercutting realisieren. Die besondere Stärke von Lasergravur liegt in der Herstellung von personalisierten oder individuellen Produkten, z.B. mit Namen, Portraits oder Logos.

> Bilder: Anregungen für Lasercutting

## Grundlagen

### Materialien

Grundsätzlich ist es sehr wichtig, vor dem Lasercutting zu klären, ob das Material bearbeitet werden darf, da es Stoffe gibt, die beim Laserschneiden lebensgefährliche Dämpfe erzeugen können. Mehr Infos finden sich in der unten stehenden Materialliste und im Abschnitt [Sicherheit](#sicherheit).

Hier eine Übersicht einiger beliebter und gut geeigneter Materialien für Lasercutting und -gravur:

- **Sperrholzplatte:** Sperrholz ist ein günstiges und sehr einfach zu laserschneidendes Material und gut für Einsteiger:innen geeignet. Gut verwendbar sind Platten mit Stärken um die 4 Millimeter. Beim Gravieren wird die innere Struktur des Holzes sichtbar, was oft zu einer interessanten Optik führt. Bastelsperrholz wird auch gern zum Sägen verwendet und kann in vielen Baumärkten oder auch online gekauft werden. Nachteile sind: Es ist sehr leicht und damit wenig stabil und bricht schnell. Zudem sind die Platten oft etwas uneben. Bei Projekten, bei denen es auf Präzision ankommt (z.B. [Stecksysteme](#stecksysteme)), kann dies zu Problemen führen - in dem Fall emfpiehlt es sich, auf MDF umzusteigen.
- **MDF:** MDF steht für "Mitteldichte Holzfaserplatte". MDF besteht aus feinen Holzfasern (meist zu ca. 80%) sowie Leim, Wasser und weiteren Zusatzstoffen; dieses Gemisch wird zu dichten Platten verpresst. Durch diese Herstellungsmethode sind MDF-Platten schwerer und stabiler als Sperrholzplatten, zudem sind sie sehr eben und haben eine gleichmäßige Dicke. MDF-Platten mit 2 bis 5 Millimeter Stärke lassen sich sehr gut laserschneiden und -gravieren. MDF ist z.B. in Onlineshops erhältlich und etwas teurer als Sperrholz.
- **Acrylglas:** Acrylglas, auch bekannt als "Plexiglas", ist ein durchsichtiger Kunststoff, der sich sehr gut laserschneiden lässt. Es gibt sowohl farbloses (volltransparentes) als auch farbiges (halbtransparentes) Acrylglas. Damit ist es sehr gut für Sichtfenster, Dekoration, Lampen, mit LED beleuchtete Aufsteller u.ä. geeignet. Im Hinblick auf Nachhaltigkeit lässt sich anmerken, dass Acrylglas nicht gut recyclebar ist - im Gegensatz zu einigen anderen Kunststoffen.
- **Pappe:** Nicht jede Pappe lässt sich gleich gut mit dem Lasercutter bearbeiten, daher sollte man beim Kauf auf gut für Lasercutting geeignetes Material achten. Da Pappe sehr leicht und instabil ist, eigent sie sich eher für dekorative Produkte. Zudem ist Pappe leicht entflammbar, weswegen man auf ein gutes Lüftungssystem im Lasercutter achten, den Lasercut-Prozess besonders gut beaufsichtigen und bei Flammenbildung stoppen sollte.
- **Textilien** 
- **Leder** 
- **Kork**
- **Kunststoffe (Plastik):** Bei Kunststoffen ist besondere Vorsicht geboten, da es viele Kunststoffsorten gibt, die beim Laserschneiden gesundheits- und lebensgefährliche Dämpfe erzeugen können, z.B. PVC. Es gibt jedoch auch Kunststoffe, die man relativ sicher schneiden und gravieren kann, z.B. Polypropylen (PP). Doch auch hier sollte man vorsichtig vorgehen und das Vorhaben mit dem Fab Lab bzw. den Inhaber:innen der Maschine absprechen. Manche Kunststoffe, z.B. HDPE, neigen dazu, nach dem Schneiden schnell wieder zusammenzuschmelzen - Laserschneiden von Kunststoff ist also herausfordernd, aber nicht unmöglich.
- **Metalle:** In Industrie- und Handwerksbetrieben gibt es Maschinen, die Metallbleche laserschneiden können. Da Lasercutter dieser Art sehr teuer sind, findet man sie eher selten in Fab Labs. Ein typischer Fab-Lab-Lasercutter kann jedoch durchaus Gravuren in Metall (z.B. Aluminium oder Stahl) einbringen.

> Bilder: Sperrholz-Gravur, weitere Materialien, evtl. LED-beleuchtete Acrylplatte

### Komponenten eines Lasercutters
Gute Lasercutter verfügen über ein geschlossenes Gehäuse und ein Abluftsystem. Es gibt auch günstige Lasercutter bzw. Lasergravierer mit offenem Aufbau. Bei diesen ist jedoch besondere Vorsicht geboten, da es leicht zu Unfällen kommen kann. In Fab Labs finden sich üblicherweise geschlossene Lasercutter mit Abluftsystem.

Die obere, aufklappbare Abdeckung ist in der Regel durchsichtig, sodass man den Lasercutprozess beobachten kann. Im Inneren befindet sich die gitterförmige Arbeitsfläche, auf die man die zu schneidende Platte legt. Die Arbeitsfläche lässt sich in der Höhe verstellen, was für die sogenannte Fokussierung des Lasers (Einstellung des Brennpunktes) sehr wichtig ist. Der Laser ist so kalibiert, dass er einen ganz bestimmten Abstand zum Werkstück haben muss, um ideal schneiden zu können. Jedes Mal, wenn man eine Platte einlegt, die eine andere Dicke als die vorherige Platte hat, sollte man den Lasercutter neu fokussieren. Manche Lasercutter können dies über eine Autofokus-Funktion automatisch durchführen, bei anderen muss man eine mitgelieferte oder eingebaute Fokussierhilfe als Abstandsmesser verwenden, um den Lasercutter manuell einzustellen.

Der Laserstrahl selbst wird oft im Inneren des Geräts erzeugt, über mehrere Spiegel umgeleitet und über Linsen fokussiert, sozusagen "scharf gestellt", ähnlich wie bei einer Brille. Der Laseraustritt ist so verbaut, dass er sich in zwei Achsen bewegen kann: in X-Richtung (nach links und rechts) und in Y-Richtung (nach vorne und hinten).

Einige Lasercutter verfügen über ein kompressorbetriebenes System, das Luft auf den Laserschneidepunkt bläst. Damit wird die Gefahr von Flammenbildung reduziert.

Eine Lüftungsanlage saugt während des Lasercuttings Luft aus dem Arbeitsraum des Gerätes ab und führt die Abluft über ein Filtersystem und einen Schlauch nach draußen. Damit werden unangenehme Gerüche verhindert und gesundheitsschädliche Dämpfe gefiltert und abgeführt.

> Bild Lasercutter mit Abluftsystem

### Parameter: Leistung und Geschwindigkeit
Beim Lasercutten gibt es vor allem zwei Parameter, die für den Prozess maßgeblich sind und vor jedem Betrieb richtig eingestellt werden müssen:

- **Leistung (in Watt oder %):** Die Leistung steht, vereinfacht gesagt, für die Energie oder Stärke des Laserstrahls.
- **Geschwindigkeit (in Millimeter pro Sekunde):** Gibt an, wie schnell sich der Laser über das Werkstück bewegt.

Bewegt sich der Laser langsam, hat er mehr Zeit, in das Material einzuwirken - er schneidet somit tiefer in die Platte. Bewegt er sich schnell, brennt er womöglich nur die Oberfläche des Werkstücks ab. Gleichzeitig hängt dies natürlich auch von der Leistung des Lasers ab. Durch das Zusammenspiel von Leistung und Geschwindigkeit lassen sich also unterschiedliche Ergebnisse erzeugen.

Je nachdem, was und wie man lasern möchte, muss man diese beiden Parameter unterschiedlich einstellen. Es gilt also, zunächst die Bedingungen zu klären:
- **Material:** Materialien wie z.B. Pappe benötigen eine geringere Laserleistung als z.B. Holz oder Kunststoffe.
- **Plattendicke:** Dicke Platten benötigen mehr Laserleistung, dünne Platten weniger Leistung.
- **Schneiden vs. Gravieren und Gravurtiefe**: Bei hoher Leistung bzw. geringer Geschwindigkeit geht der Laserstrahl durch das gesamte Material, d.h. es wird geschnitten. Bei geringer Leistung und hoher Geschwindigkeit wird nur die Oberfläche bearbeitet, es entsteht eine Gravur. Die Tiefe (und somit auch Sichtbarkeit bzw. Deutlichkeit) der Gravur lässt sich ebenfalls über die Parametereinstellung variieren. Durch tiefere und flachere Gravurflächen lässt sich eine Art Graustufeneffekt erzielen.

Oft finden sich in der Lasercutter-Software voreingestellte Profile, in denen man nur auswählen muss, welches Material und welche Plattenstärke man verwendet und ob man schneiden oder gravieren möchte - die idealen Werte für Leistung und Geschwindigkeit sind in den Profilen abgespeichert und werden bei Auswahl richtig eingestellt. In manchen Werkstätten oder Betriebsanleitungen finden sich auch Tabellen mit empfohlenen Werten für Leistung und Geschwindigkeit.

Möchte man jedoch davon abweichen oder ein bisher unerprobtes Material (für das noch kein Profil angelegt wurde) ausprobieren, muss man in der Regel mehrere Versuche durchführen, dabei die Werte Leistung und Geschwindigkeit variieren und sich so an das ideale Ergebnis herantasten.

> Bild: Screenshot Parameter-Einstellungen (z.B. Visicut)

Im Internet finden sich auch Testkarten, die für solche Materialtests entwickelt wurden. Dabei testet der Lasercutter in einem Durchlauf unterschiedliche Einstellungen aus. Anhand der fertig gelaserten Testkarte kann man dann das Ergebnis begutachten und die idealen Werte ablesen.

> Bilder Testkarte

### Schnittbreite (kerf)

Beim Trennen mittels Lasercutting wird entlang der Schnittlinie eine kleine Menge Material verbrannt, verdampft oder geschmolzen. Dies führt dazu, dass Trennlinien nicht "unendlich dünn" sind, sondern eine gewisse Breite haben - die sogenannte Schnittbreite. In vielen Programmen findet man auch den englischen Begriff für Schnittbreite, "kerf". Eine Schnittlinie kann man sich also eher wie einen Schnittkanal vorstellen - zwischen den beiden Teilen klafft eine winzig schmale Lücke.

Auch wenn die Schnittbreite mit bloßen Auge kaum erkennbar ist - sie ist oft nur einen Bruchteil eines Millimeters breit - ist es bei einigen Anwendungen wichtig, sie im Hinterkopf zu behalten. Dies gilt z.B. für Stecksysteme (mehr dazu unten im Abschnitt [Stecksysteme](#stecksysteme)), bei denen es auf einen guten Sitz der gesteckten Teile ankommt. 

Um eine Vorstellung von der Schnittbreite zu bekommen, kann man ein lasergeschnittenes Teil oder Loch mit einem Messschieber ausmessen und den Messwert mit dem Wert in der Vektorgrafik vergleichen - man wird feststellen, dass es leichte Abweichungen gibt. Anhand der Differenz zwischen gezeichneter und gemessener Länge kann man die Schnittbreite ermitteln. Diesen Wert kann man dann beim Zeichnen der Vektorgrafik als Schnittlinienversatz berücksichtigen.

> Bild kerf - in der Bildunterschrift: kleine Beispielrechnung

### Vektorgrafik
Für Lasercutting ist es wichtig, sich mit dem Konzept von Vektorgrafiken vertraut zu machen.

Eine Vektorgrafik ist eine Computergrafik, die aus Grundformen wie Linien, Kreisen, Polygonen (mehreckige Formen) und Kurven (Splines) aufgebaut ist. Die digitale Datei einer Vektorgrafik enthält dabei alle notwendigen Informationen, um die Grafik eindeutig darzustellen, z.B. Position und Länge von Linien oder Durchmesser von Kreisen. Zudem können u.a. Strichstärke und Farbe von Linen oder Füllfarbe von Formen gespeichert werden.
Damit unterscheiden sich Vektorgrafiken grundsätzlich von sogenannten Rastergrafiken, die über rasterartig angeordnete, farbige Bildpunkte (Pixel) aufgebaut sind.

Raster- und Vektorgrafiken lassen sich vor allem über zwei Methoden leicht unterscheiden:
- **Qualitätsverlust beim Skalieren (zoomen):**
  - Eine **Rastergrafik** wird beim Vergrößern (hineinzoomen) immer undeutlicher, irgendwann erkennt man einzelne Pixel
  - Eine **Vektorgrafik** hingegen bleibt beim Vergrößern stets scharf, da die Linien und Flächen nicht als Pixel, sondern über das oben beschriebene Verfahren definiert sind
- **Dateiformat:**
  - **Rastergrafiken** haben Dateiformate wie JPG/JPEG, PNG, GIF oder TIFF.
  - **Vektorgrafiken** haben Dateiformate wie SVG, DXF, AI oder unter gewissen Bedingungen auch PDF.

> Bilder: Raster- vs. Vektorgrafik, Beispiel Vektorgrafik für Lasercutting

Um eine Grafikdatei für Lasercutting verwenden zu können, muss diese in einem Vektorformat vorliegen. Hintergrund ist, dass die Linien und Kurven einer Vektorgrafik über eine Software in Steuersignale für den Lasercutter umgewandelt werden, wobei der Laser jede Linie und Kurve abfährt und laserschneidet. Der Laser "kennt" damit Anfangs- und Endpunkt einer jeden Linie und Kurve und fährt sie in einem Durchlauf ab. Mit pixelbasierten Rastergrafiken wäre dies nicht möglich, da die Software nicht erkennen kann, welche Pixel zu einer Linie gehören.

Für Gravuren hingegen können auch Rastergrafiken verwendet werden. Der Laser fährt dann die Grafik - sozusagen zeilenweise - von oben nach unten ab; jede Zeile von links nach rechts. Dunklere Pixel werden tiefer eingraviert, helle Pixel weniger tief und leere bzw. weiße Pixel werden ausgelassen, also nicht graviert. Es können auch farbige Grafiken verwendet werden, wobei sie von der Software automatisch in Graustufen umgewandelt werden.

Dateiformate wie SVG können auch eine Kombination aus Vektorgrafik und Rastergrafik enthalten, wobei Vektorlinien geschnitten und Rastergrafiken graviert werden - sofern man nicht etwas anderes einstellt.

> Bilder: Vektorgrafik, kombinierte Vektor- und Rastergrafik

In manchen Programmen ist es auch möglich, die Reihenfolge der Laserschnitte festzulegen, indem man den Vektorlinien unterschiedliche Farben gibt oder sie auf verschiedene Ebenen legt. Dies kann sinnvoll sein, wenn man z.B. erreichen möchte, dass zuerst die Inneren und zum Schluss die äußersten Linien geschnitten werden. Würde man mit dem äußersten Umriss anfangen, könnte die Platte nach dem Ausschneiden leicht kippen. Die später geschnittenen inneren Linien und Formen könnten dann verzerrt geschnitten werden oder der Laser schneidet gar nicht erst durch die gesamte Platte. Daher empfiehlt es sich, Schnittlinien stets in der Reihenfolge von innen nach außen zu schneiden.

> Bilder: farbige Vektorgrafik, Laserschnitt der Grafik - in Bildunterschrift: Reihenfolge der farbigen Linien beschreiben

### Software
Zum Zeichnen von Vektorgrafiken gibt es viele unterschiedliche Programme. Meistens wird derartige Software im professionellen Bereich eingesetzt, was die Softwarelizenzen relativ teuer macht. Es gibt aber auch gute kostenlose Alternativen:

Eine beliebte und kostenlose Open-Source-Software für **Vektorgrafikbearbeitung** ist **Inkscape**.

- **Inkscape:** https://inkscape.org

> Bild: Inkscape

Für das Zeichnen und Erstellen von **Rastergrafiken** gibt es ebenfalls viele, teilweise teure Programme.
Als kostenlose und Open-Source-basierte Alternativen gibt es:

- **Krita:** https://krita.org
- **GIMP:** https://www.gimp.org

> Bilder: Krita, GIMP

Je nach Lasercutter-Hersteller und -Modell benötigt man oft noch eine spezielle Software, die die Vektor- und Rastergrafiken in Steuersignale umwandelt und an den Lasercutter sendet. Diese Software wird üblicherweise mit dem Lasercutter mitgeliefert.

Viele Lasercutter nutzen die kostenlose Open-Source-Software Visicut (https://visicut.org). Beliebt, wenn auch nicht kostenlos, ist auch die Software Lightburn (https://lightburnsoftware.com/). Mit Lightburn können Vektorgrafiken gezeichnet und auch direkt aus der Software heraus an den Lasercutter gesendet werden, zudem verfügt das Programm über zahlreiche Komfortfunktionen speziell für Lasercutting und -gravieren.

### Unterschiede zu anderen digitalen Fertigungsmethoden
Der wichtigste Unterschied zwischen **Lasercutting und 3D-Druck** ist, dass Lasercutting in der Regel deutlich schneller abläuft als 3D-Druck. 3D-Drucke können oft mehrere Stunden dauern, während Lasercut-Teile oft in wenigen Minuten fertig sind. Je nach Form und Komplexität kann sich dies im Einzelfall aber natürlich auch ganz anders verhalten. Bevor man also ein Teil 3D-druckt, lohnt es sich, zu überlegen, ob man es auch mit Lasercutting realisieren kann, sofern Form und Material dies zulassen (mehr zum Thema im Basislernmodul 3D-Druck).

> Bild Vergleich der Dauer Lasercut vs. 3D-Druck

Auch zwischen **Lasercutting und CNC-Fräsen** gibt es typische Unterschiede. Während beim Lasercutten nur flache Teile in gleichmäßiger Dicke herstellbar sind (sozusagen "2D-Teile"), können mit CNC-Fräsen auch dreidimensionale Formen gefertigt werden. Zudem können Lasercutter nur begrenzt dicke Platten schneiden - je nach Material nur einige Millimeter bis ca. 1-2 Zentimeter Dicke - während mit CNC-Fräsen deutlich dickere Platten durchtrennt werden können. Außerdem können viele CNC-Fräsen auch Aluminium oder ähnlich harte Materialien bearbeiten, was mit Lasercuttern oft nicht möglicht ist (mehr zum Thema im Basislernmodul CNC-Fräsen).

## Designtipps

### Stecksysteme
Eine beliebte Anwendung von Lasercutting besteht in Stecksystemen - vor allem für Holzplatten. Dabei werden mehrere Teile so geformt, dass sie rechtwinkling zueinander gesteckt werden können. Eine Möglichkeit besteht darin, einen Zapfen in ein eckiges Loch zu stecken. Eine andere Methode ist der Einsatz von zinnenartigen Rändern, womit sich ganze Boxen oder ähnliche Strukturen zusammenstecken lassen.

> Bilder Stecksysteme (einmal mit Zapfen in Loch, einmal mit Zinnen / Tabbed box)

Dabei muss sichergestellt werden, dass die Zapfen nicht zu locker stecken, sondern einen festen Sitz haben. Andererseits darf die Lücke auch nicht zu eng sein, da man den Zapfen sonst nicht hineingedrückt bekommt. Hierbei muss auch die Schnittbreite (kerf) berücksichtigt werden.

Eine oft gut funktionierende Daumenregel lautet, dass Lücke und Zapfen in gleichen Dimensionen gezeichnet werden (also gleich breit und gleich hoch). Bedingt durch die Schnittbreite (kerf) des Lasers werden Lücken ohnehin etwas weiter und Zapfen etwas schmaler ausfallen als in der Zeichnung, womit der Sitz oft relativ gut ist, manchmal aber etwas zu locker. Man kann die Verbindung auch etwas enger gestalten und die Steckverbindungen vorsichtig mit einem Gummihammer einschlagen. Steckverbindungen können in der Regel auch mehrmals gelöst und wieder zusammengesteckt werden, dabei nutzt sich das Material jedoch jedesmal etwas ab, sodass die Verbindung evtl. nicht mehr fest sitzt. Auch die Verwendung von Klebstoff oder Leim ist möglich.

Bevor man sich die Mühe macht und eine steckbare Box aufwendig selbst zeichnet, empfiehlt es sich, auf bestehende **Software-Hilfsmittel** zurückzugreifen:

- Für Inkscape gibt es die kostenlose Erweiterung [Lasercut tabbed box](https://inkscape.org/de/~Neon22/%E2%98%85lasercut-tabbed-box). Damit lassen sich Länge, Breite und Höhe sowie Zapfenlänge und Schnittbreiten-Versatz (kerf) für verschiedene boxartige Produkte als Vektorgrafik generieren. Diese Vektorgrafik kann auch nachträglich in Inkscape bearbeitet werden.
- Ein weiteres Tool heißt "Boxes.py" (https://www.festi.info/boxes.py/). Hierfür ist keine Softwareinstallation notwendig, die Anwendung läuft im Browser. Dieses Open-Source-Projekt bietet eine Vielzahl von verschiedenen steckbaren Lasercut-Bausätzen, z.B. Kisten, Schubladen, Fächer oder Truhen mit Deckeln. Es können Parameter wie Länge, Breite, Höhe und Schnittbreitenversatz eingegeben werden, abschließend wird eine downloadbare SVG-Vektorgrafik erzeugt, die man direkt für Lasercutting verwenden oder vorher noch bearbeiten kann. Einige Bausätze enthalten auch "living hinges", mehr dazu [unten](#living-hinge).

> Bild tabbed box als Vektorgrafik

### 3D-CAD und Projektion
Statt Lasercut-Projekte in 2D zu zeichnen, kann man auch eine 3D-CAD-Software verwenden (mehr dazu im Basislernmodul 3D-Design und CAD). Auf diese Weise kann man ein aus mehreren Lasercut-Teilen bestehendes Produkt entwerfen und in 3D darstellen. Vorteil an dieser Methode ist, dass man direkt sehen kann, wie das fertige, zusammengesteckte Produkt aussehen wird - beim Design in 2D sieht man die einzelnen Teile nur nebeneinander und benötigt etwas Vorstellungskraft, um sich ein Bild vom fertigen 3D-Produkt zu machen.

Zudem lassen sich auf diese Weise Produkte entwerfen, die nicht nur Lasercut-Teile, sondern beispielsweise auch 3D-gedruckte oder CNC-gefräste Teile, Schrauben oder andere Elemente enthalten.

Viele CAD-Programme (z.B. FreeCAD) verfügen über Tools, mit denen man die 3D-modellierten Teile für das Lasercutting auf eine 2D-Ebene projizieren und als Vektorgrafik exportieren kann, die man dann für Lasercutting verwenden kann.

> Bild 3D-CAD + Projektion + Kombination mit 3D-Druck

### Living hinge
Eine beliebte Technik im Lasercut-Design nennt sich "living hinge" (engl. für "Biegescharnier"). Gewöhnliche Scharniere bestehen aus mehreren Bauteilen, Biegescharniere hingegen aus nur einem einzigen Teil, welches an einer oder an mehreren Stellen dünnwandig ausgestaltet oder eng geschnitten ist. Biegescharniere finden sich z.B. bei Eierpappkartons oder bei Brotdosen aus Kunststoff.

Ein living hinge lässt sich mit Lasercutting herstellen, indem viele, sehr eng aneinander liegende und leicht versetzte Schnittlinien in die Platte geschnitten werden. Die Platte wird dadurch sehr flexibel und lässt sich an der Stelle leicht biegen. Dies geht vor allem mit dünnen Holzplatten gut. Man kann es für Scharnierfunktionen, z.B. für Deckel von Truhen, verwenden oder man nutzt es, um abgerundete Kanten zu erzeugen.

> Bilder living hinge (Vektorgrafik, Foto)

### Download von Vorlagen
Statt eigene Lasercut-Zeichnungen zu entwerfen, kann man auch fertige Vorlagen aus dem Internet verwenden. Viele Portale, die eigentlich eher für 3D-Druck-Dateien gedacht sind, enthalten auch Projekte für Lasercutting. Man findet sie, indem man einfach "laser cut" oder "lasercutting" in die Suchleiste eingibt. Mehr zu dem Thema im Basislernmodul Verwendung von 3D-Modellen aus dem Internet.

### Häufige Fehler
Ein häufiger Anfängerfehler beim Erstellen von Lasercut-Vektorgrafiken ist, die Schnittlinien nicht richtig zu formatieren, sodass die Linien graviert und nicht geschnitten werden. Je nach Lasercutter und Software gibt es bestimmte Dinge, die beachtet werden müssen, damit die Software eine Linie als Schnittline erkennt und sie nicht graviert. Es lohnt sich also, vor Start des Lasercuttings die Einstellungen nochmals genau zu prüfen. 

Gelegentlich passiert auch ein Fehler, bei dem der Lasercutter jede Linie zweimal schneidet. Dies liegt meistens daran, dass man doppelte Linien in der Vektorgrafik hat. Da sie jedoch übereinanderliegen, erkennt man es am Bildschirm nicht. Hier sollte man die Tools der Software nutzen, um zu prüfen, ob doppelte Linien vorhanden sind (z.B. Ebenen nacheinander ausblenden oder Linien probeweise löschen, anschließend ggf. rückgängig machen).

Schließlich passiert es auch oft, dass ein fertig geschnittenes Bauteil nicht die gewünschte Größe hat, z.B. nur halb so groß ist, wie gewünscht. Man sollte also die Maße der Vektorgrafik genau prüfen und auch nachschauen, ob die richtigen Einheiten eingestellt sind (z.B. Millimeter und nicht Zoll).

## Vorbereitung und Ablauf eines Lasercuttings

### Sicherheit
Ein Lasercutter ist eine potenziell gefährliche Maschine und sollte niemals ohne Einweisung oder Befugnis benutzt werden. Fab Labs bieten in der Regel Einweisungen in die Sicherheit und Benutzung an, die man absolviert haben muss, bevor man das Gerät benutzen darf.

Bei ordnungsgemäßem Betrieb entsteht keine unmittelbare Gefahr für den Menschen. Falls der Betrieb jedoch nicht ordnungsgemäß verläuft, z.B. wegen Beschädigung des Gehäuses, bei Umbau und Umgehung der Sicherheitstechnik oder durch unübliche Reflexion und Streuung des Laserslichts, kann die Laserstrahlung vor allem für die Augen, aber auch für die Haut sehr gefährlich werden. Die Laserstrahlung eines Lasercutters ist unsichtbar, was die Gefahr noch vergrößert. Bei Unsicherheiten ist besondere Vorsicht geboten. Bei Defekten oder unüblichem Verhalten sollte eine Maschine nicht benutzt und das Fab-Lab-Personal verständigt werden.

Während des Lasercuttings entsteht oft ein hell leuchtender Punkt auf der bearbeiteten Platte. Man sollte es möglichst vermeiden, direkt in dieses helle Licht zu blicken, da es die Augen schädigen kann.

Neben der Gefahr durch Laserstrahlung selbst besteht auch eine Brandgefahr. Es ist wichtig, darauf zu achten, dass während des Laserns die Belüftung eingeschaltet ist und der Filter regelmäßig gewechselt wird, vor allem bei unüblicher Geruchs- oder Rauchbildung.

Ein Lasercutter sollte während des Betriebs nie unbeaufsichtigt gelassen werden. Man sollte stets in der Nähe bleiben und im Blick behalten, ob sich unübliche Flammen bilden. Im Zweifel sollte der Betrieb gestoppt werden. Man sollte wissen, wo sich der Notausschalter des Geräts befindet. Viele Lasercutter sind auch so konstruiert, dass sie beim Öffnen der oberen Abdeckung automatisch den Betrieb stoppen.

Für den unwahrscheinlichen Fall, dass ein Brand entsteht, sollte stets ein CO2-Feuerlöscher verwendet werden. Man sollte den Aufenthaltsort des CO2-Feuerlöschers kennen und sich mit seiner Bedienung vertraut machen.

Schließlich ist es wichtig zu wissen, welche Materialien man lasern darf und welche nicht. Dies ist stets mit dem Personal zu klären. Einige Kunststoffe, z.B. PVC, dürfen auf keinen Fall gelasert werden, da sie dabei gesundheitsgefährdende bis lebensgefährliche Dämpfe erzeugen.

### Lasercut-Datei
Wie in den oberen Abschnitten beschrieben, benötigt man für das Lasercutting eine Grafikdatei - Schnittlinien als Vektorgrafik, Gravuren als Rastergrafik. Wie die Daten an den Lasercutter übertragen werden, ist bei jedem Lasercutter anders. Oft wird eine spezielle Software benötigt. Viele Programme bieten eine Funktion an, die eine Schätzung der Betriebsdauer - aufgeschlüsselt nach Schneiden und Gravieren - berechnet. Bevor man den Betrieb startet, empfiehlt es sich, anhand der Werte zu prüfen, ob der Auftrag wie gewünscht durchgeführt wird. Ist etwa die berechnete Zeitdauer für Gravur unüblich hoch und die Dauer für das Schneiden gleich null, so wurde die Vektorgrafik evtl. nicht erkannt.  

### Vorbereitung
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

### Ablauf eines Lasercuttings
Üblicherweise beginnt ein Lasercutter zunächst mit den Gravuren. Der Grund liegt darin, dass ein einmal ausgeschnittenes Teil unter Umständen leicht kippen kann - nachträgliche Gravuren würden somit auf eine schräge Oberfläche treffen und nicht korrekt ausgeführt werden.

Anschließend werden die Schnittlinien ausgeführt. Das Schneiden geht für gewöhnlich deutlich schneller als das Gravieren.

Nach abgeschlossenem Lasercutting empfiehlt es sich, noch kurz zu warten, damit die Belüftungsanlage Rauch und Dämpfe absaugen kann. Danach kann die Klappe geöffnet und die Teile können entnommen werden.
Falls ein Schnitt nicht richtig durchgegangen ist, liegt dies entweder an einem falsch eingestelltem Profil (falsche Parametereinstellungen), an einer Unebenheit der Platte oder an anderen Ursachen. Oft kann es helfen, einen Lasercut-Auftrag einfach ein zweites mal auszuführen, sodass die halbfertigen Schnitte beim erneuten Durchgang ganz durchgeschnitten werden. Dabei muss die Platte exakt an die gleiche Position gelegt werden (möglichst mit Hilfe des Anschlags am Rand) oder gleich liegen gelassen werden. Es ist auch möglich, direkt am Computer einzustellen, dass der Laser zwei Durchgänge schneiden soll.

# Lizenzinformationen

(Platzhalter)

# Bildnachweise

(Platzhalter)
