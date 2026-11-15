# Smart Service HA — historia zmian

## 1.9.26 — 15 listopada 2026

### Nowe
- Panel w menu bocznym Home Assistant nazywa się teraz „ASTRA” (widoki ASTRA Mobile na telefonie, ASTRA Desktop i ASTRA Standard na komputerze i tablecie); nazwa nadana przez Ciebie zostaje bez zmian.
- W zakładce MIGIELS przycisk „Zainstaluj” / „Wypróbuj 90 dni” instaluje MIGIELS od razu, z postępem w tym samym miejscu.
- Bezpieczeństwo: PIN pod przymusem działa dokładnie jak zwykły PIN domownika, a domownikom i zaufanym telefonom, które są poza domem, wysyła cichy alarm.
- Syrenę można podłączyć przez przekaźnik — wybierasz go w Bezpieczeństwo → Alarm → Syrena.

### Ulepszenia
- Po pierwszej instalacji Smart Service HA sam pojawia się w menu bocznym Home Assistant.
- Powiadomienia o koszeniu mają czytelniejsze tytuły i mówią, co zrobić.

### Poprawki
- „Zainstaluj MIGIELS” i „Zainstaluj Bank czasu” działają od razu po instalacji Smart Service HA, bez restartu Home Assistant.
- SOS dziecka: gdy dom odrzuci SOS, telefon dziecka od razu pokazuje „SOS nie dotarło” z „Zadzwoń do rodziców”, zamiast czekać półtorej minuty.

## 1.9.25 — 15 listopada 2026

### Nowe
- W arkuszu „Goście” przy co najmniej dwóch pokojach dla gości pytanie „Gdzie śpią goście?” pozwala wybrać pokoje na czas pobytu, a MIGIELS nagrzewa tylko te pokoje.
- Panel → ASTRA: jedna strona ustawień ASTRY z wyborem krajobrazu w dużych miniaturach (7 scen, cztery pory roku).

### Ulepszenia
- Powiadomienia po kliknięciu otwierają właściwy ekran panelu, awarie i ostrzeżenia zostają na telefonie do „Odczytane”, które usuwa je z telefonów wszystkich dorosłych, a ikona pokazuje, z której aplikacji przyszły.
- Inteligentny robot sprzątający sprząta tylko te pokoje, w których przybyło brudu, jeśli zna je ze swojej mapy.
- Na czas sprzątania robot sam ustawia odpowiedni tryb i siłę ssania, a po powrocie do stacji przywraca Twoje ustawienia.
- Łączenie Smart Service HA i MIGIELS z kontem Panelu klienta jest bezpieczniejsze, bo dane połączenia przechodzą tylko między dodatkami w Twoim Home Assistant.
- Katalog „Sprawdzone przez Smart Service”: opis integracji Solarman mówi wprost, że po dodaniu integracja sama przełącza logger falownika w tryb serwera, używając fabrycznego hasła loggera.

### Poprawki
- Robot sprzątający nie rusza w godzinach ciszy nocnej także wtedy, gdy nie wciśnięto „Dobranoc”; kosiarka i nawadnianie nie zależą od ciszy nocnej.
- Na telewizorze panel zostaje tylko do podglądu także wtedy, gdy Home Assistant zmieni widok albo odświeży kartę.

## 1.9.24 — 15 listopada 2026

### Ulepszenia
- Pralka i suszarka: karta pokazuje, o której mniej więcej skończy się pranie lub suszenie („koniec ok. HH:MM”), gdy znane są już co najmniej 3 cykle.
- „Mój bank” na telefonie dziecka (widok KIDS Mobile): ile czasu można teraz wykorzystać, ile jest w banku i ostatnie zmiany.
- Wybrane pole w ustawieniach i oknach Smart Service HA ma cienką obwódkę w kolorze akcentu zamiast białej ramki.

### Poprawki
- Alarm: gdy domownik próbuje sam ustawić pierwszy PIN, widzi jasny komunikat „Pierwszy PIN ustawia administrator.”.

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
