# Parca w grupach

## Zasady gry

1. Ta sama osoba nie może zrobić funkcji i testów.

2. Każdy moduł musi zakończyć się mergem do maina.

3. Każdy moduł musi rozpocząć się nowymi branchami developerskimi.

4. Wszystkie funkcje i testy powinny znajdować się w pliku `main.py`

### Repozytorium 

1. Dobranie się w zepsoły 2 - 3 osobowe.

2. Wybranie lidera zespołu.

3. Lider tworzy repozytorium.

4. Lider dodaje członków zespołu do repozytorium. 

5. Lider tworzy README.md z tytułem *Praca w grupach* i dzisiejszą datą.

6. Członkowie zespołu klonują repozytorium (`git clone <repo>`) lub jeśli wcześniej to
zrobili to ściągają zmiany (`git pull`).

7. Każdy członek zespołu tworzy swoją gałąź od imienia i litery modułu, np. `ola-a`

8. Jeśli ktoś pracuje z IDE generującym swój filder/katalog: utwórz `.gitignore` i
dodaj katlog IDE do pliku.

### Moduł A

1. Funkcja porządkująca do prawej, której zadaniem jest uporządkowanie 
inputu i wygenerowanie stringa, który będzie prezentował dane w równych liniach, 
zaś kolumny liczbowe będą przyklejone do prawej.

Przykładowe wejście (input): 

```
[[1, 2, 10, 150], [10, 2, 1000, 2], [1, 120, 1, 1000]]
```

Oczekiwane wyjście (output): 

```
[[ 1,   2,   10,  150],
 [10,   2, 1000,    2],
 [ 1, 120,    1, 1000]]              
```

2. Analogiczna funkcja do lewej.

3. Testy dla 1. i 2. 

Przykład testu:

```
assert porzadkuj_do_prawej(input) == oczekiwany_output
```

### Moduł B

1. Funkcja wyznaczająca brakujący wierzchołek kwadratu na wykresie.

Przykładowe wejście: [[1,1], [2,3], [4,2]]

Oczekiwane wyjście: [3,0]

2. Funkcja wyznaczająca brakujący wierzchołek trójkąta równobocznego na wykresie.

Przykładowe wejście: [[1,1], [2,3]]

Oczekiwane wyjście: [[x1,y1],[x2,y2]]  (trójkąt może mieć dwie opcje)

3. Testy dla 1. i 2.


