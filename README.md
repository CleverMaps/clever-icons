# clever-icons

Tento repozitář rozšiřuje sadu ikon [Font Awesome](https://fontawesome.com/v4.7.0/icons/) o několik ikon, které nám chyběly.

## Použití

* Ručně: viz soubor `demo.html`.
* Balíčkovačem: importovat `fonts` a `style.css`.

Pro soulad s _Font Awesome_ je vhodné ve vlastním CSS třídě `.ci` nastavit stejné vlastnosti, jaké má třída `.fa` (např preprocesorem), nebo alespoň nastavit `font-size: 14px`.

## Přispívání

* Zdrojové ikony jsou nakresleny jako SVG v gridu 14×14 px. Vektory jsou optimalizovány, aby v této velikosti co nejvíc seděly na pixelovou mřížku. 

* Prosím ukládat jako `Plain SVG` – osekají se tak zbytečné tagy a soubor je menší a přehlednější. Taky je vhodné nějakým pluginem zaokrouhlit souřanice bodů, ať nejsou na milion desetinných míst.

* Zdrojové ikony se ukládají do adresáře `src`. Pak pullrequest.

## Buildování

Ideálně zbuilduji sám, toto jsou spíš poznámky pro mě:

* Pro konverzi do ikonfontu používám webovou aplikaci [IcoMoon](https://icomoon.io/app/). Pro import existujícíh ikon do ní stačí naimportovat soubor `selection.json`. V něm jsou obsaženy jednak vektory stávajícíh ikon, zároveň i nastavení exportovaného fontu.

* Nové ikony se přidají nahráním SVG. Stávající ikony nemazat a nepřejmenovávat.

* Při buildu do ikonfontu nezapomenout změnit verzi fontu (ozubené kolečko vedle tlačítka). Ostatní nastavení by se mělo převzít z nahraného jsonu.

* V repozitáři pak nahraju všechny soubory do složky `dist`. Především jsou důležité soubory s fonty, vygenerované CSS a aktualizovaný JSON.