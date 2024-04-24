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
* __mkdocs__ – Webová stránka je optimalizovaná jak na PC, tak na mobilní zařízení. Plusem je také funkce vyhledávání.
* __Šablona readthedocs__ – Tato šablona se často používá pro dokumentaci Python knihoven. U&nbsp;pokročilejších uživatelů, kteří si budou chtít bota rozšířit, se očekává znalost jazyka Python. Je tedy možné, že se s&nbsp;touto šablonou již setkali. Tato šablona je navíc dobře čitelná i při velkém přiblížení/zvětšení.

## mkdocs tahák

* `mkdocs serve`
* `mkdocs gh-deploy`

<!-- k s v z o u -->
<!-- a i -->
