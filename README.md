# PDO

* Dokumentovaným softwarem je [Discord bot pro výklad a příklady z&nbsp;matematiky](https://github.com/RadekMocek/BP)
* Hlavní instance bota je veřejně dostupná a koncoví uživatelé ji mohou používat
* Bot je ale navržen i na self-host vlastní instance, do které je možné přidávat vlastní obsah

## Skupiny uživatelů

1. Koncový uživatel hlavní instance bota (nejčastěji student VŠ)
2. Uživatel provozující vlastní instanci s&nbsp;vlastním obsahem (např. učitel matematiky, ne nutně na VŠ)

* Obě skupiny mají základní technickou znalost, nemusí ale znát platformu Discord
* (Dokumentace může posloužit i oponentovi BP pro lepší pochopení a případné otestování)

## Zvolený formát

* __Dokumentace na webu__ – Pokud chce uživatel bota použít, znamená to, že právě používá PC/mobil/tablet a je připojen k&nbsp;internetu. Web se tedy jeví jako ideální formát
* __mkdocs__ – Webová stránka je optimalizovaná jak na PC, tak na mobilní zařízení.
* __Šablona readthedocs__ – Tato šablona se často používá pro dokumentaci Python knihoven. U&nbsp;pokročilejších uživatelů, kteří si budou chtít bota rozšířit, se očekává znalost jazyka Python. Je tedy možné, že se s&nbsp;touto šablonou již setkali. Tato šablona je navíc dobře čitelná i při velkém přiblížení/zvětšení.
* Šest hlavních částí v&nbsp;levé liště:
  1. __Rychlé odkazy__ – Uživatel chce co nejrychleji pozvat bota na server nebo se dostat ke source/issues na GitHubu. Nachází se zde odkazy a nic víc.
  2. __Úvod__ – Obsahuje představení SW, shrnutí obsahu následujících "kapitol" a důležité pojmy, které se dále budou používat
  3. __Jak začít__ – pro uživatele Discordem nepolíbené
  4. __Dostupné funkce a jak je používat__ – převážně pro koncové uživatele hlavní instance bota
  5. __Provoz vlastní instance__ – pouze zprovoznění vlastní instance (ne každý musí chtít do bota přidávat vlastní obsah; tohle bude potřeba pro všechny, až mi skončí hosting :))
  6. __Přidání vlastního obsahu__ – přidání vlastních teoretických témat a generátorů příkladů do vlastní instance

## mkdocs tahák

* `mkdocs serve`
* `mkdocs gh-deploy`

<!-- k s v z o u -->
