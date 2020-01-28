# Nano E350 | BIOS konfigurieren


> #### info::Modell
> Nano E350 (160GB HD)

* Beim Rechner-Start drücken Sie die Taste `[F12]`.

* Mit den Pfeiltasten wählen Sie `[Enter Setup]` aus.

![](../../images/BIOS_NanoE350_Enter-Setup.jpg "Select "Enter Setup"")

* Mit den Pfeiltasten wählen Sie die Registerkarte `[Save & Exit]`, dann `[Restore Defaults]`, anschließend wählen Sie `[YES]`, um die Einstellungen erst neu zu setzen.

![](../../images/BIOS_NanoE350_Load-Defaults.jpg "Load BIOS defaults")

* Wählen Sie die Registerkarte `[Advanced]`. Wählen Sie `[Power On]` unter 'Power Failure' aus, anschließend `[AHCI]` unter 'OnChip SATA Type'.

![](../../images/BIOS_NanoE350_PowerON_SATA-Type_ACHI.jpg "BIOS Power Failure: Power On. SATA-Type: ACHI")

* Jetzt drücken Sie `[F10]` und wählen Sie `[YES]`, um die Änderungen abzuspeichern und den Rechner neu zu starten.**

## Wake-On-LAN (WOL)

Wenn Wake-On-LAN (WOL) gewünscht ist, muss diese Funktion nur in [Windows](/tips/wake-on-lan/README.md) freigeschaltet werden. Dieser Rechner reagiert auf Wake-On-LAN-Anfragen, trotz fehlender Einstellung im BIOS.

.

