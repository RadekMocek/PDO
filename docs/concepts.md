# Důležité pojmy

Tato sekce představuje specifické pojmy, které jsou používány v&nbsp;dalších částech manuálu a se kterými by měl být uživatel obeznámen.

## Discord

<blockquote>Discord,&emsp;DMs,&emsp;skupinová konverzace</blockquote>

__Discord__ je program, ve kterém si uživatelé mohou zasílat textové zprávy a telefonovat po internetu.

Po založení účtu si můžete přidat ostatní uživatele do přátel. Pro odeslání žádosti o&nbsp;přátelství potřebujete znát uživatelské jméno daného uživatele. Pokud je vaše žádost přijata, můžete s&nbsp;druhou stranou komunikovat pomocí textových DMs nebo hlasového hovoru. __DMs__ je zkratka pro _Direct Messages_, tedy přímé zprávy.

Discord umožňuje vytvořit __skupinovou konverzaci__ až deseti uživatelů, jejíž funkce jsou stejné jako u&nbsp;DMs. Samostatným celkem, který také umožňuje komunikaci, jsou pak Discord servery.

Discord je dostupný buď ve webové aplikaci na <a href="https://discord.com/app" target="_blank">https://discord.com/app</a>, nebo jako program pro operační systémy Windows, Linux, MacOS, Android a iOS. Podrobnější informace o&nbsp;podporovaných platformách se nacházejí <a href="https://support.discord.com/hc/en-us/articles/213491697-What-are-the-OS-system-requirements-for-Discord" target="_blank">na webu Discordu v&nbsp;sekci FAQ</a>.

## Discord server

<blockquote>server,&emsp;člen,&emsp;kanál,&emsp;role,&emsp;oprávnění,&emsp;administrátor</blockquote>

Pojem __server__ je na platformě Discord chápán jako místo, kde se nachází členové a kanály.

__Člen__ serveru je uživatel, který se na daný server připojil. Pro připojení musí být uživatel na server pozván již existujícím členem. Druhou možností je použití zvacího odkazu, který může být pro server vygenerován. Po kliknutí na tento odkaz se uživatel stane členem daného serveru. Uživatel se může přidat celkem na 100 různých serverů. Jeden server může mít v&nbsp;základu až 500 000 členů.

__Kanál__ je obvykle buď textový, nebo hlasový. Funkčně odpovídá skupinové konverzaci, zde se ale může komunikace zúčastnit jakýkoliv člen serveru, který k&nbsp;tomu má patřičná oprávnění.

Ne všichni členové serveru jsou si rovni. Nejvýše postavený člen je zakladatel daného serveru. Ten může vytvářet tzv. role, které přidělí ostatním členům.

__Role__ je sada oprávnění, která může být přidělena členům serveru.

__Oprávnění__ je pravidlo, které určuje, zdali může člen serveru provést určitou akci. Akcí může být odesílání zpráv do kanálu nebo pozvání nového člena, ale existují i akce pro správu serveru. Jednou z&nbsp;nich je i _správa rolí_. Pokud zakladatel serveru přidá členovi roli s&nbsp;oprávněním pro tuto akci, tento člen pak bude moci také přidělovat role a oprávnění.

__Administrátor__ je člen serveru se stejnojmenným oprávněním, které obchází veškerá ostatní oprávnění a umožňuje mu dělat téměř vše. Zakladatel serveru by měl jmenovat administrátorem jen ty, kterým opravdu věří.

## Discord bot

<blockquote>bot,&emsp;interaktivní prvky,&emsp;podpůrné příkazy,&emsp;argument příkazu,&emsp;starý typ příkazů,&emsp;zvací&nbsp;odkaz,&emsp;token</blockquote>

Bot je speciální typ uživatele, jehož chování je určeno programem.

Bot může na Discordu provádět mnoho akcí stejně jako běžný „lidský“ uživatel. Může např. číst a odesílat textové zprávy, připojit se do hlasového hovoru a spravovat nastavení serveru. K&nbsp;těmto akcím musí mít patřičná oprávnění. Oproti běžným uživatelů může bot navíc do svých zpráv přidávat __interaktivní prvky__ jako tlačítka. Bot se obvykle nesnaží simulovat běžného uživatele (tzv. chatbot), spíše se jedná o&nbsp;nástroj, který reaguje na předem danou sadu příkazů vykonáním příslušných akcí.

