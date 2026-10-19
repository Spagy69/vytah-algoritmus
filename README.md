# Výtah – 3ITE KYME

Zadání: navrhnout algoritmus výtahu, který lidi rozveze s kratším čekáním a kratší ujetou dráhou než základní "panelákový" výtah.

Termín odevzdání: 25. 10. 2026, 23:59.

## Co je v repu

- `vytah.html` – simulátor. Otevře se v prohlížeči, nic se nemusí instalovat. Obsahuje i manuál (karta "Manuál").
- `zadani/zadani-bezny-den-ve-skole.json` – naše zadání (400 lidí, 8 pater). Při otevření `vytah.html` ho přetáhneme do stránky nebo vybereme přes "Vybrat soubor…".

## Jak začít

1. Otevřít `vytah.html` v prohlížeči.
2. Načíst `zadani/zadani-bezny-den-ve-skole.json`.
3. Algoritmus se upravuje v `vytah.html`, v bloku `<script id="algoritmus">` (funkce `zacatek`, `rozhodni`, `nastup`). Zbytek souboru se nemá měnit.
4. Po úpravě uložit a obnovit stránku – zadání se pamatuje a načte se samo.

Zatím je v repu jen výchozí (nejhorší) verze algoritmu z šablony. Úprava algoritmu je další krok, na repu se zatím jen připravila struktura, aby do něj mohli všichni začít psát.

## Matice odpovědnosti

| Co | Kdo |
|---|---|
| Založení repa, struktura projektu | Vít Machač |
| Algoritmus výtahu | – |
| Testování a ladění na zadání | – |
| README / dokumentace | – |

(Doplnit, jak se práce reálně rozdělí.)

## AI

Repo a jeho strukturu připravil Claude (Claude Code) podle zadání z Teams. Algoritmus výtahu bude psaný manuálně – AI se u něj použije jen v mezích "AI semaforu" (hledání informací, vysvětlení chyb, kontrola kódu), ne na vygenerování celého řešení. Konkrétní využití AI se doplní, až bude algoritmus hotový.
