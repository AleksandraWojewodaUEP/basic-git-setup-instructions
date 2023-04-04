# Zadania z Pythona

## Set up 

Zadania wykonujemy na osobnej gałęzi:  `solo-python-work`, każdy w **swoim**
repozytorium.

Można wykonać poniższe instrukcje zarówno z poziomu terminala, jak i
poziomu IDE, czy eksploratora plików.

1. Utwórz w swoim repozytorium katalog: 

- Git BASH: `mkdir solo-work`

- wyklikaj w IDE (drugi przycisk myszki na katalog projektu `New` -> `Directory`) 
lub dowolnie inaczej w tym także w eksploratorze plików,

2. Wejdź do nowego katalogu i utwórz plik 

- `cd solo-work` i `touch solo_1.py`

- w IDE: drugi przycisk myszki na katalog `solo-work` -> `New` -> `Python File`,
wpisz nazwę pliku `solo_1` bez rozszerzenia.

### solo_1

Jeden blok kodu jest jednym zadaniem, np. `zadanie 1.4`. Wszystkie zadania `zadanie 1.x`
powinny znajdować się w tym samym pliku. Zadanie należy wkleić, wykonać zgodnie z 
oczekiwanym rezultatem, zacommitować z wiadomością (*message*) zawierającą informację 
jakie to zadanie.

**Zadanie 1.1** Występują dwie zmienne `hello` oraz `student`. Połącz zmienne, 
tak aby stanowiły jeden komunikat. Do wykonania zadania użyj funkcji `format()` na stringu.
Przykład: `"Lorem {}".format("ipsum")`.

```python
# zadanie 1.1

hello = "Hello"
student = "Ola"

# oczekiwany rezultat: Hello Ola
# wykorzystaj w princie zmienne hello i student
print("Hello Kasia")
```

**Zadanie 1.2** Wyprintuj przywitanie składające się z `Hello` + osoby, która 
zostanie wpisana przy pomocy funkcji `input()`. Funkcja ta zbiera wejście od użytkownika
i umieszcza w zmiennej `student`, która ma zostać wykorzystana w przywitaniu.

```python
# zadanie 1.2

student = input("Wpisz swoje imie")

print("Hello Ola")
```

**Zadanie 1.3** Stosując odpowiednią funkcję, policz liczbę studentów. Następnie 
użyj zmiennej `liczba_studentow` w `print()`, aby wyświetlić wynik.

```python
# zadanie 1.3

studenci = ["Ania", "Kuba", "Piotr", "Jan"]

# policz liczbe studentow w tablicy studenci 
# oczekiwany rezultat: Liczba studentow wynosi: 4
liczba_studentow = 0
print("Liczba studentow wynosi: 0")
```

**Zadanie 1.4** Za pomocą pętli `for` i `print()` przywitaj się z każdym studentem.

```python
# zadanie 1.4

studenci = ["Ania", "Kasia", "Piotr", "Tomek"]

# za pomoca petli i print przywitaj sie z kazdym studentem
# z tabeli studenci osobno
# oczekiwany rezultat:
# Hello Ania
# Hello Kasia
# Hello Piotr
# Hello Tomek
print("Hello Ania")
```

**Zadanie 1.5** Do zmiennej `wynik` wpisz wynik równania `liczba` ^ `potega`, następnie
użyj go w funkcji `print()`.

P.S. Matematycznie poprawne: `liczba*liczba*liczba*liczba`, ale tego rozwiązania nie zaliczę.

```python
# zadanie 1.5

liczba = 3
potega = 4

wynik = 0

# oczekiwany rezultat:
# Wynik wynosi: 81
print("Wynik wynosi: 0")
```

**Zadanie 1.6** Oblicz liczbę nawiasów otwierających w zmiennej `ciag_znakow`.

```python
# zadanie 1.6

# policz ilosc nawiasow ( w danym ciagu znakow

ciag_znakow = "edbw(hdakqas(skqskahb))adwndwb(wgwidn()dsqwhjdw)"
liczba_nawiasow_otwierajacych = 0

# oczekiwany rezultat:
# Liczba nawiasow otwierajacych wynosi: 4
print("Liczba nawiasow otwierajacych wynosi: " + str(liczba_nawiasow_otwierajacych))
```

**Zadanie 1.7** Posortuj po imieniu studentów. Możesz sortować w miejscu w tabeli
`studenci` lub stworzyć nową pomocniczą.

