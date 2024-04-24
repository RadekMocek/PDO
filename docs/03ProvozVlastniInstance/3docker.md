# Spuštění LingeBota v&nbsp;prostředí Docker

Tato sekce popisuje, jak spustit LingeBota v&nbsp;prostředí Docker. Tento postup navazuje na postup [stažení zdrojových kódů a prvního spuštění](./1prvnispusteni.md). Počítá se tedy s&nbsp;tím, že máte naklonovaný repozitář s&nbsp;botem a vyplněný konfigurační soubor `config.json`. Postup je proveden v&nbsp;operačním systému Ubuntu 22 s&nbsp;programem Docker ve verzi 26.0.

!!! caution "Upozornění: Vhodnost nasazení v&nbsp;prostředí Docker"
    Nasazení v&nbsp;prostředí Docker zlepší přenosnost řešení, ale zkomplikuje případné přidávání nového obsahu.<br><br>
    Použití Dockeru je vhodné pro dlouhodobé provozování bota, jehož obsah nechcete měnit.<br><br>
    Použití Dockeru není vhodné, pokud chcete pravidelně měnit např. teoretické materiály.

__0.__ Přejděte do adresáře `BP/Bot/`, pokud se zde již nenacházíte.

```shell
cd BP/Bot/
```

__1.__ Sestavte Docker image.

```shell
docker build --tag lingebot .
```

__2.__ Spusťte Docker container.

Pro první spuštění použijte:

```shell
docker run --name lingecont -d lingebot
```

Pro následující spuštění používejte:

```shell
docker start lingecont
```
