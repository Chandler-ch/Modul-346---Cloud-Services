# Servicemodelle
Es gibt 4 Servicemodelle, die benutzt werden. Ähnlich wie bei den Betriebsmodellen, geht es hier auch wieder um Kontrolle und wie Services gemanaged oder gehostet werden.

Hier ein gutes Bild um zu veranschaulichen wie das funktioniert:
![Pizza-Service](<Bilder/Betriebsmodell, Servicemodell Beispiel.png>)
Wenn man die Zutaten selber holen will, bedeutet das mehr Aufwand, dafür kannst du genau darüber bestimmen woher, was genau und wie die Zutaten zu dir gekommen sind. Das gleiche ist es basically mit den Modellen. Wenn ich Abteile den Services überlasse, weiss ich nicht ganz genau was da passiert, bezahle Leute dafür, dass sie meine Server warten und vertraue auf ihre Kentnisse, gute Ergebnisse zu erzielen. Und da der Kunde König ist, kann ich auch genau bestimmen, was für eine Skalierbarkeit ich haben will.


## Infrastructure as a Server | IaaS
Dieses Servicemodell beschreibt das Geschäftsmodell, was Infrastruktur vermietet statt es zu verkaufen. Es geht aber nicht darum Hardware zu buchen, da das sehr umständlich wäre, weswegen man virtuelle Software benutzt. Die Infrastruktur wird demnach softwaredefiniert bereitgestellt. Pay per use wird hier auch angewendet.
Ein gutes Beispiel für ein IaaS wäre der Amazon Web Server, bei dem Software aus dem Rechenzentrum von Amazon gemietet wird. Aber auch Microsoft Azure ist da mit drin.


## Platform as a Server | PaaS
Dieser Servicetyp hat einen Vorzug für Programmierer. Es sollte eine fertige Softwareumgebung zur Verfügung stellen, auf deren Basis man Applikationen entwickeln kann. Das Ding ist, sich nicht mehr um die ganzen Hardware Sachen und Updates kümmern zu müssen. Denn diese gibt es hier nicht. Um all das kümmert sich der PaaS Anbieter. Aspekte wie Storage und Netzwerk sind auch demnach über APIs geregelt.
Oftmals werden Services draufgestellt, die nützlich für die Entwicklung ist. Wie zum Beispiel Datenbanken oder Message Queues.
Bekannte Beispiele für Anbieter wären hierbei Heroku. Da PaaS auf Iaas aufbaut, gibt es viele Anbieter die Iaas anbieten, die auch Paas anbieten. Zum Beispiel Amazon AWS Elastic Beanstalk. Damit die aber zusammenpassen, müssen die 12 Factor Apps Regeln erfüllt sein.
Beispiel: Google App Engine



## Software as a Service | SaaS
Hier gibt es nun die vollständigen Anwendungen via Cloud. Cloud Software wäre zb Microsoft Office, Stack, Github. Software wird auch hier nicht mehr gekauft, sondern monatlich abgerechnet. Es ist sehr einfach und flexibel Software zu mieten, da Aufwendige und fehleranfällige Vorgänge nicht mehr gemacht werden müssen, wie Installation, Konfiguration, Patches/Updates. Das wird alles vollständig in die Hände des Anbieters gelegt. So kann man sich stärker auf sein Kerngeschäft fokussieren. SaaS hat aber den Nachteil, dass man geringe Anpassungen machen kann. Abhängigkeit vom Anbieter (Vendor-Lock-In). Dadurch ist die Verwendung offener Stanards und Formate sehr wichtig. Datenschutz ist bei SaaS auch noch mehr zu beachten. Man sollte sich also mit Themen wie DSGVO (EU privacy law) auseinandersetzen.



## Function as a Service | FaaS
Das hier ist ein Server, mit Infrastruktur, Betriebssystem, Umgebung und die eigentlichen Anwendungen plus die Geschäftslogik. Quasi als Plug-in. Dies sind einzelne Funktionen, die in einen fertigen Anwendungsrahmen eingebunden werden. Wie als Route in einem vorgefertigten Webserver.
Als Entwickler muss man sich nur noch um das schreiben dieser Route kümmern, alles andere wird schon von der API oder dem Cloud-Anbieter übernommen.
Diese Variante ist sehr kostengünstig, da kein zugewiesener Server vorgehalten werden muss. Das wird alles nach Aufrufen abgerechnet: Finden keine Aufrufe statt, fallen auch keine Kosten an. Das macht FaaS zu einer kostengünstigen Alternative, wobei auch die Funktionen sich leicht warten lassen.
FaaS wird häufig dafür verwendet um Funktionen zu verbinden. Backend für Single-Page-Anwendungen gibt es auch, wie Microsoft Azure oder AWS Lambda. Nachteil, hier gibt es auch wieder den Vendor-Lock-in, was die Relevanz von offenen Formaten und Standards nochmals unterstreicht.



## X as a Service | (XaaS)
Natürlich gibt es noch Zwischen-Services, die nicht genau auf die vier Servicemodelle von NIST passen. Meistens sind es Aspekte die Cross-Cutting-Concerns darstellen, wie das Bereitstellen von Datenbanken (DBaaS) oder Message-Queues (MQaaS).


## Fazit
Die Clout hat alles auf den Kopf gestellt was noch vor 10 Jahren etabliert war.Trotzdem ist die lokale Software nicht überflüssig geworden. Es ist ein "sowohl als auch" demnach sollte man Cloud wie einen Werkzeugkasten sehen, aus den man auch so benutzt, statt völlig auf Statische Server zu verzichten.

Offene Formate und Standards sind jedoch sehr wichtig um sich nicht bei einem Anbieter festzufahren und einen Vendor-Lock-In zu vermeiden. Wer unabhängig von den Anbietern denkt, der hat die Möglichkeit zwischen verschiedenen Anbietern wechseln zu können. 


## Quellen
+ Repository M346
+ Julie
+ Hr. Calisto
+ the native web GmbH