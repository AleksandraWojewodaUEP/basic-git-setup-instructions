# Pierwsze kroki

Operacje wykonywane za pomocą `git` będą wyglądać identycznie niezależnie od tego, czy korzysta się z
Linuxa/MacOS/Windowsa. `Git BASH` będzie (próbował) zachowywywać się tak samo jak terminal Linuxa/MacOS,
więc komendy używane w tutorialu się mapują. Jeśli ktoś z Państwa chcę bardziej zaprzyjaźnić się z
`Git CMD` postaram się w tutorialu zamieścić także instrukcję do CMD :). Jeśli do komendy nie ma dopisku
to znaczy, że powinna działać w każdym emulatorze/termianlu/konsoli.

## Initial commit / Init commit

O pierwszym commicie mówi się, że inicjalizuje projekt i zwykle jego wiadomość (ang. `message`) to 
`Init commit` lub `Inital commit`. Nie jest to obowiązkowe, co więcej na potrzeby zajęc można wiadomości 
commita pisać po polsku (nie rekomenduję, ale nie karam).

Aby zrobić pierwszy commit wchodzimy do repozytorium `cd example-project/` (**Jeśli założone repozytorium
nazywa się inaczej, to proszę stosować swoją nazwę :)**). (Dla przykładu na screenie po lewej CMD, po 
prawej `Git BASH`).

![img](/imgs/cmd_bash.png)

W `Git BASH` widać w prompcie w kolorze niebieskiem `(main)`. Jest to nazwa brancha, na którzym aktualnie jesteśmy.
Jest to także znak, że jesteśmy w repozytorium. CMD nie daje takiej informacji w podstawowej konfiguracji.

Tworzymy nowy plik `README.md`. Można to zrobić na wiele sposobów. Dla ćwiczenia poniżej wykonano instrukcje w terminalu.
Poniżej zamieszono instrukcje dla `vim` (1) i dla `nano` (2). Wykonując 1, nie wykonujemy 2 i odwrotnie. 
Zadanie można wykonać także na własny sposób.

### 1. vim

1. Komendą `vim README.md` tworzymy plik `README.md`[^1] (screen 1) i do niego przechodzimy (screen 2).

![img](/imgs/vim_1.png)

![img](/imgs/vim_2.png)

2. Wchodząc do `vim` jestesmy w trybie `normal`, aby móc pisać do pliku potrzebujemy przejść do trybu `insert`.
Robimy to za pomocą klawisza `i`. W lewym dolnym rogu widać zmianę trybu (patrz screen).

![img](/imgs/vim_3.png)

3. Witamy świat i do pliku wpisujemy tekst `Hello World` lub jako nagłówek H1 `# Hello World` (składnia Markdown[^1]).
Wychodzimy z trybu `insert` za pomocą klawisza `esc`. Aby zapisać i wyjść: `:wq` (`w` od `write`, `q` od `quit`).
Akceptujemy komendę enterem.

![img](/imgs/vim_4.png)

### 2. nano

1. Komendą `nano READNE.md` tworzymy plik `README.md`[^1] (screen 1) i do niego przechodzimy (screen 2).

![img](/imgs/nano_1.png)

![img](/imgs/nano_2.png)

2. Witamy świat i do pliku wpisujemy tekst `Hello World` lub jako nagłówek H1 `# Hello World` (składnia Markdown[^1]).
Plik zapisjemy `crtl + o` (dla Maka: ⌘ + o). Użytkownik dostaje pytanie, czy plik zapisać pod nazwą `README.md`.
Eneterem akceptujemy nazwę.

![img](/imgs/nano_3.png)

3. Wychodzimy z pliku `crtl + x` (dla Maka: ⌘ + x).

### Podrót do części wspólnej

Po zapisaniu pliku i wyjściu z edytora wpisujemy komendę `git status`. (Po lewej `Git CMD`, po prawej `Git BASH`).

![img](/imgs/status_1.png)

Analiza informacji zwrotnej:
```
On branch main --> jesteśmy na gałęzi main

No commit yet --> nadal nie ma żanych commitów

Untracked file: ---> lista nieśledzonych plików
  (use "git add <file>..." to include in what will be committed) --> git nam mówi, że powinniśmy je dodać, aby móc je commitnąć
	README.md

nothing added to commit but untracked files present (use "git add" to track) --> nic nie dodano do commita, ale są nieśledzone
	pliki
```

Nie trudno się domyśleć, że kolejną operacją będzie dodanie pliku: `git add README.md`.

Wykonujemy znowu komendę `git status`.

![img](/imgs/status_2.png)

Analiza informacji zwrotnej:
```
On branch main

No commits yet

Changes to be committed: --> zmiany do commitnięcia
  (use "git rm --cached <file>..." to unstage) --> jeśli to co się znalazło do commitnięcia, nie powinno się tam znaleźć użyj komendy
	new file:   README.md
```

Commitujemy: `git commit -m "Inital commit"`.

Wypychamy do repozytorium zdalnego: `git push`.

Przechodzimy do Githuba, żeby zobaczyć rezultat. Powinien wyglądać tak:

![img](/imgs/init_commit_github_1.png)

Analiza:

![img](/imgs/init_commit_github_2.png)

1. Informacje jak sklonować repozytorium.

2. Ilość commitów.

3. Kto wykonał ostatniego commita.

4. Hash ostatniego commita.

5. Jaka gałądź (ang. branch) jest wyświetlana. 


[^1]: `README.md`- plik tekstowy dołączony do kodu źródłowego w formacie `.md` (Markdown).
Wyświetla się jak swego rodzaju wstęp do projektu na głóœnej stronie repozytorium.
Więcej o formacie Markdown [tutaj](https://www.markdownguide.org/cheat-sheet/).
