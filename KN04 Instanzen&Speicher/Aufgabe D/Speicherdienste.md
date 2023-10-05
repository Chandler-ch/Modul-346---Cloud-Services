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


**Persistenz**
Es ist ein Persistent Speicher, darauf ausgelegt mit Instanzen zu funktionieren. Die Daten bleiben ebenfalls intakt falls Instanzen abbrechen oder Terminiert werden. 

**Speed**
EBS hat ebenfalls wie S3 wieder verschiedene Typen bei denen die Geschwindigkeit unterschiedlich ist.
*Generell Purpose (SSD)* - Balanced zwischen Preis und Performance, passt für die meisten Anwendungen
*Provisioned IOPS (SSD)* - Garantiert Input Output Per Second, und deswegen ziemlich gut für I/O intensive Applikationen. 
*Throughput optimized (HDD)* - Perfekt für grosse throughputs, grosse Datenmengen und Streaming. 
*Cold (HDD)* - Gut wenig kosten für Anwendungen die sowieso nicht wirklich viel abgerufen werden

**Security**
Es gibt einen Special entcrypting Service namens KMS (Key Management Service). Dieser erhöht die Datensicherheit und ansonsten gibt es die normalen Bucket Policy und access control Policy

**Location**
Bei EBS gibt es nur eine Region die zählt. Man kann zwar den ganzen Storage kopieren und dann ein zweites Storage auf einer anderen Region aufmachen aber ansonsten ist das nichts. 

**Andere Eigenschaften**
EBS hat Features wie Snapshots, Backups oder Recovery. Es gibt elastische Volumen um die Grösse zu verändern ohne die Instant herunterfahren zu müssen und bei manchen Cases kann man mehrere Volumen anhängen. 

**Use Cases:**
+ General Purpose (SSD): Suitable for web servers, small to medium-sized databases, and development/test environments.
+ Provisioned IOPS (SSD): Ideal for high-performance databases and critical applications that require consistent I/O performance.
+ Throughput Optimized (HDD): Best for big data analytics, data warehousing, and streaming workloads.
+ Cold HDD: Cost-effective for storing large amounts of rarely accessed data or backups.

*Für Objektspeicherung (AWS S3), kann man es benutzen für einen skalierbaren und haltbaren Speicher für Files, Images, Videos etc. Es ist vor allem für "Data Lakes", Backups und content distribution. Security und compliance sind also wichtige Vorteile zum speichern sensitiver Daten.
*For object storage (AWS S3), you can use it for scalable and durable storage of objects like files, images, videos, and more. It's commonly used for data lakes, content distribution, and backup/archiving. Security and compliance are also key benefits for sensitive data storage.*

-----------------------------------------------------------------------------------------------------------

# EFS

**Persistenz**
EFS ist auch sehr Skalierbar und kann angepasst werden ohne die Instant Stoppen zu müssen

**Speed:**
EFS hat genau 2 Modi die es bedient. 
*Generell Purpose (Standard)* - passt für die meisten mit wenig Latenz und moderaten Throughput. 
*Max I/O* - gemacht für Applikationen mit hohen Throughput und niedriger Latenz. 

**Security**
EFS unterstützt auch KMS, arbeitet generell viel mit encryption und Access Control wird durch POSIX Permissions gemanaged oder IAM (Identity Access Management)

**Location**
EFS ist auch regionsspezifisch, was bedeutet dass es nur in einer AWS Region einsetzbar ist.  Trotzdem kann man es von mehreren Verfügbarkeitszonen her finden. 

**Andere Eigenschaften:**
EFS ist ein vollständig gemanagter File-Storage Service, welcher automatisch die Grösse skaliert die gebraucht wird. Es ist gemacht für geteilten Zugriff, was bedeutet dass mehrere Instanzen auf einem EFS File schreiben und lesen können. 

**Use Cases:**
+ General Purpose (Standard): Suitable for web serving, content management systems, and development environments where moderate performance and shared file access are required.
+ Max I/O: Ideal for applications that require low-latency access to a large amount of data, such as big data analytics and high-performance computing workloads.


*EFS wird oft dort benutzt wo mehrere EC2 Instanzen die gleichen Storage Daten verwenden müssen, was eine gute Lösung darstellt, mit den sehr skalierbaren und reliable Speichern.*

-----------------------------------------------------------------------------------------------------------

## Quellen
+ M346 Repository
+ ChatGPT