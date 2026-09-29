# Miniatury zdjęć w Ofercie i podgląd przy zamówieniu

## Efekt
- Po dodaniu zdjęć w kroku 6 „Zdjęcia” pojawią się ich miniatury pod polem wyboru, z możliwością powiększenia i usunięcia pojedynczego zdjęcia.
- Na stronie „Dane i zamówienie” wiersz „Zdjęcia” pozwoli otworzyć podgląd dodanych fotografii bez wydłużania prawego boksu — przycisk „Przejdź do płatności” pozostanie na swoim miejscu.
- Powrót do Oferty zachowa zdjęcia w tej samej przeglądarce; „Wyczyść wszystko” usunie także zdjęcia. Widok będzie działał na telefonie i komputerze.

## Szczegóły techniczne
- Obecnie konfigurator zapisuje tylko `photoCount`, a nie pliki; zdjęcia będą przechowywane lokalnie w przeglądarce (IndexedDB) jako pliki, nie w `sessionStorage` jako duże ciągi tekstu. Konfiguracja i galeria zostaną zsynchronizowane przy wyborze, usuwaniu i przywracaniu.
- Obsługa wyboru oraz upuszczenia plików, formatów JPG/PNG i deklarowanego limitu 10 MB na zdjęcie. Czytelny komunikat dla nieobsługiwanych plików lub błędu zapisu; przy brakujących zdjęciach nie pokazywać mylącej liczby ani nie pozwalać przejść dalej tylko na podstawie starego licznika.
- Podgląd pełnego zdjęcia otwierany w oknie z zamknięciem klawiszem Escape; miniatury mają nazwy dostępne dla czytników ekranu. Zachować obecny układ Oferty i pozostałych stron.
- Sprawdzić przepływ: dodanie kilku zdjęć → miniatury → przejście do zamówienia → podgląd → powrót, usunięcie i ponowne dodanie; sprawdzić widok mobilny.

**Zakres:** To lokalny podgląd wybranych zdjęć. Obecny formularz nie wysyła jeszcze zamówień ani zdjęć do sklepu; ta zmiana nie doda wysyłki ani płatności.
