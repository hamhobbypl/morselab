# MorseLAB – Release Notes 3.4

MD5 (firmware_3_4.bin) = ea08e4688d0adffe93fa86e4325eb65d

---

# 🇵🇱 Polski

## Release Notes

### Nowe Funkcje

#### Nowy Tryb Nauki „Phrases”

Dodano nowy tryb ćwiczeń **Phrases**.

Podobnie jak istniejący tryb Drill, umożliwia ćwiczenie całych fraz zamiast pojedynczych słów.

W przeciwieństwie do Drill, użytkownik może definiować własne frazy, np. realistyczne QSO zapisane w pliku `phrases.txt`.

### Przykładowa zawartość `phrases.txt`

```txt
CQ CQ CQ DE SP8KM SP8KM K
SP8KM DE SQ5ABC = GM = UR RST 599 599 = QTH WARSZAWA <KN>
SQ5ABC DE SP8KM = TNX FER CALL = UR RST 579 579 = QTH DEBICA =
SP8KM DE SQ5ABC = NAME TOM TOM = HW CPY? =
SQ5ABC DE SP8KM = FB TOM = NAME ADAM ADAM = WX SUNNY 20C =
SP8KM DE SQ5ABC = QSL ADAM = RIG 100W = ANT DIPOLE =
SQ5ABC DE SP8KM = TNX FER QSO TOM = NICE TO MEET U =
SP8KM DE SQ5ABC = HERE ADAM ADAM = HOPE CU AGN = 73 =
SQ5ABC DE SP8KM = 73 TOM = GL =
SP8KM DE SQ5ABC = 73 = <SK>
```

#### Dodano Obsługę Prosignu `<CT>`

Dodano obsługę prosignu `<CT>`.

---

## Usprawnienia MQTT CHAT

* Zwiększono bufory komunikacji MQTT
* Dodano oddzielne wątki dla nadawania i odbioru
* Poprawiono stabilność oraz responsywność

Dodatkowo:

* Jeśli istnieje plik `rooms.txt`, domyślne pokoje (`PUBLIC1`, `PUBLIC2`, `TEST`) nie są już automatycznie wyświetlane.

---

## Usprawnienia KEYER

### Eksperymentalna Obsługa Klawiatur Bluetooth

Dodano eksperymentalną obsługę klawiatur Bluetooth w trybie KEYER.

### Nowa Wersja KEYER

Dodano nową implementację KEYER z tym samym menu konfiguracji 4 parametrów uruchamianym długim przytrzymaniem enkodera.

Typ KEYER-a konfiguruje się w pliku `ktype.txt`:

```txt
0
# KEYER TYPE CONFIGURATION
# 0 - OLD VERSION
# 1 - NEW VERSION
# 2 - WITH BLUETOOTH
# 3 - CHOOSE BETWEEN NEW VERSION OR BLUETOOTH VERSION
```

---

## Usprawnienia HEAD COPY

Dodano obsługę pliku konfiguracyjnego `headcpy.txt` dla ćwiczeń:

* HeadCopy
* CopyCallsign

Jeśli `headcpy.txt` nie jest używany, urządzenie automatycznie zapamiętuje ostatnie ustawienia użytkownika, jednak wymagane jest ich potwierdzenie przy każdym uruchomieniu.

### Przykładowa konfiguracja

```txt
18-28
0
12-18
17-22
650-900
# HEADCPY CONFIGURATION FILE
# 1 LINE: WPM VALUE OR RANGE
# 2 LINE: SPACING MODE: 0 - FWPM, 1 - BWPM
# 3 LINE: FWPM VALUE/RANGE IF LINE 2 = 0, BWPM VALUE/RANGE IF LINE 2 = 1
# 4 LINE: VOLUME VALUE OR RANGE 0-100
# 5 LINE: PITCH VALUE OR RANGE 300-2000
```

---

## Usprawnienia Ćwiczeń Odbioru

W ćwiczeniach odbioru wyjście z ćwiczenia wymaga teraz potwierdzenia.

Po krótkim naciśnięciu enkodera użytkownik może wybrać:

* RESUME
* EXIT

Zapobiega to przypadkowemu zakończeniu ćwiczenia.

---

## Usprawnienia FILEMNG

FILEMNG obsługuje teraz:

* Edycję plików bezpośrednio przez interfejs WEB
* Tworzenie nowych plików przez interfejs WEB

Znacznie upraszcza to:

