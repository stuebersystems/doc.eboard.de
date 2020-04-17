# Wake On LAN

## Was ist Wake On LAN (WoL)?

[Wake On LAN] erlaubt das automatische Hochfahren eines Computers durch einen dedizierten Netzwerkbefehl. Wake On LAN ist ein Industriestandard und muss von der Netzwerkkarte unterstützt werden.

## Voraussetzungen

Wake On LAN wird von den meisten modernen Rechnern unterstützt inklusiv alle unserer Industriecomputer. Die Voraussetzungen für einen Einsatz von Wake On LAN sind:

* Der Computer ist an eine Stromquelle angeschlossen.
* Die Netzwerkkarte des Computers unterstützt Wake-On-LAN.
* Der Computer ist über ein Netzwerkkabel mit dem LAN verbunden.

## Konfiguration

### 1. Schritt: Wake On LAN im BIOS freischalten

Im BIOS des Computers muss gegebenenfalls Wake On LAN aktiviert werden. Das Vorgehen kann sich von Computer zu Computer unterscheiden. Meistens befindet sich die Einstellung under einer Registerkarte namens `Power` bzw. `Advanced`. Aktivieren Sie diese Wake On LAN-Option, anschließend speichern und beenden Sie das BIOS-Setup.

> #### primary::Hinweis
> Falls im BIOS keine Option zur Aktivierung von Wake On LAN vorhanden ist, lesen Sie das Handbuch des Mainboards, um sicher zu sein, dass Wake On LAN unterstützt wird. Für eine genaue Beschreibung der entsprechenden BIOS-Einstellung eines von uns gelieferten Rechner, schauen Sie sich die Seite "BIOS konfigurieren" des entsprechenden Rechners in der linken Navigation an.

![](/images/BIOS-Giada-i39B-Enable-WOL.png "Wake on LAN aktivieren")

### 2. Schritt: Netzwerkkarte einstellen

1. Drücken Sie die Tastenkombination `[Windows]` + `[R]`, um das Dialogfenster Ausführen zu öffnen. Dort geben Sie den Befehl `ncpa.cpl` ein und bestätigen mit `OK`.

   ![](/images/ncpa.cpl.png)
   
2. Wählen Sie unter dem im LAN verbunden Netzwerkadapter im Kontextmenü (rechte Maustaste) die Option `Eigenschaften`.
   
   ![](/images/wake-on-lan-3.png "Wählen Sie Eigenschaften der Netzwerkkarte")

3. Wählen Sie die Schaltfläche `Konfigurieren`.
   
   ![](/images/wake-on-lan-4.png "Schaltfläche Konfigurieren wählen")

4. Unter der Registerkarte 'Energieverwaltung' aktivieren Sie die Option `Gerät kann den Computer aus dem Ruhezustand aktivieren`.
  
  ![](/images/wake-on-lan-5.png "Das Häkchen "Gerät kann den Computer aus dem Ruhezustand aktivieren" einsetzen")

### 3. Schritt: Programm zum Einschalten einstellen

Sie benötigen ein WoL-Programm bzw. eine App, um den Rechner von einem anderen Computer oder einem Smartphone aus aufzuwecken. Für Windows-Betriebssysteme empfehlen wir die kostenlose Open Source-Software [Wake on LAN von AquilaTech](https://download.stueber.de/doc/de/support/WakeOnLAN_2.11.4.exe). 

Da dem PC im ausgeschalteten Zustand keine Netzwerk- bzw. IP-Adresse zugewiesen ist, funktioniert WoL über die Hardware-Kennung des Netzwerkgeräts. Diese nennt sich [MAC-Adresse](#MAC-Adresse). Um sie herauszufinden, gehen Sie wie folgt vor:

1. Wählen Sie unter dem im LAN verbunden Netzwerkadapter im Kontextmenü (rechte Maustaste) die Option `Status`.

   ![](/images/wake-on-lan-14.png)

2. Notieren Sie sich die [MAC-Adresse].  Optional können Sie sich auch die [IP-Adresse] für das Herunterfahren aus der Ferne bzw. zum Aufbau einer Remotedesktop-Sitzung notieren.
   
   ![](/images/wake-on-lan-7.png "Mac-Adresse und IP-Adresse notieren")

3. Starten Sie nun das Programm Wake On Lan und wählen Sie `Datei > Neuer Host`.
   
   ![](/images/wake-on-lan-8.png "Wählen Sie 'Datei > Neuer Host'")

4. Auf der Registerkarte `Bildschirmeigenschaften` geben Sie einen Namen für den Rechner ein.
   
   ![](/images/wake-on-lan-16.png "Namen für den Rechner eingeben")

5. Auf der Registerkarte `Aufwachen` geben Sie die `MAC-Adresse` und die `IP-Adresse` des Rechners ein, anschließend klicken Sie auf `OK`. Wenn Sie keine IP-Adresse haben, geben Sie einfach `x` in diesem Feld ein.
   
   ![](/images/wake-on-lan-9.png "MAC-Adresse und IP-Adresse des Rechners eingeben")
   
6. Um einen Rechner hochzufahren, wählen Sie ihn mit der rechten Maustaste aus und klicken Sie auf `Aufwachen`. Optional haben Sie die Möglichkeit per die Schaltfläche `Alle hochfahren` alle Rechner auf einmal hochzufahren.
   
   ![Der Befehl "Aufwachen"](/images/wake-on-lan-11.png)

## Einen Rechner per Smartphone aufwecken

Für iOS empfehlen wir die App [EasyWOL für iOS].

![](/images/EasyWOL.iOS.jpg "EasyWOL für iOS")

Für Android empfehlen wir die App [EasyWOL für Android].

![](/images/EasyWOL.Android.png "EasyWOL für Android")

[Wake On LAN]: ../../simple-glossary.md#wakeonlan
[MAC-Adresse]: ../../simple-glossary.md#mac
[IP-Adresse]: ../../simple-glossary.md#ip
[Wake on LAN von AquilaTech]: https://github.com/basildane/WakeOnLAN/releases/download/2.11.4/WakeOnLAN_2.11.4.exe
[EasyWOL für Android]: https://play.google.com/store/apps/details?id=easy_wol.mysysadmintips.com.easywol&hl=de
[EasyWOL für iOS]: https://itunes.apple.com/de/app/easywol/id828429776?mt=8