# Seznam dostupných příkazů

Tato sekce obsahuje přehled všech podpůrných příkazů, kterými LingeBot disponuje. Jednotlivé příkazy jsou podrobněji popsány v&nbsp;následujících sekcích.

Příkaz|Popis
---|---
`/clear`|Pročistí textový kanál odesláním dlouhé zprávy tvořené neviditelnými znaky.
`/dm`|Zahájí s&nbsp;uživatelem konverzaci v&nbsp;DMs.
__`/explain`__|__Spustí rozhraní pro výklad teorie.__
__`/generate`__|__Spustí rozhraní pro generaci příkladů.__
`/help`|Zobrazí nápovědu.
`/ping`|Ověří dostupnost bota.
__`/render` `<text>`__|__Odešle do text. kanálu matematický výraz vykreslený podle parametru `<text>`.__
`/setup` `...`|sada příkazů pro nastavení

---

## Příkazy pro nastavení

`/setup lingemod` `<member>`<br>Přidá, nebo odebere roli LingeMod členovi `<member>`.

`/setup permissions get`<br>Zobrazí přehled nastavení oprávnění na daném serveru.

`/setup permissions set_buttons` `<action>` `<permission>`<br>Nastaví oprávnění `<permission>` pro interakci s&nbsp;rozhraním `<action>`.

`/setup permissions set_command` `<action>` `<permission>`<br>Nastaví oprávnění `<permission>` pro použití příkazu `<action>`.

`/setup render_theme` `<theme>`<br>Nastaví barevné schéma `<theme>` pro vykreslování matematických výrazů.

!!! note "Poznámka: Nastavení v&nbsp;DMs"
    Příkazy pro nastavení fungují pouze na serveru a v&nbsp;DMs nemají význam. Výjimkou je nastavení barevného schématu příkazem `/setup render_theme` `<theme>`. Na serveru tento příkaz nastaví schéma pro všechny vykreslené výrazy nehledě na uživatele příkazu. V&nbsp;DMs pak tento příkaz nastaví schéma pro všechny přímé zprávy včetně těch přeposlaných ze serveru.

<!--
!!! note "[!] NEPRAVDA"
    Příkazy pro nastavení mohou používat pouze administrátoři a zakladatel serveru, ostatním členům je přístup zamítnut. Výjimkou je příkaz `/setup permissions get`, který ve skutečnosti nic nenastavuje, ale pouze zobrazuje aktuální nastavení.

    Při použití `/setup render_theme` `<theme>` v&nbsp;DMs (jak je zmíněno výše), není vyžadováno, aby byl uživatel administrátorem. V&nbsp;kontextu DMs totiž žádný administrátor neexistuje a uživatel nastavuje barevné schéma pouze pro soukromou komunikaci s&nbsp;botem.
-->
