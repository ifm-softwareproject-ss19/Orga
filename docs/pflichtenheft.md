# Anforderungs- und Entwurfsspezifikation ("Pflichtenheft")

Autoren:

- Alexander Heinisch



* Link zum Source Code Repository folgt


# 1 Einführung

## 1.1 Beschreibung
    - Projektname
Ein System womit ein Fahrzeug zu dem Standort einer Drohne fahren kann. In diesem System soll es möglich sein auf dem Smartphone visuell die position der Drohne bzw des Fahrzeuges zu sehen. 

## 1.2 Ziele

Das Ziel unseres Projekts ist das automatische Aufspüren bestimmter Objekte aus der Luft und das automatisiere Navigieren eines Bodenfahrzeugs an die Stelle von diesen. Dies planen wir mit einer Drohne, die automatisch nach vorher festgelegten Objekten in einem festgelegten Raum sucht und einem Modellauto, das sich selbst den Weg zu der Position der Objekte sucht, umzusetzen. Die Drohne soll dafür nach dem Aufspüren ein mobiles Zwischengerät die Koordinaten für den aufzusuchenden Ort übermitteln, sodass diese Daten an das Auto weitergeleitet werden können, welches sich daraufhin, gesteuert von einem Raspberry Pi, zu diesem Ort begibt, um dort weitere Aktionen ausführen zu können. Diesen Vorgang wollen wir wahrscheinlich mit Augmented Reality visualisieren.

Diese Technik könnte man z.B. in der Agrarwirtschaft zum Aufspüren und Verscheuchen von Rehen auf Feldern oder als Unterstützung in unwegsamen Geländen bei Suchtrupps o.ä. nutzen.

Das Softwaresysem ist kein autonomes System und kann nicht automatisch einen bereich absuchen.

# 2 Anforderungen

## 2.1 Stakeholder

| Funktion | Name | Kontakt | Verfügbarkeit | Wissen  | Interesse & Ziele  | Relevanz  |
|---|---|---|---|---|---|---|
| Projektleiter | Alexander Heinisch | aheinisch@fh-bielefeld.de | Per E-Mail, tagsüber | Kennt embeddedd Systems                         | Vereinfachung der Ausleihprozesse  |  |



## 2.2 Funktionale Anforderungen





    - Use-Case Diagramme
    - Strukturierung der Diagramme in funktionale Gruppen

## 2.3 Nicht-funktionale Anforderungen 

### 2.3.1 Rahmenbedingungen

**Hardware**

- Raspberry PI 3 b+
    sensoren weiter aufteilen
  - Bluetooth

- DJI Spark
  - Wlan

- Smartphone
  - Android
  - Kamera

### 2.3.2 Betriebsbedingungen

Android version 7.1

### 2.3.3 Qualitätsmerkmale

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | 
Fehlertoleranz |X|-|-|-
Wiederherstellbarkeit |X|-|-|-
Ordnungsmäßigkeit |X|-|-|-
Richtigkeit |X|-|-|-
Konformität |-|X|-|-
**Benutzerfreundlichkeit** | | | | 
Installierbarkeit |-|-|X|-
Verständlichkeit |-|X|-|-
Erlernbarkeit |-|X|-|-
Bedienbarkeit |-|X|-|-
**Performance** | | | | 
Zeitverhalten |-|-|X|-
Effizienz|-|-|-|X
**Sicherheit** | | | | 
Analysierbarkeit |-|-|X|-
Modifizierbarkeit |-|-|-|X
Stabilität |-|-|X|-
Prüfbarkeit |-|-|X|-

## 2.4 Graphische Benutzerschnittstelle
    - GUI-Mockups passend zu User Stories
    - Screens mit Überschrift kennzeichnen, die im Inhaltsverzeichnis zu sehen ist
    - Unter den Screens darstellen (bzw. verlinken), welche User Stories mit dem Screen abgehandelt werden
    - Modellierung der Navigation zwischen den Screens der GUI-Mockups als Zustandsdiagramm

## 2.5 Anforderungen im Detail
    - User Stories mit Akzeptanzkritierien 
    - Optional: Name (oder ID) und Priorität ("Must", "Should", "Could", "Won't")
    - Strukturierung der User Stories in funktionale Gruppen

