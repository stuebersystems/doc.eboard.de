# Giada i39B V2 | BIOS konfigurieren

> #### info::Modell
> Giada i39B V2 (60GB HD)

* Beim Rechner-Start drücken Sie die Taste `[Entf]`.

* Drücken Sie `[F9]`, anschließend die `[Eingabetaste]`, um die Einstellungen neu zu setzen.

![](../../images/BIOS-AMI-Load-Optimized-Defaults.jpg "Load Default Values")

* Um das gewünschte Betriebssystem (z.B. Windows 10) unterstützen zu können, müssen Sie unter `Advanced` -> `Miscellaneous Configuration` mit den Pfeiltasten die passende Auswahl (d.h. Windows 8.X für Win8.X bis Win10) treffen. Bestätigen Sie mit der Eingabe-Taste.

![](../../images/BIOS-AMI-Miscellaneous.Configuration.png "Advanced - Miscellaneous Configuration")

* Unter `OS Selection` wählen Sie z.B. `Windows 8.X` aus.

![](../../images/BIOS-AMI-OS-Win8.png "Betriebssystem: Windows 8.X auswählen")

* Wählen Sie die Registerkarte `[Chipset]`, anschließend die Option `[South Bridge]` aus.

![](../../images/BIOS-AMI-South-bridge.jpg "Chipset > South BridgeRestore")

* Unter "Restore AC Power Loss" wählen Sie die Option `[Power On]` aus.

![](../../images/BIOS-AMI-AC-PowerLoss_PowerON.jpg "Chipset > South BridgeRestore")

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

![](../../images/BIOS-AMI-Save-Configuration.jpg "Einstellungen abspeichern und Rechner neustarten")

## Wake-On-LAN (WOL)

Wenn Wake-On-LAN (WOL) gewünscht ist, finden Sie die Einstellung dazu unter der Registerkarte "Advanced".

![](../../images/BIOS-AMI-Advanced-Wakeup-Config.jpg "WakeUp Konfiguration")

* Unter "Resume On LAN" wählen Sie die Option `[Resume On LAN]` aus.

![](../../images/BIOS-AMI-Advanced-Wakeup-Enable.jpg "Restore AC Power Loss: Power On")

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

## Einschalten durch Real Time Clock

Unter dieser Option kann man eine Uhrzeit einstellen, zu der das System täglich hochgefahren wird.

Diese Option befindet sich unter der Registerkarte `[Advanced]` und `[Resume on RTC Alarm]` stellen Sie die gewünschte Uhrzeit ein.

![System wacht täglich um 7 Uhr auf](../../images/BIOS_Giada-i39B_RTC-Wake.png)