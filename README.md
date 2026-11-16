# SELF — oficjalne wydania

Instalatory i aktualizacje aplikacji SELF. Kod źródłowy aplikacji nie jest publikowany w tym repozytorium.

## Pobieranie

Otwórz [najnowsze wydanie](https://github.com/zajczykjudyhopps/selfos-releases/releases/latest). SELFOS HUB wybiera instalator zgodny z systemem i architekturą komputera.

SELF Flow 5.0.1 to dotychczasowy SELF OS. Pakiet nadal instaluje aplikację pod nazwą SELF OS, zachowując lokalizację danych.

## Publikowanie kolejnego wydania

1. Otwórz publikator w SELFOS HUB: **Źródło aplikacji → Otwórz publikator wydań**.
2. Ustaw wersję i wybierz instalatory. Eksportuj do stałego folderu katalogu; używaj go ponownie, aby zachować inne aplikacje.
3. W tym repozytorium otwórz **Releases → Draft a new release**. Wybierz nowy tag, np. `self-flow-v5.0.2`, i podaj opis zmian.
4. Dodaj `catalog.json` oraz wszystkie instalatory z folderu `assets` wygenerowanego przez publikator. Pliki instalatorów załącz bezpośrednio do wydania — nie jako folder ani ZIP.
5. Kliknij **Publish release**. Wydanie musi być zwykłym, najnowszym wydaniem, a nie wersją testową (Pre-release).

Hub sam sprawdza najnowsze wydanie. Użytkownicy nie konfigurują GitHuba i nie potrzebują konta GitHub. Obecnie rozpoczęcie instalacji wymaga potwierdzenia w hubie.

Każde najnowsze wydanie musi zawierać pełny katalog i instalatory dla wszystkich aplikacji w tym katalogu. Po opublikowaniu nie podmieniaj plików: poprawki wydawaj jako nową wersję.

## Adres aktualizacji

`https://github.com/zajczykjudyhopps/selfos-releases/releases/latest/download/catalog.json`

Publicznie dostępne są wyłącznie pliki wydań i dokumentacja. Nie dodawaj tu haseł, tokenów, danych użytkowników ani kopii roboczych aplikacji.
