# Ćwiczenia

Poniżej zamieszono parę podstawowych operacji z gitem. Ćwiczenia te powinny także stanowić
wspracie w dalszej bardziej samodzielnej pracy w kolejnych tygodniach zajęć.

Zachęcam go wykonania ich z poziomu terminala. Później wsparciem będzie aplikacja okienkowa i
IDE, jednak używanie terminala pozwoli lepiej zapoznać się z poleceniami git i lepiej zrozumieć
idee systemu kontrolii wersji.

Jeśli ktoś potrzebuje motywacji zewnętrznej: **wykonanie zadań z poziomu terminala pozwoli
lepiej przyswoić materiał, który będzie obowiązywał na końcowym quizie :)**.

Aby wykonać zadania potrzebny będzie zaintsalowany Python.

Ćwiczenia można wykonać z wykorzystaniem repozytorium, które zostało wcześniej założone, jednak
jeśli ktoś chciałby wykonać ćwiczenia w innym repozytorium - nie ma problemu.

## Ćwiczenia samodzielne

### 1. Podstawowe operacje w repozytorium lokalnym i ich cofanie

1. Utwórz folder/katalog: `mkdir exercise/`.

2. Przejdź do utworzonego folderu/katalogu: `cd exercise/`.

3. Utwórz nowy plik: `touch ex_1.py`. (Plik powinien się wyświetlać w liście plików, można sprawdzić
za pomocą `ls` lub wejść w Explorer plików i sprawdzić, czy plik pojawił się w folderze repozytorium).

4. Otworzyć plik w trybie edycji.

- może być w Visual Studio Code, może być PyScripter, może buć PyCharm,

- może być terminalowy edytor plików: `vim`, `nano` lub dowolny wybrany przez użytkownika.

5. Przekleić/przepisać kod poniżej:

```
def hello(a: str) -> str:
    # TODO
    return "Hello"


print("Example")
print(hello("Ola"))

assert hello("Ola") == "Hello Ola"
assert hello("Zuzia") == "Hello Zuzia"

print("Zadanie zrobione")
```

6. Zapisz plik.

7. Dodaj plik do stagingu `git add ex_1.py`.

8. Zacommituj zmiany `git commit -m "Added first task"`, aby amina została zapisana w repozytorium 
lokalnym.

9. Cofnij commita z repozytorium lokalnego, ale nie usuwaj zmian `git reset --soft HEAD^`

10. Cofnij zmiany ze staging: `git restore --staged ex_1.py`

11. Powtórz krok 7 i 8.

12. **UWAGA! Jeśli znajdujesz się w folderze/katalogu `exercise/`, który zaraz przestanie istanieć, należy
się z niego wrócić do `example-project` (katalogu głównego repo), pozwoli na to komenda `cd ..` 
(tak, tam są dwie kropki).**
Cofnij commit z repozytorium lokalnego razem ze zmianami, które wprowadził: `git reset --hard HEAD^`.

13. Powtórz kroki 1-7.

14. Commitnij, ale w wiadomości popełnij literówkę, np. `git commit -m "Added first taks"`

15. Popraw literówkę w wiadomości `git commit --amend`. Komenda przeniesie cię do domyślnego edytora
tesktu. Edytuj wiadomość commita w edytorze i zapisz. Wiadomość commita automatycznie się 
nadpisze.

16. Wypchnij commita za pomocą komendy: `git push`. Zmiany powinny być widoczne na rpozytorium zdalnym 
na Githubie.




