---
title: Zusammenfassung von Skript von SWE
draft: false
tags:
	- zusammenfassungen
date: 2025-02-03
---
%% Copyright (c) Philipp Wagner 2025 %%

```table-of-contents
```
# 1. Begriffe
- **Software Engineering**: ingenieurmäßige Entwicklung von Software
- **Auftraggeber**: Person der die Software für einen bestimmten Einsatzzweck haben möchte
- **Auftragnehmer**: Personen, welche wissen wie man Software professionell entwickelt
- **UML**: Unified Modeling Language
- **Anwendungsfalldiagramm**: beschreibt die Zusammenhänge zwischen einer Menge von Anwendungsfällen und den daran beteiligten Akteuren
- **Aktuer**: 
	- ist außerhalb des betrachteten Systems
	- repräsentiert etwas, das im System vorhandene Anwendungsfälle benutzt
	- kann eine Person oder ein anderes System sein (insbesondere ein anderes Computersystem)
- **Anwendungsfall (engl. Use Case):**
	- beschreibt funktionale Anforderungen an das System
	- Sequenz von zusammenhängenden Interaktionen, welche der Akteur im Dialog mit System ausführt
	- Ergebnis ist für Akteur ein messbarer Wert, d.h. ein sichtbarer, quantifizierbarer oder qualifizierbarer Einfluss auf das System
	- beschreibt, was System leisten muss, nicht wie
	- kann verschiedene Ablaufvarianten umfassen
	- wird stets von Akteur ausgeführt
# 2. Einführung
- Auftraggeber teilt dem Auftragnehmer mit welche Software erstellt werden soll
- Ergebnisse müssen von Auftraggeber abgenommen werden
- Entwicklung geschieht in mehreren Stufen:
	- Aufnahme und Analyse der Anforderungen
	- technischer Entwurf des Systems
	- Programmierung im engeren Sinne
	- Test
- Dadurch entstehen mehrere Probleme:
	- u. a. zu früher/später Wechsel zur nächsten Stufe
# 3. Funktionale Anforderungen
- 2 Personengruppen, die bei der Erstellung von Software beteiligt sind
	- Auftraggeber
		- legt fest was Software leisten soll
	- Auftragnehmer
- Beide Gruppen müssen bei der Aufnahme u. Ausarbeitung der Anforderungen zusammenarbeiten
- Anwendungsfalldiagramm beschreibt kein Verhalten und keine Abläufe
- jeder Anwendungsfall hat eine Anwendungsfallbeschreibung
- Anwendungsfälle und Anwendungsfalldiagramm 
	- ein Hilfsmittel zur Ermittlung und Verwaltung von funktionalen Anforderungen
	- dienen der Kommunikation mit zukünftigen Anwendern (Auftraggeber/Fachabteilung)
	- beschreiben das externe Systemverhalten u. Interaktion der Außenstehenden mit dem System
	- keine Aussage darüber, wie das System dies leistet.
- Anwendungsfälle
	- bilden die Basis für weitere Entwicklungsschritte
	- dienen bspw. der Erzeugung von Testfällen
	- können auch Ausnahme- und Fehlverarbeitung enthalten
		- beschreiben **keine** technischen Fehler (Datenbank nicht verfügbar)
		- beschreiben fachliche Fehler
# 4. Nicht funktionale Anforderungen

Nicht funktionale Anforderungen beschreiben keine spezifischen Funktionen eines Software-Systems, sondern beziehen sich meist auf das gesamte System oder haben keine direkten Auswirkungen auf die Software-Implementierung. Sie lassen sich in folgende Kategorien unterteilen:

- **Technologische Anforderungen**
- **Qualitätsanforderungen**
- **Anforderungen an die Benutzungsoberfläche**
- **Anforderungen an sonstige Lieferbestandteile**
- **Anforderungen an durchzuführende Tätigkeiten**
- **Rechtlich-vertragliche Anforderungen**

Die ersten drei betreffen die Realisierung des Systems, während die letzten drei unabhängig davon sind.

## Technologische Anforderungen

Diese Anforderungen beeinflussen direkt die verwendeten Technologien und die Einbettung des Systems in seine Umgebung. Dazu gehören:

- Vorgaben zur **Hardware** (Prozessor, Hauptspeicher, Festplattenkapazität, Peripheriegeräte).
- Vorgaben zur **Systemsoftware** (Betriebssystem, Datenbanksysteme, Webserver, Browser-Versionen).
- Vorgaben zur **Entwicklungsumgebung** (Programmiersprache, Entwicklungswerkzeuge).

**Beispiele:**
- Das System muss unter Windows 10 laufen.
- Oracle DBMS in Version xy ist zu verwenden.
- Die Programmiersprache Java ist vorgeschrieben.

