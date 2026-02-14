---
title: 2026-02-14-Zaczynam używaćGithuba
layout: post
categories: Github
---

# Zaczynam dzisiaj przygodę z git. 

Ponieważ nie jestem zaawansowanym użytkownikiem i programistą notuję sobie w plikach markdown poszczególne etapy konfiguracji i pracy.
Jako edytora plików markdown używam programu GhostWriter chociaż równie dobrze mógłbym korzystać z każdego innego w konsoli np. nano lub Vim.
Na końcu tego pliku wskażę linki do blogów i poradników z których korzystałem.

Używam laptopa pod kontrolą systemu linux Mint 21.3.
Korzystając z konsoli utworzyłem w katalogu domowym katalog Devel a wewnątrz niego katalogi "blog_markdown" i "git_prj".
W katalogu "blog_markdown" będę umieszczał notatki w formacie markdown RR-MM-DD-Tytuł.md natomiast w katalogu "git_prj" umieszczę repozytoria github-a.

```	console
user@host~$ mkdir -p Devel Devel/blog_markdown Devel/git_prj
```

Po utworzeniu katalogu ~/Devel/git_prj należy do niego przejść używając polecenie "cd":

``` console
user@host~$ cd ~/Devel/git_prj 
```

Okazało się że do korzystania z chmury github konieczne jest zainstalowanie programu gh ponieważ polecenie git nie obsługuje autentykacji.

``` console
user@host~/Devel/git_prj$ git clone https://github.com/user/sagittarius.one
Klonowanie do „sagittarius.one”...
Username for 'https://github.com': 
Password for 'https://cinek75@github.com': 
remote: Invalid username or token. Password authentication is not supported for Git operations.
fatal: Uwierzytelnienie nie powiodło się dla „https://github.com/user/sagittarius.one/”
```


``` console 
user@host:~/devel/git_prj$ sudo apt install gh
Czytanie list pakietów... Gotowe
Budowanie drzewa zależności... Gotowe
Odczyt informacji o stanie... Gotowe   
Następujące pakiety zostały zainstalowane automatycznie i nie są już więcej wymagane:
  android-libf2fs-utils castxml catch2 cura-engine fdm-materials
  fonts-open-sans lame lib32asan5 lib32asan6 lib32atomic1 lib32gcc-11-dev
  lib32gcc-9-dev lib32gcc-s1 lib32gomp1 lib32itm1 lib32ncurses6 lib32ncursesw6
  lib32quadmath0 lib32stdc++6 lib32tinfo6 lib32ubsan1 libad9361-0 libarcus3
  libboost-atomic1.74.0 libboost-date-time1.74.0 libboost-system1.74.0
  libc6-x32 libclamav9 libcrypt-dev:i386 libeigen3-dev libf2fs-format4
  libf2fs5 libffi-dev libfmt-dev libfmt8 libgfortran-11-dev libgfortran-8-dev
  libgfortran-9-dev libglib2.0-dev-bin libgnuradio-analog3.10.1
  libgnuradio-audio3.10.1 libgnuradio-blocks3.10.1 libgnuradio-channels3.10.1
  libgnuradio-digital3.10.1 libgnuradio-dtv3.10.1 libgnuradio-fec3.10.1
  libgnuradio-fft3.10.1 libgnuradio-filter3.10.1 libgnuradio-iio3.10.1
  libgnuradio-network3.10.1 libgnuradio-pdu3.10.1 libgnuradio-pmt3.10.1
  libgnuradio-qtgui3.10.1 libgnuradio-runtime3.10.1 libgnuradio-soapy3.10.1
  libgnuradio-trellis3.10.1 libgnuradio-uhd3.10.1 libgnuradio-video-sdl3.10.1
  libgnuradio-vocoder3.10.1 libgnuradio-wavelet3.10.1 libgnuradio-zeromq3.10.1
  libiio0 libmodule-pluggable-perl libnsl-dev:i386 libodbccr2 libodbccr2:i386
  libopenblas-dev libopenblas-pthread-dev libopenexr24 libpcre2-posix3
  libpcre32-3 libpcrecpp0v5 libsavitar0 libsepol-dev libspdlog-dev libspdlog1
  libtfm1 libthrift-0.16.0 libthrift-dev libtirpc-dev:i386 libu2f-udev
  libvalacodegen-0.56-0 libx32asan5 libx32asan6 libx32atomic1 libx32gcc-11-dev
  libx32gcc-9-dev libx32gcc-s1 libx32gomp1 libx32itm1 libx32quadmath0
  libx32stdc++6 libx32ubsan1 libxsimd-dev mint-backgrounds-vanessa
  pybind11-dev python3-arcus python3-beniget python3-charon python3-flask
  python3-gast python3-itsdangerous python3-pychromecast python3-pygccxml
  python3-pynest2d python3-pyqt5.qwt python3-python-utils python3-savitar
  python3-sentry-sdk python3-shapely python3-stl python3-thrift soapysdr-tools
  sox valac-0.56-vapi valac-bin vorbis-tools wx3.0-headers
Aby je usunąć należy użyć "sudo apt autoremove".
Zostaną zainstalowane następujące NOWE pakiety:
  gh
0 aktualizowanych, 1 nowo instalowanych, 0 usuwanych i 0 nieaktualizowanych.
Konieczne pobranie 6 242 kB archiwów.
Po tej operacji zostanie dodatkowo użyte 33,7 MB miejsca na dysku.
Pobieranie:1 http://ftp.agh.edu.pl/ubuntu jammy/universe amd64 gh amd64 2.4.0+dfsg1-2 [6 242 kB]
Pobrano 6 242 kB w 3s (2 013 kB/s)  
Wybieranie wcześniej niewybranego pakietu gh.
(Odczytywanie bazy danych ... 861169 plików i katalogów obecnie zainstalowanych.
)
Przygotowywanie do rozpakowania pakietu .../gh_2.4.0+dfsg1-2_amd64.deb ...
Rozpakowywanie pakietu gh (2.4.0+dfsg1-2) ...
Konfigurowanie pakietu gh (2.4.0+dfsg1-2) ...
Przetwarzanie wyzwalacz pakietu man-db (2.10.2-1)...
```

