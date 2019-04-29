**Nr:** D 1  

**Name:** Drohne verbinden  

**Akteur:** User, Smartphone,App , Drohne  

**Trigger:** Startvorgang App  Verbinden Button in der App  Sprachbefehl verbinden  

**Kurzbeschreibung:** Der User möchte eine WIFI Verbindung zwischen Drohen und Smartphone herstellen,   damit er die Funktionen der App nutzen kann.

**Vorbedingung:** Drohne und Smarthpone sind betriebsbereit  

**Essenziele Schritte:** User macht Drohne und Smartphone betriebsbereit  
User startet App auf dem Smartphone  
App zeigt Status der WIFI Verbindung zur Drohne an  

**Ausnahmefälle:** Verbindung kann nicht hergestellt werden  
App zeigt Status an  
Erneuter Verbindungsversuch  


----

**Nr:** D 2  

**Name:** Drohne starten  

**Akteur:** User, Drohne, Smartphone  

**Trigger:** User drückt den starten Button in der App  Sprachbefehl starten  

**Kurzbeschreibung:** Der User möchte die Drohne mit der App starten, um ein Bild zu machen  

**Vorbedingungen:** Drohne und App sind Betriebsbereit und miteinander verbunden über WIFI  

**Essenziele Schritte:** User bestätigt starten Button in der App  
Drohne startet und begibt sich auf voreingestellte Starthöhe  
Wenn der Vorgang abgeschlossen ist, wird dem User eine Statusmeldung angezeigt  

**Ausnahmefälle:** Drohne startet nicht weil Akkustand zu niedrig. Statusmeldung wird auf der App angezeigt  

---

**Nr:** D 3  

**Name:** Drohne landen  

**Akteur:** User, Drohne, Smartphone  

**Trigger:** User drückt den landen Button in der App   
Akkustand der Drohne so niedrig, sodass sie automatisch den Landevorgang einleitet  
Sprachbefehl landen  

**Kurzbeschreibung:** Der User möchte die Drohne landen, um sie auszuschalten  

**Vorbedingungen:** D 1, D 2  

**Essenziele Schritte:** User bestätigt landen Button in der App  
Drohne leitet Landevorgang ein
Wenn der Vorgang abgeschlossen ist, wird dem User eine Statusmeldung angezeigt  

**Ausnahmefälle:** kritischer Akkustand erreicht, wird automatischer Landevorgang eingeleitet und Statusmeldung ausgegeben auf der App  

---

**Nr:** D 4  

**Name:** Drohne navigieren  

**Akteur:** Drohne, User, Smartphone  

**Trigger:** User drückt eines der Navigationsbuttons der App  
Sprachbefehle  

**Kurzbeschreibung:** User möchte die Drohne im Raum navigieren, um andere Perspektiven zu bekommen  

**Vorbedingungen:** D 1, D 2  

**Essenziele Schritte:** User gibt Navigationsbefehle über die App an die Drohne  
Drohne bewegt sich entsprechend  

**Ausnahmefälle:** Navigationsbefehl wird nicht durchgeführt aufgrund von Kolisionsgefahr  
Verbindungsabbruch  
App stürzt ab  

---

**Nr:** D 5  

**Name:** Photo machen  

**Akteur:** Drohne, User, Smartphone  

**Trigger:** User drückt Photo Button  
Sprachbefehl Photo machen  

**Kurzbeschreibung:** User möchte ein Photo machen, um Daten von der Umgebung auswerten zu können  

**Vorbedingungen:** D 1, D 2  

**Essenziele Schritte:** User gibt den Befehl Photo machen an die Drohne  
Drohne macht eine Aufnahme und sendet die Datei an das Smartphone  
User bekommt Statusmeldung  

**Ausnahmefälle:** Datei konnte nicht vollständig übertragen werden, auf der App wird dieser Status dem User angezeigt  

---

**Nr:** D 6  

**Name:** Lifevideofeed  

**Akteur:** User, Smartphone, Drohne  

**Trigger:** App wird gestartet  

**Kurzbeschreibung:** Der User möchte sehen, was die Kamera der Drohne gerade sieht, um die Drohne navigieren zu können  

**Vorbedingungen:** D 1, D 2  

**Essenziele Schritte:** Drohne startet Videoübertragung zum Smartphone über WIFI  
Smartphone empfängt Daten und spielt das Video in Echtzeit ab auf der App  

**Ausnahmefälle:** Übertragungsprobleme: hohe Latenz, Verbindungsabbrüche, Störungen  
Statusmeldung wird dem User ausgegeben  

---

**Nr:** D 7  

**Name:** GPS anfordern  

**Akteur:** User, Smartphone, Drohne  

**Trigger:** App fordert in einem Intervall GPS Infos von der Drohne  

**Kurzbeschreibung:** User möchte Informationen über den Standort der Drohne aktuell auf der App ausgegeben bekommen,  um seiner Neugier willen  

**Vorbedingungen:** D 1  

**Essenziele Schritte:** App startet in regelmäßigen Abschnitten Anfragen an die Drohne  
Drohne sendet Statusinformationen  
App verarbeitet Informationen und zeigt sie auf dem Display an  

**Ausnahmefälle:** Schlechte Verbindung zu Sateliten um GPS zu ermitteln  
