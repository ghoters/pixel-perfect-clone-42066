# Wyśrodkowanie głównych boksów na „Ofercie” i „Danych i zamówieniu”

## Cel
Ustawić boks konfiguratora i boks podglądu jako jedną, wyśrodkowaną względem strony całość. Ten sam układ zastosować na stronie „Dane i zamówienie”. Sekcja „Potrzebujesz pomocy?” pozostanie po lewej stronie.

## Zakres zmian
1. **Oferta — główne boksy**
   - Oddzielić pozycjonowanie dwóch głównych boksów od bocznej sekcji pomocy.
   - Wyśrodkować wspólny obszar: boks „Kogo ma przedstawiać figurka?” + boks podglądu wizualizacji.
   - Pozostawić sekcję „Potrzebujesz pomocy?” po lewej, dopasowując jej szerokość tak, aby nie nachodziła na wyśrodkowane boksy.
   - Zachować obecne proporcje między formularzem a podglądem oraz ich wewnętrzny wygląd.

2. **Oferta — pasek kroków**
   - Lewą krawędź paska ustawić dokładnie nad lewą krawędzią boksa kroku 1.
   - Prawą krawędź paska zakończyć dokładnie nad prawą krawędzią boksa podglądu wizualizacji.
   - Zachować obecne działanie przyklejonego paska i jego wygląd.

3. **Dane i zamówienie**
   - Wyśrodkować boks formularza i prawy boks podglądu jako jedną całość w tej samej szerokości i pozycji co dwa główne boksy na „Ofercie”.
   - Dopasować pasek 1–5 do ich wspólnych krawędzi.
   - Nie zmieniać wielkości tekstów, odstępów, formularza ani walidacji wprowadzonej wcześniej.

4. **Mniejsze ekrany**
   - Zachować obecny układ dwóch kolumn tam, gdzie jest na niego miejsce, i jedną kolumnę na telefonie.
   - Sekcja pomocy nadal będzie ukryta na szerokościach, na których obecnie się nie mieści.

5. **Kontrola końcowa**
   - Porównać obie podstrony przy tej samej szerokości okna.
   - Sprawdzić, czy środki obu głównych układów pokrywają się ze środkiem strony, paski pokrywają pełną szerokość boksów, a sekcja pomocy nie nachodzi na treść.
   - Sprawdzić widok telefonu i brak poziomego przewijania.

## Potwierdzony stan
Na dużym ekranie „Oferta” używa obecnie trzech kolumn: 300 px sekcji pomocy, formularza i podglądu. Cały zestaw jest wyśrodkowany, dlatego dwa główne boksy są przesunięte w prawo. Strona „Dane i zamówienie” odziedziczyła to samo przesunięcie o 320 px. Pasek „Oferty” zajmuje obecnie pełne 1780 px, zamiast zaczynać się nad boksem kroku 1.

## Szczegóły techniczne
Zmiana obejmie wyłącznie układ „Oferty” i style `.order-page`. Logika konfiguratora, formularza oraz zapisane dane pozostaną bez zmian.
