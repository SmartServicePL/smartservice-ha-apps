# Lista zmian

## 1.15.7 — 15 listopada 2026

### Poprawki
- Na szerokich monitorach (21:9 i szerszych) krajobraz ASTRY wypełnia cały ekran bez powtórzeń i bez rozciągania, a dół obrazu jest widoczny w całości.
- TRUE Zero Export: przycisk „Przygotuj (podgląd)” działa także przy pierwszym przygotowaniu automatyzacji.
- TRUE Zero Export: pomocnik zabezpieczenia powstaje sam przy włączeniu sterowania.

## 1.15.6 — 15 listopada 2026

### Nowe
- Kocioł z EMS-ESP: przy włączonym sterowaniu MIGIELS co minutę ustawia kotłowi bieżącą temperaturę wody do grzejników, a nastawa z pokrętła kotła jest górnym limitem i wraca do Twojej wartości po wyłączeniu sterowania.
- TRUE Zero Export: przycisk „Sprawdź odliczanie” krótką próbą sprawdza, czy przekaźnik sam wraca na sieć, a przekaźnikiem bez odliczania MIGIELS steruje tylko po Twojej zgodzie w oknie włączania.

### Ulepszenia
- Obniżenia temperatury, także Ciepła noc, pilnują wilgoci: pokój bez czujnika wilgotności nie schodzi w nocy poniżej 17 °C, z czujnikiem pokazującym suche powietrze — poniżej 16 °C, a pokój, w którym wilgotność przez dobę przekracza 60 %, nie jest obniżany, dopóki nie przeschnie.
- Przy kotle kondensacyjnym MIGIELS liczy koszt porannego dogrzania z temperatury wody wracającej do kotła, więc obniża temperaturę tylko tam, gdzie to się naprawdę opłaca, a Autopilot mówi, dlaczego gdzieś nie obniża („zysk za mały”, „nagrzanie droższe niż oszczędność”).
- Ciepła woda: gdy przez 6 dni woda w zasobniku ani razu nie miała 60 °C przez godzinę, grzałka z nadwyżki PV dostaje pierwszeństwo przed ładowaniem magazynu.
- Kafel zasobnika ciepłej wody pokazuje moc grzałek zmierzoną ich licznikiem (bez licznika — szacunek ze znakiem „≈”), a okno Paneli PV pokazuje, ile energii poszło do zasobnika.
- Okno Paneli PV pokazuje najnowszą prognozę produkcji z nazwą dostawcy i godziną („Prognoza z: Forecast.Solar · HH:MM”) — tę samą liczbę, którą podaje dostawca.
- Grzałka zasilana z magazynu energii (DC) jest w dziennym bilansie energii osobnym odbiorcą — widać, ile wzięła z PV, z magazynu i z sieci.

### Poprawki
- Podłogówka zasilana wprost z kotła (bez mieszacza) dostaje wodę najwyżej 45 °C, a gdy sama instalacja podaje cieplejszą, administrator widzi ostrzeżenie w Diagnostyce.

## 1.15.5 — 15 listopada 2026

### Nowe
- W arkuszu „Goście” przy co najmniej dwóch pokojach dla gości pytanie „Gdzie śpią goście?” pozwala wybrać pokoje na czas pobytu, a MIGIELS nagrzewa tylko te pokoje.
- ASTRA: krajobraz pod niebem do wyboru — 7 scen, każda w czterech porach roku; wybierasz go w Smart Service HA → Panel → ASTRA.

### Ulepszenia
- ASTRA pokazuje Księżyc w jego prawdziwej fazie — pełnia, kwadry i sierp — z delikatną poświatą.
- Gdy MIGIELS steruje głowicami, blokuje przyciski na głowicach, które to umożliwiają, a w pokoju widać „Przyciski na głowicach są zablokowane. Nastawę ustaw powyżej.”; po wyłączeniu sterowania przyciski wracają do stanu sprzed sterowania.
- Powiadomienia MIGIELS po kliknięciu otwierają właściwy ekran panelu, awarie i ostrzeżenia zostają na telefonie do „Odczytane”, a ostrzeżenia mają osobny kanał „MIGIELS — ostrzeżenia”.
- Łączenie MIGIELS i Smart Service HA z kontem Panelu klienta jest bezpieczniejsze, bo dane połączenia przechodzą tylko między dodatkami w Twoim Home Assistant.

### Poprawki
- Ciepła noc: gdy w nocy na zewnątrz jest cieplej niż 5 °C, kocioł nie grzeje, ale pokój nigdy nie wychładza się poniżej 16 °C.
- Gdy w trakcie okna próbnego ustawienia TRUE Zero Export zostaną usunięte albo staną się niepełne, okno kończy się od razu, a zanik sieci znów daje powiadomienie.
- Na telewizorze panel zostaje tylko do podglądu także wtedy, gdy Home Assistant zmieni widok albo odświeży kartę.

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
