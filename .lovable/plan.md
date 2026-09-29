# Ograniczenie siatki miniatur zdjęć (krok 6, Oferta)

## Cel
Przy dużej liczbie zdjęć siatka podglądu ma pokazywać 3 normalne miniatury i jedną przyciemnioną kafelkę „+N", a pełny podgląd wszystkich zdjęć dopiero po kliknięciu.

## Zakres zmian
Tylko `src/components/OrderPhotoGallery.tsx` (tryb pełny, nie `compact`).

## Zachowanie po zmianie
- Gdy zdjęć jest **4 lub mniej** — bez zmian: wszystkie miniaturki normalnie, każda z lupą (powiększ) i X (usuń).
- Gdy zdjęć jest **więcej niż 4**:
  - Kafelki 1–3 renderują się normalnie (lupa + usuń bez zmian).
  - Kafelka nr 4 jest przyciemniona (nakładka na zdjęciu) z licznikiem **„+N"** (N = liczba zdjęć poza siatką) i podpowiedzią, że można kliknąć.
  - Kliknięcie kafelki „+N" otwiera istniejący Dialog (lightbox) od pierwszego niewidocznego zdjęcia (indeks 3).
  - Pozostałe zdjęcia nie renderują się w siatce (mniejszy koszt), ale są dostępne w lightboxie.
- Lightbox przy więcej niż 1 zdjęciu dostaje nawigację, żeby dało się obejrzeć wszystkie:
  - strzałki poprzedni/następny (cykliczne),
  - pasek miniatur pod zdjęciem (jak w trybie `compact`), z możliwością wskoczenia na dowolne zdjęcie,
  - przycisk usuwania (X) w nagłówku lightboxa — żeby zdjęcia niewidoczne w siatce też można było usunąć; po usunięciu ostatniego zdjęcia lightbox się zamyka.

## Uwagi
- Tryb `compact` (podsumowanie na stronie zamówienia) pozostaje bez zmian.
- Usuwanie dalej idzie przez istniejący `onRemove`, więc IndexedDB i liczniki aktualizują się automatycznie.
- Mobile: siatka ma `grid-cols-3`, więc przy >4 zdjęciach pokaże się 3 normalne + kafelka „+N" w nowej linii — to akceptowalne.
