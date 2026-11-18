# SELF — oficjalne wydania

Instalatory i aktualizacje aplikacji SELF. Kod źródłowy aplikacji nie jest publikowany w tym repozytorium.

## Self Hub 0.7.1

[Instalatory Windows x64 i macOS Apple Silicon](https://github.com/zajczykjudyhopps/selfos-releases/releases/tag/self-hub-v0.7.1).

W wersji 0.7.1 Windows otrzymuje jeden zintegrowany pasek okna, bez menu File/Edit/View/Window, z natywnymi przyciskami i cienkimi ciemnymi paskami przewijania. Hub 0.7.0 pobiera tę wersję automatycznie, gdy jest wolny. Pakiet Mac 0.7.1 zachowuje zgodność wspólnego katalogu.

Poprawiono błąd ENOTEMPTY przy sprzątaniu kopii poprzedniej aplikacji. Instalacja zastępuje aplikację w dotychczasowym miejscu. Na Macu nieudana aktywacja lub weryfikacja przywraca poprzednią wersję. Nowy pasek pokazuje procent pobierania, prędkość, czas oraz osobne etapy instalacji i znika po zakończeniu.

Hub 0.7.0 sprawdza własne aktualizacje po uruchomieniu, po wznowieniu komputera i co 15 minut. Pobiera właściwy pakiet dla systemu i procesora, sprawdza rozmiar i SHA-256, a następnie automatycznie zastępuje siebie, gdy okno nie jest aktywne, nie trwa instalacja ani sesja aplikacji uruchomionej z Huba. Przy logowaniu bez zapamiętania urządzenia podmiana czeka na wylogowanie, aby nie przerywać sesji. Konto i dane aplikacji pozostają zachowane.

**Przejście ze starszego Huba do 0.7.0 wymaga jednorazowej instalacji ręcznej w dotychczasowym miejscu.** Kolejne wersje obsługuje autoaktualizacja. Rzeczywista podmiana Chata i Huba została sprawdzona na Macu, z zachowaniem danych. Instalator Windows przeszedł budowanie oraz kontrolę wersji i zawartości; pełny test na rzeczywistym Windows pozostaje do wykonania.

## Self Chat 0.4.0 — wydanie testowe

[Instalatory Windows x64 i macOS Apple Silicon](https://github.com/zajczykjudyhopps/selfos-releases/releases/tag/self-chat-v0.4.0).

Powiadomienia o wiadomościach, działanie w tle z zasobnikiem, odpowiedzi z cytatem w głównej rozmowie, zdjęcia bezpośrednio w czacie i duży podgląd 1:1. Poprawiono formularze oraz dodano trwałe usuwanie kanałów i workspace z kosza po potwierdzeniu nazwy i sprawdzeniu roli. Przed aktualizacją zamknij Chat przez Zakończ w menu zasobnika lub Cmd+Q; po instalacji otwórz przez Hub.

Chat korzysta z sesji Huba, więc Hub powinien pozostawać zalogowany. Powiadomienia wymagają zgody systemowej; profil zawiera test i informację o błędzie. Testy logiki i backendu przeszły, ale macOS odmówił banerów kopii QA. Dostarczenie powiadomień na docelowej instalacji oraz pełny test Windows pozostają do sprawdzenia. Mac ma podpis lokalny bez notaryzacji Apple i może zostać zablokowany przy pierwszym uruchomieniu.

## Katalog aplikacji

Hub 0.6.0 i nowszy korzysta z [catalog.json](https://github.com/zajczykjudyhopps/selfos-releases/blob/main/catalog.json), pobieranego z `https://raw.githubusercontent.com/zajczykjudyhopps/selfos-releases/main/catalog.json`. Flow i Chat są dostępne niezależnie od workspace’u. Ich instalatory nie są zawarte w Hubie.

Własne aktualizacje Huba korzystają z osobnego [hub-update.json](https://github.com/zajczykjudyhopps/selfos-releases/blob/main/hub-update.json). Każdy pakiet zawiera system, architekturę, rozmiar, SHA-256 i adres niezmiennego pliku z Releases tego repozytorium.

## Publikowanie kolejnych wersji

1. Zbuduj instalatory i sprawdź wersje, architektury oraz integrację logowania.
2. Utwórz nowe wydanie z nowym tagiem i instalatorami. Nie podmieniaj opublikowanych plików istniejącej wersji.
3. Sprawdź dostępność plików, rozmiary i SHA-256.
4. Dla Flow lub Chata zaktualizuj catalog.json, zachowując pozostałe aplikacje. Dla Huba zaktualizuj hub-update.json dopiero po opublikowaniu i sprawdzeniu plików wydania.
5. Hub pobierze własną aktualizację automatycznie. Instalację lub aktualizację Flow i Chata użytkownik rozpoczyna w Hubie.

## Zgodność ze starszym Hubem

Hub 0.5.0 i wcześniejszy korzysta z `/releases/latest/download/catalog.json` i wymaga kompletu plików w jednym wydaniu. Wydania Chata i Huba oznaczamy jako Pre-release, aby nie zmienić kanału starszych Hubów. Flow pozostaje dostępny pod dotychczasowymi adresami.

Publiczne są wyłącznie pliki wydań, katalogi i dokumentacja. Nie dodawaj haseł, tokenów, danych użytkowników ani kopii roboczych aplikacji.
