# InspigoConnector — wydania

Publiczne repozytorium z instalatorem **InspigoConnector**, programu łączącego
[inspigo.cloud](https://inspigo.cloud) z Subiektem GT, Navireo i Subiektem nexo PRO.

Kod źródłowy jest prywatny. Tutaj leżą wyłącznie pliki potrzebne do instalacji
i automatycznej aktualizacji.

## Instalacja

Pobierz najnowszy plik `.msi` z [wydań](../../releases/latest) i uruchom go na
komputerze, na którym pracuje Subiekt. Instalator zakłada usługę Windows
startującą z systemem oraz ikonę w zasobniku.

Program wymaga **Windows 64-bit**.

## Aktualizacja

Zainstalowany konektor sprawdza plik [`manifest.json`](manifest.json) i pobiera
nowsze wydanie sam. Aktualizacja odbywa się wyłącznie wtedy, gdy konektor nie
wykonuje żadnego zadania — nigdy w trakcie wystawiania dokumentu.

Ręczna aktualizacja to po prostu uruchomienie nowszego pliku `.msi`.

## Sprawdzenie pliku

Każde wydanie ma w manifeście skrót SHA-256. Aby go zweryfikować:

```powershell
Get-FileHash .\InspigoConnector-1.0.82.msi -Algorithm SHA256
```

## Numeracja wydań

`1.0.<liczba zapisów w repozytorium kodu>`. Trzecia część rośnie z każdym
zapisem, więc numer nigdy się nie cofa — Instalator Windows odmówiłby wtedy
aktualizacji w miejscu. Skrót zapisu, z którego powstało wydanie, jest
w manifeście w polu `commit`.

## Zgłoszenia

Problemy z konektorem zgłaszaj przez panel inspigo.cloud albo na
[kontakt@inspigo.pl](mailto:kontakt@inspigo.pl). To repozytorium nie przyjmuje
zgłoszeń dotyczących kodu, bo kodu tu nie ma.
