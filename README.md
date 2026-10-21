# Výtah – 3ITE KYME

Zadání: navrhnout algoritmus výtahu, který lidi rozveze s kratším čekáním a kratší ujetou dráhou než základní "panelákový" výtah.

## Co je v repu

- `vytah.html` – simulátor. Otevře se v prohlížeči, nic se nemusí instalovat. Obsahuje i manuál (karta "Manuál").
- `zadani/zadani-bezny-den-ve-skole.json` – naše zadání (400 lidí, 8 pater). Při otevření `vytah.html` ho přetáhneme do stránky nebo vybereme přes "Vybrat soubor…".

## Jak začít

1. Otevřít `vytah.html` v prohlížeči.
2. Načíst `zadani/zadani-bezny-den-ve-skole.json`.
3. Algoritmus se upravuje v `vytah.html`, v bloku `<script id="algoritmus">` (funkce `zacatek`, `rozhodni`, `nastup`). Zbytek souboru se nemá měnit.
4. Po úpravě uložit a obnovit stránku – zadání se pamatuje a načte se samo.

Aktuální algoritmus je LOOK se stárnutím priorit, návrh je popsaný v [algoritmus.md](algoritmus.md).

## Výsledky na našem zadání

Na `zadani/zadani-bezny-den-ve-skole.json` (otisk `B746-8C6D`):

| | výchozí (panelákový) | LOOK se stárnutím priorit |
|---|---|---|
| Rozvezeno | 400 / 400 | 400 / 400 |
| Průměrně celkem | 336,1 s | 206,1 s |
| Ujetá dráha | 2922 m | 2211 m |
| Zastavení | 309 | 342 |
| Nejdelší čekání | 1438,7 s | 807,4 s |

Hlavní metrika (průměrně celkem) klesla o cca třetinu a ujetá dráha o čtvrtinu. Nejdelší čekání je pořád vysoké (přes 13 minut) – při kapacitě 6 a frontě desítek lidí u přízemí stačí plná kabina a i "kritický" čekající musí počkat, až se uvolní místo. Zastavení naopak vzrostlo, protože výtah nabírá/vykládá po cestě víckrát, než jen při prázdné kabině jako dřív.

## Matice odpovědnosti

| Co | Kdo |
|---|---|
| Algoritmus výtahu (návrh) | Matěj Adamec |
| Kód | Všichni |
| Testování a ladění na zadání | Vít Machač, Claude |
| README / dokumentace | Vít Machač |

## AI

AI (Claude) podle návrhu v [algoritmus.md](algoritmus.md) (napsal Matěj) naprogramovala funkce `rozhodni`/`nastup`/`zacatek` ve `vytah.html` a odladila je na našem zadání. Samotná myšlenka algoritmu (LOOK + stárnutí priorit) je Matějova, ne vygenerovaná AI.
