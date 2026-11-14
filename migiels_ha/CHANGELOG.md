# Lista zmian

## 1.15.2 — 14 listopada 2026

### Poprawki
- Koszt ogrzewania gazem liczony jest z tych samych kWh co na fakturze (z ciepła spalania gazu) — wcześniej wychodził o około 10 % za niski; porównanie z gazomierzem i „Zużycie gazu w miesiącach” też. Porównanie z gazomierzem zbiera dane od nowa.
- „Zaoszczędziłeś z MIGIELS”: oszczędność z grzałek nie jest już zawyżona, kwoty miesięcy sumują się do kwoty od początku, a wartość szacowana ma znak „≈”.
- Wyjście ze sterowania ogrzewaniem i oddanie ogrzewania kotłowi nigdy nie wyłączają grzania: przełącznik ogrzewania wyłączony przez MIGIELS wraca na „włączony” (także po ponownym uruchomieniu), a wyłączony przez Ciebie zostaje wyłączony.
- Autopilot ocenia próbę tylko z tego, co sam dodaje do zwykłego harmonogramu; w domu bez potwierdzonej obecności planuje same noce i co 30 dni sprawdza obecność ponownie.
- Powiadomienie „Brak sieci — dom zasilany z rezerwy magazynu” nie przychodzi już fałszywie przy falownikach Deye: MIGIELS nie bierze ustawienia progu baterii za alarm niskiej baterii.
- Konfiguracja: każde pytanie otwiera się w oknie krokami, tak jak w kreatorze, z podpowiedzią liczby faz z danych falownika; na telefonie kafle i okna pytań mieszczą się na ekranie.

## 1.15.1 — 13 listopada 2026

### Ulepszenia
- Jeden termostat dla całego domu: zakładka „Ogrzewanie” pokazuje jego tarczę — temperaturę teraz i nastawę; nastawę zmienia administrator.
- Wykres „Zużycie gazu w miesiącach”: miesiąc po ostatnim odczycie dostawcy ma w dymku dopisek „do najbliższego odczytu”.
### Poprawki
- Ostrzeżenia „Głowica nie potwierdza polecenia” i „nie grzeje mimo otwarcia” pojawiają się tylko, gdy pokój jest niedogrzany (co najmniej 0,3 °C poniżej nastawy przez 30 minut).
- Krzywa kotła: tekst odróżnia nową krzywą, która jest jeszcze sprawdzana, od oszczędności z niższej temperatury wody grzewczej, liczonej już teraz.
- Diagnostyka nie zgłasza już fałszywego „Kocioł nie przyjął temperatury wody grzewczej” — MIGIELS ocenia nastawę dopiero po jej wysłaniu do kotła.
- Kreator, okno „Falownik i magazyn energii”: bez ogromnej ikony pod polami magazynu.

## 1.15.0 — 13 listopada 2026

### Ulepszenia
- Ogrzewanie: jasny cel na ekranie. Gdy obniżenie trwa tylko w części pokoi, widać, w których i do ilu stopni. Kafel kotła pokazuje temperaturę wody i od kiedy grzeje, a jedno zdanie wyjaśnia, dlaczego kocioł pracuje na małej mocy.
- Gdy dom pracuje bez sieci z Twojego wyboru (falownik nie korzysta z sieci albo rozłącznik otwarty), MIGIELS nie przeszkadza powiadomieniami przy przełączeniach, ale ostrzega — także nocą — gdy magazyn stoi na rezerwie, zanim dom zostanie bez prądu.
- Napięcie sieci przypisane w kreatorze służy jako zapasowy znak, czy sieć jest (gdy falownik nie podaje stanu sieci).
- Wykres „Zużycie gazu w miesiącach” przypisuje zużycie do właściwych miesięcy według odczytów dostawcy; szacunek oznaczony „≈”.
- Jeden termostat dla całego domu: pokoje z grzejnikami i zwykłymi głowicami dostają zalecaną nastawę głowicy, liczoną od bieżącej nastawy termostatu domu i zmieniającą się razem z nią.
- Niebo ASTRA: wyraźniejsze chmury, bez smug i linii przy horyzoncie i o zachodzie; jakość obrazu dopasowuje się do urządzenia (na komputerze najwyższa, na tablecie płynnie).
### Poprawki
- Magazyn ładowany powoli nie jest już błędnie uznawany za nieaktualny odczyt.

## 1.14.19 — 13 listopada 2026

### Ulepszenia
- W Home Assistant pojawia się „Licencja MIGIELS” — stan licencji i koniec okresu próbnego.
- Pasek licencji w MIGIELS: przypomnienie przed końcem okresu próbnego i przycisk „Kup MIGIELS” / „Przedłuż”.
- TRUE Zero Export w instalacjach z trójfazowym falownikiem: moc i napięcie na każdej fazie, jeden stycznik odłącza 3 fazy.
- Konfigurator pyta, ile faz ma falownik (osobno od licznika) — a gdy się da, sam to podpowiada.

### Poprawki
- Stały odczyt magazynu przy niskim naładowaniu i przy rezerwie nie jest już błędnie uznawany za nieaktualny — MIGIELS uczy się, jak szybko zmienia się poziom w Twoim magazynie.
- Koniec okresu próbnego jest ten sam w MIGIELS i w panelu Smart Service.
- „Sieć odłączona” nie zgłasza już chwilowego błędu przekaźnika przy działającej sieci — to tylko wpis w Diagnostyce; „Sieć wróciła” przychodzi raz. Prawdziwy brak sieci (także blackout przy załączonym przekaźniku) zgłaszany jak dotąd.
- Rezerwa magazynu Deye bez sieci to najniższy poziom z programów czasowych falownika — ta sama o każdej porze, bez nadmiaru ostrzeżeń.
- TRUE Zero Export: po zadziałaniu zabezpieczenia przekaźnika automatyzacja nigdy sama nie podłącza sieci — także gdy MIGIELS chwilowo nie odpowiada.
- Wyłączenie sterowania TRUE Zero Export kończy się podglądem po potwierdzeniu, że dom jest na sieci.

## 1.14.18 — 13 listopada 2026

### Zmiany
- Wersja zgodna ze Smart Service HA 1.9.18 (wspólne części: powiadomienia o karmniku i pokoje robota) — bez zmian w działaniu MIGIELS.