## Qualitätsanforderungen

Nach **ISO/IEC 25010** umfassen Qualitätsanforderungen acht Merkmale mit Teilmerkmalen:

### Funktionale Eignung
- **Vollständigkeit**: Erfüllt alle spezifizierten Aufgaben.
- **Genauigkeit**: Ergebnisse mit der erforderlichen Präzision.
- **Angemessenheit**: Unterstützt Nutzerziele effektiv.

### Effizienz
- **Zeitverhalten**: Antwort- und Verarbeitungszeiten.
- **Verbrauchsverhalten**: Nutzung von Ressourcen.
- **Kapazität**: Systemgrenzen, z. B. max. 256 MB RAM.

### Kompatibilität
- **Koexistenz**: Keine negativen Einflüsse auf andere Systeme.
- **Interoperabilität**: Fähigkeit zur Zusammenarbeit mit anderen Systemen.

### Benutzbarkeit
- **Erkennbarkeit**: Nutzer erkennen, ob das System ihren Bedürfnissen entspricht.
- **Erlernbarkeit**: Aufwand für das Erlernen der Bedienung.
- **Bedienbarkeit**: Aufwand für die Nutzung.
- **Fehlerschutz**: Schutz vor Fehlbedienung.
- **Ästhetik**: Gestaltung der Benutzeroberfläche.
- **Zugang**: Barrierefreiheit und Erreichbarkeit.

### Verlässlichkeit
- **Reife**: Stabile Funktionalität unter normalen Bedingungen.
- **Verfügbarkeit**: System ist erreichbar (z. B. 99,8% zwischen 8:00 und 18:00 Uhr).
- **Fehlertoleranz**: Funktioniert trotz Fehlern weiter.
- **Wiederherstellbarkeit**: Schnelle Wiederherstellung nach Absturz.

### Sicherheit
- **Vertraulichkeit**: Schutz vor unbefugtem Zugriff.
- **Integrität**: Schutz vor Manipulation.
- **Nicht-Abstreitbarkeit**: Nachweisbarkeit von Ereignissen.
- **Zurechenbarkeit**: Aktionen sind Personen zuordenbar.
- **Authentizität**: Sicherstellung der Identität von Nutzern und Ressourcen.

### Wartbarkeit
- **Modularer Aufbau**: Änderungen an einem Modul beeinflussen andere minimal.
- **Wiederverwendbarkeit**: Code kann in anderen Projekten genutzt werden.
- **Analysierbarkeit**: Fehler lassen sich einfach identifizieren.
- **Änderbarkeit**: Anpassbarkeit ohne negative Folgen.
- **Testbarkeit**: Einhaltung von Testkriterien ist prüfbar.

### Übertragbarkeit
- **Anpassbarkeit**: Software kann für verschiedene Umgebungen konfiguriert werden.
- **Installierbarkeit**: Software lässt sich in unterschiedlichen Systemen installieren.
- **Austauschbarkeit**: Software kann durch eine andere ersetzt werden.

## Anforderungen an die Benutzungsoberfläche

Diese Anforderungen betreffen das visuelle und akustische Erscheinungsbild des Systems. Sie definieren, wie die funktionalen Anforderungen für den Benutzer dargestellt und bedient werden sollen.

Zu den Themenbereichen gehören:

- **Bedienkonzept**: Art der Interaktion (z. B. Maus- und/oder Tastaturbedienung). Einheitlichkeit mit bestehenden Systemen (z. B. Office-Pakete).
- **Rahmenbedingungen für die Gestaltung**: Vorgaben für Layout, Benutzerwissen und Erfahrung.
- **Erscheinungsbild der Bedienelemente**: Unternehmensvorgaben zu Farben, Schriftarten und -größen, sowie Internationalisierung.
- **Ergonomische Standards**: Richtlinien wie **ISO 9241-10** (Grundsätze der Dialoggestaltung).

Anforderungen an die Benutzungsoberfläche kommen von den zukünftigen Benutzern (Dauernutzer, gelegentliche Nutzer, Wartungstechniker) sowie aus Marketing und Vertrieb.

**Dokumentation:** 
- Textform ist selten geeignet.
- Besser sind visuelle Darstellungen, Tabellen oder Prototypen.

## Anforderungen an sonstige Lieferbestandteile

Diese Anforderungen umfassen alle zusätzlichen Produkte, die für den Betrieb des Systems erforderlich sind, wie:

- **Dokumentation** (Hardware-/Software-Dokumentation)
- **Handbücher** (Benutzer-, Installations-, Wartungshandbücher)
- **Schulungsunterlagen**
- **Installationssoftware**

**Herkunft:** Diese Anforderungen kommen von den zukünftigen Nutzern, dem Betriebsteam und der IT-Abteilung.