__Příkaz__ je textová zpráva se speciálním formátem, na kterou bot po jejím odeslání reaguje vykonáním určité akce. V&nbsp;roce 2021 Discord představil tzv. __podpůrné příkazy__, které unifikují ovládání botů. Všechny podpůrné příkazy začínají lomítkem a je k&nbsp;dispozici jejich našeptávání. Např.:

* `/help` – Bot odešle do textového kanálu zprávu, která obsahuje seznam jeho dostupných příkazů.
* `/hod_kostkou` – Bot odešle do textového kanálu zprávu, která obsahuje číslo od jedné do šesti.
* `/secti 2 2` – Bot odešle do textového kanálu zprávu s&nbsp;číslem 4. Jedná se o&nbsp;příkaz s&nbsp;dvěma argumenty.

__Argument příkazu__ je //TODO

Kromě podpůrných příkazů může bot reagovat i na interaktivní prvky nebo běžné textové zprávy. Před představením podpůrných příkazů měl obvykle bot svůj prefix – např. vykřičník – a pak příkazem pro nápovědu bylo `!help` namísto `/help`. Tento __„starý typ příkazů“__ lze používat i dnes např. pro příkazy správy u&nbsp;kterých nechceme, aby byly součástí našeptávání.

Bota lze na server přidat pomocí jeho speciálního __zvacího odkazu__. Jedná se o&nbsp;odkaz na webovou stránku s&nbsp;dialogem pro přidání bota. Součástí dialogu je vývěrový seznam všech serverů, kam má daný uživatel oprávnění bota přidat. Po zvolení serveru a potvrzení se bot na server připojí.

Boti tedy obvykle operují na serverech, lze s&nbsp;nimi komunikovat ale i v&nbsp;DMs. Bota si nelze přidat do přátel, pro zahájení DMs je tedy nutné s&nbsp;ním mít společný server, odkud ho lze kontaktovat. Bota nelze pozvat do skupinové konverzace.

Vlastního bota lze vytvořit na webu _Discord Developer Portal_, kde je mu v&nbsp;podstatě založen účet včetně nastavení uživatelského jména a profilového obrázku. Oproti běžnému uživateli, který se přihlašuje pomocí uživatelského jména a hesla, se bot přihlašuje pomocí ověřovacího __tokenu__. Token je uložen v&nbsp;programu, který bota ovládá. Tento program musí být někde neustále spuštěný. Tokeny vašich botů uchovejte v&nbsp;tajnosti. Při prozrazení tokenu může být účet vašeho bota tzv. odcizen: někdo předefinuje jeho chování svým vlastním programem.

!!! Note "Upřesnění: Bot vs. Aplikace"
    Jako Discord aplikace se označuje vše, co oficiálním způsobem komunikuje s&nbsp;Discord API. K&nbsp;aplikaci pak může být přiřazen bot, který je její uživatelskou reprezentací.

    Bota lze od běžného uživatele rozeznat podle toho, že má vedle svého jména napsáno _BOT_, při psaní tohoto manuálu (19. 4. 2024) byl ale tento nápis změněn na _APLIKACE_. Je tedy možné, že v&nbsp;oficiálním názvosloví dojde ke změnám. Tento manuál bude prozatím používat starý pojem _bot_.

## LingeBot a LingeMod

__LingeBot__ je Discord bot zaměřený na výklad teorie a generování příkladů z&nbsp;lineární algebry. Zároveň do prostředí do textového kanálu přináší možnost vykreslování matematických výrazů.

Neplést si s&nbsp;__LingeMod__. To je role, kterou LingeBot vytvoří na každém serveru, jakmile se na něj připojí. Pomocí této role lze určit, jací uživatelé mají přístup k&nbsp;jakým příkazům.

## Hlavní a vlastní instance LingeBota

LingeBot má otevřený zdrojový kód. Ten je možné si stáhnout a spustit. Do programu je ale nutné vložit token. Pokud uživatel do tohoto programu vloží token svého vlastního bota, pak se jedná o&nbsp;__vlastní instanci LingeBota__.

__Hlavní instance LingeBota__ je ta, kterou provozuje autor zdrojového kódu LingeBota.
