# Spuštění LingeBota na platformě Docker

__1.__ Naklonujte si repozitář `RadekMocek/BP` a přesuňte se do složky `BP/Bot/`

```shell
mkdir LingeBot
cd LingeBot/
git clone https://github.com/RadekMocek/BP
cd BP/Bot/
```

__2.__ Vytvořte a vyplňte soubor `config.json` (lze využít `config-example.json`)

```shell
cp config-example.json config.json
vim config.json
```

```json
{
  "tokenProduction": "token_for_main_bot_account",
  "tokenTesting": "token_for_secondary_bot_account",
  "isProduction": true,
  "secret1": "link_to_google_forms"
}
```

<details>
  <summary>Poznámka ke kofiguraci `config.json`</summary>
  
  Konfigurace obsahuje dva tokeny pro snadnější přepínání mezi produkčním a testovacím botem.<br>
  Produkční bot je ten, který běží 24/7 a je používán koncovými uživateli. Jeho token je hodnotou `tokenProduction`.<br>
  Testovací bot je ten, který se používá příležitostně pro testování nových funkcí vývojářem. Jeho token je hodnotou `tokenTesting`.<br>

  Hodnota `isProduction` přepíná mezi produkčním a testovacím botem: `true` pro produkční a `false` pro testovací.<br>
  Pokud není potřeba testovacího bota, je možné ponechat `isProduction` nastaveno na `true` a vyplnit token pouze pro `tokenProduction`. Dokud není nastaveno `isProduction` na `false`, na hodnotě `tokenTesting` nezáleží.<br>

  `secret1` momentálně slouží pro uchování odkazu na dotazník, v&nbsp;pozdějších verzích bude pravděpodobně odstraněn.

</details>

__3.__ Sestavte Docker image

```shell
docker build --tag lingebot .
```

__4.__ Spusťte Docker container

Pro první spuštění použijte:

```shell
docker run --name lingecontainer -d lingebot
```

Pro následující spuštění použijte:

```shell
docker start lingecontainer
```
