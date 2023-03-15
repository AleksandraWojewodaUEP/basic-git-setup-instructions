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

1. Utwórz folder/katalog: `mkdir exercise/`.

2. Przejdź do utowrzonego folderu/katalogu: `cd exercise/`.

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

