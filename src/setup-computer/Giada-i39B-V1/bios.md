# Giada i39B V1 | BIOS konfigurieren

> #### info::Modell
> Giada i39B V1 (60GB HD)

Wählen Sie die passende Anleitung für Ihren Giada i39B Rechner:

## BIOS-Art: Phoenix SecureCore Tiano

* Beim Rechner-Start drücken Sie die Taste `[F2]`.

* Drücken Sie `[F9]`, anschließend die `[Eingabetaste]`, um die Einstellungen neu zu setzen.

![](../../images/BIOS_i39B_F9_Load_Defaults.jpg "Load Default Values")

* Mit den Pfeiltasten wählen Sie die Registerkarte `[Advanced]`, anschließend unter `[State After G3]` wählen Sie `[State S0]` aus.

![](../../images/BIOS_i39B_PowerON.jpg "Restore AC Power Loss: Power On")

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

![](../../images/BIOS_i39B_F10_Save_and_Exit.jpg "Einstellungen abspeichern und Rechner neustarten")

## Wake-On-LAN (WOL)

Wenn Wake-On-LAN (WOL) gewünscht ist, finden Sie die Einstellung dazu unter der Registerkarte "Advanced".

![](../../images/BIOS-Giada-i39B-Enable-WOL.jpg "BIOS-Einstellung zu Wake-On-LAN (WOL)")

## BIOS-Art: American Megatrends Inc

* Beim Rechner-Start drücken Sie die Taste `[Entf]`.

* Drücken Sie `[F9]`, anschließend die `[Eingabetaste]`, um die Einstellungen neu zu setzen.

![](../../images/BIOS-AMI-Load-Optimized-Defaults.jpg "Load Default Values")

* Mit den Pfeiltasten wählen Sie die Registerkarte `[Chipset]` und wählen Sie die Option `[South Bridge]` aus.

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

