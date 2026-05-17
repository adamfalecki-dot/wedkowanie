# CLAUDE.md

## Czym jest ten projekt

Skill AI (`wedkowanie-suwalszczyzna.skill`) — baza wiedzy wędkarskiej dla regionu Suwalszczyzny i Mazur. Plik `.skill` to archiwum ZIP z plikami Markdown.

## Struktura

```
wedkowanie-suwalszczyzna.skill (ZIP)
├── SKILL.md                         — definicja skilla, routing, reguły
└── references/
    ├── fishing-base.md              — kanon: region, łowiska, sprzęt, preferencje
    ├── fish-species.md              — gatunki ryb regionu, okresy ochronne, wymiary
    ├── techniques.md                — techniki: spinning, gruntowa, spławikowa, feeder, muchowa
    ├── baits-lures.md               — przynęty naturalne i sztuczne, dobór
    ├── seasonal-calendar.md         — kalendarz brań, żerów, sezonowość
    ├── waters-guide.md              — przewodnik po łowiskach regionu
    └── regulations.md               — przepisy PZW, limity, okresy ochronne, wymiary
```

## Zasady nieprzekraczalne

- **Region Suwalszczyzna/Mazury zawsze** — jeziora, rzeki i regulaminy tego regionu.
- **Przepisy PZW obowiązkowe** — okresy ochronne, wymiary ochronne, limity połowu. Nigdy nie doradzaj łamania przepisów.
- **Konkretne łowiska** — odpowiedzi odwołują się do konkretnych zbiorników, nie ogólników.
- **Sezonowość** — porady dostosowane do aktualnej pory roku, temperatury wody, ciśnienia.
- **Polskie nazwy i produkty** — polskie sklepy wędkarskie, polskie marki przynęt.
- **Brak zgadywania** — jeśli brakuje info o łowisku/warunkach, zadaj 1 pytanie.

## Praca z plikiem .skill

```powershell
Expand-Archive -Path wedkowanie-suwalszczyzna.skill -DestinationPath skill-extracted -Force
# po edycji:
Compress-Archive -Path skill-extracted\* -DestinationPath wedkowanie-suwalszczyzna.skill -Force
```
