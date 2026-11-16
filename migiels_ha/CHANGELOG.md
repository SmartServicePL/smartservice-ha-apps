# Lista zmian

## 1.15.8 — 16 listopada 2026

### Nowe
- Diagnostyka informuje administratora, gdy prognoza produkcji PV stale myli się w dni słoneczne i pochmurne, co zwykle znaczy złe ustawienia instalacji w integracji prognozy (MIGIELS niczego w niej nie zmienia).

### Ulepszenia
- Prognoza PV: plan prowadzi prognoza, która w Twoim domu myli się najmniej, a poprawka MIGIELS jest liczona osobno dla dni słonecznych i pochmurnych i działa tylko wtedy, gdy zmniejsza błąd dobowy co najmniej o 10 %.
- Korekta temperatury nie zaczyna nauki od nowa po dodaniu innej prognozy w kreatorze ani po wymianie urządzenia, a najwyższą i najniższą temperaturę na kolejne dni poprawia osobno dla każdej prognozy.
- Szansa opadu w prognozie godzinowej dopasowuje się do deszczomierza domu, gdy po co najmniej 200 godzinach pomiarów widać, że jest wtedy trafniejsza.
- Ikona pogody pokazuje deszcz od 0,2 mm w godzinie i od 1 mm w dniu, dzień z krótkimi opadami ma ikonę „przelotny deszcz”, a dzień i noc zmieniają się według wysokości słońca nad Twoim domem.
- Prognoza na 12 godzin mieści się w kaflu na każdej szerokości ekranu i pokazuje opad pod każdą godziną z opadem.
- Ekran ładowania ASTRY znika płynnie dopiero wtedy, gdy cały widok jest gotowy, bez mignięcia innego widoku.
- Niebo ASTRY porusza się także przy włączonym w urządzeniu ograniczeniu ruchu — wtedy stoi tylko krajobraz.

### Po aktualizacji
- Nic do zrobienia.

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
