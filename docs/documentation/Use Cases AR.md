**Nr:**  AR 1

**Name:**  AR wird gestartet

**Akteur:**  User, Smartphone, Drohne, Auto

**Trigger:**  User startet die AR Funktion

**Kurzbeschreibung:**  Der User startet die AR Funktion 

**Vorbedingungen:**  

**Essenziele Schritte:**  Der User startet die AR Funktion. In der App wird der Kamera Feed des Smartphones angezeigt. 

**Ausnahmefälle:**  App erhält keine GPS Daten von Drohne oder Auto

**Fragen:**  --



**Nr:**  AR 2

**Name:**  Marker werden gesetzt/aktualisiert

**Akteur:**  User, Smartphone, Drohne, Auto

**Trigger:**  App erhält GPS Infos

**Kurzbeschreibung:**  Im Kamera Feed wird mithilfe der GPS Daten die Position der Drohne und des Autos angezeigt in AR

**Vorbedingungen:**  AR 1

**Essenziele Schritte:**  Die App erhält GPS Daten der Drohne und des Autos. In dem Kamera Feed wird mit AR das Auto und die Drohne angezeigt.

**Ausnahmefälle:**  App erhält keine GPS Daten von Drohne oder Auto

**Fragen:**  --



**Nr:**  AR 3

**Name:**  Pfad des Autos wird Angezeigt

**Akteur:**  User, Smartphone, Drohne, Auto

**Trigger:**  User startet die AR Funktion

**Kurzbeschreibung:**  Mithilfe der GPS daten wird versucht den Weg des Autos darzustellen.

**Vorbedingungen:**  AR 2

**Essenziele Schritte:**  Marker für die Position des Autos und der Drohne werden Gesetzt. Ein möglicher Weg vom Auto zur Drohne wird erstellt. Der Weg wird im Kamera Feed durch AR angezeigt

**Ausnahmefälle:**  App erhält keine GPS Daten von Drohne oder Auto

**Fragen:**  --



