# Flip iPhone — Flip Claude

System agentowy do flipowania używanych iPhone'ów w PL (odkup ≤ ~700 zł, odsprzedaż z marżą, **tylko wysyłka**).

## Jak to działa
- **Orchestrator** (`CLAUDE.md`) — jedyny, który pisze do Eryka. Prowadzi cykl.
- **Pod-agenci** (`.claude/agents/`):
  - `flip-olx` — scout OLX.pl
  - `flip-vinted` — scout Vinted.pl
  - `flip-wycena` — filtr + wycena netto + drafty lowball
- **Rutyna:** codziennie 10:00 (Europe/Warsaw) — świeży pass rynku → wycena → max 2 wiadomości do Eryka.

## Dokumentacja
- `CLAUDE.md` — pełny mandat orchestratora (mózg projektu).
- `docs/wycena-kanon.md` — reguły wyceny (max buy, target exit, hard-stopy, net).
- `docs/drafty-styl.md` — styl draftów lowball.

## Stan
- `state/shortlist.json` — poprzedni shortlist (diff między cyklami).
- `state/inbox/` — awaryjny kanał: surowe oferty/linki od Eryka, gdy scraping zablokowany.

## Ograniczenia
- Nic „na żywo" (kontakt ze sprzedawcą / zakup / publikacja) bez zgody Eryka.
- Marketplace/FB — pominięte na stałe.
- Odbiór osobisty — skip.
