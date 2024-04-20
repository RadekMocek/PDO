# Výklad teorie pomocí příkazu `/explain`

## Princip příkazu `/explain`

Po zadání příkazu `/explain` se v textovém kanálu objeví rozhraní pro výklad teorie. Výklad funguje tak, že bot do textového kanálu odesílá zprávy, které obsahují výpisky z konkrétního matematického tématu. Tyto výpisky jsou vytvořeny provozovatelem bota.

Teoretické materiály se dělí na témata, která se pak dělí na podtémata. Po zadání píkazu `/explain` se nejprve objeví výběrový seznam, kde si uživatel zvolí jedno téma, které ho zajímá. V textovém kanálu se pak vždy nachází zprávy patřící k jednomu podtématu vybraného tématu. Mezi podtématy lze přepínat pomocí tlačítek nebo nově objeveného výběrového seznamu.

!!! caution "Upozornění"
    Při přepínání mezi podtématy jsou nejprve do kanálu odeslány zprávy nového podtématu a následně jsou smazány zprávy starého podtématu. Při tomto procesu (který může chvilku trvat) nebudou ovládací prvky reagovat. Pokud je zpráv více, může se proces na chvíli zastavit, jedná se o rate limit ze strany Discordu.

!!! tip
    Používání výkladu teorie v textovém kanálu, kde komunikují nebo používají bota i jiní uživatelé, může být nepřehledné až chaotické. Zprávy odeslané botem se mohou zamíchat s cizími zprávami a teoretické výpisky pak nebudou dobře čitelné.

    Proto je výklad teorie vhodné používat v kanálech s omezeným přístupem nebo v DMs. Pro zahájení konverzace v DMs slouží příkaz `/dm`.

## Rozhraní příkazu `/explain`
