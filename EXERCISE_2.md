# Ćwiczenia

**Zajęcia zrealizowano w IDE PyCharm[^1].** Zajęcia nie muszą być realizowane z wykorzystaniem IDE, 
jednak jest ono zdecydowanie udogodnieniem. Inne polecane IDE to: Visual Studio Code, PyScripter
(tylko dla Windowsa, nie mam pewności co do jakości wsparcia dla Gita). Student może korzystać z
dowolnego, zależnie od swoich preferencji, jednak bardziej egzotyczne rozwiązania na własną
odpowiedzialność ;)

## Otworzenie projektu w PyCharmie (lub innym IDE)

Wybieramy PyCharma. Jeśli wcześniej nie został otwarty żaden projekt wyświetli się okno, w którym 
użytkownik będzie mógł wybrać utworzenie projektu lub otwarcie istniejącego. Wybieramy otwarcie
istniejącego i wybieramy projekt `example-project` (lub inaczej nazwane repozytorium założone
na potrzeby zajęć).

Jeśli program PyCharm otworzył się z innym projektem należy w menu górnym wybrać **File -> Open**
i wybrać interesujący nas projekt.

Ta operacja powinna wyglądać podobnie dla każdego innego IDE.

Przyjrzyjmy się screenowi poniżej:

![img](/imgs/ex_2_1.png)

1. Widok projektu, plików i zewnętrznych bibliotek.

2. Edycja wybranego pliku, jeśli nie wyświetla się żaden plik można wybrać go z okna 
oznaczonego 1.

3. Panel komend Gita. Niebieska strzałka oznaczała pobranie danych z repozytorium zdalnego
`git pull`, zielony "ptaszek" będzie oznaczał wykonanie commita (operacje: `git add` i `git commit`),
strzałka zielona (najbardziej po prawej) będzie oznaczała `git push`, czyli wypchnięcie zmian
do repozytorium zdalnego. 

4. To sekcja gdzie może być otwarty terminal, wynik wywoływanego skryptu lub inne zależnie 
od wyboru (dolny pasek: `Git`, `Python Packages` itd).

5. Komenda `Run` uruchomienie wybranego skryptu.

## Utworzenie nowego pliku z zadaniem 2

W katalogu `excercise/` utwórz nowy plik `ex_2.py`. 
Drugim przyciskiem myszki w sekcji 1. kliknij w katalog `excercise/` i wybierz opcję `New` ->
`Python File`. Wpisz nazwę pliku `ex_2` (rozszerzenie `.py` zostanie automatycznie dodane).
IDE zapyta, czy plik ma zostać dodany do repozytorium (czyli zostanie pod spodem wykonana 
operacja `git add ex_2.py`). Można wyrazić zgodę lub zrobić to później. Jeśli się wyraziło
plik powinien podświetlić się w panelu 1. w kolorze niebieskim, jeśli nie to podświetli się
na czerwono[^2].

Proces tworzenia pliku w innych IDE powinien wyglądać podobnie i nie powinien stanowić problemu.

Tylko sugestia, nie polecenie:
Utorzenie pliku może dobyć się także przez terminal: `touch ex_2.py` :) (Całość ćwiczeń można 
wykonać w terminalu, edytowanie plików można wykonać np. za pomocą `nano` lub `vim`).

Struktura projektu powinna prezentować się następująco:

```bash
example-project/
├── exercise
│   ├── ex_1.py
│   └── ex_2.py
└── README.md
```

## Zadania do wykonania

1. Wklej kod poniżej do pliku ex_2.py i go zacommituj (instrukcja commitowania z
z poziomu IDE poniżej kodu):

```python
# trojkat

a = 10
b = 20
c = 15
h = 12

obwod = a + b + c
pole = int((h * a) / 2)

print("Obwod trojkata wynosi " + str(obwod) + ", zas pole wynisi " + str(pole) + ".")
```

Aby commitnąć z poziomu PyCharma (podobnie będzie wyglądało także w innych IDE) wybieram
zielony ✔️ ("ptaszek") w prawym górnym rogu lub opcję "Commit" w menu. Z lewej strony powinien
pojawić się panel commita:

![img](/imgs/ide_commit.png)