**Dokumentation:** Meist in Textform.

## Anforderungen an durchzuführende Tätigkeiten

Diese Anforderungen definieren Standards und Prozesse für die Entwicklung, Einführung oder den Betrieb des Systems. Beispiele:

- **Einsatz von Standards oder Methoden**, z. B. **V-Modell XT** (Vorgehensmodell für Bundesprojekte).

**Dokumentation:** In Textform.

## Rechtlich-vertragliche Anforderungen

Diese Anforderungen betreffen die rechtlichen und vertraglichen Rahmenbedingungen für die Entwicklung und Nutzung des Systems. Sie regeln:

- **Rechte** an Software-Artefakten (Nutzung, Weiterverwendung)
- **Gewährleistung** für Leistungen und Produkte
- **Verschwiegenheitspflichten**
- **Mitwirkungspflichten** des Auftraggebers

**Herkunft:** Einkauf, Vertrieb, Rechtsabteilung.

**Dokumentation:** In Textform.

# 5. Domänenmodell

Das **Domänenmodell** beschreibt den Problembereich eines Softwaresystems durch Klassen, Attribute und Beziehungen. Es stellt reale oder gedankliche Gegenstände dar, jedoch keine Software-Artefakte wie GUI-Fenster oder Datenbanken.

## Bedeutung des Domänenmodells

- Reduziert die Lücke zwischen Anforderungen und technischer Umsetzung.
- Viele Klassen aus dem Domänenmodell finden sich später im Software-Design wieder.

## Objekte und Klassen

- **Objekte**: Reale oder gedankliche Gegenstände mit Eigenschaften.
- **Klassen**: Abstraktion von Objekten mit gemeinsamen Eigenschaften.
- **Attribute**: Merkmale einer Klasse.
- **Beziehungen**: Verbindungen zwischen Objekten und Klassen.

**Namensgebung:**
- Objektnamen beginnen mit Kleinbuchstaben (z. B. `meinBuch`).
- Klassennamen beginnen mit Großbuchstaben (z. B. `Buch`).
- Attribute sind Substantive und beginnen mit Kleinbuchstaben.

**Multiplizität:**
- `[Min..Max]` gibt an, wie viele Werte ein Attribut haben kann.
  - `autor[1..2]` → genau 1 bis 2 Autoren.
  - `autor[0..*]` → 0 bis beliebig viele Autoren.

## Beziehungen zwischen Klassen

- Beziehungen zwischen Objekten werden im **Objektdiagramm** als Linien dargestellt.
- Beziehungen zwischen Klassen sind Linien im **Klassendiagramm**.
- **Leserichtung** wird durch ein Dreieck angezeigt.
- **Rollennamen** beschreiben die Funktion einer Klasse in der Beziehung.

**Multiplizitäten:**
- `1` → genau eine Instanz.
- `0..1` → maximal eine Instanz.
- `*` → beliebig viele Instanzen.

**Komposition:**
- Eine **Ganzes-Teile-Hierarchie**, bei der Teile ohne das Ganze nicht existieren können.
- Beispiel: Eine `Rechnung` besteht aus mehreren `Rechnungspositionen`.

## Konstruktion eines Domänenmodells

1. **Klassen identifizieren**:
   - Substantive aus Anforderungsdokumenten extrahieren.
   - Unterscheiden, ob es sich um eine Rolle oder ein Attribut handelt.

2. **Attribute zuordnen**:
   - Sind meist primitive Datentypen (String, Zahl, Datum).
   - Keine technischen Details enthalten.

3. **Beziehungen modellieren**:
   - Dauerhafte Verbindungen berücksichtigen.
   - Nicht zu viele Beziehungen modellieren, um das Modell übersichtlich zu halten.

## Spezielle Arten von Beziehungen

- **Komposition**: Teile sind vom Ganzen existenzabhängig (`Rechnung` → `Rechnungsposition`).
- **Assoziative Klassen**: Beziehungen mit zusätzlichen Attributen (z. B. `Ergebnis` in `Student` → `Prüfung`).
- **Analysemuster**:
  - **Liste**: Eine Gruppe gleichartiger Objekte (`Bestellung` → `Bestellposition`).
  - **Exemplartyp**: Ein Objekt mit mehreren Instanzen (`Buchtitel` → `Buch`).
  - **Baugruppe**: Eine flexible **Ganzes-Teile-Beziehung**, in der Teile ausgetauscht werden können (`Auto` → `Motor`).

## Geschäftsregeln

- Regeln, die unabhängig von der Software gelten (z. B. **Umsatzsteuer bei Rechnungen**).
- Werden textuell dokumentiert und ergänzen das Domänenmodell.

# 6. Sequenzdiagramm

