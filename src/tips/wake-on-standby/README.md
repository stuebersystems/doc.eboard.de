# Wake On Standby

### Was ist Wake On Standby?

Mit [Wake On Standby](../../simple-glossary.md#wakeonstandby) kann man erreichen, dass der Computer zu einer bestimmen Uhrzeit per Zeitplan automatisch in den Energiesparmodus wechselt und anschließend zu einer vorgegebenen Uhrzeit wieder aufwacht.

### Wie wird es eingerichtet?

Wake On Standby ist nur durch Unterstützung eines Zeitgebers durch den Computer möglich. Die meisten modernen Computer unterstützen einen Zeitgeber. Unsere Industriecomputer unterstützen dies auch. Falls Ihr Computer die notwendige Fähigkeit nicht besitzt, [setzen Sie sich mit uns in Verbindung](http://www.stueber.de/contact.php) und wir unterstützen Sie gerne beim Kauf eines [Industriecomputers](../../setup-computer/Step-DS503/index.html).

In unserem Beispiel zeigen wir Ihnen, wie Sie Ihren Computer auf 19 Uhr abends \(Standby\) bzw. auf 8 Uhr morgens \(Wakeup\) einstellen.

> Wenn es sich bei Ihrem Computer um einen von uns gelieferten Industriecomputer handelt, können Sie direkt zu Schritt 2 springen. Ansonsten beginnen Sie mit Schritt 1, um zu prüfen, ob Ihr Computer Wake On Standby unterstützen kann.

## 1. Schritt: Energieoptionen einstellen {#energieoptionen-einstellen}

### Leerlaufzeit nach unbeaufsichtigter deaktivieren

* Um das unerwartete Ausschalten des Rechners zu vermeiden, muss die Energieoption **Leerlaufzeit nach unbeaufsichtigter** deaktivieren werden. Laden Sie folgende [Registry-Datei](ftp://ftp.stueber.de/pub/bin/de/windowsembedded/Leerlaufzeit_nach_unbeaufsichtigter-deaktivieren.reg) herunter und führen Sie sie aus. 

![](/images/wake-on-standby-1.png)

**Alternativ können Sie die Einstellung manuell einsetzen:**

* Drücken Sie die Tastenkombination `Windows` + `R`, um den Dialog `Ausführen` zu öffnen.

* Dort geben Sie den Befehl `regedit` ein und bestätigen mit `OK`.

* Klicken Sie bei der Anfrage der Benutzerkontensteuerung auf `Ja`. Die Windows-Registry öffnet sich.

* Klicken Sie sich durch folgende Schlüssel (Ordner) hindurch:

`Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Power\PowerSettings\7bc4a2f9-d8fc-4469-b07b-33eb785aaca0`

Falls die letzten Schlüssel noch nicht existieren, dann müssen Sie diese erstellen. Dazu klicken Sie mit der rechten Maustaste in das rechte Fenster. Im Kontextmenü wählen Sie `Neu` > `Schlüssel`.

* Doppelklicken Sie auf den Schlüssel `ACSettingIndex` (für Netzbetrieb) oder auf den Schlüssel `DCSettingIndex` (für Akkubetrieb). Falls die Schlüssel noch nicht existieren, dann müssen Sie diese erstellen. Dazu klicken Sie mit der rechten Maustaste in das rechte Fenster. Im Kontextmenü wählen Sie `Neu` > `DWORD-Wert` (REG_DWORD).

* In beiden Feldern geben Sie den Wert `0` ein:

![](/images/ACSettingsIndex.png)

> #### primary::Hinweis
>
> Diese Änderungen werden ggf. erst nach einem Neustart aktiv

### Ruhezustand deaktivieren

* Starten Sie die Eingabeaufforderung `cmd.exe` mit der Option `Als Administrator ausführen` 

![](/images/CMD-as_administrator.png)

und tippen Sie dann den folgenden Befehl ein:

![](/images/hibernate_off.png)

Bestätigen Sie mit `ENTER`. Dies hilft Ihnen dabei, Probleme und Konflikte beim Aufwachen zu vermeiden.

### Energiesparplan Höchstleistung einstellen
  
1. Aus dem Windows-Startmenü wählen Sie die `Systemsteuerung` und dann  
   `Anzeige > Kleine Symbole`, anschließend wählen Sie `Energieoptionen`.

   ![](/images/wake-on-standby-1.png "Energieoptionen auswählen")

2. Wählen Sie den Energiesparplan `Höchstleistung` aus, anschließend wählen Sie `Energiesparplaneinstellungen ändern`.

   ![](/images/wake-on-standby-2.png "Energiesparplaneinstellungen ändern")

3. Wählen Sie `Niemals` neben `Bidschirm ausschalten` und `Energiesparmodus nach` aus, anschließend wählen Sie `Erweiterte Energieeinstellungen ändern`.

   ![](/images/wake-on-standby-3.png "Erweiterte Energieeinstellungen")

4. Wählen Sie `Zurzeit nicht verfügbare Einstellungen ändern`.

   ![](/images/wake-on-standby-4.png "Nicht verfügbare Einstellungen ändern")

5. Unter `Energie sparen > Zeitgeber zur Aktivierung zulassen > Einstellung`  
   wählen Sie `Aktivieren` und anschließend `OK`.

   ![](/images/wake-on-standby-5.png "Zeitgeber zur Aktivierung zulassen")

## 2. Schritt: Standby-Modus konfigurieren

1. Aus dem Windows-Startmenü wählen Sie die `Systemsteuerung`, dann `Anzeige > Kategorie Kleine Symbole`, dann `Verwaltung` und dann `Aufgabenplanung`.

   ![](/images/wake-on-standby-6.png "Verwaltung auswählen")

   ![](/images/wake-on-standby-7.png "Aufgabenplanung auswählen")

2. Wählen nun im linken Menü `Aufgabenplanung (Lokal) > Aufgabeplanungsbibliothek`, anschließend klicken Sie im rechten Menü unter `Aktionen` auf `Einfache Aufgabe erstellen`.

   ![](/images/wake-on-standby-8.png "Einfache Ausgabe erstellen")

3. Geben Sie einen Namen für die Aufgabe z.B. „Schlaf“ ein und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-9.png "Schlaf eingeben")

4. Bleiben Sie bei der Auswahl `Täglich` und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-10.png "Wählen Sie "Täglich" aus")

5. Geben Sie unter `Datum und Zeit` ein, wann die Aktivierung abends stattfinden soll \(z.B. 19 Uhr\) und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-11.png "Datum und Uhrzeit eingeben")

