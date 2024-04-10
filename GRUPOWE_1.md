# Hello Team!

Przed wami zadanie grupowe. 
Zostaliście podzieleni na #todo osobowe grupy i przed Wami grupowe zadanie.
W ramach jednej grupy współdzielicie jedno repozytorium, do którego każdy dostarcza swoją część zadania.

Zadania zostały opisane skrótowo. 

Ostatecznie oczekuje się od zespołu, że dostarczy gotowe rozwiązanie, za co punty będą przydzielane
ze zbiorową odpowiedzialnością.

## Gałąź (ang. _branch_)

Każde zdanie należy wykonywać na swojej gałęzi, chyba że treść zadania głosi inaczej.

Gałąź jest ruchomym wskaźnikiem do Twoich zmian.
Jest wykorzystywany w codziennej pracy w dostarczaniu oprogramowania. 
Gałęzie pozwalają na:

- oddzielenie kodu na różnej fazie dostarczania
- umożliwia pracę nad różnymi funkcjonalnościami bez ryzyka kolizji
- ułatwia testowanie i wdrażanie
- pracę programistów nad jednym kodem źródłowym w ramach różnych zadań
- śledzenie zmian
- cofanie zmian
- utrzymanie historii zmian
- i wiele wiele więcej.

Zwykle pewne gałęzie dedykowane są specyficznym zadaniom.
Zależnie od polityki organizacji gałąź główna __main__ (wcześniej __master__) zwykle
jest dedykowana najnowszej wersji oprogramowania lub jej najbardziej stabilnej wersji.
Gałąź __production__ może być gałęzią z kodem produkcyjnym (dedykowana użytkownikowi końcowemu).
Gałąż __staging__ / __stag__ może być gałęzią pretendującą w najbliższym czasie (releasie) produkcją.
Gałąź __testing__ może służyć testom. Często też wprowadza się numerację lub specjalne oznaczenia.
Gałęzie __PIO_1234_figures__ / __io_1234__ / __1234__ mogą oznaczać zadanie o 1234 z Projektu Inżynieria Oprogramowania.
Konwencja zależy od organizacji lub od zespołu. Często także od API różnych systemów do zarządzani projektem 
np. Jira, która udostępnia możliwość automatycznego przypisywania gałęzi do zadań.

Istnieje wiele różnych konwentów nazewnictwa gałęzi, w tym także od imienia programisty: __AW_1234__ / __aw_1234__.

Zespół w ramach zajęć na IO wybiera własny sposób nazewnictwa gałęzi. 

Każde zadanie ma być zrealizowane na osobnej gałęzi.
W ramach zadania można commitować wielokrotnie (min. 2 razy):
```bash
git add <pilk>
git commit -m "Treść wiadomości"
```
Można commitować także z IDE (wedle uznania).

Aby wypchnąć zmiany na repo zdalne pierwszy raz z danej gałęzi, należy wskazać gałąź zdalną.
```bash
git push --set-upstream origin <nazwa gałęzi>
```
Nazwa gałęzi lokalnej i zdalnej może być (a nawet zwykle jest) taka sama.
Zdarza się, że przypisujemy gałąź lokalną do gałęzi zdalnej pod inną nazwą najczęściej, 
gdy chcemy poprawić nazwę gałęzi.
`origin` oznacza w tym przypadku oryginalne repo zdalne.
Zdarza się, że posiadamy wiele repozytoriów zdalnych tego samego projektu (rozwinięcie na zajęciach).
`--set-upstream` to ustawienie strumienia danych. 
Kolejne zmiany w ramach istniejącej już gałęzi można wypychać już za pomocą komendy `git push`.

## Punkty [0 - 10]

Punkty częściowo są przydzielane wspólnie, częściowo indywidualnie.
Zadanie 1 jest przeznaczone dla osoby prognącej zaangażować się bardziej w stronę pisania dokumentacji, 
mniej programowania. 
Zadania mają tendencję bycia trudniejszymi wraz ze wzrostem numeracji.
Zadanie ostatnie jest z dodatkowym punktem za trudność zarówno dla testera, jak i programisty. 
Programista musi samodzielnie wymyślić sposób rozwiązania zadania.
Typy, miejsca po przecinku itd.
Następnie opisać to w ramach komentarzy w kodzie, aby było to weryfikowalne ze strony testera.
Tester musi ująć założenia programisty w testach.
Za wykonanie trudnych zadań będzie można uzyskać więcej pkt.

Na Moodle link do repo wraz z listą osób w zespole wrzuca jedna osoba zgodnie z opisem zadania.
Pozostałym osobą punkty zostaną naliczone przez prowadzącego (nie muszą nic robić).

Jeżeli w grupie znajduje się osoba z IOS, należy to zgłosić prowadzącej.

## Deadline - dzienni

Za wykonanie zadania na zajęciach: max punktowy.

Później, ale przed świętami (tj. 27.03 włącznie): -1 dla każdego.

Później, ale przed zajęciami w 1. tygodniu kwietnia: -2 pkt dla każdego.

Później: 0 pkt.

## Deadline - zaoczni 

Za wykonanie zdania do dnia następnego spotkania w ramach IO (włącznie):
max punktowy.

## Zadania cz. 1

### Zadanie 1 [piśmienne] [1 pkt wspólnie]

