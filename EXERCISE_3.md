# Zadanie 3

W tutorialu zosatną przedstawione takie zagadnienia jak gałąź (ang. *branch*) oraz PR
(ang. *pull request*).

## Gałąź (ang. *branch*)

Przed rozpoczęciem opowieści o gałeziach (czy też jak wprowadził dr Kałużny - macki :) ) 
opowiemy trochę jak Git przechowywuje dane.

Git przechowuje serię migawek (ang. *snapshots*). 
W obiekcie commita znajdują się: wskaźnik do migawki zmain, które zostały wprowadzone w 
danym commicie, nazwa oraz mail użytkownika, który je wprowadził, wiadomość (ang. *message*)
oraz wskaźniki do commitów poprzedzających dany commit (zero wskaźników dla commita
iniclaizującego, jeden dla zwykłego commita i jeden lub wiele dla commita megującego).

Odwołując się do naszych zajęć, gdzie historia commitów może wyglądać następująco:

![img](/imgs/ex_3_1.png)


Na zrzucie widać, że pierwszym commitem był `README.md` (choć powienien być to `Init commit`).
Obiekt tego commitu nie posiada żadnego wskaźnika poprzedniego commita. Przypiszmy commitom
litery alfabetu od `a` dla najstarszego commita (czyli: `README.md`) i kolejno `b` dla 
`Added first task` itd. Obiekt commit `b` będzie wskazywał swojego poprzendika, czyli 
commit `a` itd.

Gałąź więc będzie swego rodzaju wskaźnikiem do commita, przy czym wskaźnik będzie się zmieniał
z każdym commitem dla danej gałeżni. Można więc stwierdzić, że wskaźnik gałezi będzie wskaźnikiem
na najświeższego commita w danej gałęzi.

Koncept wydaje się bardzo złożony, jednak pamiętajmy, ze powstał bezpośrednio z praktyki. 

Gałeźnie powstały na potrzeby zarządzania wersjami danego projektu, znacząco ułatwiają 
pracę zespołów wielosobowych (powiedziałabym nawet, że wieloprocesowych), porządkują proces
dostarczania oprogramowania i choć wyżej opisana gałęzie z niskopoziomowego poziomu, to
wysokopoziomowo są dużo łatwiejsze do zrozumienia.

## Zadania samodzielne

Stwórz nową gałąź w repozytorium (gałąź nie musi nazywać się jak w przykładzie):

```
git checkout -b moj_nowy_branch
```

Przyjrzyjmy się temu poleceniu. `chechout` "wymeldowuje" z obecnej gałezi (np. `main` lub `master`).
Flaga `-b` jest potrzebna do stworzenia nowej gałęzi i przeskoczenia na nią. Osttanim 
elementem jest `moj_nowy_branch`, który jest nazwą nowej gałęzi.

Osobnym tematem jest kwestia nazywania gałęzi. W wielu organizacjach nazwy gałęzi bezpośrednio 
odwołują się np. do numeru zadania. Nazwa sugeruje lub pozwala na łatwe zidentyfikowanie jaki
fragmet oporogramowania jest udoskonalany lub jaka funkcja (funckjonalność) się z nim wiąże. 
Poza tym jeszcze jeszcze wiele innych strategii nazywania gałęzi i warto przy przystopięniu 
do danego projektu o to zapytać lub przejrzeć jak nazywane są gałęzi. Jak klika 
specyficznych nazw, które są zarezerowane (ale tylko zwyczajowo) dla specjalnych zadań, 
należą do nich:

- `main` (odchodzi się od `master`) gałąź główna, bardzo często wykorzystywana jest jako 
"najświeższa" wersja kodu, więc częstotliwość zmian na tej gałęzi będzie bardzo częsta, 

- `staging` (czasem w skrócie `stag`, spotkałam się też z `stg`) - można przetłumaczyć
jako "pretender" do bycia produkcją; jest to jakaś wersja stablina, która w najbliższym czasie 
zostanie dostarczona do użytkownika końcowego (pretenduje do bycia produkcją),

- `production` (czasem w skrócie `prod`) - gałąź zawierająca kod produkcyjny, czyli kod 
budujący oporgramowanie, które użytkuje użytkonik końcowy (przykładowo na takiej gałęzi 
może trzymać swój kod źródłowy Facebook, a my jako użytkonicy końcowi z niego korzystamy),

- `dev` / `testing` - wszystkie środowisko utrzymywane dla testów, ale często dla użytku 
wewnętrznego organizacji, gdzie omawiane są jakieś funkcje (funkcjonalności), które już 
zostały zaimpleemntowane, ale jeszcze niedostaecznie przestestowane lub utrzymywane z danych
powodów (np. wydanie produktu wtedy, kiedy marketing uzna, że jest to słuszne, inwestor 
zarząda itd.).

Jak wspomniałam wyżej to jedynie zwyczajowe użycie tych nazw. Organizacje samodzielnie 
ustalają politykę zarządzania kodem, w tym także politykę nadawania nazw gałęziom.

Poza specyficznymi gałęziami, zwykle spełniającymi specyficzne funkcje, są jeszcze te 
na których buduje się konkretne rozwiązania, koncepcja nazywania gałęzi robocznych różni się od
organizacji, ale przykłądowo może wyglądać tak:

- `of-235-spell-check` / `s3-984-database-migration` / `jira-167` / `infra-71` - przykłądowe nazwy gałęzi,
które odnoszą się do danego projektu w organizacji oraz numeru zadania, a często także minimalistycznego
streszczenia. Streszczenia stosuje się często, gdyż bywa, że powstaje więcej niż jedna gałąź dla 
zadania - typową sytuacją może być osobne budowanie backendu i frontendu dla tego samego zadania, albo 
budowanie rozwiązania, a później dobudowanie poprawki: `of-235-fix` :)

> **TIP** Poza oficjalną dokumentacją Git na stronie inetrentowej warto jeszcze zapoznać się z 
flagą `--help`, które otwiera pomoc dla danej komendy. Możesz wypróbować komendę np. 
`git checkout --help`. Konsola/terminal w dolnej częsci podpowie ci jak wyjść z pomocy.


```
# kwadrat

# prostokat

# rownoleglobok

# romb

# trapez

# kolo


def trojkat(bok_a, bok_b, bok_c, wysokosc_a):
    obwod = bok_a + bok_b + bok_c
    pole = (bok_a * wysokosc_a) / 2
    return obwod, pole


def kwadrat(bok):
    # TODO
    return 0, 0


def prostokat(bok_a, bok_b):
    # TODO
    return 0, 0


def rownoleglobok(bok_a, bok_b, wysokosc_a):
    # TODO
    return 0, 0


def romb(bok, wysokosc):
    # TODO
    return 0, 0


def trapez(bok_a, bok_b, bok_c, bok_d, wysokosc_a):
    # TODO
    return 0, 0


def kolo(promien):
    # TODO
    return 0, 0


assert trojkat(10, 15, 16, 8) == (41, 40)
assert kwadrat(20) == (80, 400)
assert prostokat(12, 10) == (44, 120)
assert rownoleglobok(6, 5, 2) == (22, 12)
assert romb(10, 5) == (40, 50)
assert trapez(10, 15, 7, 14, 2) == (45, 25)
# TODO dopisz 2 testy dla kola i dla kazdej innej figury po jednym dodatkowym tescie

```
