# MIGIELS — Menedżer Instalacji Grzewczej i Energii

Lokalny menedżer ogrzewania i energii dla Home Assistant. Czyta odczyty Twojej
instalacji, sprawdza ich jakość, uczy się zachowania domu i podpowiada, kiedy
i jak grzać oraz jak wykorzystać energię z paneli PV.

**MIGIELS liczy i doradza — sterowanie jest Twoją decyzją.** Urządzeniami
(grzałki z nadwyżki OZE, ogrzewanie CO, głowice TRV, ładowanie magazynu
z sieci) sterują automatyzacje Home Assistant, które MIGIELS przygotowuje
z danych kreatora. Każda zaczyna w podglądzie — tylko zapisuje w dzienniku,
co by zrobiła. Sterowanie włącza administrator, świadomie i osobno dla każdej
automatyzacji; wyjście ze sterowania przywraca bezpieczny stan albo stan
sprzed włączenia. MIGIELS działa w całości lokalnie; Twoje dane nie są nigdzie
wysyłane.

## Co pokazuje

- **Energia** — produkcja PV, zużycie domu, sieć i magazyn na żywo, bilans
  dnia, taryfa i cena energii oraz **nadwyżka OZE dla grzałek** 230 V i DC
  (np. 48 V z banku energii) — także przy Zero Export i pracy wyspowej.
- **Ogrzewanie** — temperatury i potrzeby pomieszczeń, obiegi i pompy, krzywa
  grzewcza, praca źródła ciepła i zapotrzebowanie na ciepło.
- **CWU** — temperatura zasobnika, praca grzałek, czas do osiągnięcia limitu
  i energia z OZE.
- **MeteoFusion** — prognoza pogody łącząca pomiar z Twojego domu z prognozami
  z Home Assistant.
- **Ustawienia** — kreator konfiguracji krok po kroku, jakość odczytów i stan
  wszystkich silników.

Każda liczba pochodzi z odczytu o znanej jakości — brak danych to jawny stan,
nigdy wymyślona wartość.

## Po co

- zużywać nadwyżkę PV na grzanie wody i domu zamiast ją tracić, bez poboru
  z sieci i bez rozładowywania magazynu;
- widzieć w jednym miejscu, co dzieje się z ogrzewaniem, ciepłą wodą
  i energią;
- dostawać porady oparte na danych z Twojego domu, a nie na ogólnych
  założeniach.

## Wymagania

- Home Assistant OS albo Supervised (obsługa aplikacji), procesor 64-bitowy
  amd64 lub aarch64.
- Home Assistant 2025.10 lub nowszy.
- Konto administratora Home Assistant do konfiguracji.
- Do automatyzacji, powiadomień i panelu na telefon: broker **Mosquitto**
  i opcja dodatku **Encje w Home Assistant**.

## Integracje

MIGIELS korzysta z encji, które już masz w Home Assistant. Potrzebne są tylko
te części, które opiszesz w kreatorze:

| Część | Potrzebne odczyty | Przykładowe integracje |
| --- | --- | --- |
| Ogrzewanie | temperatury pomieszczeń, temperatura zewnętrzna, praca źródła ciepła, zasilanie, pompy, grzałki | termostaty i czujniki (Zigbee2MQTT, ZHA), kocioł (np. EMS-ESP), przekaźniki (np. Shelly) |
| Pogoda (przy ogrzewaniu) | prognoza pogody i czujnik temperatury na zewnątrz | dowolna integracja pogodowa z prognozą (1–3), stacja pogodowa opcjonalnie |
| Energia | moc PV, sieci, domu, magazynu i jego naładowanie; liczniki energii | integracja falownika (np. Solarman/Deye, Victron) |
| CWU | temperatura zasobnika, stan grzałek | czujniki i przekaźniki |

Opcjonalnie:

- ceny dynamiczne RCE MIGIELS pobiera sam z PSE (od 0.46.0) — integracja
  RCE PSE w Home Assistant nie jest potrzebna; stałe taryfy polskich
  sprzedawców są w katalogu wbudowanym w MIGIELS;
- **Forecast.Solar** lub **Solcast** — prognoza produkcji PV z ustawień
  Energii Home Assistant;
- stacja pogodowa z czujnikiem nasłonecznienia (W/m²).

## Pierwsze kroki

1. Zainstaluj i uruchom dodatek, a potem otwórz MIGIELS z paska bocznego.
2. W konfiguracji dodatku wklej **Kod instalacji** z panelu klienta
   (https://panel.smartservice.net.pl → Kod dla MIGIELS).
3. Odpowiadaj na pytania **kreatora konfiguracji** — przy każdym elemencie
   instalacji wskażesz jego encję.
4. Po potwierdzeniu konfiguracji karty pokazują wyniki; modele uczą się
   w kolejnych dniach.
5. Sterowanie (gdy chcesz): **Ustawienia → Automatyzacje → Przygotuj
   (podgląd)**, kilka dni obserwacji, potem **Włącz sterowanie**.

Instrukcja krok po kroku — zakładka **Dokumentacja**. Zmiany wersji — **Lista
zmian**. MIGIELS jest w fazie rozwoju.

## Licencja

Korzystanie z oprogramowania na warunkach regulaminu Smart Service:
https://panel.smartservice.net.pl
Use of this software is subject to the Smart Service terms:
https://panel.smartservice.net.pl
