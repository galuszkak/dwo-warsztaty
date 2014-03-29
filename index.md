Włącz się w ruch Open Source
============================


1. Tutorial
-------------------

Instalacja gita

Ubuntu:

    sudo apt-get install git

OS X:
    
    brew install git

Windows:

    Download git from here: !TODO


Korzystanie z GitHuba. FAQ.

1. Co to jest fork?
2. Jak zgłosić błąd?
3. Jak śledzić projekt?
4. Używanie numerów ticketa?
5. Branche, jak je przeglądać, po co są, jak je zamykać?

Tutorial

1. Pobrać repozytorium https://github.com/piotrekbass/dwo2014-warsztaty
2. Stworzyć brancha na którym będziemy pracować <code>git branch moj_branch</code>
3. <code>git checkout moj_branch</code>
4. Dopisać funkcję i test do niej test. 
5. Stworzyć forka
6. <code> git remote add nazwa_remote https://github.com/moj_login/dwo2014-warsztaty</code>
7. <code>git commit -a</code>
8. <code>git push nazwa_remote moj_branch</code>
9. Stworzyć Pull Requesta do głównego repozytorium
10. And it's done :)


2. Współpraca, kultura, dobre praktyki
--------------------------------------

Jeżeli chcesz wejść w jakieś projekt open source pamiętaj by wcześniej:

1. Przeczytać collaboration / development docs. Jest to istotne, gdyż znajdziesz tam informację jakie zasady panują w projekcie.
2. Gdy zaczniesz pracę nad jakimś ticketem napisz o tym w issues. Często zdarza się, że ktoś także, możę pracować nad danym ticketem i Twoja praca może się zmarnować.
3. Staraj się stosować do uwag i proponowanych rozwiązań przez core developerów. Często mają oni większą wiedzę o projekcie jaki i większą możliwość pomocy, jeżeli chodzi o wykorzystanie już istniejącego kodu.
4. Bądż miły. Jeżeli ktoś odrzucił Twój Pull Request, to nie znaczy, że nie szanuje Twojej pracy. Możliwe, że potrzebujesz zastosować się do zaleceń obowiązujących w projekcie. 
5. Code review ma ci pomóc. Jest to darmowa pomoc od społeczności. Wykorzystaj to mądrze!
6. Jeżeli czegoś nie wiesz to zawsze pytaj. Społeczności zależy na Twoim wkładzie i chcą ci pomóc.
7. Pisz testy. Zawsze. Jeżeli projekt nie ma napisanych testów zaproponuj, że je napiszesz.
8. Pamiętaj o dokumentacji. Twoja przygoda z projektem może trwać, tylko parę Pull Requestów, dlatego, jeżeli projekt ma dokumentację to opisz tam zmiany lub działanie nowego kodu który stworzyłeś.
9. Nie wysyłaj Pull Requesta, jeżeli nie odpaliłeś testów lokalnie.
10. 


3. CI a Open Source
-------------------

Dzisiaj wiele projektów Open Source zyskuje na tym, że istnieje wiele usług które zwiększają jakość rozwoju projektu. Usługi te są często darmowe, przez co twórcy projektu nie muszą ponosić kosztu utrzymania dużej infrastruktury.

Poniżej przedstawię parę usług z których warto korzystać przy tworzeniu lub angażowaniu się w projekt open source



4. Narzędzia do pair programming
--------------------------------

Często istnieje problem zdalnej współpracy na tym samym kodzie. Tutaj znajdziesz narzędzia które pomogą ci wspólnie pracować nad jednym kawałkiem kodu z paroma osobami.

1. MadEye.io 
2. Tmux + własny server (polecam)
3. Cloud9 (c9.io)
4. TeamViewer (odradzam)


4. Przydatne linki
------------------