| **Name**| **In meiner Rolle als**...|   ...**möchte ich**...   | ..., **so dass**... | **Erfüllt, wenn**... | **Priorität**   |
|:-----|:----------:|:-------------------|:-------------|:---------|:----------------|
| Drohne verbinden  |Benutzer| eine WLAN verbindung mit der Drohne aufbauen|ich app nutzen kann| Verbindung hergestellt | Muss |
| Drohne starten  |Benutzer|Drohne starten|die Drohne steuern kann| Drohne starthöhe erreicht hat | Muss |
| Drohne landen  |Benutzer|Drohne landen|ich Drohne abschalten kann| Drohne ladevorgang abgeschlossen hat| Muss |
| Drohne navigieren  |Benutzer|Drohne lenken|ich Drohne stueerrn kann| Drohne position verändern kann| Muss |
| Bild aufnehmen  |Benutzer|ein Photo machen|ich das Bild verarbeiten kann| Photo zum Smartphone gesendet wurde| Muss |
| Video aufnehmen  |Benutzer|eine Aufnahme machen|ich das Video verarbeiten kann| Video zum Smartphone gesendet wurde| Muss |
| GPS auslesen |Benutzer|die GPS Koordinaten der Drohen ausgegeben bekommen|die Daten wieterverarbeitet werden können| GPS wird auf dem Smartphone angezeigt| Muss |


# 3 Technische Beschreibung

## 3.1 Systemübersicht

![Systemarchitektur](./img/systemarchitektur.svg)

## 3.2 Softwarearchitektur

![Softwarearchitektur](./img/softwarearchitektur.svg)

## 3.3 Schnittstellen

In diesem Projekt haben wir 2 Geräteschnittstellen.

    - Schnittstellenbeschreibung
    - Auflistung der nach außen sichtbaren Schnittstelle der Softwarebausteine

## 3.4 Datenmodell 

Keine Daten werden persistieren.

## 3.5 Abläufe

Kommunikation 
    - Aktivitätsdiagramme für relevante Use Cases
    - Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases

## 3.6 Entwurf
    - Detaillierte UML-Diagramme für relevante Softwarebausteine

# 4 Projektorganisation

## 4.1 Annahmen
    - Nicht durch den Kunden definierte spezifische Annahmen, Anforderungen und Abhängigkeiten
    - Verwendete Technologien (Programmiersprache, Frameworks, etc.)
    - Aufteilung in Git-Repositories gemäß Software- und Systemarchitektur und Softwarebbausteinen 
    - Einschränkungen, Betriebsbedingungen und Faktoren, die die Entwicklung beeinflussen (Betriebssysteme, Entwicklungsumgebung)
    - Interne Qualitätsanforderungen (z.B. Softwarequalitätsmerkmale wie z.B. Erweiterbarkeit)

## 4.2 Verantwortlichkeiten
    - Zuordnung von Personen zu Softwarebausteinen aus Kapitel 3.1 und 3.2
    - Rollendefinition und Zuordnung

| Softwarebaustein | Person(en) |
|----------|-----------|
| Drohnen Steuerung | Jakob Tissen | 
| AR | Nick  |
| Fahrzeugstruktur | Kevin Gerzen | 
| Kollisionschecker | Andre Grellmann |
  

### Rollen

#### Softwarearchitekt
Entwirft den Aufbau von Softwaresystemen und trifft Entscheidungen über das Zusammenspiel der Softwarebausteine.

#### Frontend-Entwickler
Entwickelt graphische oder andere Benutzerschnittstellen, insbesondere das Layout einer Anwendung.

#### Backend-Entwickler
Implementiert die funktionale Logik der Anwendung. Hierbei werden zudem diverse Datenquellen und externe Dienste integriert und für die Anwendung bereitgestellt.

### Rollenzuordnung

| Name     | Rolle     |
|----------|-----------|
| Alexander Heinisch | Projektleiter |
| Nick |  |
| AGrellmann |  |
|  |  |


## 4.3 Grober Projektplan
    - Meilensteine

### Meilensteine
* KW 19 (12.05)
  * Abgabe Pflichtenheft
* KW 20 (13.05) / Projekt aufsetzen
  * Repository Struktur
* KW 23 (31.05) / Tests sind Fertig
  * Spezifizieren 
  * implementierung der Tests
  * Testfälle laufen erfolgreich durch
* KW 27 (26.06) / Implementation fertig
  * manuelle Abnahmetests
  * Verbindung der Systeme manuell testen
* KW 28 (03.07) / Vorstellung
  * Präsentation / Software-Demo

# 5 Anhänge

## 5.1 Glossar 
    - Definitionen, Abkürzungen, Begriffe

## 5.2 Referenzen
    - Handbücher, Gesetze

## 5.3 Index



