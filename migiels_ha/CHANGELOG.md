# Lista zmian

## 1.15.11 — 17 listopada 2026

### Ulepszenia
- Węzeł cieplny Danfoss ECL: gdy zmienisz nastawę na sterowniku, MIGIELS szanuje ją przez 2 doby, potem wraca do sterowania od tej wartości i nigdy jej nie przekracza. Nastawy są zapisywane w kolejności, którą regulator przyjmuje, a po odrzuconym zapisie MIGIELS próbuje ponownie raz, po dobie.
- Bez połączenia z kontem Smart Service MIGIELS działa teraz do 14 dni (wcześniej 7).
- Okres próbny jest liczony odpornie na cofnięcie zegara i przerwy w połączeniu.

### Poprawki
- Węzeł cieplny Danfoss ECL: dzienna zmiana nastaw idzie codziennie o tej samej porze (wcześniej mogła wypaść co drugi dzień).
- Powiadomienie o braku sieci i pracy z rezerwy magazynu przychodzi teraz od razu także w ciszy nocnej.

### Po aktualizacji
- Nic do zrobienia.

## 1.15.10 — 16 listopada 2026

### Ulepszenia
- Autopilot ciepła: w domach z grzejnikami, gdzie pełne obniżenie nocne się nie opłaca, obniża w nocy o 0,5 °C — tylko gdy rano dogrzewa na czas i wychodzi na plus. W Diagnostyce widać plan nocy albo powód, dlaczego nie.
- Szybkie akcje na telefonie bez przeskakującej karuzeli: trzy najważniejsze kafle i „Więcej”, które rozwija resztę pod spodem.
- Rolety można ułożyć po swojemu: „Ułóż” w widoku Rolety zmienia kolejność pokoi i rolet oraz ukrywa te, których nie potrzebujesz; układ jest zapamiętany na wszystkich Twoich urządzeniach.
- Szybkie akcje na telefonie pokazują się każdej osobie w wyborze i kolejności ustawionych przez administratora w Smart Service HA.

### Poprawki
- Po animacji logo ASTRA od razu pokazuje gotowy, właściwy widok, bez chwilowego widoku Standard.
- Grzałki zasilane nadwyżką z paneli nie wyłączają się już w dzień, gdy magazyn zgłasza stan naładowania tylko przy zmianie o cały procent.
- TRUE Zero Export szybciej uznaje dane magazynu za aktualne, gdy magazyn stoi, a przy dużym poborze nadal czeka na świeży odczyt.

### Po aktualizacji
- Nic do zrobienia.

## 1.15.9 — 16 listopada 2026

### Ulepszenia
- W Smart Service HA ustawienia MIGIELS są w menu bocznym pod pozycją MIGIELS, a nie w osobnym rzędzie zakładek.

### Po aktualizacji
- Nic do zrobienia.

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
