# Jak zacząć

## Założenie konta na [Githubie](https://github.com/)

Założenie konta na Githubie nie powinno stanowić wyzwania. 
Można założyć konto na maila prywatnego lub **uczelnianego**, jedyne co
trzeba mieć na uwadze to ewentualne maile-notyfikacje. Jeśli ktoś posiada
już konto na Githubie może podpiąć pod konto dodatkowego maila uczelnianego
lub po prostu pracować na tym koncie bez zmian.

## Instalacja Git

Poniżej przedstawione zostały tutoriale do zainstalowania Gita dla wybranych systemów operacyjnych.
Nie są to jedyne istaniejące sposoby i użytkownik może korzystać z innych możliwych opcji.
Efektem oczekiwanym jest zainstalowany i działający Git.

### Dla systemu Windows

1. Pobranie [Gita dla Windowsa](https://git-scm.com/download/win).
**64-bit Git fo Windows Setup**.

2. Otwarcie pliku jeszcze z przeglądarki lub przejście do pobranego pliku za pomocą Przeglądarki Plików (Explorera).

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
jednak nie jest on wymagany przez prowadzącego, nie jest to jednak rekomendowany wybór,
- łatwiejszym (nieterminalowym) wyborem będzie `Notepad++` lub inny znany użytkownikowi edytor z
listy wybieranej, 
- czymś między `vim` a edytorem w okienku (np. `Notepad++`) będzie `nano`, polecany dla osób,
które chcą edytor w terminalu, ale `vim` im (jeszcze :) ) nie odpowiada. 

Prowadzący w miarę mozliwości czasowych na zajęciach będzie wspierał wszystkie 3 opcję w przypadku 
problemów, które mogą pojawić się na zajęciach.

P.S. Uprzejmie przypominam, że to nie jest wybór na całe życie. Zawsze można zmienić domyślny edytor :).

![Alt text](/imgs/git_vim_4.png)

7. Wybór nazwy głównej gałeźni (z ang. `branch`). Jakiś czas temu dokonano przejścia z nazwy `master`
na nazwę `main`. Wybór należy do użytkownika, jednak zgodnie z głównym nurtem będzie wybranie `main`. 
Na zajeciach przykłady będą wykorzystywały `main` jako główną gałąź.

![Alt text](/imgs/git_main_5.png)

8. `Adjusting your PATH environment` 

- na zajęciach prezentowane będą opcje, które wymagają także uniksowych narzędzi (tak jak na screenie),
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
oraz ich wykorzystanie w praktyce. Użytkownik może przejść przez zajęcia wykorzystując dowolne ustawienie.

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
Sposób instalacji dla innych dystrybucji dostępny w oficjalnej 
dokumentacji Gita.

Sprawdzenie, czy Git się zainstalował:

```
git --version
```

Przykładowy oczekiwany rezultat:

![Alt text](/imgs/git_linux_v_1.png)

(1:0 dla Linuxa)

### Dla macOS za pomocą `homebrew`