Załóż puste prywatne repozytorium na [Github](https://github.com/).
Dodaj wszystkich użytkowników ze swojego zespołu do edycji repo (_stworzone repo_ --> _Settings_ --> _Collabolators_)
oraz prowadzącego zajęcia [AW](https://github.com/AleksandraWojewodaUEP).

### Zadanie ogólne [dla wszystkich]

Skolonuj stworzone na potrzeby zadania repo: `git clone <link do repo>`.
Stwórz dla siebie gałąź zgodnie z konwencją wybraną przez zespół `git checkout -b <nazwa brancha>`.

### Zadanie 2 [piśmienne] [3 pkt dla dev, 2 pkt dla testera]

W katalogu głównym repo stwórz plik `README.md`. 
Za pomocą MarkDown ([Przykładowy MD CheetSheat](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet))
zbuduj plik zawierający spis członków zespołu oraz ustalenia dot. nazewnictwa gałęzi.
Dodatkowo opisz, co zawiera repo. 
Informacja ta ma w pierwszej kolejności powiedzieć, czego dotyczy sam projekt.
Na samym końcu skonstruuj tabelę, w której wypisz 10 powszechnie znanych książek.
Tabela powinna zawierać kolumny tytuł i autor. 
Pomieszaj autorów w stosunku do książek.
Wykorzystaj przynajmniej kilka formatowań za pomocą MarkDown.
Zostaw kilka literówek w tekście, ale nie w członkach zespołów :)

### Zadanie 3 [programistyczne] [3 pkt dla dev, 2 pkt dla testera]

W katalogu głównym repo stwórz katalog `area`, następnie w katalogu `area` stwórz plik
`area_calc.py`.
W pliku zaprogramuj cztery funkcje `def` liczące pole powierzchni wybranych przez siebie figur.
Przykład: 
```python
# komentarz
def zwracam_zero_niezaleznie_co_przyjme(cokolwiek):
    return 0
```
W jednej z funkcji popełnij błąd w obliczeniach :)

### Zadanie 4 [programistyczne] [3 pkt dla dev, 2 pkt dla testera]

W katalogu głównym repo stwórz katalog `circum`, następnie w katalogu `circum` stwórz plik
`circum_calc.py`.
W pliku zaprogramuj cztery funkcje `def` liczące obwód wybranych przez siebie figur.
Przykład: 
```python
# komentarz
def zwracam_zero_niezaleznie_co_przyjme(cokolwiek):
    return 0
```
W jednej z funkcji popełnij błąd w obliczeniach :)

### Zadanie 5 [programistyczne] [3 pkt dla dev, 2 pkt dla testera]

W katalogu głównym repo stwórz katalog `volume`, następnie w katalogu `volume` stwórz plik
`volume_calc.py`.
W pliku zaprogramuj trzy funkcje `def` liczące objętość wybranych przez siebie brył.
Przykład: 
```python
# komentarz
def zwracam_zero_niezaleznie_co_przyjme(cokolwiek):
    return 0
```
W jednej z funkcji popełnij błąd w obliczeniach :)

### Zadanie 6 [programistyczne] [4 pkt dla dev, 3 pkt dla testera]

W katalogu głównym repo stwórz katalog `math`, następnie w katalogu `math` stwórz plik
`math_calc.py`.
W pliku zaprogramuj cztery funkcje `def` z listy poniżej wybierz, co mają robić:
- dzielenie `a` przez `b` z zaokrągleniem do drugiego miejsca po przecinku
- zwracanie reszty z dzielenia `a` przez `b`
- potęgowanie
- przeliczanie ułamków godziny na minuty: 1h --> 60 min; 1,5h --> 90 min; 1/4h --> 15 min
- przeliczanie cali na cm lub odwrotnie
- przeliczanie km na mile lub odwrotnie
- przeliczanie ile samochód pali na 100km na ile mil wystarczy galon i odwrotnie

Przykład: 
```python
# komentarz
def zwracam_zero_niezaleznie_co_przyjme(cokolwiek):
    return 0
```
W jednej z funkcji popełnij błąd w obliczeniach :)

## Zadania cz. 2

Każde zadanie, poza 1., wymaga sprawdzenia przez inną osobę niż ta, która je wykonywała.
W ramach zespołu wymieńcie się zadaniami, ale w taki sposób, aby nie wystąpiła para, 
która sprawdza zadania sobie nawzajem. 
Sprawdzenia dokonujemy na gałęzi zadania.

Aby zmienić gałąź można wykorzystać polecenie:
```bash
git checkout <nazwa_brancha>
```

Dla zadania piśmiennego należy sprawdzić literówki oraz treść tabeli.

Dla zadania programistycznego należy:
* utworzyć w danym katalogu pliku `tests.py`
* w pliku `tests.py` importować sprawdzane funkcje
* napisać testy sprawdzające działanie funkcji
```python
assert zwracam_zero_niezaleznie_co_przyjme(7)==0
```
* za pomocą testów znaleźć niedziałającą funkcję i ją poprawić.

Poprawki wypchnąć.

## Zadania cz. 3: Łączenie gałęzi [3 pkt wspólnie]

Zadaniem zespołu jest doprowadzenie do połączenia zadań na gałęzi `main`. 
Każde zadanie, które przeszło przez testowanie można uznać za gotowe do złączenia.
Łączenia dokonuje osoba odpowiedzialna za zadnie (nie tester).

Poniżej przedstawiono kroki mające doprowadzić do pożądanego efektu bez kolizji.
Istnieje wiele strategi mergowania i kolejne poznamy na następnych zajęciach.
Użytkownik może wykorzystać dowolną znaną mu metodę.

Pobranie najnowszego `main`
```bash
git checkout main
git pull
```

Pobranie najnowszej gałęzi z zadaniem
```bash
git checkout <branch_z_zadaniem>
git pull
```

Złączenie `main` do gałęzi zadaniowej
```bash
git merge main
```

Wypchnięcie zmiany
```bash
git push
```

Złączenie gałęzi zadaniowej do `main`
```bash
git checkout main
git merge <branch_z_zadaniem>
```

Wypchnięcie `main` ze zmianami z <branch_z_zadaniem>
```bash
git push
```