* Dodawanie własnych ćwiczeń
* Zarządzanie plikami tekstowymi i konfiguracyjnymi

---

## HAM CLOCK (HAMCLK)

Dodano nowy moduł HAM CLOCK wyświetlający:

* Czas UTC
* Czas lokalny na podstawie lokatora
* Aktywność słoneczną
* Status propagacji dla pasm 80m, 40m, 20m i 10m

Moduł potrafi również:

* Nadawać czas alfabetem Morse’a
* Literować czas głosem z plików mp3

Wybudzanie ze screensavera może nastąpić przez:

* zaprogramowane zdarzenia czasowe (co 10 minut lub co 1 godzinę),
* enkoder,
* klucz telegraficzny.

Dane słoneczne pobierane są z usług NOAA Space Weather:

* SFI / Solar Flux
* Kp Index

### Przykładowa konfiguracja `hamclk.txt`

```txt
KO00RC
2
23
20
17
1
1
+2
# HAMCLK CONFIGURATION FILE
# 1 LINE: LOCATOR
# 2 LINE: 0 - NO MORSE, 1 - MORSE EVERY HOUR, 2 - MORSE EVERY 10 MIN
# 3 LINE: WPM
# 4 LINE: FWPM
# 5 LINE: VOLUME
# 6 LINE: 0 - VOICE SPELLING OFF, 1 - VOICE SPELLING ON
# 7 LINE: SPELLING FOLDER 0 - LETTERSEN, 1 – LETTERS
# 8 LINE: UTC OFFSET IF AUTO FROM LOCATOR IS NOT WORKING
```

---

## Zmiany UI / Menu

* Przeniesiono UPGRADE przed SETUP w głównym menu
* Dodano okna potwierdzeń dla:

  * UPGRADE
  * DEFAULTS

---

# 🇬🇧 English

## Release Notes

### New Features

#### New “Phrases” Training Mode

Added a new **Phrases** exercise mode.

Similar to the existing Drill exercise, it allows practicing complete phrases instead of single words.

Unlike Drill, users can define their own custom phrases, for example realistic QSO exchanges stored in `phrases.txt`.

### Example `phrases.txt`

```txt
CQ CQ CQ DE SP8KM SP8KM K
SP8KM DE SQ5ABC = GM = UR RST 599 599 = QTH WARSZAWA <KN>
SQ5ABC DE SP8KM = TNX FER CALL = UR RST 579 579 = QTH DEBICA =
SP8KM DE SQ5ABC = NAME TOM TOM = HW CPY? =
SQ5ABC DE SP8KM = FB TOM = NAME ADAM ADAM = WX SUNNY 20C =
SP8KM DE SQ5ABC = QSL ADAM = RIG 100W = ANT DIPOLE =
SQ5ABC DE SP8KM = TNX FER QSO TOM = NICE TO MEET U =
SP8KM DE SQ5ABC = HERE ADAM ADAM = HOPE CU AGN = 73 =
SQ5ABC DE SP8KM = 73 TOM = GL =
SP8KM DE SQ5ABC = 73 = <SK>
```

#### Added `<CT>` Prosign Support

Added support for the `<CT>` prosign.

---

## MQTT CHAT Improvements

* Increased MQTT communication buffers
* Added separate threads for transmit and receive operations
* Improved stability and responsiveness

Additionally:

* If `rooms.txt` exists, default rooms (`PUBLIC1`, `PUBLIC2`, `TEST`) are no longer displayed automatically.

---

## KEYER Improvements

### Experimental Bluetooth Keyboard Support

Added experimental Bluetooth keyboard support in KEYER mode.

### New KEYER Version

Added a new KEYER implementation with the same 4-parameter long-press encoder configuration menu.

KEYER type selection is configured in `ktype.txt`:

```txt
0
# KEYER TYPE CONFIGURATION
# 0 - OLD VERSION
# 1 - NEW VERSION
# 2 - WITH BLUETOOTH
# 3 - CHOOSE BETWEEN NEW VERSION OR BLUETOOTH VERSION
```

---

## HEAD COPY Improvements

Added support for the `headcpy.txt` configuration file for:

* HeadCopy
* CopyCallsign

If `headcpy.txt` is not used, the device automatically remembers the last user preferences, but confirmation is required every time.

### Example Configuration

