# clever-icons

Tento repozitář rozšiřuje sadu [Font Awesome](https://fontawesome.com/v4.7.0/icons/) o několik ikon, které nám chyběly.

![zoom-selection](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/zoom-selection.svg?sanitize=true)\
zoom-selection

![zoom-selection-dashed](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/zoom-selection-dashed.svg?sanitize=true)\
zoom-selection-dashed

![ruler](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/ruler.svg?sanitize=true)\
ruler

![ruler-triangle](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/ruler-triangle.svg?sanitize=true)\
ruler-triangle

![fullscreen](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/fullscreen.svg?sanitize=true)\
fullscreen

![fullscreen-box](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/fullscreen-box.svg?sanitize=true)\
fullscreen-box

![preview](https://raw.githubusercontent.com/CleverMaps/clever-icons/master/src/preview.svg?sanitize=true)\
preview

## Použití

* Buď ručně: viz soubor `demo.html`.
* Nebo balíčkovačem: importovat `fonts` a `style.css`.

Pro soulad s _Font Awesome_ je vhodné ve vlastním CSS nastavit třídě `.ci` stejné vlastnosti, jaké má třída `.fa` (např. preprocesorem), nebo alespoň nastavit `font-size: 14px`.

Zápis v HTML je pak obdobný jako u _Font Awesome_ (viz demo).

## Přispívání

* Zdrojové ikony jsou nakresleny jako SVG v gridu 14×14 px. Stejně tak je ručně nastaven viewBox. Vektory jsou optimalizovány, aby v této velikosti co nejvíc seděly na pixelovou mřížku. 

* Výsledný soubor prosím zoptimalizovat (např. pomocí [SVGO](https://jakearchibald.github.io/svgomg/)). Nebo aspoň uložit jako _Plain SVG_ ať neobsahuje balast.

* Zdrojové ikony se ukládají do adresáře `src`. Pak pullrequest.

## Buildování

Do webfontu ideálně zbuilduji sám. Toto jsou spíš poznámky pro mě:

* Pro konverzi používám aplikaci [IcoMoon](https://icomoon.io/app/). Pro import existujících ikon stačí naimportovat soubor `selection.json`. V něm jsou obsaženy jednak vektory stávajícíh ikon, zároveň i nastavení exportovaného fontu.

* Nové ikony se přidají nahráním SVG. Stávající ikony nemazat a nepřejmenovávat.

* Při buildu do ikonfontu nezapomenout změnit verzi fontu (ozubené kolečko vedle tlačítka). Ostatní nastavení by se mělo převzít z nahraného JSONu.

* V repozitáři pak nahraju celý obsah ZIPu do složky `dist`. Především jsou důležité soubory s fonty, vygenerované CSS a aktualizovaný JSON.