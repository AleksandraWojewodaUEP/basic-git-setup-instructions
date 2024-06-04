# Zadanie GRUPOWE 2 HP

<em>Szanowna Pani / Szanowny Panie,

Mamy przyjemność poinformowania Pani/Pana, że został(a) Pan(i) przyjęty/a do Szkoły Magii i Czarodziejstwa Hogwart. 
Dołączamy listę niezbędnych książek i wyposażenia.

Rok szkolny - semestr Grupowe_2_zaoczni rozpoczyna się 28 kwietnia. 
Oczekujemy Państwa potwierdzenie commitem nie później niż 19 maja 2024 r.

Z wyrazami szacunku,

Aleksandra Wojewoda

Nauczyciel IO


Załącznik 1

Studenci powinni mieć:

Jeden zwykły program git (pod dowolny system)

Jedno konto na Githubie

Jedno IDE (preferowane VSC lub PyCharm - w czarnym ustawieniu)

Jeden komplet kluczy SSH lub ewentualnie działający zestaw login i hasło do HTTP

**UWAGA! Wszystkie commity studentów powinny być zaopatrzone w odpowiednio ustawione naszywki z imieniem, 
nazwiskiem i internetową pocztą sowią.**
</em>

## Podział na domy! 

Proszę wprowadzić Tiarę Przydziału.

![img](/imgs/tiara.gif)

## Organizacja domu

