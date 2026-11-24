# Warcraft III TFT Trainer

Tabela Cheat Engine do klasycznego **Warcraft III: The Frozen Throne 1.26a**. Surowce, zdrowie, budowa, ruch oraz narzędzia do eksperymentowania z wieżami w rozgrywce lokalnej.

**[Pobierz trainer v5 — war3_towers_v5.CT](https://github.com/arasusx-cyber/warcraft-iii-tft-trainer/raw/refs/heads/main/war3_towers_v5.CT)**

## Wymagania

- Windows i Cheat Engine z obsługą Lua.
- Klasyczny Warcraft III TFT **1.26a**, proces `war3.exe`.
- `Game.dll` w wersji **1.26.0.6401**. Adresy w tabeli dotyczą tej wersji; tabela nie jest przeznaczona do Reforged ani innych aktualizacji gry.

Repozytorium zawiera tabelę trainera. Pliki gry, `Game.dll` i Cheat Engine nie są dołączone.

## Funkcje

| Obszar | Dostępne opcje |
| --- | --- |
| Surowce | Osobne zamrażanie dla lokalnego i wybranego gracza; ustawiane złoto, drewno i zużyta żywność. |
| Zdrowie | God mode dla własnych jednostek oraz wybranego gracza; ograniczenie zdrowia wrogów do 1 HP. |
| Budowa i szkolenie | Osobne przełączniki dla własnego i wybranego gracza; tryb szybki i INSTANT. |
| Wieże | Zwiększenie zasięgu broni i wykrywania celów własnych budynków z atakiem. |
| Zamiana wież | Jednorazowa przemiana własnych wież na typ z listy **22 wież**: cztery rasy, wysokie elfy oraz wieże misji „Przeprawa”. Przycisk cofnięcia ostatniej zamiany. |
| Niezniszczalność | Zdejmowanie flagi niezniszczalności z cudzych jednostek i interaktywnych obiektów mapy. |
| Dodatkowe opcje do testów | Brak cooldownu, mnożnik prędkości własnych jednostek, ręczne przesuwanie bohatera przez przeszkody, ochrona własnych bohaterów przed skryptowym `KillUnit` i autopilot armii. |

Przy zamianie wież właściciel jest sprawdzany przed każdą przemianą. Domyślny zakres obejmuje typy wież z listy. Dodatkowe zaznaczenie rozszerza zakres na własne budynki z atakiem, w tym niestandardowe wieże i uzbrojone ratusze.

## Uruchomienie

1. Zrób osobny zapis gry, uruchom misję i otwórz tabelę `.CT` w Cheat Engine.
2. Wybierz proces **`war3.exe`**.
3. Włącz **PANEL GRACZY**, a następnie potrzebne opcje pod nim. God mode, budowa i surowce dla siebie oraz dodatkowego gracza mają osobne przełączniki.
4. Dla opcji **WYBRANY gracz** ustaw jego ID w panelu. Opcje **MOJE** wykrywają lokalne ID automatycznie.
5. Pozostałe samodzielne opcje znajdują się niżej w tabeli.

Przy aktualizacji wyłącz wpisy starej tabeli przed otwarciem nowej. Wyłącz opcje przed zmianą procesu w CE.

### Zamiana wież jednym kliknięciem

Włącz **ZAMIANA MOICH WIEŻ**, wybierz typ w otwartym oknie i kliknij **Zamień moje wieże**. Operacja obejmuje istniejące wieże; dla później zbudowanych kliknij ponownie.

Przycisk **Cofnij ostatnią zamianę** przywraca typy nadal żywych i własnych jednostek objętych ostatnią operacją. Zamknięcie okna lub wyłączenie wpisu nie cofa przemian. Historia cofania jest przechowywana tylko podczas działania tego wpisu w CE.

### Surowce w v5

Pod przełącznikami surowców znajdują się status, licznik aktualizacji i wykryte ID gracza. Złoto, drewno oraz zużyta żywność są obsługiwane niezależnie — niedostępny stan żywności nie blokuje pozostałych zasobów. Opcja nie zmienia limitu pojemności żywności.

## Stan projektu

To rozwijana tabela dla konkretnej wersji gry. Część wcześniejszych funkcji była testowana przez autora w rozgrywce; nowe opcje oraz poprawka Lua v5 mają również testy symulowane. Nie wszystkie kombinacje opcji, mapy i misje zostały sprawdzone w uruchomionej grze. Opcje oznaczone w tabeli jako testowe lub eksperymentalne zachowują ten status.

Tabela służy do gry lokalnej i eksperymentów. Niezsynchronizowane zmiany pamięci w multiplayerze mogą rozłączyć rozgrywkę. Skrypty fabuły, teleportowanie i warunki porażki działają niezależnie od części tych opcji.

## Zgłaszanie problemów

W [Issues](https://github.com/arasusx-cyber/warcraft-iii-tft-trainer/issues) podaj wersję gry i CE, nazwę misji, nazwę opcji oraz dokładny komunikat błędu. Przy problemach z surowcami dołącz status i licznik aktualizacji widoczne pod wpisem.

## Źródła pomocnicze

- [UnryzeC/MemHackAPI](https://github.com/UnryzeC/MemHackAPI) — opisy struktur i wywołań silnika, w tym przemiany jednostek w wersji 1.26a.
- [sumneko/w3x2lni](https://github.com/sumneko/w3x2lni) — identyfikatory i nazwy typów wież w danych gry.
- [Cheat Engine](https://github.com/cheat-engine/cheat-engine) — format tabeli i API Lua.

Plik `.CT` zawiera skrypty Lua i Auto Assembler dostępne do przejrzenia przez **Change script** w Cheat Engine.
