# Důležité pojmy

Tato sekce představuje specifické pojmy, které jsou používány v&nbsp;dalších částech manuálu a se kterými by měl být uživatel obeznámen.

---

## Discord

__Discord__ je program, ve kterém si uživatelé mohou zasílat textové zprávy a telefonovat po internetu.

Pro Discord se často používá označení „platforma“ ve smyslu _social media platform_, tedy softwarový systém, který po internetu poskytuje uživatelům službu sociálního média.

Po založení účtu na platformě Discord si můžete přidat ostatní uživatele do seznamu přátel. Pro odeslání žádosti o&nbsp;přátelství potřebujete znát uživatelské jméno daného uživatele. Pokud je vaše žádost přijata, můžete s&nbsp;druhou stranou komunikovat v&nbsp;DMs.

---

## DMs

__DMs__ je zkratka pro _Direct Messages_, tedy přímé zprávy.

Jedná se o&nbsp;místo, kde na platformě Discord probíhají komunikace typu _jeden na jednoho_. Zde si uživatel může se svými jednotlivými přáteli posílat textové zprávy a soubory. V&nbsp;DMs lze zahájit i&nbsp;hlasový hovor.

---

## Skupinová konverzace

__Skupinová konverzace__ je místo, kde může komunikovat až 10 uživatelů najednou.

Kromě počtu členů jsou funkce skupinové konverzace totožné s DMs.

---

## Discord server

Pojem __server__ je na platformě Discord chápán jako izolované místo, kde se nachází členové a kanály.

---

## Člen

__Člen__ serveru je uživatel, který se na daný server připojil a může se účastnit zdejší komunikace.

Pro připojení musí být uživatel na server pozván již existujícím členem. Druhou možností je použití zvacího odkazu, který může být pro server vygenerován. Po kliknutí na tento odkaz se uživatel stane členem daného serveru.

Uživatel se může připojit celkem na 100 různých serverů. Jeden server může mít v&nbsp;základu až 500&nbsp;000 členů.

---

## Kanál

__Kanál__ je místo na serveru, kde probíhá konkrétní komunikace. Je obvykle buď textový, nebo hlasový. Funkčně odpovídá skupinové konverzaci, zde se ale komunikace může zúčastnit jakýkoliv člen serveru, který k&nbsp;tomu má patřičná oprávnění.

---

## Role

__Role__ je sada oprávnění, která může být přidělena členům serveru.

Ne všichni členové serveru jsou si rovni. Nejvýše postavený člen je zakladatel daného serveru. Ten může vytvářet tzv. role, které přidělí ostatním členům.

---

## Oprávnění

__Oprávnění__ je pravidlo, které určuje, zdali může člen serveru provést určitou akci. Akcí může být odesílání zpráv do kanálu nebo pozvání nového člena, ale existují i akce pro správu serveru. Jednou z&nbsp;nich je i _správa rolí_. Pokud zakladatel serveru přidá členovi roli s&nbsp;oprávněním pro tuto akci, tento člen pak bude moci také přidělovat role a oprávnění.

---

## Administrátor

__Administrátor__ je člen serveru se stejnojmenným oprávněním, které obchází veškerá ostatní oprávnění a umožňuje mu dělat téměř vše. Zakladatel serveru by měl jmenovat administrátorem jen ty, kterým opravdu věří. Zakladatel serveru nemusí sám sobě přiřazovat administrátorskou roli, protože má automaticky oprávnění na všechny akce.

---

## Discord bot

__Bot__ je speciální typ uživatele, jehož chování je určeno programem.

Bot může na Discordu provádět mnoho akcí stejně jako běžný „lidský“ uživatel. Může např. číst a odesílat textové zprávy, připojit se do hlasového hovoru a spravovat nastavení serveru. K&nbsp;těmto akcím musí mít patřičná oprávnění. Oproti běžným uživatelům může bot navíc do svých zpráv přidávat interaktivní ovládací prvky jako tlačítka. Bot se obvykle nesnaží simulovat běžného uživatele (tzv. chatbot), spíše se jedná o&nbsp;nástroj, který reaguje na předem danou sadu příkazů vykonáním příslušných akcí.

Boti obvykle operují na serverech, lze s&nbsp;nimi ale komunikovat i v&nbsp;DMs. Bota si nelze přidat do přátel, pro zahájení DMs je tedy nutné s&nbsp;ním mít společný server, odkud ho lze kontaktovat. Bota nelze pozvat do skupinové konverzace.

### Vytvoření bota a jeho ověřovací token

