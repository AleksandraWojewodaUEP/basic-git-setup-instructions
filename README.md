# Minimalistyczna instrukcja jak się zasetupować na zajęcia

## Założenie konta na [Githubie](https://github.com/)

Założenie konta nie powinno stanowić dla Państwa problemu :).

## Instalacja Git

Poniżej przedstawione zostały tutoriale do zainstalowania Gita dla wybranych systemów operacyjnych.
Nie są to jedyne istaniejące sposoby i użytkownik może korzystać z innych możliwych opcji.
Efektem oczekiwanym jest zainstalowany i działający Git.

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

15. `Configuring extra options` i `Configuration expermiental option`

Generalnie dodatkowe opcje zależą od preferencji użytkownika, dla potrzeb zajęć można przeklikać opcje 
domyślne (screeny poniżej). Użytkownik może dobrać dodatkowe konfiguracje według własnego uznania.

![Alt text](/imgs/git_extra_opt_13.png)

![Alt text](/imgs/git_experimental.png)

16. Następnie powinien pojawić się pasek instalacji, a potwierdzeniem zainstalowania będzie:

![Alt text](/imgs/git_end_15.png)

#### Podsumowanie

Gratulację! Na Twoim Windowsie jest Git.

### Dla systemu Ubuntu/Debian

Nieobowiązkowe, ale zalecane (zaktualizowanie paczek):

```
sudo apt update
sudo apt upgrade
```

Instalacja Gita:

```
sudo apt install git
```

Dla innych linuksowych dystrybucji jest równie łatwo.

Sprawdzenie, czy Git się zainstalował:

```
git --version
```

Przykładowy oczekiwany rezultat:

![Alt text](/imgs/git_linux_v_1.png)

(1:0 dla Linuxa)

### Dla macOS za pomocą `homebrew`

Instalacja:

```
brew install git
```

Sprawdzenie, czy instalacja się powiodła:

```
git --version
```

Oczekiwanym rezulattem jest informacja o wersji oporgramowania Git na danej maszynie
(podobnie jak dla Linuxa).

### Podsumowanie

Więcej dostępnych informacji o pobieraniu Gita jest dostępnych na oficjalnej 
[stronie internetowej Gita](https://git-scm.com/downloads).

## Konfigracji Gita lokalnie

Dla wszystkich systemów operacyjnych operacja ta powinna wyglądać tak samo.
W Windowsie wybieramy `Git BASH`. W Linuxie/Macu terminal.

Ustawienie nazwy i maila użytkownika:

```
git config --global user.name "Imię Nazwisko"
git config --global user.email "niu@ue.poznan.pl"
```

W odpowiednich miejscach wpisz swoje dane. Przełącznik `--global` nie jest wymagany, 
szczególnie w przypadku wykorzystywania jednej maszyny dla wielu użyrkoników Gita.
Przykładowo użytkownik uczelniany, prywatny i służbowy.
Można stworzyć konfigurację, która zezwala na odseparowanie od siebie kont Gitowych[^2].

W przypadku ewentualnego błędu/literówki polecenie można wykonac ponownie.

> **_Tip:_**  Będąc w terminalu (lub emulatorze terminala) strzałka w górę pozwala na przywołanie komend.
Szczególnie przydatne jeśli chcemy danej komendy użyć dwa razy lub komendy są od siebie nieznacznie róźne, 
więc "nie opłaca" się jej przepisywać. 

![Alt text](/imgs/git_config_1.png)

Aby sprawdzić wprowadzone dane można w katalogu użytkownika sprawdzić plik `.gitconfig`.

**Uwaga! Następujące komendy są uniksowe, więc mogą nie działać dla Git CMD, ale będą dla Git BASH**

W terminalu wpisz `pwd`. Komenda ta wyświetla ścieżkę dostępu do bieżącego katalogu. 
Dla Windowsa powinna być `/c/User/<nazwa użytkownika>` dla Linuxa `/home/<nazwa użytkownika>`.
Jeśli nie jesteś w tym katalogu komenda `cd` sprowadzi cię do katalogu domowego (czyli katalogu użytkownika).
W katalogu domowym jest ukryty[^3] plik `.gitconfig`. 
Do pliku można zajrzeć z poziomu terminala np.:

- jedynie podgląd: komenda `cat .gitconfig` (komenda `cat` wyświetla zawartość danego pliku),
- w trybie edycji: komenda `nano .gitconfig` (wyjście z programu ctrl + x) lub `vim .gitconfig` (vim w trybie
wyświetlania, aby edytować wybierz i, aby wyjść z tryby edycji esc, aby wyść z programu wyjdź z trybu edycji
esc, aby wyjść z niemodyfikowanego pliku 
:q, z modyfikowanego, ale bez zapisu :q!, zapisz i wyjdź :wq),

> **_Tip:_** Wpisz do terminala `cat .gitc` i wciśniej tab. Nazwa pliku powinna samodzielnie się uzupełnić.
Tab uzupełnia komendy/nazwy plików jeśli jest to możliwe.

![Alt text](/imgs/git_config_2.png)

## Połączenie konta na Githubie z lokalnym setupem



[^1]: *GNU General Public License* jest wirusową licencją open-sourcową, która zobowiązuje
dostawców oprogramowania do dostarczenia kodu źródłowego oprogramowania użytkownikowi. 
[^2]: Zagadnienie dla chętnych realizowane indywidialnie na dyżurach lub po wcześniejszym umówieniu
się z prowadzącym.
[^3]: Ukryty plik (lub katalog) to plik, który domyślnie nie jest wyświetlany. 
Nazwa pliku zawiera na przedzie `.`. Wpisz komendę `ls` (wylistuj pliki) w terminal, następnie wpisz
komendę `ls -a` (wylistuj wszystkie pliki). W przypadku pierwszego ukryte pliki nie zostaną wyświetlone.
