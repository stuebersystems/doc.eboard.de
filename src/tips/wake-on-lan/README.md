# Wake On LAN

## Was ist Wake On LAN (WoL)?

[Wake On LAN] erlaubt das automatische Hochfahren eines Computers durch einen dedizierten Netzwerkbefehl. Wake On LAN ist ein Industriestandard und muss von der Netzwerkkarte unterstützt werden.

## Voraussetzungen

Wake On LAN wird von den meisten modernen Rechnern unterstützt inklusiv alle unserer Industriecomputer. Die Voraussetzungen für einen Einsatz von Wake On LAN sind:

* Der Computer ist an eine Stromquelle angeschlossen.
* Die Netzwerkkarte des Computers unterstützt Wake-On-LAN.
* Der Computer verfügt über eine Internetverbindung.
* Der Computer ist über ein Netzwerkkabel mit dem Internet verbunden.

## Konfiguration

### 1. Schritt: Wake On LAN im BIOS freischalten

Im BIOS des Computers muss gegebenenfalls Wake On LAN aktiviert werden. Das Vorgehen kann sich von Computer zu Computer unterscheiden. Meistens befindet sich die Einstellung under einer Registerkarte namens `Power` bzw. `Advanced`. Aktivieren Sie diese Wake On LAN-Option, anschließend speichern und beenden Sie das BIOS-Setup.

> #### primary::Hinweis
> Falls im BIOS keine Option zur Aktivierung von Wake On LAN vorhanden ist, lesen Sie das Handbuch des Mainboards, um sicher zu sein, dass Wake On LAN unterstützt wird. Für eine genaue Beschreibung der entsprechenden BIOS-Einstellung eines von uns gelieferten Rechner, schauen Sie sich die Seite "BIOS konfigurieren" des entsprechenden Rechners in der linken Navigation an.

![](/images/BIOS-Giada-i39B-Enable-WOL.png "Wake on LAN aktivieren")

### 2. Schritt: Netzwerkkarte einstellen

1. Klicken Sie im Windows-Startmenü auf `Systemsteuerung` und dort auf `Anzeige > Kleine Symbole`.
 
2. Klicken Sie auf `Netzwerk- und Freigabecenter`.
   
   ![](/images/wake-on-lan-1.png "Systemsteuerung > Netzwerk- und Freigabecenter")

3. Wählen Sie nun im linken Menü `Adaptereinstellungen ändern`.
   
   ![](/images/wake-on-lan-2.png "Adaptereinstellungen ändern")

4. Wählen Sie unter dem Netzwerkadapter im Kontextmenü (rechte Maustaste) der Netzwerkkarte die Option `Eigenschaften`.
   
   ![](/images/wake-on-lan-3.png "Wählen Sie Eigenschaften der Netzwerkkarte")

5. Wählen Sie die Schaltfläche `Konfigurieren`.
   
   ![](/images/wake-on-lan-4.png "Schaltfläche Konfigurieren wählen")

6. Unter der Registerkarte 'Energieverwaltung' aktivieren Sie die Option `Gerät kann den Computer aus dem Ruhezustand aktivieren`.
  
  ![](/images/wake-on-lan-5.png "Das Häkchen "Gerät kann den Computer aus dem Ruhezustand aktivieren" einsetzen")

### 3. Schritt: Programm zum Einschalten einstellen

Um den Rechner aus der Ferne herunterfahren zu können, muss folgender Wert in die Windows-Registrierung des entfernten Rechners eingespielt werden:

1. Öffnen Sie die Registrierungseditor.

2. Suchen Sie den folgenden Schlüssel und wählen Sie ihn aus:
  
   ````
   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\system
   ````

3. Klicken Sie auf `Bearbeiten > Neu` und wählen Sie `DWORD-Wert` aus.

4.  Geben Sie "LocalAccountTokenFilterPolicy" als Namen für den DWORD-Wert ein, und drücken Sie die `EINGABETASTE`.

5. Klicken Sie auf `LocalAccountTokenFilterPolicy` und dann auf `Bearbeiten > Ändern`. Ein Dialogfenster öffnet sich.

6. Geben Sie im Feld `Wert` "1" ein und bestätigen Sie mit `OK`.

7. Schließen Sie den Registrierungseditor.

### 4. Schritt: Programm zum Einschalten einstellen

Sie benötigen ein WoL-Programm bzw. eine App, um den Rechner von einem anderen Computer oder einem Smartphone aus aufzuwecken. Für Windows-Betriebssysteme empfehlen wir die kostenlose Open Source-Software [Wake on LAN von AquilaTech] (auch in deutscher Sprache verfügbar). 

Da dem PC im ausgeschalteten Zustand keine Netzwerk- bzw. IP-Adresse zugewiesen ist, funktioniert WoL über die Hardware-Kennung des Netzwerkgeräts. Diese nennt sich [MAC-Adresse]. Um sie herauszufinden, gehen Sie wie folgt vor:

1. Starten Sie die Eingabeaufforderung und geben Sie
   ````
   ipconfig /all
   ````
   ein. Bestätigen Sie mit `ENTER`.

3. Notieren Sie sich die [MAC-Adresse]. Notieren Sie sich auch die [IP-Adresse] für das Herunterfahren aus der Ferne bzw. zum Aufbau einer Remotedesktop-Sitzung.
   
   ![](/images/wake-on-lan-7.png "Mac-Adresse und IP-Adresse notieren")

4. Starten Sie nun das Programm Wake On Lan und wählen Sie `Datei > Neuer Host`.
   
   ![](/images/wake-on-lan-8.png "wählen Sie 'Datei > Neuer Host'")

5. Auf der Registerkarte `Aufwachen` geben Sie die `MAC-Adresse` und die `IP-Adresse` des Rechners ein.
   
   ![](/images/wake-on-lan-9.png "MAC-Adresse und IP-Adresse des Rechners eingeben")

5. Auf der Registerkarte `Herunterfahren` geben Sie den Benutzernamen und das Passwort des Rechners ein. Wenn der Rechner sich in keiner Domain befindet, geben Sie einfach den Computernamen des Rechners im Feld  `Domäne` ein. Die Option `Methode für das Herunterfahren` bleibt auf `WMI`.

   > #### 
   > Bei den von uns gelieferten Rechnern gibt es einen einzigen aktivierten Benutzer namens `user` mit standardmäßig keinem Kennwort.
   
   ![](/images/wake-on-lan-10.png "Windows-Zugangsdaten zum Herunterfahren eingeben")

6. Um einen Rechner herunterzufahren, wählen Sie ihn mit der rechten Maustaste aus und klicken Sie auf `Herunterfahren`. Optional haben Sie die Möglichkeit per Schaltfläche `Notfallabschalt` alle Rechner auf einmal herunterzufahren.
   
   ![Der Befehl "Herunterfahren"](/images/wake-on-lan-12.png)
   
   ![Das Dialogfenster "Runterfahren"](/images/wake-on-lan-13.png)

7. Um einen Rechner hochzufahren, wählen Sie ihn mit der rechten Maustaste aus und klicken Sie auf `Aufwachen`. Optional haben Sie die Möglichkeit per die Schaltfläche `Alle hochfahren` alle Rechner auf einmal hochzufahren.
   
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