Vlastního bota lze vytvořit na webu _Discord Developer Portal_, kde je mu v&nbsp;podstatě založen účet včetně nastavení uživatelského jména a profilového obrázku. Oproti běžnému uživateli, který se přihlašuje pomocí uživatelského jména a hesla, se bot přihlašuje pomocí ověřovacího __tokenu__. Token je uložen v&nbsp;programu, který bota ovládá. Tento program musí být někde neustále spuštěný. Tokeny vašich botů uchovejte v&nbsp;tajnosti. Při prozrazení tokenu může být účet vašeho bota tzv. odcizen: někdo předefinuje jeho chování svým vlastním programem.

!!! Note "Upřesnění: Bot vs. Aplikace"
    Jako Discord aplikace se označuje vše, co oficiálním způsobem komunikuje s&nbsp;Discord API. K&nbsp;aplikaci pak může být přiřazen bot, který je její uživatelskou reprezentací.

    Bota lze od běžného uživatele rozeznat podle toho, že má vedle svého jména napsáno _BOT_, při psaní tohoto manuálu (19. 4. 2024) byl ale tento nápis změněn na _APLIKACE_. Je tedy možné, že v&nbsp;oficiálním názvosloví dojde ke změnám. Tento manuál bude prozatím používat starý pojem _bot_.

---

## Příkaz

__Příkaz__ je textová zpráva se speciálním formátem, na kterou bot po jejím odeslání reaguje vykonáním určité akce.

### Podpůrný příkaz

V&nbsp;roce 2021 Discord představil tzv. __podpůrné příkazy__, které unifikují ovládání botů. Všechny podpůrné příkazy začínají lomítkem a je k&nbsp;dispozici jejich našeptávání. Např.:

* `/help`
  * Bot odešle do textového kanálu zprávu, která obsahuje nápovědu k&nbsp;jeho používání.
* `/hod_kostkou`
  * Bot odešle do textového kanálu zprávu, která obsahuje číslo od jedné do šesti.
* `/secti` `<a>` `<b>`
  * Bot odešle do textového kanálu zprávu s&nbsp;číslem, které odpovídá součtu `<a>` + `<b>`.
  * Jedná se o&nbsp;příkaz s&nbsp;dvěma vstupními parametry.
  * Např.:
    * `/secti` `2` `3` pošle číslo 5.
    * `/secti` `8` `7` pošle číslo 15.

### Parametr příkazu

__Parametr příkazu__ je požadovaná informace, kterou musí uživatel vyplnit, aby mohl být příkaz odeslán a proveden. Každý příkaz má 0 až _N_ vstupních parametrů.  Parametr obvykle ovlivňuje výstup daného příkazu. Nejčastějšími typy parametru jsou číslo a textový řetězec. U&nbsp;podpůrných příkazů je součástí našeptávání i zvýraznění a kontrola vstupních parametrů. Nelze tedy odeslat příkaz se špatně vyplněnými parametry.

### Prefixový příkaz

__Prefixový příkaz__ je starý druh příkazu, který místo lomítka začíná prefixem. Prefix může být tvořen jedním či více znaky a je určen autorem bota.

Kromě podpůrných příkazů může bot reagovat i na běžné textové zprávy. Před představením podpůrných příkazů měl obvykle každý bot svůj prefix – např. vykřičník – a reagoval na zprávy odeslané do textového kanálu, které začínaly tímto prefixem. V&nbsp;případě vykřičníku by pak příkazem pro nápovědu bylo `!help` namísto podpůrného `/help`.

Tento druh příkazů lze používat i dnes např. pro příkazy správy u&nbsp;kterých nechceme, aby byly součástí našeptávání. LingeBot má pro tyto účely prefix <code>$> </code>.

---

## Zvací odkaz bota

Bota lze na server přidat pomocí jeho speciálního __zvacího odkazu__. Jedná se o&nbsp;odkaz na webovou stránku s&nbsp;dialogem pro přidání bota. Součástí dialogu je výběrový seznam všech serverů, kam má daný uživatel oprávnění bota přidat. Po zvolení serveru a potvrzení se bot na server připojí.

---

## LingeBot

__LingeBot__ je Discord bot zaměřený na výklad teorie a generování příkladů z&nbsp;lineární algebry. Zároveň do prostředí do textového kanálu přináší možnost vykreslování matematických výrazů.

---

## LingeMod

__LingeMod__ je role, kterou LingeBot vytvoří na každém serveru, jakmile se na něj připojí. Pomocí této role mohou administrátoři upřesnit, jací uživatelé mají přístup k&nbsp;jakým příkazům.

---

## Hlavní a vlastní instance LingeBota

LingeBot má otevřený zdrojový kód. Ten je možné si stáhnout a spustit. Do programu je ale nutné vložit token. Pokud uživatel do tohoto programu vloží token svého vlastního bota, pak se jedná o&nbsp;__vlastní instanci LingeBota__.

__Hlavní instance LingeBota__ je ta, kterou provozuje autor zdrojového kódu LingeBota.
