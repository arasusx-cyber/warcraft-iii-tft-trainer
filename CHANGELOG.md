# Historia zmian

## v5

- Poprawka ścieżek uruchamiania surowców po zgłoszeniu błędu Lua `too many C levels`.
- Wyszukiwanie symboli bez dodatkowych callbacków Lua, blokada ponownej inicjalizacji i ochrony przed ponownym wejściem w timer.
- Pierwsza aktualizacja zasobów odroczona do zakończenia aktywacji wpisu.
- Niezależna obsługa złota, drewna i zużytej żywności.
- Widoczny status, licznik aktualizacji, ID gracza i maska brakujących zasobów.
- 25 przypadków regresji logiki surowców sprawdzonych w symulatorze CE; dokładnej przyczyny błędu w sesji użytkownika nie odtworzono w uruchomionym CE.

## v4

- Okno jednorazowej zamiany własnych wież na jeden z 22 typów różnych ras i kampanii.
- Kolejka przemian wykonywanych w pętli gry, licznik wyniku i możliwość przerwania.
- Cofnięcie ostatniej zamiany z ponowną kontrolą tożsamości i właściciela jednostek.
- Osobna opcja rozszerzenia zakresu na własne budynki z atakiem.
- 70 przypadków kodu natywnego i 8 przypadków obsługi okna/kolejki sprawdzonych w symulacji.

## v3

- Duży zasięg broni i wykrywania celów własnych wież.
- Zdejmowanie flagi niezniszczalności z cudzych jednostek i interaktywnych obiektów mapy.
- Przeniesienie obsługi ręcznego ruchu bohatera do pętli schedulera gry; zachowywany status i dodatkowe liczniki diagnostyczne.

## Wcześniejsze funkcje

Panel własnego i dodatkowego gracza, ochrona HP, wrogowie do 1 HP, szybka budowa i szkolenie, zamrażanie surowców, cooldown, mnożnik ruchu oraz eksperymentalny autopilot armii.

Testy symulowane opisane powyżej nie zastępują sprawdzenia działania w grze.