```python
# zadanie 1.7

# posortuj alfabetycznie (od imienia) studentow
studenci = ["Anna Szczesny", "Tomasz Nijaki", "Barbara Kowalska", "Jan Niezbedny"]

# oczekiwany rezultat:
# Anna Szczesny
# Barbara Kowalska
# Jan Niezbedny
# Tomasz Nijaki
print("Alfabetyczna lista studentow wynosi: ")
for student in studenci:
    print(student)
```

**Zadanie 1.8** Posortuj po nazwisku studentów. Możesz sortować w miejscu w tabeli
`studenci` lub stworzyć nową pomocniczą.

```python
# zadanie 1.8

# posortuj alfabetycznie (od nazwiska) studentow
studenci = ["Anna Szczesny", "Tomasz Nijaki", "Barbara Kowalska", "Jan Niezbedny"]

# oczekiwany rezultat:
# Barbara Kowalska
# Jan Niezbedny
# Tomasz Nijaki
# Anna Szczesny
print("Alfabetyczna lista studentow wynosi: ")
for student in studenci:
    print(student)
```

**Zadanie 1.9** Policz wszystkich studentów z tablicy, których nazwisko zaczyna się na N.
Wynik zapisz do zmiennej `liczba_n`, który następnie wykorzystaj do wyświetlenia w `print()`.

```python
# zadanie 1.9

# policz wszystkich studentow z tablicy, ktorych nazwisko zaczyna sie na N
studenci = ["Anna Szczesny", "Tomasz Nijaki", "Barbara Kowalska", "Jan Niezbedny"]

liczba_n = 0
print("Liczba studentow na N wynosi: 0")
```

**Zadanie 1.10** W zmiennych `wykres_x` kolejno znajdują się punkty dla wykresów.
Zbadaj każdy z nich, czy jest możliwe, aby wyznaczyć dla punktów na wykresach 
1, 2 i 3 funkcję liniową. 

Rysunek pomocniczy:

![img](/imgs/auxiliary_drawing_1_10.png)

Po zrobieniu zadania widać jak nieefektywny jest kod dla zadania 1.10. 
Wiele linii kodu zostało powtórzonych. Dlatego w kolejnych zadaniach 
będziemy budować kod, który jest wykorzystywany wielokrotnie.

```python
# zadanie 1.10

# zmienne poniezej preprezentuja ulozenie punktow na wykresie,
# do zadania dolaczono takze rysunek pomocniczy
wykres_1 = [[2, 4], [4, 4], [6, 4]]
wykres_2 = [[2, 3], [4, 4], [6, 5]]
wykres_3 = [[2, 3], [4, 3], [5, 4]]

# zbadaj kazdy wykres, czy dla wyznaczonych punktow istnieje funkcja
# liniowa laczaca punkty
# jesli sie nie da, to zwroc False
# jesli sie da, zwroc True

wykres_1_funkcja_liniowa = False
wykres_2_funkcja_liniowa = False
wykres_3_funkcja_liniowa = False

if wykres_1_funkcja_liniowa:
    print("Dla punktow w wykres_1 mozna wyznaczyc funkcje liniowa.")
else:
    print("Dla punktow w wykres_1 nie mozna wyznaczyc funkcji liniowej.")

if wykres_2_funkcja_liniowa:
    print("Dla punktow w wykres_2 mozna wyznaczyc funkcje liniowa.")
else:
    print("Dla punktow w wykres_2 nie mozna wyznaczyc funkcji liniowej.")

if wykres_3_funkcja_liniowa:
    print("Dla punktow w wykres_3 mozna wyznaczyc funkcje liniowa.")
else:
    print("Dla punktow w wykres_3 nie mozna wyznaczyc funkcji liniowej.")

# oczekiwany rezultat:
# Dla punktow w wykres_1 mozna wyznaczyc funkcje liniowa.
# Dla punktow w wykres_2 mozna wyznaczyc funkcje liniowa.
# Dla punktow w wykres_3 nie mozna wyznaczyc funkcji liniowej.

```

**Po wykonaniu zadań posprzątaj plik. Jeśli pojawiły się namiarowe `print()` usuń je i 
zacommituj. Dobrą praktyką jest "sprzątanie kodu", zwykle towarzyszy temu commit 
z taką lub podobną wiadomością: `Cleaning up` / `Sprzatanie`.**