```txt
18-28
0
12-18
17-22
650-900
# HEADCPY CONFIGURATION FILE
# 1 LINE: WPM VALUE OR RANGE
# 2 LINE: SPACING MODE: 0 - FWPM, 1 - BWPM
# 3 LINE: FWPM VALUE/RANGE IF LINE 2 = 0, BWPM VALUE/RANGE IF LINE 2 = 1
# 4 LINE: VOLUME VALUE OR RANGE 0-100
# 5 LINE: PITCH VALUE OR RANGE 300-2000
```

---

## Receive Training Improvements

Receive exercises now require confirmation before exiting.

After a short encoder press, users can choose:

* RESUME
* EXIT

This prevents accidental termination of exercises.

---

## FILEMNG Improvements

FILEMNG now supports:

* Editing files directly through the WEB interface
* Creating new files through the WEB interface

This greatly simplifies:

* Adding custom exercises
* Managing text and configuration files

---

## HAM CLOCK (HAMCLK)

Added a new HAM CLOCK module displaying:

* UTC time
* Local time based on locator
* Solar activity
* Band propagation status for 80m, 40m, 20m and 10m

The module can also:

* Send time in Morse code
* Spell time using mp3 voice files

Wake-up from screen saver is possible via:

* scheduled time events (every 10 minutes or every 1 hour),
* encoder,
* Morse key.

Solar data is retrieved from NOAA Space Weather services:

* SFI / Solar Flux
* Kp Index

### Example `hamclk.txt` Configuration

```txt
KO00RC
2
23
20
17
1
1
+2
# HAMCLK CONFIGURATION FILE
# 1 LINE: LOCATOR
# 2 LINE: 0 - NO MORSE, 1 - MORSE EVERY HOUR, 2 - MORSE EVERY 10 MIN
# 3 LINE: WPM
# 4 LINE: FWPM
# 5 LINE: VOLUME
# 6 LINE: 0 - VOICE SPELLING OFF, 1 - VOICE SPELLING ON
# 7 LINE: SPELLING FOLDER 0 - LETTERSEN, 1 – LETTERS
# 8 LINE: UTC OFFSET IF AUTO FROM LOCATOR IS NOT WORKING
```

---

## UI / Menu Changes

* Moved UPGRADE before SETUP in the main menu
* Added confirmation dialogs for:

  * UPGRADE
  * DEFAULTS

---

# 🇩🇪 Deutsch

## Release Notes

### Neue Funktionen

#### Neuer Trainingsmodus „Phrases“

Ein neuer Übungsmodus **Phrases** wurde hinzugefügt.

Ähnlich wie der bestehende Drill-Modus ermöglicht er das Üben kompletter Phrasen statt einzelner Wörter.

Im Gegensatz zu Drill können Benutzer eigene Phrasen definieren, z. B. realistische QSO-Beispiele in der Datei `phrases.txt`.

### Beispielinhalt von `phrases.txt`

```txt
CQ CQ CQ DE SP8KM SP8KM K
SP8KM DE SQ5ABC = GM = UR RST 599 599 = QTH WARSZAWA <KN>
SQ5ABC DE SP8KM = TNX FER CALL = UR RST 579 579 = QTH DEBICA =
SP8KM DE SQ5ABC = NAME TOM TOM = HW CPY? =
SQ5ABC DE SP8KM = FB TOM = NAME ADAM ADAM = WX SUNNY 20C =
SP8KM DE SQ5ABC = QSL ADAM = RIG 100W = ANT DIPOLE =
SQ5ABC DE SP8KM = TNX FER QSO TOM = NICE TO MEET U =
SP8KM DE SQ5ABC = HERE ADAM ADAM = HOPE CU AGN = 73 =
SQ5ABC DE SP8KM = 73 TOM = GL =
SP8KM DE SQ5ABC = 73 = <SK>
```

#### Unterstützung für `<CT>` hinzugefügt

Unterstützung für das Prosign `<CT>` wurde hinzugefügt.

---

## MQTT CHAT Verbesserungen

* MQTT-Kommunikationspuffer vergrößert
* Separate Threads für Senden und Empfangen hinzugefügt
* Stabilität und Reaktionsfähigkeit verbessert

Zusätzlich:

* Falls `rooms.txt` existiert, werden die Standardräume (`PUBLIC1`, `PUBLIC2`, `TEST`) nicht mehr automatisch angezeigt.

---

## KEYER Verbesserungen

### Experimentelle Bluetooth-Tastaturunterstützung

Experimentelle Unterstützung für Bluetooth-Tastaturen im KEYER-Modus hinzugefügt.

