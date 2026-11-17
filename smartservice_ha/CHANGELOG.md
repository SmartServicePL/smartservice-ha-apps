# Smart Service HA — historia zmian

## 1.9.30 — 16 listopada 2026

### Ulepszenia
- Domownicy: administrator ustawia każdej osobie, które szybkie akcje widzi na telefonie i w jakiej kolejności.
- Szybkie akcje na telefonie bez przeskakującej karuzeli: trzy najważniejsze kafle i „Więcej”, które rozwija resztę pod spodem.
- W opisie modułu robota nowy wiersz „Ustawienia robota”: na czas sprzątania Smart Service HA dobiera tryb, ssanie, wodę mopa, przejazdy i trasę, a po powrocie do stacji wracają Twoje ustawienia.

### Poprawki
- Po animacji logo ASTRA od razu pokazuje gotowy, właściwy widok, bez chwilowego widoku Standard.
- Gdy automatyzacji modułu nie da się odświeżyć po aktualizacji, Smart Service HA nie ponawia już tego w nieskończoność i zostawia jedno jasne ostrzeżenie.

### Po aktualizacji
- Nic do zrobienia.

## 1.9.29 — 16 listopada 2026

### Ulepszenia
- Panel nie ma już górnej belki: logo jest nad menu, a ustawienia MIGIELS są w menu bocznym pod pozycją MIGIELS.

### Poprawki
- Inteligentne sprzątanie znów samo uruchamia robota. W wersjach 1.9.26–1.9.28 automatyzacja robota przestawała działać po ponownym uruchomieniu Home Assistanta.

### Po aktualizacji
- Nic do zrobienia — automatyzacje robotów odświeżą się same.

## 1.9.28 — 16 listopada 2026

### Nowe
- Kreator „Ustaw alarm”: po instalacji administrator przechodzi Bezpieczeństwo krok po kroku (centrala, czujniki, zagrożenia, syrena, domownicy, czasy, powiadomienia), z propozycjami z danych domu, a każdy krok zapisuje się dopiero po „Dalej”.
- Robot sprzątający sam dobiera wodę mopa, liczbę przejść, trasę i siłę ssania — ciszej, gdy ktoś jest na piętrze, bez dodatkowej mocy przy słabej baterii — a po sprzątaniu przywraca Twoje ustawienia.
- Ogrzewanie podpowiada pokoje rzadko używane: gdy czujnik przez co najmniej 10 z ostatnich 14 dni nikogo w ciągu dnia nie wykrył, możesz obniżyć w tym pokoju temperaturę w harmonogramie.
- Nowe światła, rolety i inne urządzenia dodane w Home Assistant do obszaru pokoju same pojawiają się w tym pokoju na panelu.

### Ulepszenia
- Bezpieczeństwo bez centrali alarmowej mówi to jednym zdaniem z przyciskiem instalacji centrali, a dodawanie czujników i syren czeka, aż centrala będzie gotowa (zapisane czujniki zostają).
- Alarm można włączyć już z jednym czujnikiem dowolnego rodzaju — z syreną wyje, bez syreny wysyła powiadomienia.
- Przy czujnikach i syrenach w Bezpieczeństwie widać nazwę pokoju z Home Assistant.
- Pogoda w panelu i w ASTRZE pokazuje nowy stan „przelotny deszcz”.
- Ekran ładowania ASTRY znika płynnie dopiero wtedy, gdy cały widok jest gotowy, bez mignięcia innego widoku.
- Niebo ASTRY porusza się także przy włączonym w urządzeniu ograniczeniu ruchu — wtedy stoi tylko krajobraz.

### Poprawki
- Urządzenia: gdy odczyt się nie uda, panel próbuje ponownie po 30 sekundach, zamiast bez przerwy odświeżać ekran.

### Po aktualizacji
- Nic do zrobienia.

## 1.9.27 — 15 listopada 2026

### Poprawki
- Krajobraz ASTRY: sceny „Gdańsk” i „Tczew” zostały usunięte — kto miał którąś wybraną, ma teraz „Las i łąka”.
- Na szerokich monitorach krajobraz ASTRY wypełnia cały ekran bez powtórzeń i bez rozciągania.

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