Tak jak na screenie odhaczamy pliki, które chcemy, aby zostały dodane (`git add`)
i w okienku poniżej wpisujemy wiadomość commita. Na dole panalu mamy opcję `Commit` -
zatwierdzenie commita, `Commit and Push` - zatwierdzenie i wypchnięcie zmian do
repozytorium zdalnego (w naszym przypadku na Githuba). IDE może zapytać do jakiej 
gałęzi (ang. *branch*) ma dostarczyć zmiany, zasugeruje `main` lub `master`. 
Akceptujemy sugestię.

2. **W kolejnej części dla każdej figury powinien być osobny commit!**
Wykonaj analogiczne zadanie dla figur: prostokąt, koło, trapez i romb.
Dla każdej figury powinien występować osobny commit! Kod dla wszystkich
pięciu figur powinien znajdować się w pliku `ex_2.py` ([przykładowy kod do 
uzupełnienia](https://github.com/AleksandraWojewodaUEP/example-project/blob/main/exercise/ex_2.py)). 
Oczekiwany efekt to plik `ex_2.py` drukujący (`print`) informacje na temat 5
różnych figur. Oczekiwana historia commitów to:

![img](/imgs/ex_2_2.png)

3. Ostatnim zadaniem jest zapoznanie z `.gitignore`. `.gitignore` to plik, który zawiera
informacje, które pliki (a także foldery/katalogi[^3]) mają zostać zignorowane. Aktualizowanie
i utrzymywanie `.gitignore` jest powszechną praktyką. Jeśli zadania zostały wykonane w IDE
PyCharm komenda `git status` powinna zwrócić taki status:

![img](/imgs/gitignore_1.png)

Katalog `.idea/` to katalog ukryty (kropka przed nazwą katalogu - konwencja UNIX'owa), 
który zawiera konfiguracje dla PyCharma.
Zarówno katalogu jak i jego zawartości się nie śledzi w repozytorium (czyli się ignoruje :)).
Żeby Git ignorował dany katalog lub pliki trzeba wymienić go w pliku `.gitignore`, z kolei ten 
musi znajdować się katalogu głównym repozytorium, czyli w naszym przypadku w `example-project`.

Do `.gitignore` wpisuje się wszelkiego rodzaju moduły/paczki/skompilowane pliki, których
nie powinno się śledzić. Więcej na ten temat można znaleźć
[tutaj](https://git-scm.com/docs/gitignore).

P.S. W puli pytań zaliczeniowych na pewno pojawi się pytanie o `.gitignore`.

Aby zignorować `.idea/` należy utworzyć plik `.gitignore` w katalogu głównym. Można tego 
dokonać zarówno z poziomu termianla/konsoli, jak i samego IDE. Struktura projektu powinna
wyglądać następująco:

![img](/imgs/gitignore_2.png)

Do pliku należy wpisać:

```
.idea/
```

Jeśli nie korzystasz z PyCharma i nie masz `.idea/` do ignorowania możesz wpisać tam pliki
robocze `vim`, więc plik będzie wyglądać następująco:

```
*.swp
```

Następnie plik dodać `git add .gitignore` i commitnąć `git commit -m "Added .gitignore"`
(można także z poziomu IDE).

Oczekiwana historia commitów na zaliczenie zadania to:

![img](/imgs/ex_2_3.png)

Aby uzyskać punkty z zadania należy do wrzutki na Moodle wrzucić zrzut ekranu z commitami oraz
link do repozytorium.


[^1]: *PyCharm* dostępny jest dla studentów w ramach studenckiej licencji. Aby otrzymać licencje
należy zarejestrować mail z poczty uczelnianej w formularzu, następnie założyć konto z 
wykorzystaniem tego maila. Licencja powinna być widoczna w użytkowniku na panelu strony
internetowej.

[^2]: Nie wszystkie IDE posiadają tą funkcję (funkcjonalność) domyślnie, ale wiele oferuje wraz
z jakimś pluginem. We wszystkich IDE od JetBrain podświetlanie domyślnie wygląda tak samo. 
Więcej o znaczeniu kolorów można przeczytać w oficjalnej dokumentacji.

[^3]: Wszystko w Linuxie jest plikiem, więc powiedzenie pliki lub katalogi niekoniecznie
jest poprawne, bo katalog jest plikiem, acz wydaje mi się, że takie ujęcie jest łatwiejsze
do zrozumienia, nie trzeba o tym wiedzieć. Dla ciekawskich: [Explain "In Linux and UNIX, 
everything is a file"](https://askubuntu.com/questions/1103937/explain-in-linux-and-unix-everything-is-a-file#:~:text=The%20%22Everything%20is%20a%20file,filesystem%20layer%20in%20the%20kernel.)