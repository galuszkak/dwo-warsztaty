Python Open Source
==================

## Jak programować? Jak być Pythonistą/Pythonistką? ##

### Zen of Python ###

Beautiful is better than ugly.

Explicit is better than implicit.

Simple is better than complex.

Complex is better than complicated.

Flat is better than nested.

Sparse is better than dense.

Readability counts.

Special cases aren't special enough to break the rules.

Although practicality beats purity.

Errors should never pass silently.

Unless explicitly silenced.

In the face of ambiguity, refuse the temptation to guess.

There should be one-- and preferably only one --obvious way to do it.

Although that way may not be obvious at first unless you're Dutch.

Now is better than never.

Although never is often better than *right* now.

If the implementation is hard to explain, it's a bad idea.

If the implementation is easy to explain, it may be a good idea.

Namespaces are one honking great idea -- let's do more of those!

## Zestaw startowy ##

### Podstawowy ###

*   Platforma:
    * Linux, Mac OS X, Windows + znajomość menagera paczek tego systemu
*   Python:
    * 2.7 w górę (na warsztaty rekomenduję 2.7)
*   System kontroli wersji:
    * Git
    * Mercurial
    * Bazaar
    <code>sudo apt-get install git</code>
*   Edytor tekstu/kodu lub IDE:
    * Vim
    * gedit
    * PyCharm, Eclipse, Aptana
    <code>sudo apt-get install vim</code>


## Podstawowywa konfiguracja projektu ##

### Virtualenv ###

Virtualenv to proste narzędzie umożliwiające tworzenie wirtualnych środowisk dla Pythona.
Pozwala na zarządzanie zależnościami i ich wersjami, dzięki temu możemy uniknąć konfliktów związanych z koniecznością instalacji/reinstalacji Pythona i jego bibliotek globalnie przy zmianie projektu/kontekstu.

Każdy projekt powinien mieć własny virtualenv.

Instalacja:

<code>
sudo pip install virtualenv
</code>

lub

<code>
sudo apt-get install python-virtualenv
</code>

[Na innych systemach](http://www.virtualenv.org/en/latest/#installation)

Tworzenie i aktywacja virtualenva:

Najpierw warto utworzyć katalog, który będzie przechowywał wszystkie virtualenvy:

    $ mkdir .virtuals
    $ cd .virtuals

Tworzenie i aktywacja:

    $ virtualenv example-virtualenv
    $ cd example-virtualenv
    $ source bin/activate

W efekcie:

    (example-virtualenv)~/.virtuals/example-virtualenv$

### Pip - pythonowy package manager ###

Instalacja bibliotek Pythona:

<code>
pip install <nazwa biblioteki>
</code>

Odinstalowywanie:

<code>
pip uninstall <nazwa biblioteki>
</code>

W celu łatwego zarządzania zależnościami warto utworzyć sobie w projekcie plik requirments, który będzie zawierał nazwy bibliotek wraz z wersjami:

    $ touch requirements.txt
    $ vim requirements.txt
    <nazwa-biblioteki>==<wersja-biblioteki>

Następnie, aby zainstalowac zależności z pliku:

    $ pip install -r requirements.txt

Aby "zamroźić" stan obecnego środowiska do pliku wraz z wersjami:

    $ pip freeze >> output_file.txt

### Repozytorium projektu ###

Rekomenduję, aby na potrzebę warsztatów repozytorium stworzyć na GitHubie, a następnie sklonować je na dysk.

    $ git clone git@github.com:<github username>/<nazwa projektu>.git
    $ cd <nazwa-projektu>

## Let's do magic! ##

### Keep calm and learn to code.. Keep calm and code on.. ###

Bardzo krótko o standardach kodowania w Pythonie:
*    Do wcięć zamiast tabulatora używaj 4 spacji
*    Maksymalna ilość znaków w linii: 79
*    Nazewnictwo:
     * nazwy klas - upper camelCase: NazwaKlasy
     * nazwy zmiennych lokalnych - styl z podkreśleniami: to_jest_moja_zmienna
     * nazwy funkcji - styl z podkreśleniami: to_jest_nowa_funkcja()
     * nazwy metod w klasie - styl z podkreśleniami: to_jest_moja_metoda
     * stałe: styl z podkreśleniami z dużymi literami: MOJA_STALA

Więcej [tutaj-Style Guide] (http://legacy.python.org/dev/peps/pep-0008/)

## Dokumentacja (Sphinx) ##

### Setup ###

Folder dla dokumentacji:

 <code>
 mkdir doc
 </code>

Instalacja Sphinxa:

<code>
pip install sphinx
</code>

Setup konfiguracji (w nawiasach [tu] podane są domyślne opcje):

<code>
sphinx-quickstart
</code>

### reStructuredText ###

[Syntax] (http://sphinx-doc.org/rest.html#rst-primer)

### Renderowanie ###

<code>
make html
</code>

## Porady ##

1. Stosuj zasady Zen of Python.
2. Pisz testy.
3. Pisz i aktualizuj dokumentację.
4. Dbaj o jakość kodu.
5. Daj swój kod do przeglądu (pisz tak, zebyś nie musiał wstydzić się swojego kodu).
6. Pamiętaj, że Twój kod będą używali i rozwijali inni - zrób im przysługę i dbaj o przestrzeganie standardów kodowania (używaj też sensownego nazewnictwa).
7. Używaj sensownego nazewnictwa też wobec branchy, commitów itd..
8. Czytaj kod innych.
9. Ucz się dobrych praktyk, dobrych wzorców, projektuj swój kod. Te umiejętności będą Ci potrzebne niezależnie od technologii, w której piszesz.
10. Rozwijaj się, zachowaj otwartość na inne technologie.

Partycypowanie w projektach Open Source uczy i pozwala utrwalić te zasady.

## Sciągi! ##

[git, virtualenv, pip, tworzenie dokumentacji](https://dont-be-afraid-to-commit.readthedocs.org/en/latest/cheatsheet.html)

[Style Guide] (http://legacy.python.org/dev/peps/pep-0008/)

[jak włączać się w projekty Open Sourcowe - na przykładzie Django](https://docs.djangoproject.com/en/1.6/internals/contributing/)

[jeszcze więcej o pracy z Gitem i GitHubem](https://docs.djangoproject.com/en/1.6/internals/contributing/writing-code/working-with-git/)










