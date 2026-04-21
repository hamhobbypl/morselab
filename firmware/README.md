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

6. W **KEYER** dodano obsługę **prosignów w makrach**.

7. W **BEACON** dodano obsługę **prosignów w makrach**.

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

6. Added **prosign support in macros** in **KEYER**.

7. Added **prosign support in macros** in **BEACON**.

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

6. Unterstützung für **Prosigns in Makros** im **KEYER** hinzugefügt.

7. Unterstützung für **Prosigns in Makros** im **BEACON** hinzugefügt.

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
