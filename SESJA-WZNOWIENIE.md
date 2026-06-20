# Sesja — wznowienie (grafiki pomeczowe)

**Data zapisu:** 2026-06-20
**Temat:** System robienia **grafik pomeczowych** (wynik meczu → grafika na social media) dla turnieju „Lubańska Plażówka 2026".

## Gdzie jesteśmy
- Faza: **brainstorming** (skill `superpowers:brainstorming`) — jeszcze NIE projektujemy/kodu. Najpierw design + akceptacja.
- Losowanie par: gotowe, działa (turniej-losowanie.vercel.app). Kamil ma „kilka rzeczy do poogarniania", ale priorytet = grafiki pomeczowe.
- Strona turnieju: kompletna. `index.html` (1139 linii, jeden plik) na GitHub Pages.

## Co już ustalone (kontekst techniczny)
Dane meczów SĄ już w `index.html`:
- `DB.cats[cid]` (cid = `m`/`k`/`x`), w środku: `groups`, `scores`, `picks`, `bscores`, `seed`, `advance`, `start`.
- Wynik meczu: `cats[cid].scores[key]`, key = `${gi}-${a}-${b}` (grupa, indeks pary A, indeks pary B); sety **S1/S2/S3** + małe punkty.
- `matchStat()` liczy sety/małe punkty; drabinka = `picks`/`bscores`.
- `allTeams()` zwraca nazwy par. Wygląd: czarne tło, hero zachód słońca, fonty Anton/Oswald, akcent pomarańcz/ember.

## Otwarte pytania (do dokończenia brainstormu)
1. **Visual companion** — zaproponowany (makiety w przeglądarce), Kamil jeszcze nie odpowiedział tak/nie.
2. Gdzie żyje generator: część strony turnieju czy osobne narzędzie?
3. Jak powstaje PNG: HTML/CSS → screenshot/render po stronie klienta, czy API obrazkowe (Higgsfield/n8n)?
4. **n8n + Vercel** — Kamil mówi, że ma tam projekty powiązane z tym tematem. DO SPRAWDZENIA po zalogowaniu (patrz niżej).

## Zaległe logowania (żeby zajrzeć do projektów Kamila)
- **Vercel (MCP):** link OAuth wygasł — wywołać ponownie `mcp__plugin_vercel_vercel__authenticate` i dać nowy link. (Vercel CLI nie zainstalowany).
- **n8n (MCP):** Kamil ma wpisać `/mcp` w konsoli i wybrać „claude.ai n8n".

## Następny krok po wznowieniu
1. Zalogować n8n + Vercel, **obejrzeć istniejące projekty** (czy generator grafik już częściowo istnieje w n8n/Vercel).
2. Dokończyć brainstorming (pytania 1–3 wyżej), spisać design do `docs/superpowers/specs/`.

---
### Jak wznowić sesję
W katalogu `~/Desktop/wiedza-2xkpro` odpal Claude Code i napisz:
> „Wznawiamy grafiki pomeczowe do turnieju — przeczytaj `~/dev/turniej-plazowka/SESJA-WZNOWIENIE.md` i kontynuuj."