### Neue KEYER-Version

Neue KEYER-Implementierung mit demselben 4-Parameter-Konfigurationsmenü per langem Druck auf den Encoder hinzugefügt.

Die KEYER-Auswahl wird über `ktype.txt` konfiguriert:

```txt
0
# KEYER TYPE CONFIGURATION
# 0 - OLD VERSION
# 1 - NEW VERSION
# 2 - WITH BLUETOOTH
# 3 - CHOOSE BETWEEN NEW VERSION OR BLUETOOTH VERSION
```

---

## HEAD COPY Verbesserungen

Unterstützung für die Konfigurationsdatei `headcpy.txt` hinzugefügt für:

* HeadCopy
* CopyCallsign

Wenn `headcpy.txt` nicht verwendet wird, merkt sich das Gerät automatisch die letzten Einstellungen, eine Bestätigung ist jedoch weiterhin erforderlich.

### Beispielkonfiguration

```txt
18-28
0
12-18
17-22
650-900
# HEADCPY CONFIGURATION FILE
# 1 LINE: WPM VALUE OR RANGE
# 2 LINE: SPACING MODE: 0 - FWPM, 1 - BWPM
# 3 LINE: FWPM VALUE/RANGE IF LINE 2 = 0, BWPM VALUE/RANGE IF LINE 2 = 1
# 4 LINE: VOLUME VALUE OR RANGE 0-100
# 5 LINE: PITCH VALUE OR RANGE 300-2000
```

---

## Verbesserungen beim Empfangstraining

Beim Verlassen von Empfangsübungen ist jetzt eine Bestätigung erforderlich.

Nach kurzem Druck auf den Encoder kann gewählt werden:

* RESUME
* EXIT

Dadurch wird ein versehentliches Beenden verhindert.

---

## FILEMNG Verbesserungen

FILEMNG unterstützt jetzt:

* Bearbeiten von Dateien direkt über das WEB-Interface
* Erstellen neuer Dateien über das WEB-Interface

Dies vereinfacht:

* Hinzufügen eigener Übungen
* Verwaltung von Text- und Konfigurationsdateien

---

## HAM CLOCK (HAMCLK)

Neues HAM CLOCK Modul hinzugefügt mit Anzeige von:

* UTC-Zeit
* Lokaler Zeit basierend auf Locator
* Sonnenaktivität
* Ausbreitungsstatus für 80m, 40m, 20m und 10m

Das Modul kann außerdem:

* Zeit in Morsecode senden
* Zeit per mp3-Sprachausgabe buchstabieren

Aufwecken aus dem Bildschirmschoner möglich durch:

* geplante Zeitereignisse (alle 10 Minuten oder jede 1 Stunde),
* Encoder,
* Morsetaste.

Solardaten werden von NOAA Space Weather Diensten geladen:

* SFI / Solar Flux
* Kp Index

### Beispiel `hamclk.txt`

```txt
KO00RC
2
23
20
17
1
1
+2
# HAMCLK CONFIGURATION FILE
# 1 LINE: LOCATOR
# 2 LINE: 0 - NO MORSE, 1 - MORSE EVERY HOUR, 2 - MORSE EVERY 10 MIN
# 3 LINE: WPM
# 4 LINE: FWPM
# 5 LINE: VOLUME
# 6 LINE: 0 - VOICE SPELLING OFF, 1 - VOICE SPELLING ON
# 7 LINE: SPELLING FOLDER 0 - LETTERSEN, 1 – LETTERS
# 8 LINE: UTC OFFSET IF AUTO FROM LOCATOR IS NOT WORKING
```

---

## UI / Menü Änderungen

* UPGRADE vor SETUP im Hauptmenü verschoben
* Bestätigungsdialoge hinzugefügt für:

  * UPGRADE
  * DEFAULTS


## MorseLAB Firmware v2.9 – Release Notes

https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_9.bin

## 🇵🇱 Polski

### Zmiany względem wersji 2.5

1. Dodano **FILE MANAGER** do zarządzania plikami na karcie SD przez Wi-Fi
   (Menu główne: `FILEMNG`).

2. W **TUTOR** dodano oznaczenie `*` przy ćwiczeniach – po załadowaniu własnego kontentu z karty SD widać, które ćwiczenia z niego korzystają.

3. Dodano opcję w **TUTOR → config → No File**, która:

   * przywraca domyślny kontent z urządzenia,
   * porzuca dane wczytane z pliku.

