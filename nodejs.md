NodeJS Open Source
==================

1. Dobre praktyki
--------------------------------------

1. Zamieść plik licencji.
2. Opisz projekt - wypełnij README
3. Wszystkie zależności umieszczaj w package.json
4. Dziel zależności na produkcyjne i deweloperskie (--save, --save-dev)
5. Wykonuj inspekcję kodu (jshint, jslint)
6. Określe reguły walidacyjne kodu w pliku (.jshintrc)
7. Automatyzuj czynności (gulp, grunt)
8. Dodaj node_modules do .gitignore
9. Stosuj to samo formatowanie kodu w całym projekcie
10. Pisz testy - dokumentują kod.

2. Styl kodowania
--------------------------------------

1. Nazywaj funkcje
> Nazywaj nawet te najmniejsze funkcje w ten sposób dokumentujesz kod i określasz lokalizację ewentualnego błędu.
2. Unikaj closures
> Umieść definicję funkcji po inną funkcją. Eliminuje to wile nieumyślnych wycieków pamięci jakie może powodować closure.
3. Pisz wiele małych funkcji
> V8 optymalizuje kod. Im więcej małych funkcji tym większa szansa, że zostaną one zamieniona na funkcje inline. Poza tym małe funkcje zwiększają czytelność kodu i dokumentuje go tym samym ułatwiają jego utrzymanie.
4. Pilnuj stylu programowania
> Używaj jednakowego stylu programowania w całym projekcie. Stosuj narzędzia do sprawdzania go (np. jsstyle).
5. Pamiętaj, że testy to Twój najlepszy przyjaciel.