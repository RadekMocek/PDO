# Markdown soubory a pravidla pro jejich zápis

Tato sekce popisuje, co jsou Markdown soubory a jaká jsou pravidla pro jejich zápis v&nbsp;ekosystému LingeBota. Tyto soubory se používají pro tvorbu teoretických materiálů (příkaz `/explain`) a tutoriálů pro počítaní příkladů (příkaz `/generate`). Tato sekce obsahuje obecná pravidla, která platí pro obě oblasti použití Markdown souborů.

Markdown je odlehčený značkovací jazyk. Markdown soubory jsou textové soubory, ve kterých lze – podle určitých pravidel zápisu – změnit formátování částí textu. Formátováním se myslí např. kurzíva, tučné písmo, nadpisy, odrážkové seznamy, odkazy a obrázky.

Syntax jazyka Markdown není příliš standardizovaná a Discord má tedy svou sadu pravidel a podporovaných formátování. LingeBot do něj navíc nějaké funkce přidává. Soubory musí mít příponu `.MD` (velkými písmeny), aby je mohl LingeBot najít. Pro jejich tvorbu lze použít jakýkoliv textový editor, např. VS Code s&nbsp;rozšířením <a href="https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint" target="_blank">markdownlint</a>.

---

## Obecná pravidla pro Markdown na platformě Discord

Tato tabulka obsahuje dostupné Markdown formátování na platformě Discord:

Název|Vstup|Výstup
---|---|---
Kurzíva|`_text_` nebo `*text*`|_text_
Tučné|`**text**`|__text__
Podtržené|`__text__`|<u>text</u>
Spoiler|<code>&#124;&#124;text&#124;&#124;</code>|<span class="spoiler">text</span>
Odkaz|`[text](https://example.com)`|<a href="https://example.com" target="_blank">text</a>
Nadpis<br>první úrovně|`# text`|<h1 style="margin-bottom:0">text</h1>
Nadpis<br>druhé úrovně|`## text`|<h2 style="margin-bottom:0">text</h2>
Nadpis<br>třetí úrovně|`### text`|<h3 style="margin-bottom:0">text</h3>
Nečíslovaný<br>seznam|`* Alice`<br>`* Bob`|<ul style="margin-bottom:0"><li>Alice</li><li>Bob</li></ul>
Číslovaný<br>seznam|`1. Alice`<br>`1. Bob`|<ol style="margin-bottom:0"><li>Alice</li><li>Bob</li></ol>
Zdrojový kód|<code>&#96;text&#96;</code> pro jednořádkový<br><code>&#96;&#96;&#96;text&#96;&#96;&#96;</code> pro víceřádkový|`text`
Citace|`> text` pro jednořádkovou<br>`>>> text` pro víceřádkovou|<blockquote style="margin-bottom:0">text</blockquote>

## Vykreslení matematických výrazů v&nbsp;Markdown souborech

LingeBot přidává možnost psaní matematických výrazů v&nbsp;Markdown souborech. Když bot odesílá zprávy z&nbsp;tohoto souboru do textového kanálu, část se zapsaným matematickým výrazem je nahrazena obrázkem, ve kterém je výraz vykreslen. Styl zápisu matematických výrazů je [stejný jako u&nbsp;příkazu `/render`](../02HlavniInstance/3render.md/#pravidla-pro-zapis-matematickych-vyrazu).

Pro zápis matematického výrazu:

* Na samostatný řádek napište `$$$render`
* Na další řádky napište požadovaný výraz
* Zápis ukončete napsáním `$$` opět na samostatný řádek

___Např.:___

```md
Běžný text ...

$$$render
[a,b;c,d]
$$

... běžný text pokračuje.
```

___se vykreslí jako:___

Běžný text ...

![s](../img/svg/k8i10UcZBH.svg)

... běžný text pokračuje.

---

## Horní a dolní indexy v&nbsp;Markdown souborech

LingeBot přidává možnost psaní horních a dolních indexů v&nbsp;Markdown souborech. Horní index se v&nbsp;textu označuje pomocí HTML značky `<sup>` a dolní index pomocí HTML značky `<sub>`.

Discord sám o&nbsp;sobě horní a dolní indexy nepodporuje, proto jsou obsahy značek převedeny na Unicode znaky. Může se ale stát, že daný Unicode znak ve verzi horního/dolního indexu neexistuje. Protože dolních indexů je v&nbsp;sadě Unicode méně, bot při zpracování textu naformátuje neexistující znaky, které jsou označené jako dolní index, jako jednořádkový zdrojový kód. Díky tomu se text více odlišuje od zbytku a tváří se jako pomocný symbol. U&nbsp;neexistujících znaků ve verzi horního indexu žádný takovýto mechanismus není a z&nbsp;implementačních důvodů je text odeslán ve formátu TeX, viz tabulka:

Vstup|Výstup
---|---
`(_a_ + _b_)<sup>2</sup>`|(_a_ + _b_)²
`2<sub>a</sub>`|2ₐ
`2<sup>a</sup>`|2ᵃ
`2<sub>Ω</sub>`|2`Ω`
`2<sup>Ω</sup>`|2^{Ω}

---

## Obrázky v&nbsp;Markdown souborech

Do Markdown souborů lze vkládat obrázky z&nbsp;internetu. Pro jejich korektní umístění ve výsledném odeslaném textu musí být jejich odkazy vloženy mezi „dvoudolary“ podobně jako u&nbsp;vykreslování matematických výrazů:

* Na samostatný řádek napište `$$`
* Na samostatný řádek vložte internetový odkaz na daný obrázek
* Zápis ukončete napsáním `$$` opět na samostatný řádek

___Např.:___

```md
Běžný text ...

$$
https://radekmocek.github.io/PDO/img/010302.png
$$

... běžný text pokračuje.
```

___se vykreslí jako:___

Běžný text ...

![w](https://radekmocek.github.io/PDO/img/010302.png)

... běžný text pokračuje.