Proszę o wyłonienie prefekta, ustalenie wspólnej techniki przydzielania zadań i nazewnictwa gałęzi.
Prefekt musi stworzyć forka [wskazanego repozytorium](https://github.com/AleksandraWojewodaUEP/io_grupowe_2_hp) 
(zaklęcie duplikujące).
Każde zadanie ma zostać zrealizowane na odrębnej gałęzi (chyba że polecenie mówi inaczej), 
po zakończeniu zadania, wystawiamy PR.
Ktoś inny musi zatwierdzić PR swoim komentarzem lub żądaniem zmian. 
Po poprawkach gałąź może zostać złączona do gałęzi pomocniczej `staging`.

### PR i kontrola kodu

#### Programowanie 

1. Przejście na nową gałąź zadania `git checkout -b <nazwa nowej gałęzi>`.
2. Zrobienie zadania lub jego części.
3. Wypchnięcie zadania `git push` lub jeśli jest to pierwszy push z danej gałęzi `git push --set-upstream origin <nazwa gałęzi>`.

#### Przed PR (nieobowiązkowe, rekomendowane)

Warto przed PR się scalić z stagingiem. 
1. Upewnij się, że na swojej maszynie (komputerze) masz najnowszy `staging`. 
Jeśli nie masz - `git checkout staging` i `git pull`. 
2. Przejdź na gałąź zadania `git checkout <nazwa gałeżi zadania>`.
3. Scal zmiany z `staging` do siebie - `git merge staging` ("zaproś" `staging` do siebie).
4. Wypchnij zmiany - `git push`.

#### Wystawienie PR

1. Wejście w repo na Githubie. 
2. Wejście w zakładkę *Pull requstes*. 
3. Wejście w *New pull request*.
4. Wybranie odpowiednich gałęzi do scalenia.
Poniżej przedstawiono dwa obrazki obrazujące wystawianie PR. 
Dopilnuj, aby wystawić PR do swojego repozytorium, **NIE** do repozytorium prowadzącej. 
PR ma doprowadzić do scalenia zmian z Twojego zadania programistycznego/piśmiennego na `staging`, 
a w ostatecznym rezultacie na `main`.
![wrong pr](/imgs/pr_wrong.png)
![good pr](/imgs/pr_good.png) 

#### Akceptacja PR

1. Znalezienie recenzenta (ang. *reviewer*) kodu w ramach zespołu. 
2. Jeśli recenzent wskaże miejsca do poprawy, należy je poprawić i ponownie prosić recenzenta o opinie (powtarzać aż do skutku).
3. Jeśli recenzent zaakceptował zmiany, należy je scalić (można "wyklikać" w Githubie lub zrobić to z poziomu lokalnego workspace).

## Część I - Tag v 1.0 Hedwiga

Następujące zadania należy zrobić pod tagiem. 
Ma to nastąpić po poprawnym sprawdzeniu działania zadań.

### Zadanie 0 - .gitignore

W pliku .gitignore zbierz wszystkie elementy, które należy ignorować, 
np. pliki pomocnicze, foldery/katalogi IDE itd.
Zadanie zrób bezpośrednio na gałęzi `main`.

### Zadanie 1 - piśmienne

W pliku README.md napisz jaki dom reprezentuje zespół. 
Umieść przynajmniej jeden obraz, który będzie przetrzymywany w katalogu/folderze `imgs/`.
Umieść listę uczestników domu, ale tak, aby zawierały linki do ich kont na Githubie.
Umieść informacje dot. zasad współpracy.
Najważniejsze informacje **pogrub**, nazwy własne napisz *kursywą*, 
a nazwa domu ma być w barwach tego domu.
Zakazane praktyki przekreśl, zaś nazwy gałęzi lub strukturę nazwy gałęzi zapisz jako `kod w tekście`.

### Zadanie 2 - programistyczne 

W pliku main.py zaprogramuj funkcję `wyslij_sowe`, 
która przyjmuje dwa ciągi znaków: 
adresata, treść listu, funkcja ma wyświetlać (`print`) informację o wysłaniu sowy,
odczekać 1 sekundę i zwrócić `True`,
jeśli operacja się powiodła lub `False`, jeśli się nie powiodła. 
Operację zrandomizuj `True` ma wypadać w 90%, zaś `False` w 10%. 

### Zadanie 3 - programistyczne 

W pliku main.py zaprogramuj funkcję `licz_sume`, 
która ma przyjmować słownik, w którym mogą występować następujące klucze: 
geleon, sykl, knut. 
Dla każdego z kluczy wartość będzie reprezentowana przez listę, 
wskazującą na ilość monet danego rodzaju w jednym stosie. 
Funkcja ma zwracać słownik informujący o wielkości funduszu po jego przeliczeniu 
na monety o największym nominale. 
Przy czym 1 geleon = 17 sykli, 1 sykl = 21 knutów.

Przykładowe wejście:
```python
{
    "galeon" : [1, 3, 5],
    "sykl" : [18, 20, 10],
    "knut" : [30, 40, 7]
}
```

Oczekiwane wyjście:
```python
{
    "galeon" : 12,
    "sykl" : 0,
    "knut" : 14
}
```

### Zadanie 4 - programistyczne

W pliku main.py zaprogramuj funkcję `wybierz_sowe_zwroc_koszt`, 
która będzie przyjmować następujące parametry: 
potwierdzenie odbioru, odległość, typ, specjalna.

| odległość\typ | list |     paczka      |
|:-------------:| :-----: |:---------------:|
|    lokalna    | 2 knuty |    7 knutów     |
|    krajowa    | 12 knutów| 1 sykl 2 knuty  |
| dalekobieżna  | 20 knutów | 2 sykle 1 knut |

* potwierdzenie odbioru +7 knutów
* dla opcji specjalna: wyjec &rarr; +4 knuty, list gończy &rarr; +1 sykl
* **nie używaj w kodzie polskich znaków**

Przykładowe wywołanie:
```python
wybierz_sowe_zwroc_koszt(True, 'lokalna', 'list', 'wyjec')
```

Oczekiwane wyjście:
```python
{
    "galeon" : 0,
    "sykl" : 0,
    "knut" : 13
}
```

### Zadanie 5 - programistyczne

W pliku main.py zaprogramuj funkcję `waluta_dict_na_str`, 
która przyjmie słownik informujący o wielkości funduszu po jego przeliczeniu na monety o największym nominale i przepisze na cenę.
* jeśli wartość jakiegoś bilonu jest zerowa, pomiń ją,
* wersja łatwiejsza: nie musisz odmieniać słów ~~knutów, knuty, sykle, sykli, galeony itd.~~ 
możesz zostać przy knut, sykl, galeon.

Przykładowe wejścia:
```python
{
    "galeon" : 0,
    "sykl" : 0,
    "knut" : 13
}

{
    "galeon" : 17,
    "sykl" : 2,
    "knut" : 13
}
```

Oczekiwane wyjścia:
```python
"13 knut"

"17 galeon 2 sykl 13 knut"
```

* **nie umieszaj spacji na początku ani na końcu ciągu wyjściowego**

### Zadanie 6 - programistyczne

W pliku main.py zaprogramuj funkcję `waluta_str_na_dict`, 
która przyjmie ciąg znaków i przepisze na cenę w słowniku.
* jeśli wartość jakiegoś bilonu jest zerowa, mimo to umieść klucz w słowniku,
* podpowiedź: podziel ciąg po spacji, co drugi ciąg traktuj jak klucz, jeśłi zaczyna się na `g` uznaj to za galeon, 
jeśli na `s` jako sykl, jeśli na `k` jako knut.
* 
Przykładowe wejścia:
```python
"13 knut"

"17 galeon 2 sykl 13 knut"
```

Oczekiwane wyjścia:
```python
{
    "galeon" : 0,
    "sykl" : 0,
    "knut" : 13
}

{
    "galeon" : 17,
    "sykl" : 2,
    "knut" : 13
}
```

### Zadanie 7 - programistyczne

**UWAGA! Zadanie wymaga zadania 5! 
Jeśli nie ma zadania 5 na `main` należy zainicjalizować funkcję wydmuszkę.**

W pliku main.py zaprogramuj funkcję `nadaj_sowe`, 
która przyjmie następujące dane wejściowe:
* adresat &rarr; str
* tresc wiadomosci &rarr; str
* potwierfdzenie odbioru &rarr; True/False
* odleglosc &rarr; lokalna/krajowa/dalekobieżna
* typ &rarr; list/paczka
* specjalna &rarr; nie dotyczy/wyjec/list gończy

Za pomocą funkcji `wybierz_sowe_zwroc_koszt` oblicz koszt sowy, który 
Następnie do pliku `poczta_nadania_lista.csv` dopisz nowy wiersz z następującymi danymi:
* adresat &rarr; str
* treść wiadomości &rarr; str
* koszt przesyłki &rarr; oblicz za pomocą funkcji `wybierz_sowe_zwroc_koszt`, a następnie przekonwertuj na ciag znaków za pomocą funkcji `waluta_dict_na_str`
* potwierdzenie odbioru &rarr; True/False, gdzie True ma być zapisane jako TAK, zaś False jako NIE

**Funkcja ma nic nie zwracać (brak `return`).**


### Zadanie 8 - programistyczne 

W pliku main.py zaprogramuj funkcję `poczta_wyslij_sowy`, 
która będzie przyjmować ścieżkę do pliku `.csv`, 
gdzie będą występować następujące kolumny:
* adresat &rarr; str
* treść wiadomości &rarr; str
* koszt przesyłki 
* potwierdzenie odbioru &rarr; TAK/NIE

Następnie wyślij sowy z listy za pomocą funkcji `wyslij_sowe`.
* Jeśli sowa doleciała, policz koszt zgodnie z taryfą z kolumny koszt przesyłki.
* Jeśli sowa nie doleciała:
  * potwierdzenie odbioru = TAK → wyzeruj koszt (klient nie płaci),
  * potwierdzenie odbioru = NIE → policz koszt zgodnie z taryfą z kolumny koszt przesyłki.

Następnie zapisz rezultat w pliku, którego nazwa będzie miała następujący schemat 
`output_sowy_z_poczty_dzien_miesiac_rok.csv` i następujące kolumny:
* adresat, 
* tresc wiadomosci, 
* koszt przesylki, 
* potwierdzenie odbioru, 
* rzeczywisty koszt.

## Z staging na main

Po wykonaniu zadań, jeśli trafią na `staging`, można scalić je na `main` i otagować zgodnie z poleceniem. 

## Tagi

Tag dla repozytorium Git jest trochę jak kolorowe karteczki z zaznaczeniem jakiegoś 
ważnego/ulubionego fragmentu. 
Jest to swego rodzaju wskaźnik na dany moment w historii repozytorium, 
w odróżnieniu od gałęzi (analogicznie zakładka w książce) nie przesuwa się w ramach
postępu w tworzeniu oprogramowania (czytania książki).

Tag służy do oznaczenia wersji oprogramowania.
Zwykle oznaczenia są dwu lub trzyelementowe tj. `v0.1` lub `v2.17.3`.
Przy czym składniki liczbowe wersji traktuje się od najważniejszego do najmniej ważnego.
Czy dla `v.2.17.3` ogólnie będzie można powiedzieć, że jest to wersja druga oprogramowania,
na dalszym planie będzie 17, a na końcu 3.

W Git rozróżnia się dwa rodzaje tagów: 
* tag lekki (ang. *lightweight tag*) - zajmuje mniej miejsca w repozytorium i nie przetrzymuje dodatkowych
metadanych, jest po prostu wskaźnikiem na danego commita,
* tag adnotowany (ang. *annotated tag*) - zajmuje więcej miejsca i przetrzymuje metadane.

Podstawowe komendy ułatwiające pracę z tagami:
* `git tag` - wyświetl listę tagów, 
* `git tag -l v0.2*` - wyświetli wszystkie tagi, rozpoczynające się od v0.2,
* `git tag -a v0.1 -m "Widamość dla taga"` - stworzenie taga adnotowanego
  (przełącznik `-a`),
* `git tag v0.1` - stworzenie taga lekkiego,
* `git push origin v0.1` - wypchnięcie taga.

Taga można stworzyć zarówno z poziomu workspace, jak i "wyklikać" w Githubie.

Więcej do poczytania o tagach można znaleźć w [oficjalnej dokumentacji](https://git-scm.com/book/en/v2/Git-Basics-Tagging).


## GitHub Actions workflows

Jednym z najłatwiejszych sposobów weryfikacji jakości kodu jest ich automatyczne sprawdzanie. 
Można spotkać się z wieloma sposobami na automatyzowanie zadań, 
tym które będziemy wykorzystywać na zajęciach będzie usługa Github Actions.
Służy ona automatyzacji zadań w repozytoriach git.
Github Actions umożliwia tworzenie i uruchamianie przypływów pracy (ang. *workflows*), 
które mogą wykonywać określoną pracę po spełnieniu określonych warunków.
Może to być nowy commit lub wygenerowanie nowej PR.
Korzystanie z tego typu automatyzacji wspiera ciągłą integrację i ciągłe dostarczanie (CI/CD).
Co w konsekwencji prowadzi do przyśpieszenia i ulepszenia procesu dostarczania,
ale też dbania o jego jakość.

Przykładowy przepływ pracy realizowany na zajęciach witał się z prefektem w zespole.

Aby go stworzyć, tworzyliśmy plik `hello.py`, który zawierał linię kodu:
```python
print("Hello Ola")
```
Następnie tworzyliśmy przepływ pracy w folderze/katalogu: `.github/workflows/` w pliku `hello.yml`.
Przepływ wyglądał następująco:
```yaml
name: Przywitanie z prefektem

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

permissions:
  contents: read

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - name: Set up Python 3.10
      uses: actions/setup-python@v3
      with:
        python-version: "3.10"
    - name: Powitanie
      run: python hello.py
```
W pliku deklarowano nazwę, następnie na jakie akcje operacje mają się wykonać automatycznie.
W tym przypadku było to na nowy commit oraz na PR w obu przypadkach jedynie dla gałęzi `main`. 
Następnie ustawiono odpowiednie zgody i zdefiniowano `jobs`.
`jobs` odpalane są na najnowszym Ubuntu z Pythonem w wersji 3.10.
Ostatnim elementem jest wywołanie pliku `hello.py`.

Na koniec projektu grupy zobowiązane są do stworzenia podstawowych testów dla zadań w projekcie 
i automatyczne ich uruchamiania dla każdego nowego commita i PR na gałęzi głównej (najczęściej *main*).
Każdy użytkownik ma napisać testy (jeden lub wiele) do jednej funkcji zadania z części programistycznej.
Do testów można wykorzystać `assert`.
Testy można napisać w jednym pliku np. `tests.py` lub osobno dla każdego użytkownika.
Następnie należy zdefiniować nowego yaml'a z automatycznym ich uruchomieniem.
Testy powinny kończyć się ich poprawnym (na zielono) wykonaniem.
