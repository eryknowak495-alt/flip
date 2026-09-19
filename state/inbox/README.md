# Inbox (awaryjny kanał danych)

Gdy scraping OLX/Vinted jest zablokowany (egress), Eryk może tu wrzucać surowe oferty/linki:
- wklej linki lub tekst ogłoszeń do pliku `.md` / `.txt` w tym folderze,
- scouty (`flip-olx`, `flip-vinted`) sprawdzają ten folder, gdy `WebFetch` zwróci `EGRESS_BLOCKED`,
- `flip-wycena` przetwarza je normalnie (filtr + net + drafty).

Format nieistotny — wystarczą linki albo skopiowany tekst ogłoszenia.
