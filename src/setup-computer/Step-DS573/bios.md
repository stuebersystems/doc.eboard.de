# Step DS573 | BIOS Konfigurieren

> #### info::Modell
> Step DS573 (120GB HD)

* Beim Rechner-Start drücken Sie die Taste `[F2]`.

* Drucken Sie die Taste `[F9]`, anschließend wählen Sie `[YES]`, um die Einstellungen erst neu zu setzen. 

![](../../images/BIOS_DS573_F9_Load-Defaults.jpg "Werkseinstellung laden")

* Wählen Sie die Schaltfläche `Advanced`.

![](../../images/BIOS_DS573_Advanced.jpg "Advanced Optionen")

* Wählen die Registerkarte **Power**, anschließend wählen Sie unter "After Power Failure" die Option `Power On` aus.

![](../../images/BIOS_DS573_PowerON.jpg "After Power Failure: Power On")

* Um die Änderungen abzuspeichern, drucken Sie die Taste `[F10]`. Drücken Sie die Taste `[Eingabe]`, um "Yes" zu bestätigen.

![](../../images/BIOS_DS573_F10_Save_and_Exit.jpg "F10: BIOS-Änderungen abspeichern")

## Wake-On-LAN (WOL)

Wenn Wake-On-LAN (WOL) gewünscht ist, muss diese Funktion nur in [Windows](/tips/wake-on-lan/README.md) freigeschaltet werden. Dieser Rechner reagiert auf Wake-On-LAN-Anfragen, trotz fehlender Einstellung im BIOS.

## Wake system from RTC

Unter dieser Option kann man eine Uhrzeit einstellen, zu der das System täglich hochgefahren wird.

Diese Option befindet sich unter der Registerkarte `[Power]` und `[Wake system from S5]`.

![](../../images/BIOS_Step-DS573-RTCWake.jpg "System wacht täglich um 10 Uhr auf")




