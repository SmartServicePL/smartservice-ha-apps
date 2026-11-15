# Lista zmian

## 1.15.4 — 15 listopada 2026

### Ulepszenia
- Pola w kreatorze i w oknach konfiguracji mają kolor karty zamiast czarnego tła, a wybrane pole ma cienką obwódkę w kolorze akcentu.
- „Co dokupić” w kreatorze prowadzi na wspólną stronę polecanych urządzeń Smart Service.

### Poprawki
- Na telewizorze przez Google Cast panel MIGIELS działa zawsze tylko do podglądu — niczego nie da się tam przypadkiem przełączyć.

## 1.15.3 — 14 listopada 2026

### Ulepszenia
- Gdy magazyn energii jest pełny, a falownik zaczyna ograniczać produkcję PV, MIGIELS próbuje włączyć kolejny stopień grzałki, żeby ta energia nie przepadała — przy poborze z sieci lub z magazynu grzałka od razu wraca.

### Poprawki
- Oszczędność przy buforze z wężownicą liczona jedną regułą na każdym ekranie, także za poprzednie miesiące — kwoty ogrzewania i ciepłej wody mogą się zmienić, a drobne ujemne kwoty pokazujemy jako 0 zł.
- Grzałki: postój, w którym termostat grzałki odciął grzanie, nie jest już liczony jako oszczędność z nadwyżki, a karta ciepłej wody nie pokazuje nocnego „z magazynu” z samego postoju; kwoty sprzed aktualizacji zostają bez przeliczenia.
- Chwilowy błąd odczytu ustawień falownika (np. nagłe 0 albo „niedostępne”) nie zmienia już rezerwy ani planu — przez 15 minut MIGIELS bierze ostatnią dobrą wartość, a Diagnostyka pokazuje „Odczyt ustawień falownika niepewny”.
- Wyjście ze sterowania ogrzewaniem: przełącznik wyłączony przez Ciebie w trakcie wyjścia nie trafia już do „Nie wróciło” i zostaje wyłączony.
- Na telefonie harmonogram pokazuje nazwę dni nad godzinami, a kreator i Konfiguracja podpowiadają, że wygodniej skonfigurować MIGIELS na komputerze albo tablecie; opis głowic elektronicznych w kreatorze mówi, że MIGIELS ustawia zawór tylko w głowicach, które pozwalają ustawić jego otwarcie.

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