Ein **Sequenzdiagramm** stellt den Austausch von Nachrichten zwischen Akteuren und Objekten in einer zeitlich begrenzten Situation dar. Es zeigt die Reihenfolge und den Ablauf der Interaktionen.

## Elemente eines Sequenzdiagramms

- **Objekte**: Werden durch Rechtecke mit gestrichelten Linien (Lebenslinien) dargestellt.
- **Akteure**: Benutzer oder externe Systeme, die mit dem System interagieren.
- **Nachrichten**: Kommunikation zwischen Objekten, dargestellt als Pfeile mit Nachrichtenname.

## Nachrichtentypen

1. **Synchrone Nachricht**:
   - Sender wartet auf die Antwort.
   - Dargestellt mit **voller Pfeilspitze**.
   - Beispiel: Funktionsaufruf innerhalb eines Systems.

2. **Asynchrone Nachricht**:
   - Sender wartet nicht auf die Antwort.
   - Dargestellt mit **offener Pfeilspitze**.
   - Beispiel: Ereignisgesteuerte Kommunikation.

3. **Rückgabe-Nachricht**:
   - Dient der Übermittlung des Ergebnisses einer synchronen Nachricht.
   - Dargestellt mit **gestrichelter Linie und offener Pfeilspitze**.

## Kontrollstrukturen in Sequenzdiagrammen

- **Bedingte Ausführung (`opt`)**:
  - Eine Nachricht wird nur gesendet, wenn eine **Bedingung** erfüllt ist.
  - Dargestellt durch ein Rechteck mit der Bedingung `[Bedingung]` oben links.

- **Alternative (`alt`)**:
  - Mehrere **alternative Abläufe**, unterteilt durch gestrichelte Linien.
  - Beispiel: Falls eine Bedingung nicht zutrifft, wird ein anderer Pfad genommen.

- **Iteration (`loop`)**:
  - Wiederholte Ausführung einer Nachricht.
  - Iterationsbedingung steht im `loop`-Block (`loop [i=1..10]`).

## Parameter und Rückgabewerte

- **Parameter** stehen in Klammern nach dem Nachrichtennamen:  
  `nachricht1(parameter1, parameter2)`
- **Rückgabewerte**:
  - Direkt vor dem Nachrichtennamen (`rückgabe := nachricht2(parameter)`).
  - Oder bei der Rückgabe-Nachricht (`rückgabe1` mit gestricheltem Pfeil).

## Anwendung von Sequenzdiagrammen

- **Verfeinerung von Anwendungsfällen**:  
  - Beschreibt detailliert, wie Akteure mit dem System interagieren.
- **Visualisierung von Kontrollfluss**:  
  - Zeigt die Reihenfolge der Aufrufe und Rückgaben im System.

# 7. Systemsequenzdiagramm und Operationskontrakte

## Systemsequenzdiagramm (SSD)

Ein **Systemsequenzdiagramm (SSD)** zeigt die Interaktion zwischen einem **Akteur** und dem **System**. Es beschreibt, welche **Systemoperationen** aufgerufen werden und welche **Daten ein- oder ausgegeben** werden.

### Zweck des SSD
- **Ermittlung von Systemoperationen** aus den Anwendungsfallbeschreibungen.
- **Definition der Schnittstelle** zwischen Akteur und System.
- **Übergang von Anwendungsfällen zur technischen Modellierung.**

### Regeln zur Erstellung eines SSD
- Eine **Systemoperation** entspricht einer **Aktion des Akteurs** mit der entsprechenden **Systemreaktion**.
- **Eingaben des Akteurs** werden als **Parameter** modelliert.
- **Systemantworten** werden als **Rückgabewerte** dargestellt.
- Das System wird als **Black Box** behandelt (keine internen Abläufe).

### Beispielhafte Systemoperationen
```text
Operation: starteNeuenVerkauf()
Querverweis: Anwendungsfall „Verkauf durchführen“
Vorbedingungen: Kein aktueller Verkauf existiert.
Nachbedingungen: 
- Ein neues Verkaufsobjekt wurde erzeugt.
- Das Verkaufsobjekt wurde mit der Kasse verknüpft.
```
``` text
Operation: erzeugePosition(id, menge)
Querverweis: Anwendungsfall „Verkauf durchführen“
Vorbedingungen: Ein aktiver Verkauf existiert.
Nachbedingungen: 
- Eine neue Verkaufsposition wurde erzeugt.
- `menge` wurde der Verkaufsposition zugewiesen.
- Die Verkaufsposition wurde mit dem aktiven Verkauf verknüpft.
```
## Operationskontrakte

Ein **Operationskontrakt** ist eine textuelle Beschreibung einer Systemoperation und beschreibt deren Auswirkungen auf das **Domänenmodell**.

