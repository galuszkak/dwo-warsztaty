# Ruby <3 Open Source #

## Standardy w Ruby ##

Tworząc kod w języku Ruby warto stosować kilka prostych zasad.
Część z nich to powszechnie przyjęte założenia samej składni języka,
a część to dobre praktyki, które wypracowano przez lata.

Standard kodowania:
- kod powinien być czytelny
- nazwy klas i modułów zapisane są CamelCase
- nazwy metod i zmiennych zapisane są snake_case

Dobre praktyki:
- klasa nie ma więcej niż 100 lini kodu
- metoda nie ma więcej niż 5 linii kodu
- jedna linia nie ma więcej niż 79 znaków

## Prosty gem w języku Ruby ##

### Tworzenie repozytorium ###

Kod źródłowy, który ma być Open Source warto trzymać w jakimś otwartym repozytorium.
W świecie języka Ruby bardzo popularny jest [Github](http://github.com/).
Po zalogowaniu na Githuba, w górnym menu wybieramy Create new -> New repository.
Wpisujemy nazwę gemu i wybieramy licencję oczywiście Open Source (np. MIT License).
Następnie tworzymy repozytorium klikając w przycisk Create repository.
Tak stworzone repo możemy sklonować lokalnie używając polecenia:

<code>
git clone git@github.com:[nazwa-uzytkownika]/[nazwa-gemu].git
</code>

W bieżącej ścieżce powstanie katalog [nazwa-gemu].

### Tworzenie gemu ###

<code>
bundle gem [nazwa-gemu]
</code>

Pierwszym plikiem, który powinno się edytować jest gemspec.
Sekcje obowiązkowe to: name, version, authors, email, summary.
Sekcje dodatkowe to: description, homepage, itd.

### Tworzenie kodu ###

Można już pisać kod? Nie! Najpierw testy!

### Pisanie testów ###

Środowisko Ruby stara się zachować wysoką jakość tworzonego kodu.
Dlatego jeśli kod ma być rozwijany przez kilka osób testy są niezbędne.
Dla gemów jest to również rodzaj dokumentacji.
Testy pozwalają definiować funkcjonalności.
Sprawiają, że powstały kod jest najprostrzy z możliwych.
Panuje tutaj [reguła KISS](http://en.wikipedia.org/wiki/KISS_principle).

Istnieje wiele frameworków do testowania kodu w Ruby. Można używać:
- RSpec
- Minitest
- Cucumber
- i wiele innych

#### RSpec ####

RSpec jest bardzo popularny.
Jest łatwy w instalacji i osłudze.
Posiada wiele dodatkowych gemów.

0. Należy przejść do głównego katalogu gemu:
<code>
cd [nazwa-gemu]
</code>

1. Dodanie gemu do Gemfile lub pliku gemspec:
<code>
gem 'rspec'
</code>

2. Dociągnięcie gemu i zależności:
<code>
bundle install
</code>

3. Generowanie struktury katalogów:
<code>
rspec --init .
</code>

Powstanie katalog spec, w którym przechowywane będą testy.
Dodatkowo utworzony zostanie plik .rspec zawierający ustawienia RSpeca.
Warto go przeedytować i dopisać linijkę:
<code>
--format documentation
</code>
Dzięki temu uruchamiane testy będą bardziej komunikatywne.

4. Powiązanie testów z kodem.
Należy edytować plik /spec/spec_helper.rb i w nagłówku tego pliku dopisać gdzie znajduje się kod.
<code>
require '[nazwa-gemu]'
</code>

Nie należy podawać katalogu /lib w ścieżce, wystarczy sama nazwa.

Uruchamianie testów:
<code>
rspec spec
</code>

### Kod źródłowy ###

Ruby to język zgodny z [Agile Manifesto](http://agilemanifesto.org/iso/pl/).
Konwencja ponad konfigurację występuje również w gemach.

Struktura katalogów:
* /lib zawiera kod
* /spec zawiera testy

Wewnątrz tych katalogów struktura plików i katalogów powinna być taka sama.
Dzięki temu trzymając się konwencji wiele rzeczy można zautomatyzować.

### Automatyzacja procesów ###

Istnieje wiele narzędzi do automatyzacji często powtarzalnych czynności.
Jednym z takich narzędzi jest guard.

#### Guard ####

Popularne gemy związane z guardem:
* guard - gem służący do sekwencyjnego uruchamiania procesów
* guard-bundler - gem automatyzujący uruchamianie bundlera
* guard-rspec - gem automatyzujący uruchamianie testów

1. Dodanie gemów do Gemfile lub pliku gemspec:
<code>
gem 'guard'
gem 'guard-bundler'
gem 'guard-rspec'
</code>

2. Dociągnięcie gemów i zależności:
<code>
bundle install
</code>

3. Instalacja i konfiguracja:
<code>
guard init
</code>

W katalogu głównym gemu powstanie plik Guardfile.
Znajduje się w nim konfiguracja, które procesy automatyzować.

Uruchamianie guarda:
<code>
guard
</code>

### Wypuszczanie gemu do użytku ###

Aby umożliwić innym łatwe użytkowanie gemu można go wrzucić na specjalny serwer.
Jednym z najpopularniejszych serwerów jest [RubyGems](http://rubygems.org).

## Linki ##

- [Instalacja i konfiguracja](https://github.com/fractalsoft/dotfiles)
- [RVM - Ruby Version Manager](https://rvm.io/)
- [Dokumentacja Ruby](http://www.ruby-doc.org/)
- [Tworzenie gemu](http://railscasts.com/episodes/245-new-gem-with-bundler?view=asciicast)
- [RubyGems](http://rubygems.org/)
- [coderwall](https://coderwall.com/welcome)
- [Travis](https://travis-ci.org/)
- [Gemnasium](https://gemnasium.com/)
- [coveralls](https://coveralls.io/)
- [Code Climate](https://codeclimate.com/)
- [waffle](https://waffle.io/)