4. W ćwiczeniach **HeadCopy** oraz **CopyCall sign** dodano opcję:
   **"Repeat after copy fail?"**, która określa, czy:

   * urządzenie ma automatycznie powtarzać materiał po błędnej próbie,
   * czy przejść dalej bez powtórzenia.
     (W HeadCopy można użyć znaku `?` jako odpowiedzi pomocniczej.)

5. W ćwiczeniu **SendWord** dodano opcję ukrywania bieżącego słowa,
   co umożliwia nadawanie z pamięci.

6. W **KEYER** dodano obsługę **prosignów w makrach** &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

7. W **BEACON** dodano obsługę **prosignów w makrach** &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

8. Usunięto opcję **TUTOR → config → Timeout** – parametr jest teraz ustawiany bezpośrednio w ćwiczeniach 100HeadCopy, 100SendWord.

9. Naprawiono błąd w trybie **Ultimatic Mode**.

---

## 🇬🇧 English

### Changes compared to version 2.5

1. Added **FILE MANAGER** for managing SD card files over Wi-Fi
   (Main menu: `FILEMNG`).

2. In **TUTOR**, exercises using custom SD card content are now marked with `*`.

3. Added option in **TUTOR → config → No File**, which:

   * restores built-in device content,
   * discards loaded file data.

4. In **HeadCopy** and **CopyCall sign** exercises, added option:
   **"Repeat after copy fail?"** to control whether:

   * the device automatically repeats after a failed attempt,
   * or proceeds without repeating.
     (In HeadCopy, `?` can be used as a helper input.)

5. In **SendWord**, added option to hide the current word,
   enabling transmission from memory.

6. Added **prosign support in macros** in **KEYER** &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

7. Added **prosign support in macros** in **BEACON** &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

8. Removed **TUTOR → config → Timeout** – timeout is now configured per exercises 100HeadCopy, 100SendWord.

9. Fixed bug in **Ultimatic Mode**.

---

## 🇩🇪 Deutsch

### Änderungen gegenüber Version 2.5

1. **FILE MANAGER** hinzugefügt zur Verwaltung von SD-Karten-Dateien über Wi-Fi
   (Hauptmenü: `FILEMNG`).

2. Im **TUTOR** werden Übungen, die benutzerdefinierte SD-Inhalte verwenden, jetzt mit `*` markiert.

3. Neue Option in **TUTOR → config → No File**, die:

   * den internen Gerätekontent wiederherstellt,
   * geladene Dateidaten verwirft.

4. In den Übungen **HeadCopy** und **CopyCall sign** wurde die Option
   **"Repeat after copy fail?"** hinzugefügt, um festzulegen, ob:

   * das Gerät nach einem Fehler automatisch wiederholt,
   * oder ohne Wiederholung fortfährt.
     (Im HeadCopy kann `?` als Hilfseingabe verwendet werden.)

5. In **SendWord** wurde eine Option hinzugefügt, das aktuelle Wort auszublenden,
   um das Senden aus dem Gedächtnis zu ermöglichen.

6. Unterstützung für **Prosigns in Makros** im **KEYER** hinzugefügt &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

7. Unterstützung für **Prosigns in Makros** im **BEACON** hinzugefügt &lt;AR&gt; &lt;SK&gt; &lt;KN&gt; &lt;AS&gt; &lt;BK&gt;.

8. Option **TUTOR → config → Timeout** entfernt – die Zeitsteuerung erfolgt jetzt direkt in den Übungen 100HeadCopy, 100SendWord.

9. Fehler im **Ultimatic Mode** behoben.

---



Wersja 2.5 https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_5.bin

Zmiany: 

Poprawki w ustawianiu VOLUME


*******************************************************


Wersja 2.4 https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_4.bin

Zmiany: 

Dodałano moduł OVLEARN w głównym menu. Żeby z niego skorzystać trzeba wgrać na kartę nowy katalog "overlearn" z plikami treningowymi na kartę SD. 

Pozycje [1]-[32] to ćwiczenia przygotowane przez LICW.

20 pozycji do wykorzystanie na własne pliki:

{"[33] User File 1", "/overlearn/UserFile_1.txt"},

{"[34] User File 2", "/overlearn/UserFile_2.txt"},

{"[35] User File 3", "/overlearn/UserFile_3.txt"},

{"[36] User File 4", "/overlearn/UserFile_4.txt"},