### Bestandteile eines Operationskontrakts:

1. **Operation**: Name der Systemoperation mit Parametern.
2. **Querverweis**: Bezug zu einem Anwendungsfall.
3. **Vorbedingungen**: Notwendige Bedingungen vor der Ausführung.
4. **Nachbedingungen**: Auswirkungen auf das Domänenmodell.

### Arten von Nachbedingungen:

- **Objekte erzeugen**: „Ein neues Objekt wurde erstellt.“
- **Attribute setzen**: „Attribut X wurde auf Wert Y gesetzt.“
- **Beziehungen ändern**: „Objekt A wurde mit Objekt B verknüpft.“

### Beispiel: Operationskontrakte für ein Verkaufssystem
```text
Operation: beendeVerkauf()
Querverweis: Anwendungsfall „Verkauf durchführen“
Vorbedingungen: Ein aktiver Verkauf existiert.
Nachbedingungen: 
- Der Verkauf wurde als abgeschlossen markiert.
- Die Verkaufsdaten wurden zur Abrechnung gespeichert.
```
```text
Operation: bezahle(betrag)
Querverweis: Anwendungsfall „Verkauf durchführen“
Vorbedingungen: Ein aktiver Verkauf existiert.
Nachbedingungen: 
- Eine Bezahlung wurde registriert.
- Der erhaltene Betrag wurde gespeichert.
- Falls Wechselgeld erforderlich, wurde es berechnet.
- Ein Beleg wurde gedruckt.
```
## Zusammenhang zwischen SSD und Operationskontrakten

- **Systemsequenzdiagramme** helfen bei der Identifikation von Systemoperationen.
- **Operationskontrakte** beschreiben, wie sich diese Operationen auf das **Domänenmodell** auswirken.
- Gemeinsam bilden sie die **Schnittstelle des Systems** und definieren, welche Daten ein- und ausgegeben werden.

Mit **Systemsequenzdiagrammen** und **Operationskontrakten** wird der **Übergang vom Anforderungsmanagement zur Systemarchitektur** geschaffen.
# 8. Logische Architektur

Die **logische Architektur** beschreibt die Organisation eines Software-Systems durch **Pakete, Subsysteme und Schichten**. Sie hilft bei der Strukturierung des Codes und stellt sicher, dass verschiedene Komponenten unabhängig voneinander entwickelt und gewartet werden können.

## Ziel der logischen Architektur
- **Trennung der Verantwortlichkeiten** in verschiedene Schichten.
- **Reduzierung der Komplexität** durch Modularisierung.
- **Unabhängigkeit von technischen Details** in der Fachlogik.

## Drei-Schichten-Architektur

Die klassische **Drei-Schichten-Architektur** unterteilt das System in:
1. **Präsentationsschicht** (UI – User Interface)
2. **Anwendungsschicht** (Geschäftslogik)
3. **Technische Schicht** (Datenhaltung, Infrastruktur)

### 1. Präsentationsschicht
- Stellt **Daten** auf der **Benutzeroberfläche** dar.
- Enthält keine Geschäftslogik.
- Leitet Benutzeraktionen an die Anwendungsschicht weiter.
- Beispiele: **Web-Oberflächen, mobile Apps, Desktop-Anwendungen.**

### 2. Anwendungsschicht
- Enthält die **fachliche Logik** des Systems.
- Implementiert die Systemoperationen aus dem **Systemsequenzdiagramm (SSD)**.
- **Kommuniziert mit der technischen Schicht**, kennt aber keine technischen Details.
- Verwaltet die **Geschäftsregeln** und den **Zustand der Anwendung**.

### 3. Technische Schicht
- Verwaltet die **persistenten Daten** (Datenbank, Dateisystem).
- Implementiert **technische Dienste** (Logging, Sicherheitsmechanismen, Kommunikation mit externen Systemen).
- Ist **unabhängig** von der Anwendungsschicht.
- **Beispiel:** Zugriff auf ein relationales Datenbanksystem (RDBMS).

## Vorteile einer Schichtenarchitektur

- **Geringere Kopplung**: Änderungen in einer Schicht beeinflussen die anderen nicht direkt.
- **Erhöhte Wartbarkeit**: Geschäftslogik ist unabhängig von der Benutzeroberfläche.
- **Erweiterbarkeit**: Leichtere Anpassung an neue Technologien (z. B. Web statt Desktop).
- **Wiederverwendbarkeit**: Teile der technischen Schicht können in anderen Projekten genutzt werden.

## Paketierung in der logischen Architektur

### Pakete
- Pakete sind **Gruppen von Klassen mit ähnlichen Verantwortlichkeiten**.
- Sie ermöglichen eine **bessere Strukturierung des Codes**.
- **Hierarchische Pakete** (Paket in einem Paket) helfen, große Systeme zu organisieren.

