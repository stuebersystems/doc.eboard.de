# Giada F105D | BIOS konfigurieren

> #### info::Modell
> Giada F105D (120GB HD)

* Beim Rechner-Start drücken Sie die Taste `[Entf]`.

* Drücken Sie `[F9]`, anschließend die `[Eingabetaste]`, um die Einstellungen neu zu setzen.

![BIOS-Einstellungen neusetzen](../../images/BIOS_Giada-F105D_F9_Load-Defaults.jpg)

Unter der Registerkarte `Chipset` wählen Sie `South Cluster Configuration`, anschließend `Miscellaneous Configuration`. Unter **State After G3** wählen Sie `S0 State` aus.

![S0 State einstellen](../../images/BIOS_Giada-F105D_PowerON.jpg)

Unter der Registerkarte `Advanced` wählen Sie `CSM Configuration`. Unter **Boot option filter** wählen Sie `UEFI only` aus. Unter **Storage** wählen Sie `UEFI` aus.

![UEFI einstellen](../../images/BIOS_Giada-F105D_UEFI.jpg)

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

![Einstellungen abspeichern und Rechner neustarten](../../images/BIOS_Giada-F105D_F10_Save_and_Exit.jpg)

# Wake-On-LAN (WOL)

## WoL im BIOS freischalten

Wenn Wake-On-LAN (WOL) gewünscht ist, finden Sie die Einstellung dazu unter der Registerkarte `Advanced` -> `Wake Configuration`.

![Wake Konfiguration](../../images/BIOS_Giada-F105D_Wake-Configuration.jpg)

* Unter "Wake On Lan" wählen Sie die Option `[Enabled]` aus.

![Wake On LAN (WoL) im BIOS freischalten](../../images/BIOS_Giada-F105D_Advanced-Wakeup-Config.jpg)

* Drücken Sie `[F10]`, anschließend die `[Eingabetaste]`, um die Einstellungen abzuspeichern und den Rechner neu zu starten.

![Einstellungen abspeichern und Rechner neustarten](../../images/BIOS_Giada-F105D_Advanced-Wakeup-Config_F10.jpg)

## WoL in Windows freischalten

* Unter Windows in den Einstellungen des LAN-Adapters aktivieren Sie die Eigenschaft `Wake-On-LAN herunterfahren`:

![LAN-Adapter "Wake-On-LAN herunterladen" in Windows freischalten](../../images/Wake-On-Lan_herunterfahren.png)

Weitere Informationen zu Wake-On-LAN (WOL) finden Sie [hier](/tips/wake-on-lan/README.md)

# Wake system from RTC

Unter dieser Option kann man eine Uhrzeit einstellen, zu der das System täglich hochgefahren wird.

Diese Option befindet sich unter der Registerkarte `[Advanced]` und `[Wake system from RTC]`.

![System wacht täglich um 7 Uhr auf](../../images/BIOS_Giada-F105D_RTC-Wake.jpg)


