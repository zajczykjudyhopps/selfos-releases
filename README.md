# SELF — oficjalne wydania

Instalatory i aktualizacje aplikacji SELF. Kod źródłowy aplikacji nie jest publikowany w tym repozytorium.

## Self Chat 0.3.0 — wydanie testowe

[Instalatory Windows x64 i macOS Apple Silicon](https://github.com/zajczykjudyhopps/selfos-releases/releases/tag/self-chat-v0.3.0).

Workspace’y są dostępne jako klikalne przyciski na przewijanym lewym pasku. Konto, znajomi i grupy są wspólne z Self Hub. Do testu na Windows użyj Self Hub 0.6.0 oraz Self Chat 0.3.0. Pełny test rozmowy na dwóch rzeczywistych komputerach pozostaje do wykonania.

## Katalog Self Hub 0.6.0 i nowszych

Katalog znajduje się w [catalog.json](https://github.com/zajczykjudyhopps/selfos-releases/blob/main/catalog.json). Hub pobiera go z:

`https://raw.githubusercontent.com/zajczykjudyhopps/selfos-releases/main/catalog.json`

Każdy pakiet ma jawny system, architekturę, rozmiar, SHA-256 i adres instalatora z Releases tego repozytorium. Nowy Hub pobiera Chat z GitHuba i nie zawiera jego instalatora. Flow i Chat są dostępne w jednym katalogu, niezależnie od workspace’u.

## Publikowanie kolejnych wersji

1. Zbuduj instalatory i sprawdź wersje, architektury oraz integrację logowania.
2. Utwórz nowe wydanie z nowym tagiem i dodaj instalatory. Nie podmieniaj opublikowanych instalatorów istniejącej wersji.
3. Sprawdź dostępność plików, rozmiary i sumy SHA-256.
4. Zaktualizuj główny catalog.json, zachowując wpisy pozostałych aplikacji. Pakiety mogą wskazywać różne niezmienne tagi wydań; nie trzeba ponownie dodawać instalatorów Flow przy wydaniu Chata.
5. Użytkownik odświeża katalog w Hubie i rozpoczyna instalację lub aktualizację.

## Zgodność ze starszym Hubem

Hub 0.5.0 i wcześniejszy korzysta z `/releases/latest/download/catalog.json` i wymaga kompletu plików w tym jednym wydaniu. Wydanie Chata 0.3.0 jest oznaczone jako Pre-release, aby nie zmienić kanału starszych Hubów. Obecne wydanie Flow pozostaje dostępne pod dotychczasowymi adresami. Zainstaluj Hub 0.6.0, aby korzystać z nowego wspólnego katalogu.

Publiczne są wyłącznie pliki wydań, katalog i dokumentacja. Nie dodawaj haseł, tokenów, danych użytkowników ani kopii roboczych aplikacji.