### Abhängigkeiten zwischen Paketen
- **Gestrichelte Pfeile** zeigen Abhängigkeiten zwischen Paketen.
- Eine **lose Kopplung** zwischen Paketen ist wünschenswert.

**Beispiel:**  
- Ein **UI-Paket** könnte eine **Web-UI** und eine **Native-UI** enthalten.
- Beide greifen auf ein **Geschäftslogik-Paket** zu.
- Die Geschäftslogik nutzt wiederum ein **Datenbank-Paket** in der technischen Schicht.

---

## Zusammenhang zwischen SSD, Systemoperationen und Architektur

- **Systemsequenzdiagramme (SSD)** definieren die **Systemoperationen**.
- Diese Operationen werden in der **Anwendungsschicht** implementiert.
- Die **Präsentationsschicht** ruft diese Operationen auf.
- Die **technische Schicht** sorgt für die Speicherung und Verwaltung der Daten.

**Beispiel: Verkaufsprozess**
4. **Verkäufer** gibt Daten in der **Benutzeroberfläche (UI)** ein.
5. **UI** ruft die passende **Systemoperation** in der **Anwendungsschicht** auf.
6. Die **Anwendungsschicht** verarbeitet die Anfrage und speichert die Daten in der **technischen Schicht**.

---

Die logische Architektur definiert somit die **Struktur des Systems** und ermöglicht eine **klare Trennung der Verantwortlichkeiten** für eine **effiziente Entwicklung und Wartung**.

# 9. Klassendiagramm im Entwurf

Das **Klassendiagramm** beschreibt die Struktur des Systems im **Entwurf** genauer als das **Domänenmodell**. Es definiert **Klassen, Attribute, Methoden und Beziehungen** mit höherer Präzision.

## Unterschiede zum Domänenmodell
- **Mehr technische Details** (Datentypen, Sichtbarkeiten, Methoden).
- **Beziehungen sind präziser modelliert**.
- **Generalisation und Spezialisierung** werden berücksichtigt.
- **Attribute und Methoden werden vollständig beschrieben**.

---

## Elemente eines Klassendiagramms im Entwurf

### 1. Klassen
- Eine Klasse wird als **Rechteck mit drei Bereichen** dargestellt:
  1. **Name der Klasse**
  2. **Attribute mit Typen, Sichtbarkeiten und optionalen Standardwerten**
  3. **Methoden (Operationen) mit Parametern und Rückgabewerten**

**Beispiel:**
```text
Artikel
----------------------
- artikelnummer: int
- bezeichnung: String
- preis: BigDecimal = 0.0
----------------------
+ setzePreis(neuerPreis: BigDecimal): void
+ gibBezeichnung(): String
```
### 2. Sichtbarkeiten

