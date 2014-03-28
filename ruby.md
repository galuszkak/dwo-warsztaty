Ruby Open Source
================

# Ruby <3 Open Source #

## Prosty gem w języku Ruby ##

### Tworzenie repozytorium ###

Kod źródłowy, który ma być Open Source warto trzymać w jakimś otwartym repozytorium.
W świecie języka Ruby bardzo popularny jest [Github](http://github.com/).
Po zalogowaniu na Githuba, w górnym menu wybieramy Create new -> New repository.
Wpisujemy nazwę gemu i wybieramy licencję oczywiście Open Source (np. MIT License).
Następnie tworzymy repozytorium klikając w przycisk Create repository.

<code>
git clone git@github.com:[nazwa-uzytkownika]/[nazwa-gemu].git
</code>

### Tworzenie gemu ###

<code>
bundle gem [nazwa-gemu]
</code>

Pierwszym plikiem, który powinno się edytować jest gemspec.
Sekcje obowiązkowe to: name, version, authors, email, summary.
Sekcje dodatkowe to: description, homepage, itd.

### Tworzenie kodu ###

Ruby to język zgodny z [Agile Manifesto](http://agilemanifesto.org/iso/pl/).
Konwencja ponad konfigurację występuje również w gemach.

...
