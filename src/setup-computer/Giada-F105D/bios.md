# Giada F105D | BIOS konfigurieren

> #### info::Modell
> Giada F105D (120GB HD)

* Beim Rechner-Start drücken Sie die Taste `[Entf]`.

* Drücken Sie `[F9]`, anschließend die `[Eingabetaste]`, um die Einstellungen neu zu setzen.

![](../../images/BIOS_Giada-F105D_F9_Load-Defaults.jpg "BIOS-Einstellungen neusetzen")

Unter der Registerkarte `Chipset` wählen Sie `South Cluster Configuration`, anschließend `Miscellaneous Configuration`. Unter **State After G3** wählen Sie `S0 State` aus.

![](../../images/BIOS_Giada-F105D_PowerON.jpg "S0 State einstellen")

Unter der Registerkarte `Advanced` wählen Sie `CSM Configuration`. Unter **Boot option filter** wählen Sie `UEFI only` aus. Unter **Storage** wählen Sie `UEFI` aus.

![](../../images/BIOS_Giada-F105D_UEFI.jpg "UEFI einstellen")

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

![](../../images/BIOS_Giada-F105D_F10_Save_and_Exit.jpg "Einstellungen abspeichern und Rechner neustarten")

# Wake-On-LAN (WOL)

Wenn Wake-On-LAN (WOL) gewünscht ist, finden Sie die Einstellung dazu unter der Registerkarte `Advanced` -> `Wake Configuration`.

![](../../images/BIOS_Giada-F105D_Wake-Configuration.jpg "WakeUp Konfiguration")

* Unter "Wake On Lan" wählen Sie die Option `[Enabled]` aus.

![](../../images/BIOS_Giada-F105D_Advanced-Wakeup-Config.jpg "Restore AC Power Loss: Power On")

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

* Unter Windows in den Einstellungen des LAN-Adapters aktivieren Sie **Wake-On-LAN herunterfahren**:

![](../../images/Wake-On-Lan_herunterfahren.png "Wake-On-Lan herunterfahren aktivieren")

Weitere Informationen zu Wake-On-LAN (WOL) finden Sie [hier](/tips/wake-on-lan/README.md)

# Wake system from RTC

Unter dieser Option kann man eine Uhrzeit einstellen, zu der das System täglich hochgefahren wird.

Diese Option befindet sich unter der Registerkarte `[Advanced]` und `[Wake system from RTC]`.

![](../../images/BIOS_Giada-F105D_RTC-Wake.jpg "System wacht täglich um 7 Uhr auf")


