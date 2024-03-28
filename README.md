# Mapa inwestycji gminnych

Wspólny projekt realizowany w ramach [Sieci Analityków Danych Miejskich](https://danemiejskie.pl/).

> [!Note]
> 🔎🗺️ [Zobacz webmapę](https://mchmurkowski.github.io/adm-mapa-inwestycji/).
> Webmapa hostowana przy pomocy [GitHub Pages](https://pages.github.com/).

## Cel projektu

Stworzenie wizualizacji mapowej inwestycji w gminie. Udokumentowanie procesu tworzenia wizualizacji w celu zapewnienia jego replikowalności i transferowalności.

### Potencjalni odbiorcy projektu

- mieszkańcy
- przedstawiciele NGOs
- dziennikarze
- badacze / studenci
- przedsiębiorcy
- kadra zarządzająca
- współpracownicy
- pracownicy innych urzędów / instytucji

## Generator danych testowych

[Generator danych testowych](https://github.com/mchmurkowski/adm-mapa-inwestycji/blob/main/generator/test-data-generator.ipynb) pozwala wygenerować testowy zbiór danych inwestycji w postaci pliku csv, który można wykorzystać przy tworzeniu projektu w QGIS.

## Projekt QGIS

Przykładowy projekt QGIS dostępny jest w formie pliku GeoPackage (`adm-mapa-inwestycji.gpkg`) w folderze [qgis](https://github.com/mchmurkowski/adm-mapa-inwestycji/tree/main/qgis).

## Wzorzec

Udostępniamy specjalny wzorzec [adm-mapa-inwestycji.html](https://github.com/mchmurkowski/adm-mapa-inwestycji/blob/main/qgis/template/adm-mapa-inwestycji.html), który został przygotowany na potrzeby projektu i jest wykorzystywany przez wtyczkę [qgis2web](https://github.com/qgis2web/qgis2web) do wygenerowania strony internetowej z webmapą. Wzorzec wykorzystuje bibliotekę CSS [Bulma](https://bulma.io/).

> [!TIP]
> W celu skorzystania ze wzorca należy go umieścić we właściwym folderze wtyczki qgis2web.