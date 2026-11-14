# Smart Service HA — historia zmian

## 1.9.23 — 14 listopada 2026

### Ulepszenia
- Kosiarka Worx Vision Cloud dostaje swój harmonogram koszenia.
- Powiadomienia robota i kosiarki: każde urządzenie osobno, błędy z dźwiękiem, a „wymaga uwagi” znika dopiero, gdy urządzenie znów pracuje; gdy zawór nawadniania się nie zamknie, dostajesz od razu powiadomienie z dźwiękiem.

### Poprawki
- Alarm: pierwszy PIN domownika ustawia teraz tylko administrator.
- Usunięty albo chwilowo niedostępny telefon nie zatrzymuje już powiadomień do pozostałych domowników ani pracy robota.
- Aktualizacja MIGIELS nie rusza przy uzbrojonym alarmie.
- Bez MIGIELS menu MIGIELS pokazuje ofertę zamiast „Zaktualizuj”, komunikat o ponownym uruchomieniu Home Assistant znika po restarcie, a stan połączenia z kontem zmienia się od razu po „Połącz” i „Rozłącz”.
- Na telefonie i tablecie napisy w menu, w ustawieniach modułów i na kaflach nie są już ucinane ani nie nachodzą na siebie; Pokoje z wieloma piętrami nie przesuwają się w bok.

### Po aktualizacji
- Sprawdź w Bezpieczeństwie, kto ma PIN, i usuń te, których nie nadawałeś.

## 1.9.22 — 14 listopada 2026

### Poprawki
- Wyjazd ze zwierzętami: harmonogram karmnika PetKit wraca po wyjeździe także po restarcie Home Assistant lub chwilowym braku połączenia z PetKit (nie wraca, jeśli zmieniłeś go sam).
- Robot: długi opis stanu (problem razem z przeszkodą) nie przerywa już automatyzacji — powiadomienie „wymaga uwagi” i samodzielne wznawianie działają.
- Robot: „Usuń moduł” i „Przywróć” nie usuwają połączeń pokoi zrobionych przez Ciebie i działają także po usunięciu robota z Home Assistant; gdy Home Assistant chwilowo nie odpowiada, zatrzymują się z komunikatem.
- Kosiarka Worx: po przycięciu krawędzi koszenie całego trawnika rusza tylko za dnia i poza ciszą nocną; krótki wyjazd z bazy (odświeżenie stanu robota) nie odbywa się w nocy ani zimą.
- Nawadnianie: strefa otwarta z panelu zamyka się po najdłuższym czasie sekcji + 5 min także w trakcie trwającego cyklu.
- „Wycisz telefon w szkole”: godzina „wyciszony od” i przypomnienie o 22:00 według czasu domu; telefon nie jest wyciszany, gdy Smart Service HA nie może zapamiętać jego poprzedniego trybu (inaczej nie dałoby się go przywrócić).
- Panel: komunikat błędu podaje właściwy dodatek, dymek „Zgłoś problem” pokazuje opis zamiast „[object Object]”, a na karcie długa nazwa kamery nie wchodzi pod godzinę i okno urządzenia bez wykresu nie ma pustej belki.

## 1.9.21 — 13 listopada 2026

### Ulepszenia
- Szybkie akcje „Sprzątanie”, „Kosiarka” i „Nawadnianie” (przy dodanym module): stan urządzeń i przyciski Start / Do stacji (robot), Koś / Do stacji (kosiarka), a dla stref nawadniania Nawadniaj / Zatrzymaj. Start robota i kosiarki jest wyłączony z powodem: w ciszy nocnej, a kosiarki także poza sezonem.
- Szybkie akcje jako karuzela (od pięciu kafli): przewijasz palcem lub myszą w kółko, kafel na środku jest wyróżniony.
- Widok urządzenia: praca (od kiedy, powierzchnia, czas, pokój, ostatnia praca) i materiały eksploatacyjne z czujników samego urządzenia — „WYMIEŃ” przy 15 % i mniej albo gdy urządzenie zgłasza wymianę.
- Oś tygodnia w widoku urządzenia: prace z ostatnich 7 dni z przerwanymi, pominiętymi, deszczem i ciszą nocną, suma tygodnia i porównanie z poprzednim; „Po sezonie” dla kosiarki i nawadniania.
- Na Starcie baner nawadniania „nawadnia · strefa”, gdy trwa nawadnianie.
### Poprawki
- Pytanie „Zwierzęta jadą z Wami?” przy wyjeździe działa — Smart Service HA zakłada teraz jego pomocnik.

## 1.9.20 — 13 listopada 2026

### Zmiany
- Wersja zgodna z MIGIELS 1.15.0 (wspólna karta: jeden cel na ekranie ogrzewania, wykres gazu w miesiącach) — bez zmian w działaniu Smart Service HA.

## 1.9.19 — 13 listopada 2026

### Ulepszenia
- Pomoc i konto: stan licencji MIGIELS z przyciskiem zakupu albo przedłużenia.
- Karmnik PetKit: „Nakarm” w szybkich akcjach — liczba porcji na przewijanym pasku (przy modelach na gramy z wagą), wybór pojemnika z poziomem karmy, podgląd z kamery karmnika, przycisk „Wydaj N porcji”. Na Starcie karmnik pojawia się tylko, gdy kończy się karma.
- Wyjazd: pytanie „Zwierzęta jadą z Wami?” — gdy jadą, bez powiadomień o karmie i żwirku, a harmonogram karmnika jest wstrzymany (gdy integracja na to pozwala).
- Cisza nocna ma własną, wyróżnioną kartę na górze Powiadomień: stan na teraz, co wstrzymuje, a godziny wybierasz przewijanymi bębnami z „OK”.
- Oświetlenie zewnętrzne: „Załóż automatyzację” działa.
- Oświetlenie: tryb „Automatycznie” — bez okien światło przy każdym ruchu, z oknami próg z historii czujnika.
### Poprawki
- Karta oferty MIGIELS bez ceny — cena i zakup tylko w panelu Smart Service.
