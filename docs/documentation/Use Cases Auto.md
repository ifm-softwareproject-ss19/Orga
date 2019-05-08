**Nr:** A1  
**Name:** Auto und Smartphone verbinden  
**Akteur:** Auto, Smartphone, User  
**Trigger:** User startet die App
**Kurzbeschreibung:** Das Smartphone verbindet sich über Bluetooth mit dem Auto  
**Vorbedingungen:** --  
**Essenzielle Schritte:** Die App starten, nach Bluetooth-Geräten suchen, mit dem Auto verbinden
**Ausnahmefälle:** Die Bluetooth-Verbindung scheitert  
**Fragen:**  
---
**Nr:** A2  
**Name:** Auto nach GPS fahren lassen  
**Akteur:** Auto, Smartphone, Drohne  
**Trigger:** Drohne erkennt ein Objekt  
**Kurzbeschreibung:** Das Auto fährt automatisch zu den GPS-Koordinaten von der Drohne  
**Vorbedingungen:** A1  
**Essenzielle Schritte:** Die Drohne erkennt ein Objekt und sendet die PGS-Koordinaten an das Smartphone, Das Smartphone leitet die Daten an das Auto weiter, Das Auto fährt zu den GPS-Koordinaten
**Ausnahmefälle:** Der Weg ist Blockiert, kein GPS-Sgnal  
**Fragen:**  
---
**Nr:** A3  
**Name:** Objekten ausweichen  
**Akteur:** Auto  
**Trigger:** Ultraschallsensor
**Kurzbeschreibung:** Das Auto erkennt Objekte mithilfe des Ultraschallsensors und weicht ihnen aus  
**Vorbedingungen:**  A2
**Essenzielle Schritte:** Ultraschallsensoren überwachen, Hindernissen ausweichen  
**Ausnahmefälle:**  
**Fragen:**  
