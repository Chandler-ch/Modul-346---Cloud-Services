# S3
**Persistenz**
Hat S3 auf jeden Fall. Daten bleiben bestehen, auch wenn eine Instanz heruntergefahren oder Terminiert wird.

**Geschwindigkeit**
Hängt sehr davon ab was man kauft.
+ *Standard* - Niedrige Latenz, geeignet für häufig abgerufene Dateien
+ *Intelligent* Tiering - Verschiebt Objekte automatisch zwischen 2 Ebenen um Kosten zu optimieren und die Leistung aufrechtzuerhalten
+ *One-Zone-IA* - Wenig kosten, hat aber nur eine Verfügbarkeitszone, was die Haltbarkeit einschränkt.
+ *Glacier* - Entwickelt für Archivierung mit wenig Abrufen
+ *Glacier Deep Archive* - Noch extremer, entwickelt für Langzeitarchivierungen.

**Security**
S3 bietet Bucket Policy, IAM roles, Access Control Lists, Data encryption.. ziemlich robust.

**Location**
Man kann auswählen für welche Staaten es gilt, aber grundsätzlich wie die Standard S3 Klasse, sind die Objekte global verfügbar.


**Other Characteristics**
- Data Durability ist wirklich unfassbar hoch (99,99999999999%) und S3 bietet somit eine hohe Verfügbarkeit.
- Man kann Daten jederzeit auf eine andere Region transportieren, wenn die Latenz und die kosten niedriger sind.
- Der Ablauf, Objeke zu anderen Klassen zu verschieben ist automatisch möglich aufgrund von Regeln.
- Man kann den Objekten Metadaten zuweisen, damit man sie besser organisieren kann.


**Use Cases**
*Standard S3* - Hosting static websites, storing application data, backups
*Intelligent-Tiering* - Data lakes, analytics workloads with changing access patterns
*One-Zone-IA* -  Infrequently accessed data with lower durability requirements
*Glacier* - Long-term archiving, compliance data storage
*Glacier Deep Archive* - Data archiving with the lowest cost requirements




-----------------------------------------------------------------------------------------------------------

# EBS



-----------------------------------------------------------------------------------------------------------

# EFS



-----------------------------------------------------------------------------------------------------------

## Quellen
+ M346 Repository
+ ChatGPT