No to ponawiam próbę dostępu do github-a tym razem za pomocą "gh".

``` console
user@host:~/devel/git_prj$ gh repo clone Cinek75/sagittarius.one
Welcome to GitHub CLI!

To authenticate, please run `gh auth login`.
user@host:~/Devel/git_prj$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Paste an authentication token
Tip: you can generate a Personal Access Token here https://github.com/settings/tokens
The minimum required scopes are 'repo', 'read:org', 'workflow'.
? Paste your authentication token: 
```

i tutaj przerwałem wykonywanie programu kombinacją klawiszy ctrl + c.
Kolejne podejście i tym razem wskazujemy na autentykację za pośrednictwem przeglądarki i protokołu HTTPS. W konsoli zostanie wygenerowany klucz, który wkleimy w okno przeglądarki i potwierdzimy, że zgadzamy się na dostęp klienta git do repozytorium.

``` console
user@host:~/Devel/git_prj$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferstred protocol for Git operations? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: F238-D3DE
- Press Enter to open github.com in your browser... 
Otwieram w istniejącej sesji przeglądarki.
✓ Authentication complete. Press Enter to continue...

- gh config set -h github.com git_protocol https
✓ Configured git protocol
✓ Logged in as Cinek75
```

Teraz już możemy wydać polecenie:
``` console
user@host:~/Devel/git_prj$ gh repo clone Cinek75/sagittarius.one
Klonowanie do „sagittarius.one”...
remote: Enumerating objects: 60, done.
remote: Counting objects: 100% (60/60), done.
remote: Compressing objects: 100% (55/55), done.
remote: Total 60 (delta 25), reused 12 (delta 2), pack-reused 0 (from 0)
Pobieranie obiektów: 100% (60/60), 17.59 KiB | 1.26 MiB/s, gotowe.
Rozwiązywanie delt: 100% (25/25), gotowe.
```
No i proszę w katalogu ~/Devel/git_prj w podkatalogu sagittarius.one zostało umieszczone moje repozytorium.

``` console
user@host:~/Devel/git_prj$ ls
sagittarius.one

```
#### Przydatne Linki:
1. [mmcschool - markdown-kompletny-poradnik-dla-poczatkujacych](
https://mmcschool.pl/frontend/markdown-kompletny-poradnik-dla-poczatkujacych/9348/ "mmcschool - markdown-kompletny-poradnik-dla-poczatkujacych")
2. [zenbox - jak-dziala-git-przewodnik-dla-poczatkujacych](
https://zenbox.pl/blog/jak-dziala-git-przewodnik-dla-poczatkujacych/ "zenbox - jak-dziala-git-przewodnik-dla-poczatkujacych")
3. [ghostwriter.kde.org/documentation](
https://ghostwriter.kde.org/documentation/ "ghostwriter.kde.org/documentation")