Instalacja [Homebrew](https://brew.sh/) (komendę wklejamy do terminala).

Instalacja Git za pomocą brew (homebrew):

```
brew install git
```

Sprawdzenie, czy instalacja się powiodła:

```
git --version
```

Oczekiwanym rezultatem jest informacja o wersji oprogramowania Git na danej maszynie
(podobnie jak dla Linuxa).

#### Rozwiązywanie problemów

Lista problemów z zajęć:

1. `zsh: command not found: brew` --> 
[stackoverflow](https://stackoverflow.com/questions/36657321/after-installing-homebrew-i-get-zsh-command-not-found-brew).

### Podsumowanie

Więcej dostępnych informacji o pobieraniu Gita jest dostępnych na oficjalnej 
[stronie internetowej Gita](https://git-scm.com/downloads).

## Konfigracji Gita lokalnie

Dla wszystkich systemów operacyjnych operacja ta powinna wyglądać tak samo.
W Windowsie wybieramy `Git BASH` lub `Git CMD`. W Linuxie/Macu terminal.

Ustawienie nazwy i maila użytkownika (komendy wpisujemy osobno, najpierw jedną, potem drugą) 
(rozwiązanie ewentualnych problemów poniżej w sekcje "Rozwiązanie problemów"):

```
git config --global user.name "Imię Nazwisko"
git config --global user.email "niu@student.ue.poznan.pl"
```

W odpowiednich miejscach wpisz swoje dane. Przełącznik `--global` nie jest wymagany, 
szczególnie w przypadku wykorzystywania jednej maszyny dla wielu użytkowników Gita.
Przykładowo użytkownik uczelniany, prywatny i służbowy.
Można stworzyć konfigurację, która zezwala na odseparowanie od siebie kont Gitowych[^2].

W przypadku ewentualnego błędu/literówki polecenie można wykonać ponownie.

> **_Tip:_**  Będąc w terminalu (lub emulatorze terminala) strzałka w górę pozwala na przywołanie komend.
Szczególnie przydatne, jeśli chcemy danej komendy użyć dwa razy lub komendy są od siebie nieznacznie różne, 
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
- w trybie edycji: komenda `nano .gitconfig` (wyjście z programu `ctrl + x`) lub `vim .gitconfig` 
	- vim uruchomi się w trybie wyświetlania, 
	- aby edytować wybierz `i`, 
	- aby wyjść z tryby edycji `esc`, 
	- aby wyjść z programu: wyjdź z trybu edycji `esc` następnie:
		- aby wyjść z niemodyfikowanego pliku `:q` (dwukropek q), 
		- aby wyjść z modyfikowanego, ale bez zapisu `:q!` (dwukropek q wykrzyknik), 
		- aby zapisać zmiany i wyjść z vima `:wq` (dwukropek w q).

> **_Tip:_** Wpisz do terminala `cat .gitc` i wciśniej tab. Nazwa pliku powinna samodzielnie się uzupełnić.
Tab uzupełnia komendy/nazwy plików jeśli jest to możliwe.

![Alt text](/imgs/git_config_2.png)

### Rozwiązanie problemów

Cześć osób znalazła się w takim położeniu:

![Alt text](/imgs/problem_1.png)

Aby z niego wyjść, można wyjść z komendy bez jej wykonywania za pomocą klawiszy `ctrl + c` (polecam kliknąć 
kilka razy).

## Wygenerowanie klucza SSH

Klucz SSH będzie potrzebny do połączenia lokalnego setupu z kontem na Githubie.
Uwierzytelnianie może odbyć się na wiele sposobów. Za pomocą tokena, klucza SSH, czy 
klucza GPG. Do tego jeszcze kwestia szyforwania. Na zajęciach dozwolona jest dowolna 
metoda, ale dla początkujących tutorial będzie przechodził przez proces ustawiania
uwierzetylniania za pomocą klucza SSH. 

Do wygenerowania klucza SSH służy komenda `ssh-keygen`. Na terminalu powinno wyświetlić się pytanie
o nazwę plików zawierających parę klucz publiczy i prywatny. Enter pozowli na wybranie opcji domyślnej.
Jeśli użytkownik posiada już klucz o nazwie domyślnej można nadpisać plik lub użyć istniejącego klucza, 
lub wybrać inną nazwę dla pary. 
**Ten sam klucz SSH nie może zostać wykorzystany do dwóch kont na Githubie.** 
(Konfiguracja wielu użytkowników dla jednej maszyny [^2]).
Przez kolejne opcje także można przejść Enterem. Operacja zakończona powodzeniem wyświetli `randomart image`.

![Alt text](/imgs/ssh_keygen.png)

(Czy można podzielić się swoim `randomart image`?[^4])

Klucze trzymane są w katalogu ukrytym[^3] `.ssh`. Można sprawdzić ich obecność przechodząc do katalogu 
`.ssh`, który znajduje się w katalogu domowym (komenda sprawdzająca do katalogu domowego: `cd`).
W katalogu `.ssh` wykonaj komendą `ls` (lub `ls -l` - wyświetl listę ze szczegółami,
wtedy każdy plik jest w osobnej linii). W katalogu powinny znajdować się pliki `id_rsa` i `id_rsa.pub`.
Pierwszy to klucz prywatny - tego nigdzie nie publikujemy/dodajemy/dzielimy się. Drugi plik to klucz
publiczny, to go będziemy dodawać do konta na Githubie.

![Alt text](/imgs/ssh_keys_check.png)

> **_Tip:_** Na screenie jak przeszłam z katalogu domowego do katalogu `.ssh`, 
po operacji przejścia widać jak zmianiła się nazwa katalogu w znaku zachęty (źółta część). 
Znak zachęty w ustawieniach domyślnych Git BASH dla Windowsa będzie wyświetlał katalog
w którym obecnie się znajdujemy. Znak zachęty może wyglądać różnie na wszystkich systemach, 
jest w pełni modyfikowalny.
Bardzo częto jednak domyślnie jest tego samego koloru co teskt wpisywany przez użytkownika,
jednak jak wcześniej wspomniano można to zmodyfikować[^2]. 

## Połączenie konta na Githubie z lokalnym setupem

1. Wejście w ustawienia (`Settings`) z paska wybieranego w prawym górnym roku na UI Githuba.

![Alt text](/imgs/github_1.png)

2. Wejście w `SSH and GPG keys` w lewym pasku i wybranie `New SSH key`

![Alt text](/imgs/github_2.png)

3. **Windows** Przejdź do przeszukiwacza plików (ang. `Files explorer`) i przejdź do folderu `.ssh`.
W folderze powinny znajdować się klucze `id_rsa` i `id_rsa.pub`. **UWAGA! W nowszych Windowsach
w explorerze plików nie widać rozszerzenia klucza publicznego, można go poznać po ikonce z małym
`P`.** Najedź myszką na klucz publiczny i kliknij drugim przyciskiem myszki. `Otwórz za pomocą...`
i wybierz edytor tekstu, np. Notatnik. Skopiuj zawartość (crtl + A, ctrl + C) - **nie kopiuj ręcznie,
istnieje wysokie prawdopodbieństwo, że któryś znak zostanie pominięty.**

![Alt text](/imgs/github_3.png)

![Alt text](/imgs/github_4.png)

**MacOS** Skopiowanie klucza może odbyć się przez terminal. 
Przechodzimy do katalogu z kluczami `cd ~/.ssh/`.
Printowanie na standardowe wyjście odbywa się za pomocą komendy `cat id_rsa.pub`.
Aby skopiować do schowka wystarczy wyjście z poprzedniej komendy podać jako wejście
do kolejnej `pbcody` za pomocą `|`. Cała komenda będzie prezentować się tak: 
`cat id_rsa.pub | pbcopy`. Klucz wklej do formularza na Githubie za pomocą ⌘ + v.

**Linux**
Przechodzimy do katalogu z kluczami `cd ~/.ssh/`.
Printowanie na standardowe wyjście odbywa się za pomocą komendy `cat id_rsa.pub`.
Aby skopiować do schowka wystarczy wyjście z poprzedniej komendy podać jako wejście
do kolejnej `xclip -selection clipboard` za pomocą `|`. 
Cała komenda będzie prezentować się tak: 
`cat id_rsa.pub | xclip -selection clipboard`. 
Klucz wklej do formularza na Githubie za pomocą crtl + v.

4. Nadaj kluczowi nazwę. Nazwa powinna wskazywać na maszynę, z której pochodzi klucz. W moim przypadku
koncepcja nazywania kluczy to `jumper_<marka_laptopa>_<dopisek>`, jednak sposób nazwania klucza zależy
od użytkonika i nie musi mapować się do sugestii z podpunktu lub z screena. 
Do formularza w polu `Key` wklej swój klucz publiczny. 

![Alt text](imgs/github_5.png)

Klucz powinien być widoczny w zakładcze `SSH keys`.

## Stworzenie repozytorium

1. Przejdź do rozwijanego menu w prawym górnym rogu przy ikonce użytkonika i wejdź w zakładkę
`Your Repositories`.

![Alt text](/imgs/new_repo_1.png)

2. Nadaj nazwę repozytorium, wybierz opcję `Public`, resztę opcji pozostaw pustych.

![Alt text](/imgs/new_repo_2.png)

3. Po zatwierdzeniu nowego repozytorium na ekranie powinna znaleźć się informacja o `Quik setup`.
**Z niebieskiego pola wybierz opcję `SSH` (patrz screen)**. Skopiuj link do repozytorium z pola.

![Alt text](/imgs/new_repo_2_1.png)

4. Zamknij okno terminala i otwórz nowe.
Przejdź do terminala/konsoli/emulatora. Przejdź do folderu/katalogu, w którym
ma znajdować się repozytorium. 
**UWAGA! Nie umieszczaj repo w `.ssh/`!**
Sklonuj repozytorium `git clone <link z niebieskiego pola>` 
Podczas pobierania repozytorium może pojawić się zapytanie o nawiązanie połaczenia z nowym hostem. 
Jeśli chcemy pobrać repo, trzeba się na nie zgodzić wpisując `yes`[^5] (patrz screen). 
Komendą `ls` można zobaczyć, czy repozytorium zostało poprawnie sklonowane.

![Ale text](/imgs/new_repo_3.png)

Gratulacje! Twoje repo jest na Twojej maszynie.

[^1]: *GNU General Public License* jest wirusową licencją open-sourcową, która zobowiązuje
dostawców oprogramowania do dostarczenia kodu źródłowego oprogramowania użytkownikowi. 
[^2]: Zagadnienie dla chętnych realizowane indywidialnie na dyżurach lub po wcześniejszym umówieniu
się z prowadzącym.
[^3]: Ukryty plik (lub katalog) to plik, który domyślnie nie jest wyświetlany. 
Nazwa pliku zawiera na przedzie `.`. Wpisz komendę `ls` (wylistuj pliki) w terminal, następnie wpisz
komendę `ls -a` (wylistuj wszystkie pliki). W przypadku pierwszego ukryte pliki nie zostaną wyświetlone.
[^4]: [Link](https://superuser.com/questions/1621434/can-you-publish-your-ssh-key-randomart)
[^5]: Zgadzając się na pobranie kodu wykonywalnego powinniśmy być świadomi, że na daną maszynę 
zostanie pobrany kod wykonywalny. Jeśli nie ufamy autrom kodu/nie znamy ich/mamy podejrzenia
co do działania kody, że są one szkodliwe dla naszego komputera, nie zezwalajmy na takie połączenie.
Proces można zakończyć negatywnie za pomocą `no` lub `ctrl + c` (zakończ komendę).
