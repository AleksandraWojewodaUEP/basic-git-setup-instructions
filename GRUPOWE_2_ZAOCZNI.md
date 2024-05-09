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