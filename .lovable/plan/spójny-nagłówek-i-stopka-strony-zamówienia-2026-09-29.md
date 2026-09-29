# Spójny nagłówek i stopka strony zamówienia

## Zakres
- Dodać na `/zamowienie` dokładnie ten sam nagłówek nawigacyjny i tę samą stopkę, które są używane na stronie głównej i na `/oferta`; pokazywać je także wtedy, gdy konfiguracja figurki nie została jeszcze ukończona.
- Dopasować górną część strony zamówienia do `/oferta`: tę samą szerokość obszaru treści, odstęp od nagłówka, wielkość i wysokość wiersza etykiety, tytułu i opisu oraz rytm przed paskiem postępu. Zachować treść właściwą dla zamówienia i jego pięć etapów.
- Pozostawić formularz, panel podsumowania, ceny, walidację i wygląd pozostałych dwóch stron bez zmian; skorygować jedynie lokalne style strony zamówienia potrzebne do spójnego przejścia między podstronami.

## Technicznie i sprawdzenie
- Wykorzystać istniejące `SiteHeader` i `SiteFooter`, bez ich kopiowania ani modyfikowania; dopasować `.order-page` do typografii i kontenera użytych na `/oferta`.
- Sprawdzić przejście `/oferta` → `/zamowienie` oraz wygląd obu stron na komputerze i telefonie, w tym pusty stan zamówienia, brak nakładania się elementów i obecność stopki.
