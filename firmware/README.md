Wersja 2.2
https://github.com/hamhobbypl/morselab/blob/main/firmware/firmware_2_2.bin


Zmiany:
1. Możliwośc ustawiania WPM RX(MIN MAX), FWPM/BWPM RX(MIN MAX), TONE(MIN MAX) i VOLUME(MIN MAX) na wejściu ćwiczeń Head Copy i  Copy Callisign

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