{"[37] User File 5", "/overlearn/UserFile_5.txt"},

{"[38] User File 6", "/overlearn/UserFile_6.txt"},

{"[39] User File 7", "/overlearn/UserFile_7.txt"},

{"[40] User File 8", "/overlearn/UserFile_8.txt"},

{"[41] User File 9", "/overlearn/UserFile_9.txt"},

{"[42] User File 10", "/overlearn/UserFile_10.txt"},

{"[43] User File 11", "/overlearn/UserFile_11.txt"},

{"[44] User File 12", "/overlearn/UserFile_12.txt"},

{"[45] User File 13", "/overlearn/UserFile_13.txt"},

{"[46] User File 14", "/overlearn/UserFile_14.txt"},

{"[47] User File 15", "/overlearn/UserFile_15.txt"},

{"[48] User File 16", "/overlearn/UserFile_16.txt"},

{"[49] User File 17", "/overlearn/UserFile_17.txt"},

{"[50] User File 18", "/overlearn/UserFile_18.txt"},

{"[51] User File 19", "/overlearn/UserFile_19.txt"},

{"[52] User File 20", "/overlearn/UserFile_20.txt"}



*******************************************************

Wersja 2.2
https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_2.bin


Zmiany:
1. Możliwość ustawiania WPM RX(MIN MAX), FWPM/BWPM RX(MIN MAX), TONE RX(MIN MAX) i VOLUME RX (MIN MAX) na wejściu ćwiczeń Head Copy i  Copy Callisign. Wartość jest losowana pomiędzy MIN MAX. Żeby zachować realizm zmienia się dopiero w następnej próbie (AGN lub błędna próba nie zmienia wartości)

2. Śledzenie w ćwiczeniach DAILY.

3. Zapis TOP score jeśli w DrillWord - domyślne słowo to BENSBESTBENTWIRE.



*******************************************************
Wersja 2.0
https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_00.bin 


Zmiany:
1. Dodano ćwiczenia Warmup, Exercise, Drill zgodnie z dokumentem https://cwops.org/wp-content/uploads/2022/03/Everyday-Send-Code-WR7Q-ver.-7.pdf

2. Dodano ćwiczenie Pyramid.

3. Dodano ćwiczenie DrillWord - domyślne słowo BENSBESTBENTWIRE, jeśli załadujemy plik z karty wtedy pierwsze słowo jest z pliku z karty.


*******************************************************

Wersja 1.04
https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_1_04.bin


Zmiany:
1. Dodano opcję szybkiej zmiany WPM, FWPM/BWPM, TX space, VOLUME w ćwiczeniach nadawania, odbioru i Practice.
Wywołanie - długie naciśnięcie enkodera.
 W KEYER zostaje po staremu, bo tak jest szybciej w przypadku pracy.
2. Zaimplementowano dwuznaki AR SK KN AS BK w Practice i KEYER + KEYER LOG
3. W opcji „logger” widać status i nazwę bieżącego pliku jeśli jest włączone logowanie. Można zatrzymać i wznowić logowanie do nowego pliku.
Przejrzyście i zrozumiale...
4. Pliki konfiguracyjne mogą być na ścieżce „/” lub „/configs/”. Można sobie dzięki temu uporządkować kartę.
5. Konfiguracja dla serwera chat może być zamieszczona w pliku chat.txt - 1 linia adres serwera MQTT, 2 linia hasło do serwera MQTT. Użytkownik to ID urządzenia.
Można uruchomić swój serwer chat (broker MQTT). Jeśli jest plik chat.txt  nie będzie się łączył do mojej maszyny tylko do tej wskazanej. Nie zadziałają też sprawdzenia aktualnej ilości użytkowników na kanale, bo to po API jest zrobione.
6. Poprawiono generowanie losowe CALLSING w ćwiczeniach odbioru i kopiowania, wcześniej były takie za bardzo „Amerykańskie”
7. Dodano w ćwiczeniach z literowaniem możliwość wyboru języka. Tzn. katalog letters jest jako default, ale jeśli oprogramowanie znajdzie katalog lettersEN zapytam który język ma być użyty Default czy ENGLISH.
8. Dodano ustawianie zegara ręczne jak nie ma wifi, wtedy też można logować KEYER.
Do tej pory trzeba było się synchronizować z NTP, a teraz pyta nas czy chcemy manualnie podać jak nie ma czasu z NTP. 

*******************************************************