6. Bleiben Sie bei der Auswahl `Programm starten` und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-12.png "Programm starten auswählen")

7. Fügen Sie bitte folgendes ein:

   * unter `Programm/Skript`: **C:\Windows\System32\rundll32.exe**
   * neben `Argumente hinzufügen (optional)`: **powrprof.dll,SetSuspendState 0,1,0**

   ![](/images/wake-on-standby-13.png "Skriptpfad angeben")

8. Klicken Sie `Weiter`.

9. Bevor Sie auf `Fertig stellen` klicken, stellen Sie sicher, dass Sie das folgende Häkchen gesetzt haben:

   ![](/images/wake-on-standby-14.png "Eigenschaften für diese Aufgabe öffnen")

10. Danach wählen Sie bitte folgende Häkchen aus:

    ![](/images/wake-on-standby-15.png "Sicherheitsoptionen auswählen")

11. Klicken Sie jetzt auf `OK`, dann ist der zweite Schritt abgeschlossen.

## 3. Schritt: Wake-Up-Modus konfigurieren

1. Wählen Sie wie schon im zweiten Schritt beschrieben `Aufgabenplanung (Lokal) > Aufgabeplanungsbibliothek` und dann `Einfache Aufgabe erstellen`.

   ![](/images/wake-on-standby-8.png "Einfache Ausgabe erstellen")

2. Geben Sie einen Namen ein z.B „Wach“ und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-16.png "Namen der Aufgaben zum Waken eintippen")

3. Bleiben Sie bei der Auswahl `Täglich` und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-10.png "Täglich auswählen")

4. Geben Sie unter `Datum und Zeit` ein, wann die Aktivierung morgens stattfinden soll \(z.B. 8 Uhr\) und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-17.png "Datum und Uhrzeit eingeben")

5. Bleiben Sie bei der Auswahl `Programm starten` und klicken Sie `Weiter`.

   ![](/images/wake-on-standby-12.png "Programm starten auswählen")

6. Unter `Programm/Skript` fügen Sie bitte folgendes ein: **ipconfig**.

   ![](/images/wake-on-standby-18.png "Skript angeben")

7. Klicken Sie `Weiter`.

8. Bevor Sie `Fertig stellen` klicken, stellen Sie sicher, dass Sie das folgende Häkchen gesetzt haben:

   ![](/images/wake-on-standby-19.png "Eigenschaften für diese Aufgabe öffnen")

9. Danach wählen Sie bitte folgende Häkchen aus:

   ![](/images/wake-on-standby-20.png "Sicherheitsoptionen einstellen")

10. Unter der Registerkarte `Bedingungen` setzten Sie folgendes Häkchen:

    ![](/images/wake-on-standby-21.png "Computer zum Ausführen der Aufgabe reaktivieren")

    Sie haben jetzt Wake On Standby aktiviert!



