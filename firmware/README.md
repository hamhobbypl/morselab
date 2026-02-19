Wersja 2.4 https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_4.bin

Zmiany: 

1. Dodano szybkie obroty enkodera w SETUP/VOLUME i na wejściu HeadCopy i CopyCall w ustawianiu VOLUME.
   
2. Dodałano moduł OVLEARN w głównym menu. Żeby z niego skorzystać trzeba wgrać na kartę nowy katalog "overlearn" z plikami treningowymi na kartę SD. 

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
