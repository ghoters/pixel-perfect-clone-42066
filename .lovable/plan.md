# Podstrona „Zamówienie zostało złożone" (`/potwierdzenie`)

## Cel
Po kliknięciu „Zapłać i złóż zamówienie" na `/platnosc` przechodzimy na nową podstronę `/potwierdzenie`, wyglądającą 1-1 jak załączona grafika, z tym samym nagłówkiem (SiteHeader) i stopką (SiteFooter) co pozostałe podstrony.

## Zawartość strony
- Duże kółko z ikoną ptaszka (niebieskie, na jasnoniebieskim tle).
- Nagłówek „Zamówienie zostało złożone!".
- Tekst: „Dziękujemy za zaufanie. Otrzymaliśmy Twoją płatność i rozpoczynamy przygotowanie Twojej figurki."
- Karta „Numer zamówienia": wygenerowany numer (#1038-style, losowy 4-cyfrowy), pod nim „Na Twój adres e-mail wysłaliśmy potwierdzenie zamówienia."
- Sekcja „Co teraz?" — 5 kroków z ikonami i numerami:
  1. Weryfikujemy przesłane zdjęcia — Sprawdzimy, czy materiały pozwolą na przygotowanie modelu.
  2. Przygotujemy projekt 3D — Na podstawie Twoich zdjęć stworzymy indywidualną figurkę.
  3. Otrzymasz projekt do akceptacji — Przed rozpoczęciem druku pokażemy Ci przygotowany model.
  4. Drukujemy i wykańczamy figurkę — Następnie zajmiemy się drukiem, obróbką i malowaniem.
  5. Wysyłamy gotowe zamówienie — Bezpiecznie zapakujemy i wyślemy Twoją figurkę.
- Pełnej szerokości przycisk „Przejdź do panelu zamówienia →" (przenosi na stronę główną; panel zamówienia nie istnieje — to podgląd).
- Pasek postępu z poprzednich podstron, z aktywnym krokiem 4 (Potwierdzenie) i zaznaczonymi jako wykonane krokami 1–3 — dla ciągłości wizualnej.
- Zachowanie przy braku zakończonej płatności (bezpośrednie wejście na URL): prosty komunikat z linkiem do konfiguratora, jak na innych podstronach procesu.

## Podejście techniczne
- Nowy plik `src/routes/potwierdzenie.tsx` (trasa `/potwierdzenie`) z własnym `head()` (tytuł, description, og, twitter:card).
- Płatność pozostaje podglądem (brak realnej bramki): kliknięcie „Zapłać i złóż zamówienie" zapisuje podsumowanie w sessionStorage i przechodzi na `/potwierdzenie` (link TanStack Router).
- Style w `src/styles.css` w sekcji payment (klasy `confirm-*`, tę same paletę `--payment-*` i kartę `payment-card`), bez zmian w innych podstronach.
- Numer zamówienia generowany losowo przy każdym złożeniu (sesyjnie, bez bazy).

## Weryfikacja
- Test w przeglądarce: pełny przebieg Oferta → Dane i dostawa → Płatność → Potwierdzenie, screenshot porównawczy z makietą, widok mobilny.
