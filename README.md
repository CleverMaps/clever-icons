# clever-icons

Tento repozitář rozšiřuje sadu [Font Awesome](https://fontawesome.com/v4.7.0/icons/) o několik ikon, které nám chyběly:

> ![zoom-selection](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/zoom-selection.svg?sanitize=true) ci-zoom-selection
>
> ![zoom-selection-dashed](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/zoom-selection-dashed.svg?sanitize=true) ci-zoom-selection-dashed
>
> ![ruler](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/ruler.svg?sanitize=true) ci-ruler
>
> ![ruler-triangle](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/ruler-triangle.svg?sanitize=true) ci-ruler-triangle
>
> ![fullscreen](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/fullscreen.svg?sanitize=true) ci-fullscreen
>
> ![fullscreen-box](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/fullscreen-box.svg?sanitize=true) ci-fullscreen-box
>
> ![preview](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/preview.svg?sanitize=true) ci-preview
>
> ![layers](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/layers.svg?sanitize=true) ci-layers (optimized for 16px)
>
> ![sort-asc-down](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/sort-asc-down.svg?sanitize=true) ci-sort-asc-down
>
> ![sort-asc-up](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/sort-asc-up.svg?sanitize=true) ci-sort-asc-up
>
> ![sort-desc-down](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/sort-desc-down.svg?sanitize=true) ci-sort-desc-down
>
> ![sort-desc-up](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/sort-desc-up.svg?sanitize=true) ci-sort-desc-up
>
> ![filter-round](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/filter-round.svg?sanitize=true) ci-filter-round
>
> ![filter-round-cross](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/filter-round-cross.svg?sanitize=true) ci-filter-round-cross
>
> ![filter-cross](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/filter-cross.svg?sanitize=true) ci-filter-cross
>
> ![coin-czk](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/coin-czk.svg?sanitize=true) ci-coin-czk (optimized for 28px)
>
> ![coin-eur](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/coin-eur.svg?sanitize=true) ci-coin-eur (optimized for 28px)
>
> ![czech-post](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/czech-post.svg?sanitize=true) ci-czech-post (optimized for 28px)
>
> ![arrow-up](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/arrow-up.svg?sanitize=true) ci-arrow-up
>
> ![arrow-down](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/arrow-down.svg?sanitize=true) ci-arrow-down
>
> ![ca-badge](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/ca-badge.svg?sanitize=true) ci-ca-badge
>
> ![calendar-cross](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/calendar-cross.svg?sanitize=true) ci-calendar-cross
>
> ![coin-czk-inv](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/coin-czk-inv.svg?sanitize=true) ci-coin-czk-inv
>
> ![coin-eur-inv](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/coin-eur-inv.svg?sanitize=true) ci-coin-eur-inv

## Použití

* Buď ručně: viz soubor `demo.html`.
* Nebo balíčkovačem: importovat `fonts` a `style.css`.

Pro soulad s _Font Awesome_ je vhodné ve vlastním CSS nastavit třídě `.ci` stejné vlastnosti, jaké má třída `.fa` (např. preprocesorem), nebo alespoň nastavit `font-size: 14px`.

Zápis v HTML je pak obdobný jako u _Font Awesome_ (viz demo).

## Přispívání

* Zdrojové ikony jsou nakresleny jako SVG v gridu 14×14 px. Stejně tak je ručně nastaven viewBox. Vektory jsou optimalizovány, aby v této velikosti co nejvíc seděly na pixelovou mřížku.

* Výsledný soubor prosím zoptimalizovat (např. pomocí [SVGO](https://jakearchibald.github.io/svgomg/)). Nebo aspoň uložit jako _Plain SVG_, ať neobsahuje balast.

* Zdrojové ikony se ukládají do adresáře `src`. Pak pullrequest.

## Buildování

Do webfontu ideálně zbuilduji sám. Toto jsou spíš poznámky pro mě:

* Pro konverzi používám aplikaci [IcoMoon](https://icomoon.io/app/). Pro import existujících ikon stačí naimportovat soubor `selection.json`. V něm jsou obsaženy jednak vektory stávajícíh ikon, zároveň i nastavení exportovaného fontu.

* Nové ikony se přidají nahráním SVG. Stávající ikony nemazat a nepřejmenovávat.

* Při buildu do ikonfontu nezapomenout změnit verzi fontu (ozubené kolečko vedle tlačítka). Ostatní nastavení by se mělo převzít z nahraného JSONu.

* V repozitáři pak nahraju celý obsah ZIPu do složky `dist`. Především jsou důležité soubory s fonty, vygenerované CSS a aktualizovaný JSON.