- **public (+)** → Attribut oder Methode ist von überall sichtbar.
- **private (-)** → Zugriff nur innerhalb der Klasse.
- **protected (#)** → Zugriff nur innerhalb der Klasse und von abgeleiteten Klassen.
- **Paket-Sichtbarkeit (default, kein Symbol)** → Zugriff nur innerhalb des Pakets.

### 3. Beziehungen zwischen Klassen

- **Assoziation**: Zeigt eine Beziehung zwischen zwei Klassen.
- **Aggregation (leere Raute)**: Eine Klasse enthält eine andere, aber diese kann unabhängig existieren.
- **Komposition (gefüllte Raute)**: Eine Klasse enthält eine andere, und diese ist von ihr abhängig (z. B. ein `Kurs` hat `Teilnehmer`).
- **Generalisierung (Vererbung, Pfeil mit leerer Spitze)**: Eine Klasse erbt Eigenschaften einer anderen.
- **Abhängigkeit (gestrichelte Linie mit Pfeil)**: Eine Klasse nutzt eine andere, ohne eine feste Beziehung.
---
## Generalisierung und Spezialisierung

- **Generalisierung (Vererbung)**:
    - Eine **Unterklasse erbt** von einer **Oberklasse**.
    - Vererbte Methoden können **überschrieben** werden.
    - **Symbol**: Linie mit **leerer Pfeilspitze** von Unterklasse zur Oberklasse.

**Beispiel:**
```text
Fahrzeug
----------------------
+ geschwindigkeit: int
+ bewege(): void
----------------------

PKW (erbt von Fahrzeug)
----------------------
+ anzahlTüren: int
+ öffneTür(): void
```
**Spezialisierung**:

- Eine abgeleitete Klasse erweitert oder spezialisiert die Funktionalität der Oberklasse.
- Wird genutzt, um **gemeinsame Attribute und Methoden in einer Basisklasse** zu bündeln.
---
## Abstrakte Klassen und Schnittstellen

### 1. Abstrakte Klassen

- Eine Klasse, die **nicht instanziiert** werden kann.
- Enthält **abstrakte Methoden**, die in abgeleiteten Klassen überschrieben werden müssen.
- **Symbol**: Kursiv geschriebener Klassenname.

**Beispiel:**
```text
abstract class Tier {
    abstract void macheGeräusch();
}
```
### 2. Schnittstellen (`interface`)

- Definiert eine Menge von Methoden, die von anderen Klassen implementiert werden **müssen**.
- **Unterscheidung zu abstrakten Klassen**: Enthält **keine Implementierungen**.
- **Symbol**: `<<interface>>` über dem Klassennamen.

**Beispiel:**
```text
<<interface>> Fahrbar {
    + starteMotor(): void
    + stoppeMotor(): void
}
```
---
## Parametrisierte Klassen (Generics)

- **Nutzen**: Erlauben es, mit **generischen Datentypen** zu arbeiten.
- **Beispiel in Java**:
```Java
class Box<T> {
    private T inhalt;
    
    public void setInhalt(T inhalt) {
        this.inhalt = inhalt;
    }
    
    public T getInhalt() {
        return inhalt;
    }
}
```
- Wird verwendet für **Listen, Sammlungen und generische Algorithmen**.
---
## Fazit

- Das **Klassendiagramm im Entwurf** ist detaillierter als das **Domänenmodell**.
- Es definiert **Attribute, Methoden und Beziehungen** präzise.
- **Generalisierung, Abstrakte Klassen und Schnittstellen** helfen bei der Modellierung.
- **Parametrisierte Klassen** ermöglichen eine flexible Wiederverwendbarkeit.

Das Klassendiagramm bildet die **Grundlage für die Implementierung des Systems**.

# 10. Sequenzdiagramm (Fortsetzung)

Ein **Sequenzdiagramm** beschreibt den Ablauf der Interaktion zwischen Objekten in einer zeitlichen Abfolge. Es wird verwendet, um das **dynamische Verhalten eines Systems** zu modellieren.

---

## Wiederholung: Grundelemente eines Sequenzdiagramms

- **Objekte**: Rechtecke mit gestrichelter **Lebenslinie**.
- **Akteure**: Benutzer oder externe Systeme.
- **Nachrichten**: Pfeile mit Methodenaufrufen.
- **Rückgabewerte**: Gestrichelte Pfeile.

---

## Erweiterte Konzepte in Sequenzdiagrammen

### 1. Objektlebensdauer und Aktivierungsbalken
- Ein **Objekt existiert** ab dem Zeitpunkt, an dem es erzeugt wird.
- Seine **Lebenslinie** kann durch ein **X** beendet werden.
- **Aktivierungsbalken** zeigt an, wann ein Objekt aktiv ist.

### 2. Selbstaufrufe (Rekursion)
- Eine **Methode ruft sich selbst** auf.
- Dargestellt als **Pfeil, der von einer Lebenslinie auf sich selbst zeigt**.

### 3. Erzeugung und Zerstörung von Objekten
- **Objekterzeugung**: Nachricht mit **Pfeilspitze auf ein neu erstelltes Objekt**.
- **Objektzerstörung**: Dargestellt durch ein **X** am Ende der Lebenslinie.

---

## Kontrollstrukturen in Sequenzdiagrammen

### 1. Bedingungen (`opt`, `alt`)
- **`opt` (optional)**: Nachricht wird nur gesendet, wenn die Bedingung erfüllt ist.
- **`alt` (Alternative)**: Mehrere mögliche Abläufe mit `else`-Zweig.

**Beispiel für `alt`:**
```text
alt [Benutzer ist eingeloggt]
    zeigeDashboard()
else
    zeigeLogin()
```
### 2. Schleifen (`loop`)
- Wird für **wiederholte Nachrichten** verwendet.
- Schleifenbedingung wird in eckigen Klammern `loop [Bedingung]` notiert.
### 3. Nebenläufigkeit (`par`)
- Dient zur Darstellung von **parallelen Abläufen**.
- **Mehrere Aktionen können gleichzeitig stattfinden**.
---
## Modularisierung mit Interaktionsverweisen (`ref`)

- Erlaubt das **Einfügen eines anderen Sequenzdiagramms**.
- Wird verwendet, um **Komplexität zu reduzieren**.
- Symbolisiert durch ein **Rechteck mit dem Namen der referenzierten Sequenz**.

**Beispiel:**
```text
ref [Buchung durchführen]
```
---
## Fazit

- Sequenzdiagramme helfen, das **dynamische Verhalten** eines Systems zu visualisieren.
- **Kontrollstrukturen** wie `opt`, `alt` und `loop` ermöglichen **flexible Abläufe**.
- **Interaktionsverweise (`ref`)** vereinfachen die Darstellung komplexer Szenarien.
- Diese Diagramme dienen als **Vorlage für die Implementierung** der Geschäftslogik.
# 11. Zustandsdiagramm

Ein **Zustandsdiagramm** beschreibt das **dynamische Verhalten eines Objekts** durch seine möglichen **Zustände** und **Übergänge**.

## Elemente eines Zustandsdiagramms

- **Zustände**: Repräsentieren verschiedene Phasen eines Objekts.
- **Übergänge**: Zeigen, wie ein Objekt von einem Zustand in einen anderen übergeht.
- **Ereignisse**: Lösen den Zustandswechsel aus.
- **Startzustand**: Anfangszustand eines Objekts (dargestellt als schwarzer Punkt).
- **Endzustand**: Zustand, in dem das Objekt seine Verarbeitung beendet (schwarzer Kreis mit Umrandung).

### Beispielhafte Zustände eines Bestellprozesses:
```text
[Bestellt] → Zahlung erhalten → [Bezahlt] → Ware versendet → [Versendet] → Ware erhalten → [Abgeschlossen]
```
### Erweiterte Konzepte:
- **Wächterbedingungen (Guards)**: Bedingungen für Übergänge `[wenn Zahlung bestätigt]`.
- **Nebenläufige Zustände (Fork/Join)**: Ein Objekt kann sich in mehreren Zuständen gleichzeitig befinden.
---
# 12. Aktivitätsdiagramm

Ein **Aktivitätsdiagramm** beschreibt den **Ablauf eines Prozesses** mit **Aktionen** und **Steuerflüssen**.

## Elemente eines Aktivitätsdiagramms:

- **Startknoten** (schwarzer Punkt).
- **Aktionsknoten** (abgerundetes Rechteck).
- **Übergänge** (Pfeile zwischen Aktionen).
- **Entscheidungen (`diamond`-Symbol)**: Kontrollstrukturen (`if`, `else`).
- **Zusammenführungen (Join/Fork)**: Parallele Abläufe.

### Beispielhafter Ablauf:
```text
[Bestellung aufgeben] → [Zahlung prüfen] → [Ware versenden] → [Bestellung abgeschlossen]
```
**Unterschied zu Sequenzdiagrammen**:

- Sequenzdiagramme zeigen **Interaktion zwischen Objekten**.
- Aktivitätsdiagramme modellieren **Abläufe** unabhängig von Objekten.
---
# 12. Anwendungsfalldiagramm
Ein **Anwendungsfalldiagramm** zeigt die **Funktionen eines Systems aus Sicht der Akteure**.
## Elemente:
- **Akteure**: Externe Benutzer oder Systeme (Strichmännchen-Symbol).
- **Anwendungsfälle**: Beschreiben **Funktionen**, die Akteure nutzen.
- **Assoziationen**: Verbindungen zwischen Akteuren und Anwendungsfällen.
- **Include-Beziehungen** (`<<include>>`): Wiederverwendbare Funktionen.
- **Extend-Beziehungen** (`<<extend>>`): Optionale Erweiterungen eines Anwendungsfalls.
### Beispiel:
```text
[Benutzer] → (Einloggen) → (Konto verwalten)
```
## Nutzen:
- Modelliert **Systemanforderungen** auf hoher Ebene.
- Unterstützt **Projektplanung und Kommunikation** mit Stakeholdern.
---
# 13. Komponenten- und Verteilungsdiagramme
## 13.1. Komponentendiagramm
- Zeigt **Module und ihre Abhängigkeiten**.
- **Komponenten** sind wiederverwendbare Software-Bausteine (`<<component>>`).
- **Schnittstellen** definieren **Kommunikation** zwischen Komponenten.
## 13.2. Verteilungsdiagramm
- Modelliert die **physische Verteilung** eines Systems.
- Zeigt, welche Software auf welchen **Hardware-Knoten** läuft.
### Beispielhafte Komponenten:
```text
<<component>> Webserver
<<component>> Datenbank
```
**Nutzen**:
- Unterstützt **Systemarchitektur und Deployment-Planung**.
---
# 14. Fazit

Die UML-Diagramme decken verschiedene Aspekte eines Systems ab:

- **Struktur**: Klassendiagramm, Komponentendiagramm.
- **Dynamik**: Sequenzdiagramm, Zustandsdiagramm, Aktivitätsdiagramm.
- **Funktionale Sicht**: Anwendungsfalldiagramm.
- **Technische Sicht**: Verteilungsdiagramm.

Diese Modelle helfen bei der **Analyse, Entwicklung und Dokumentation** von Softwaresystemen.