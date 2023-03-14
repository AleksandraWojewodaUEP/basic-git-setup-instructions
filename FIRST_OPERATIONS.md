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

![Alt text](/imgs/cmd_bash.png)

W `Git BASH` widać w prompcie w kolorze niebieskiem `(main)`. Jest to nazwa brancha, na którzym aktualnie jesteśmy.
Jest to także znak, że jesteśmy w repozytorium. CMD nie daje takiej informacji w podstawowej konfiguracji.

Tworzymy nowy plik `README.md`. Można to zrobić na wiele sposobów. Dla ćwiczenia poniżej wykonano instrukcje w terminalu.
Poniżej zamieszono instrukcje dla `vim` (1) i dla `nano` (2). Wykonując 1, nie wykonujemy 2 i odwrotnie. 
Zadanie można wykonać także na własny sposób.

### 1. **vim** 

1. Komendą `vim README.md` tworzymy plik `README.md`[^1] (screen 1) i do niego przechodzimy (screen 2).



