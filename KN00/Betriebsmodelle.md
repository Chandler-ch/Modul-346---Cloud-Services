# Betriebsmodelle
Kurz zur Definition von Betriebsmodellen. Betriebsmodelle sind die Strukturen oder Pläne, wie die Server oder das Unternehmen aufgebaut ist.
Wenn wir uns Betriebsmodelle ansehen, gibt es verschiedene interessante Kandidaten:

## On-Premises
On-Premises nutzen serverbasierte Software, für eine Installatino auf der eigenen IT-Umgebung. Das heisst die Verantwortung liegt voll und ganz beim Benutzer selber. Sicherheitstechnisch auf einem ganz hohem Level. Jedoch Geldmässig und vom generellen Aufwand her, ist das viel zu viel, was auch dazu führt, dass diese Art von Betriebsmodell an Relevant verliert.

POSITIV
+ Hochsicherheit
+ Unabhängig
+ Lokal

NEGATIV
+ Enorme Kosten (Wartung, Updates)
+ Grosser Aufwand (Backup, Updates)
+ Nicht Flexibel skalierbar



## Private Cloud
Das Private Cloud Modell ist quasi die upgegradete Version des On-Premier Modells. Die Daten werden ebenfalls auf Servern gehostet. Anders als beim On-Premises Modell wird die Software durch das Cloud System gemietet, sodass sich die grosse Sicherheit mit einer hohen Skalierbarkeit vereint.
Wichtig noch anzumerken ist, dass bei einer Private Cloud nur mein Unternehmen Zugriff auf die Server/Hardware hat.
Beispiele: VMWare, Hyper-V-Lösungen

POSITIV
+ Hohe Sicherheit
+ Hohe Skalierbarkeit und Flexibel

NEGATIV
+ Teuer
+ Bei eigenem Hosting grosser Verwaltungsaufwand


## Public Cloud
Hier ist erstmal alles über die Cloud geregelt. Mein Unternehmen legt unsere Daten in die Hände der Cloud Betreiber, sodass diese die Verwaltung und Wartung übernehmen. Diese verstehen was sie tun und deswegen können wir von ihrem Wissen profitieren und gleichzeitig uns nicht selbstständig darum kümmern.
Doch die Leistung könnte eingeschränkt werden, wenn mehrere Unternehmen den gleichen Server mieten.
Beispiele: Google Drive, DropBox, OneDrive


POSITIV
+ Die Betreiber kennen sich gut aus
+ Reduzierung der Ausgaben
+ Freie Skalierung

NEGATIV
+ Nicht so sicher wie vorherige Modelle wegen dem Internet


## Hybrid Cloud
Die Hybrid Cloud verbindet alle Vorteile der drei Betriebsmodelle von davor: Unternehmen wägen ab, welche Anwendungen sie auf eigenen Rechnern betreiben wollen und welche sie auf die Public Cloud ausladen um Kosten zu sparen. So haben sie die volle Kontrolle über die Sicherheit der Daten und profitieren von der grossen Flexibilität der Public Cloud.
Beispiel bei Office 365 werden Public- als auch Private-Cloud Systeme benutzt. Man kann auf Office 365 zugreifen für die Emailkommunikation, aber auch ein eigenes Outlook auf dem Terminalserver benutzen.


POSITIV
+ Flexibel und Skalierbar
+ Günstig
+ Sicherheit verbessert durch die Nutzung von On-Premise bzw. Private Cloud Strukturen bei wichtigen Daten

NEGATIV
+ Zusätzlicher Aufwand


## Quellen
-Julie
-Hr. Calisto
-Kurs Gitlab Repository
-Internet