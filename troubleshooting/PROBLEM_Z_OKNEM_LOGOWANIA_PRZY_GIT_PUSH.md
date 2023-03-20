# "Jak próbuję `git push` to otwiera mi się przeglądarka i muszę się zalogować do Githuba, a dodałem_am klucze ssh"

Dzieję, że tak, bo zamiast SSH zostało wybranne HTTPS. Jeśli korzystają Państwo ze swojej maszyny
na zajęciach to polecam SSH:

![img](/imgs/new_repo_2_1.png)

Jeśli korzystają Państwo z komputera uczelnianego to lepiej będzie HTTPS. 

## Jak to naprawić i nie musieć się logować przez przeglądarkę?

Najszybciej będzie usunąć repozytorium i je sklonować ponownie przy użyciu SSH (screen wyżej).
Jeśli już mają Państwo repo z kodem link do klonowania znajdą Państwo wchodząć do repozytorium 
zdalnego --> Code --> opcja SSH :) Wtedy w wybranym miejscu wpisujemy komendę 
`git clone <wklej ze schowka>` i powinno działać.
