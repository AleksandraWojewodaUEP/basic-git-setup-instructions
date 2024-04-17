# Zadanie GRUPOWE 2 HP

<em>Szanowna Pani / Szanowny Panie,

Mamy przyjemność poinformowania Pani/Pana, że został(a) Pan(i) przyjęty/a do Szkoły Magii i Czarodziejstwa Hogwart. 
Dołączamy listę niezbędnych książek i wyposażenia.

Rok szkolny - semestr Grupowe_2 rozpoczyna się 11 kwietnia lub 17 kwietnia zależnie od grupy. 
Oczekujemy Państwa potwierdzenie commitem nie później niż 

dla grupy środowej: 23 kwietnia
dla grupy czwartkowej: 17 kwietnia

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
Prefekt musi stworzyć forka wskazanego repozytorium (zaklęcie duplikujące).
Każde zadanie ma zostać zrealizowane na odrębnej gałęzi, po zakończeniu zadania, wystawiamy PR.

## Część I


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
Operację zrandomizuj `True` ma wypadać w 85%, zaś `False` w 15%. 

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
* dla opcji specjalna: wyjec --> +4 knuty, list gończy --> +1 sykl
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


