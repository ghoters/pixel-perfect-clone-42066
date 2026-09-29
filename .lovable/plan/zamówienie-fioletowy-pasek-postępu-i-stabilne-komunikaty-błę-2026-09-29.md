# Zamówienie: fioletowy pasek postępu i stabilne komunikaty błędów

## Cel

Dwie poprawki w sekcji 1. „Dane kontaktowe" na stronie `/zamowienie`:

1. **Pasek postępu reaguje na wypełnienie pól** — gdy użytkownik wpisze dane w pole i je opuści (Enter, Tab lub kliknięcie gdzieś na stronie), krok „Dane i zamówienie" na górnym pasku postępu zmienia kolor na fiolet — ten sam `--primary` (oklch(0.59 0.24 274)), który na stronie oferty oznacza aktywne kroki konfiguratora.
2. **Komunikaty „To pole jest wymagane." nie przesuwają układu** — miejsce pod komunikatem błędu jest zarezerwowane na stałe, więc sekcje 2–4 ani panel boczny nie przeskakują w dół, gdy błąd się pojawia lub znika.

## Zakres zmian

Tylko `src/routes/zamowienie.tsx` i lokalne style `.order-page` w `src/styles.css`. Strony główna i oferta pozostają bez zmian.

### 1. Fioletowy pasek postępu

- Śledzenie wypełnienia trzech pól kontaktowych (imię i nazwisko, e-mail, telefon) w stanie komponentu.
- Zdarzenie `onBlur` na polach (obejmuje Enter, Tab i kliknięcie poza polem) zapisuje aktualną wartość pola.
- Gdy wszystkie trzy pola są niepuste, krok 2 na pasku postępu dostaje stan „ukończony": kółko z ikoną zaznaczenia i etykieta w kolorze `--primary` (fiolet jak w ofercie), zamiast obecnego `--order-blue`.
- Kroki 3–5 pozostają neutralne; krok 1 „Konfiguracja" bez zmian (już oznaczony jako ukończony).
- Dodanie klasy `.order-progress-step.is-done` w `src/styles.css` z kolorem `--primary` dla kółka i etykiety; bieżący krok (`.is-current`) zachowuje fiolet zamiast niebieskiego, gdy dane są kompletne.

### 2. Stabilne komunikaty błędów

- W komponencie `Field` komunikat błędu renderowany zawsze (pusty, gdy brak błędu), a w CSS `.order-error` dostaje stałą wysokość (np. `min-height` odpowiadającą jednej linii tekstu) — pojawienie się tekstu nie zmienia wysokości pola.
- To samo dla komunikatów przy wyborze paczkomatu i zgodach (`.order-agreements`), żeby żaden błąd nie przesuwał treści.
- Układ siatki pól kontaktowych i adresu kuriera pozostaje bez zmian — zmienia się tylko rezerwacja miejsca pod błąd.

## Weryfikacja

- Playwright przy 1280 px i 390 px: wpisanie danych + Enter/klik poza pole → krok 2 staje się fioletowy; wysłanie pustego formularza → komunikaty błędów pojawiają się bez przesunięcia sekcji poniżej (porównanie pozycji elementów przed/po).
- Brak błędów builda i konsoli.
