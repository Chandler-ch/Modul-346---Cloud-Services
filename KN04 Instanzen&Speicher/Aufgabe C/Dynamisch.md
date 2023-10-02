## Vorbereitung
Wie immer setzen wir eine neue Instanz auf, dieses mal jedoch mit Microsoft, statt Ubuntu. Hierbei ist alles wie normal, bis auf die Security Group, bei welcher wir eine bereits bestehende nehmen, welche wir zu einem späteren Zeitpunkt für RDP konfigurieren.

Wir fügen also noch eine Inbound-Rule festlegen, sodass RDP Zugriff möglich ist.

![inbound](inbound-rules.png)

## Verbinden
Um zu Verbinden brauchen wir exakt 3 Dinge um den RDP zufriedenzustellen.
* DNS-Name
* Administrator
* Password
Und da wir das Passwort noch nicht haben, holen wir es uns jetzt.
Wir gehen unter den Instanzen auf die ID unserer Instanz und kommen dann zu einem Tab namens "RDP Client".Zuunterst in dieser Seite bekommen wir das Passwort was wir brauchen. Unter "Get Password". Jedenfalls laden wir hier unseren Private Key, passend zum Key Pair was wir ausgewählt haben, hoch.

![Decrypt](Decrypten.png)

Jetzt wird das Password decryptet an der Seite angezeigt.

## RemoteDesktopVerbindung
Für die Verbindung sind 3 wichtige Schritte nötig.
Erstens, wir müssen in die Firewall gehen unter dem Control Panel
Hier fügen wir unsere gespeicherten Daten aus dem RDP-Client Tab rein.

![RDV](RDV.png)

-----------------------------------------------------------------------------------------------------------

Hier muss ich leider erstmal pausieren, die Aufgabe kann ich noch nicht vollständig lösen.

## Quellen
+ Repository M346
+ Microsoft
+ Youtube