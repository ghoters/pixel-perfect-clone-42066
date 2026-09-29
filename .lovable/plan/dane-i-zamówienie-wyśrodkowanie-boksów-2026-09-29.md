# Dane i zamówienie — wyśrodkowanie boksów

## Cel
Oba boksy (formularz po lewej + podgląd figurki po prawej) oraz pasek kroków mają tworzyć jedną grupę wyśrodkowaną na stronie — tyle samo wolnej przestrzeni po lewej i po prawej stronie boksów.

## Stan obecny (zmierzony w podglądzie)
Zmierzyłem układ w podglądzie przy szerokości ekranu 1837 px, tej samej co u Ciebie:

- Grupa boksów (formularz + podgląd + pasek kroków 1–5) ma szerokość 1300 px.
- Wolna przestrzeń: 269 px po lewej i 269 px po prawej — identycznie.
- Centrowanie działa przy każdej szerokości okna (blok zawsze ustawia się na środku).

Czyli: układ już teraz jest dokładnie taki, jaki opisujesz — boksy razem, na środku, z równą wolną przestrnią po obu stronach.

## Plan
1. Odświeżyć podgląd (F5 / ponowne otwarcie strony), aby mieć pewność, że widzisz aktualny stan.
2. Potwierdzić, że boksy wyglądają u Ciebie wyśrodkowane z równymi marginesami.
3. Żadnych zmian w kodzie nie potrzeba — dopóki nie potwierdzisz inaczej.

## Co jeśli nadal widzisz przesunięcie?
Napisz, przy jakiej szerokości okna i co dokładnie widzisz (np. „więcej miejsca po prawej”) — wtedy poprawię. Ewentualna różnica rzędu kilkunastu px może pochodzić od paska przewijania przeglądarki po prawej stronie; mogę ją wyrównać, jeśli to o to chodzi.
