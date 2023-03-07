# Minimalistyczna instrukcja jak się zasetupować na zajęcia

## Założenie konta na [Githubie](https://github.com/)

Założenie konta nie powinno stanowić dla Państwa problemu :).

## Instalacja Git

### Dla systemu Windows

1. Pobranie [Gita dla Windowsa](https://git-scm.com/download/win).
**64-bit Git fo Windows Setup**.

2. Otwarcie pliku jeszcze z przeglądarki lub przejście do pobranego pliku za pomocą przeglądarki plików.

![Alt text](/imgs/git_in_downloads.png "Optional titl")

3. Uruchomienie pliku instalacyjnego. Wybranie opcji `Run`.

![Alt text](/imgs/git_installer_1.png)

4. Zaakceptowanie licencji GNU GPL[^1]. Wybranie opcji `Next`.

![Alt text](/imgs/git_gnu_gpl_2.png)

5. `Select Components`. Zalecam wybranie wskazanych (domyślnych) opcji.

![Alt text](/imgs/git_select_components_3.png)

6. Wybór domyślnego edytora tekstu. 
Wybór ten bezpośrednio zależy od preferencji użytkownika.

- na zajęciach przez prowadzącego będzie wykorzystany głównie `vim` (wybór jak na screenie poniżej),
jednak nie jest on wymagany przez prowadzącego,
- łatwiejszym (nieterminalowym) wyborem będzie `Notepad++` lub inny znany użytkownikowi edytor z
listy wybieranej, 
- czymś między `vim` a edytorem w okienku (np. `Notepad++`) będzie `nano`, polecany dla osób,
które chcą edytor w terminalu, ale `vim` im (jeszcze :) ) nie odpowiada. 

Prowadzący w miarę mozliwości czasowych na zajęciach będzie wspierał wszystkie 3 opcję w przypadku 
problemów, które mogą pojawić się na zajęciach.

P.S. Uprzejmie przypominam, że to nie jest wybór na całe życie. Zawsze można zmienić domyślny edytor :).

![Alt text](/imgs/git_vim_4.png)

"The only gym where it's possible to quit"
![Alt text](/imgs/vim_meme.png "Znalezione w czeluściach r/linuxmeme")

7. Wybór nazwy głównej gałeźni (z ang. `branch`). Jakiś czas temu dokonano przejścia z nazwy `master`
na nazwę `main`. Wybór należy do użytkownika, jednak zgodnie z głównym nurtem będzie wybranie `main`. 
Na zajeciach przykłady będą wykorzystywały `main` jako główną gałąź.

![Alt text](/imgs/git_main_5.png)

8. `Adjusting your PATH environment` 

- na zajęciach prezentowane będą opcje które wymagają także uniksowych narzędzi (tak jak na screenie),
- pozostałe opcje pozwolą przejść przez ćwiczenia na zajęciach, także opcja wybrana na screenie nie jest
opcją obowiązkową,
- opcja `Use Git from Bash only` jest szczególnie polecana, jeśli użytkownik chce nie ingerować w `PATH`.

![Alt text](/imgs/git_path_6.png)

9. `Choosing the SSH executable`

![Alt text](/imgs/git_openssh_7.png)

Użytkownik może zdecydować się na opcję o wyborze zewnętrzego `OpenSSH`.

10. `Choosing HTTPS transport backend`

![Alt text](/imgs/git_https_8.png)

11. `Configuring the line ending conversions`

![Alt text](/imgs/git_line_ending_9.png)

12. `Configuring the terminal emulator to use with Git Bash`

![Alt text](/imgs/git_terminal_10.png)

13. `Choose the default behavior of git pull`

Pytanie z odpowiedzią typu "to zależy". W pierwszej fazie polecam opcję domyślą (jak na screenie).
Wraz ze wzrostem umiejętności korzystania z Gita łatwiejsze będzie zrozumienie pozostałych dostępnych opcji
oraz ich wykorzystanie w praktyce. Użytkownik może przejść przez zajęcia wykorzystując dowlne ustawienie.

![Alt text](/imgs/git_pull_11.png)

14. `Choose a credential helper`

![Alt text](/imgs/git_c_helper_12.png)


[^1] *GNU General Public License* jest wirusową licencją open-sourcową, która zobowiązuje
dostawców oprogramowania do dostarczenia kodu źródłowego oprogramowania użytkownikowi. 

