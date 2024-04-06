# Mapa inwestycji gminnych

Celem wspólnego projektu realizowanego w ramach [Sieci Analityków Danych Miejskich](https://danemiejskie.pl/) było stworzenie wizualizacji mapowej inwestycji w gminie oraz udokumentowanie procesu tworzenia wizualizacji w celu zapewnienia jego replikowalności i transferowalności.

> [!NOTE]
> 🔎🗺️ [Zobacz webmapę](https://mchmurkowski.github.io/adm-mapa-inwestycji/).
>
> Dane prezentowane na webmapie mają charakter poglądowy i zostały wygenerowane przy pomocy [generatora danych testowych](https://github.com/mchmurkowski/adm-mapa-inwestycji#generator-danych-testowych) dla obszaru Siemianowic Śląskich.
>
> Webmapa hostowana przy pomocy [GitHub Pages](https://pages.github.com/).

## Jak korzystać?

Pobranie repozytorium: `git clone https://github.com/mchmurkowski/adm-mapa-inwestycji.git`.

### Generator danych testowych

[Generator danych testowych](generator/test-data-generator.ipynb) pozwala wygenerować testowy zbiór danych inwestycji w postaci pliku .csv, który można wykorzystać przy tworzeniu projektu w QGIS.

> [!TIP]
> Notatnik (plik) można otworzyć i dostosować do własnych potrzeb np. w [Jupyter Notebook/Lab](https://jupyter.org/) czy [Google Colab](https://colab.research.google.com/). W celu prawidłowego działania wymagana będzie instalacja bibliotek [Faker](https://faker.readthedocs.io/en/master/) i [pandas](https://pandas.pydata.org/docs/). 

### Projekt QGIS

Przykładowy projekt [QGIS](https://www.qgis.org/pl/site/) dostępny jest w formie pliku GeoPackage (`adm-mapa-inwestycji.gpkg`) w folderze [qgis](qgis/). Plik zawiera zarówno projekt, jak i warstwy.

> [!TIP]
> W celu otwarcia projektu w QGIS należy wybrać *Projekt* 👉 *Otwórz z* 👉 *GeoPackage ...*, a w oknie dialogowym w polu *Połączenie* wskazać pobrany plik .gpkg oraz wybrać nazwę projektu w polu *Projekt*.

> [!IMPORTANT]
> Ewentualne zdjęcia inwestycji będzie należało ponownie przyporządkować w tabeli atrybutów warstwy *Inwestycje* w polu *foto_sciezka*. 

### Wzorzec

Udostępniamy specjalny wzorzec [adm-mapa-inwestycji.html](template/adm-mapa-inwestycji.html), który został przygotowany na potrzeby projektu i jest wykorzystywany przez wtyczkę [qgis2web](https://github.com/qgis2web/qgis2web) do wygenerowania strony internetowej z webmapą. Wzorzec wykorzystuje bibliotekę CSS [Bulma](https://bulma.io/).

> [!IMPORTANT]
> W celu skorzystania ze wzorca należy go umieścić we właściwym folderze wtyczki qgis2web. Aby odnaleźć folder w QGIS, należy wybrać *Ustawienia* 👉 *Profile użytkownika* 👉 *Otwórz katalog aktywnego profilu*, a po otwarciu katalogu plik wzorca umieścić w folderze `python/plugins/qgis2web/templates/`.