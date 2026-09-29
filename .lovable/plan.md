# Ujednolicenie strony „Dane i zamówienie” z „Ofertą”

## Cel
Powiększyć i przesunąć zawartość strony „Dane i zamówienie”, aby po przejściu z „Oferty” główne boksy zachowywały podobną pozycję, szerokość i skalę tekstu. Zachować obecny układ wewnętrzny, odstępy i kolejność elementów.

## Zakres zmian
1. **Wyrównanie głównych boksów na dużym ekranie**
   - Dopasować lewą krawędź formularza do lewego boksu konfiguratora z „Oferty”.
   - Dopasować prawy „Podgląd figurki” do położenia i szerokości prawego podglądu na „Ofercie”.
   - Rozszerzyć cały układ formularza i podglądu z obecnych 1224 px do przestrzeni odpowiadającej dwóm głównym kolumnom „Oferty”.

2. **Dopasowanie paska kroków**
   - Zachować wcześniejszą zasadę: pasek zaczyna się równo z lewym boksem formularza i kończy na prawej krawędzi podglądu.
   - Przesunąć go razem z nową pozycją boksów, bez zmiany jego treści i działania.

3. **Powiększenie treści strony zamówienia**
   - Zwiększyć teksty nagłówków, opisów, etykiet pól, podsumowania i przycisków do skali zbliżonej do „Oferty”.
   - Proporcjonalnie powiększyć pola, ikony i kontrolki tam, gdzie jest to potrzebne, aby tekst nie wyglądał na ściśnięty.
   - Zachować obecne rozmieszczenie tekstów, odstępy wewnętrzne i hierarchię informacji.

4. **Mniejsze ekrany**
   - Na szerokościach, na których „Oferta” nie pokazuje lewej kolumny pomocniczej, pozostawić boksy „Dane i zamówienie” na pełnej dostępnej szerokości.
   - Zachować obecne przejście do jednej kolumny na telefonie i brak nakładania tekstów.

5. **Kontrola końcowa**
   - Porównać obie strony przy tej samej szerokości okna oraz sprawdzić przejście „Oferta” → „Dane i zamówienie”.
   - Zweryfikować wyrównanie lewych i prawych krawędzi, skalę tekstu, pasek kroków oraz widok mobilny.

## Potwierdzony stan
Przy szerokości 1823 px „Oferta” wykorzystuje układ o szerokości 1780 px, a jej główny formularz i prawy podgląd zajmują dwie prawe kolumny. Strona „Dane i zamówienie” centruje obecnie oba boksy w obszarze 1224 px, dlatego są mniejsze i przesunięte względem „Oferty”. Nagłówki obu stron zaczynają się już w tym samym miejscu i nie wymagają przesuwania.

## Szczegóły techniczne
Zmiany pozostaną ograniczone do stylów `.order-page`; strona „Oferta” i jej działanie nie zostaną zmienione. Logika formularza, walidacja i dane zamówienia pozostaną bez zmian.
