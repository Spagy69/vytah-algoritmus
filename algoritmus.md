# Algoritmus výtahu

Použijeme **LOOK s dávkováním a stárnutím priorit**. Výtah jede jedním
směrem a otáčí se až tehdy, když v tomto směru už není další užitečný
požadavek. Díky tomu zbytečně nejezdí ke krajním patrům budovy.

## Jak funguje

1. Když je kabina prázdná, jede k nejdéle čekajícímu člověku.
2. Při jízdě nahoru nabírá čekající, kteří chtějí jet nahoru. Při jízdě
   dolů nabírá analogicky lidi jedoucí dolů.
3. Na každém patře nejdříve vystoupí lidé, kteří tam mají cíl, a potom
   nastoupí vhodní čekající, pokud je v kabině místo.
4. Výtah zastavuje pouze tam, kde někdo vystupuje nebo kde může někoho
   nabrat. Nezastavuje v prázdných patrech.
5. Když už v aktuálním směru není žádný požadavek, změní směr a obslouží
   druhou stranu.

## Stárnutí priorit

Aby někdo nečekal příliš dlouho, používáme dva časové limity:

- po **60 sekundách** dostane čekající přednost při nejbližší změně směru,
- po **120 sekundách** se jeho patro stane okamžitou prioritou.

Tím zachováme krátké průměrné čekání, ale zároveň zabráníme hladovění
jednoho směru.

## Důležitá omezení

Čekající osoba má v zadání známý pouze směr jízdy. Její cílové patro
poznáme až po nástupu, proto nelze předem naplánovat přesné cíle všech
zastávek. Po každém nástupu se plán znovu přepočítá.

Při plné kabině výtah nezastavuje kvůli nástupu, ale pouze kvůli výstupu.
Když nikdo nečeká, zůstane stát a čeká na nový požadavek.

## Deploy - https://spagy69.github.io/vytah-algoritmus/