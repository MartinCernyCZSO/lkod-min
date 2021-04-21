# Lokální katalog ČSÚ - test
Metadata lokálního katalogu otevřených dat ČSÚ v JSON-LD.

## Záznamy datových sad
Pro přidání či editaci záznamu použijte [formulář NKOD v režimu LKOD](https://data.gov.cz/formulář/registrace-datové-sady).
Režim se přepíná ikonou ozubeného kolečka vedle tlačítka stažení vyplněného záznamu.
Tam je také potřeba vyplnit IRI poskytovatele a IRI datové sady. Výsledný soubor uložte do repozitáře.
Uložení automaticky spustí [GitHub Action](https://github.com/features/actions), která repozitář projde, a vytvoří [soubor katalogu](katalog.jsonld) na základě [šablony](katalog-šablona.jsonld) a nalezených datových sad.

### IRI datových sad
Je třeba se ujistit, že IRI datové sady vyplněné v záznamu na tento záznam po jeho uložení do repozitáře povede.
V tomto repozitáři je vzorová datová sada, jejíž IRI je `https://raw.githubusercontent.com/opendata-mvcr/lkod-min/main/datové-sady/datová-sada.jsonld`.
Toto IRI zjistíte po kliknutí na tlačítko `Raw` při prohlížení souboru přes rozhraní GitHub.
Skládá se vždy z `https://raw.githubusercontent.com/`, `organizace/`, `repozitář/`, `jméno-větve/`, `cesta k souboru v repozitáři`.

Tato IRI datových sad lze také použít pro opětovné načtení záznamu do [formuláře NKOD](https://data.gov.cz/formulář/registrace-datové-sady) pro jeho editaci.
Ve formuláři staří v prvním kroku dole kliknout na "Načíst záznam z URL", a IRI datové sady tam vyplnit.

### IRI katalogu
Při [registraci lokálního katalogu do NKOD](https://data.gov.cz/formulář/registrace-lokálního-katalogu) pak stačí zvolit jako Typ API lokálního katalogu `DCAT-AP Dokumenty` a do URL LKOD API vyplnit URL [souboru katalogu](katalog.jsonld) podobně, jako pro datové sady, tedy např. `https://raw.githubusercontent.com/opendata-mvcr/lkod-min/main/katalog.jsonld`
