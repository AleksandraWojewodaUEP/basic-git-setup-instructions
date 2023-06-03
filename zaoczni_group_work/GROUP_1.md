# Praca w grupach 

## Repozytorium 

1. Dobranie się w zespoły 

2. Wybranie lidera

3. Liter tworzy repozytorium dla zespołu 

4. Lider dodaje członków zespołu do repozytorium 

5. Każdy z członków zespołu pracuje na swoim branchu, po zakończeniu
Każdej sekcji wszyscy mergują się do gałęzi głównej. 

## Zadania cz. A

1. W pliku `main.py` powinno znajdować się:

- funkcja licząca objętość sześcianu i jego pole powierzchni, 

- funkcja licząca objętość kuli, 

- testy sprawdzające działanie funkcji dla sześciana, przykład:

```python
assert nazwa_funckji(parametry,) == spodziewany_wynik
```

- testy sprawdzające działanie funckji dla kuli.

**UWAGA! Ta sama osoba nie może wykonywać funkcji dla figury i 
dla tej samej figury.**

## Zadania cz. B

- Zmiana wymagań! Kula jednak ma być stożkiem,

- zmana dotyczy także testów,

- dopisz kolejną figurę: strosłup, 

- dopisz testy dla ostrosłup.

## Zadanie cz. C

1. W pliku `salary.py`.

- Za pomocą instrukcji i założęń z 
[link](https://www.biznes.gov.pl/pl/portal/0083) 
stwórz klasę `Pracownik` z funkcjami: `__init__`, `__str__`, 
`oblicz_netto`, `oblicz_koszty_pracodawcy`, `wygeneruj_raport`. 
`oblicz_netto` ma zwracać wartość flouat z dwoma miejscami po przecinku, 
tak samo koszty pracodawcy, które mają zwracać tzw. brutto brutto. 
`wygeneruj_raport` nie ma nic zwracać (return), 
ma wyśwteilać (print) tzw. pasek z kosztem/składką i jej wartością. 
Dane wejściowe: imię, nazwisko, pensja_brutto
Każdą funckję ma wykonać inny student w zespole, 
chyba że jest ich za mało, wtedy wybrane osoby mogą wziąć dwie.

- Dopisz testy klasy `Pracownik` dla `__str__`, `oblicz_netto` i
`oblicz_koszty_pracodawcy`, testów nie może pisać ta sama osoba, 
co pisała funkcje.

- Napisz generator w pliku `generator.py`, który w folderze/katalodu 
`data` wygenreuje plik csv `pracownicy.csv` z imieniem, nazwiskiem i pseudolosową pensją 
z przedziału 1000 do 10000.

- Zadeklaruj pętle, która będzie wczytywać dane z pliku 
`data/pracownicy.csv` i kolejno wykonywać wszystkie funcje z klasy
`Pracownik`.

2. Wszystko powinno być na gałęzi głównej!

3. Wrzuć wykonane zadanie do wrzutki na Moodle. Pamiętaj, każdy z 
zespołu wrzuca zadanie do swojej wrzutki.
