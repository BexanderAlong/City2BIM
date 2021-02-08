# RoadMap CityBIM-Plugin

## OGR
- Teil von GDAL f�r Verarbeitung von Vektordaten
- Viele Driver f�r Lesen bestimmter Datenformate

### Installation
- Folgende NuGet-Pakete m�ssen eingebunden werden:
  - [GDAL](https://www.nuget.org/packages/GDAL/)
  - [GDAL Native](https://www.nuget.org/packages/GDAL.Native/)

### Startpunkte f�r GDAL / OGR
- [Vector API Tutorial](https://gdal.org/tutorials/vector_api_tut.html)
  - Ist haupts�chlich f�r C / C++ und Python beschrieben. Aber die Grundkonzepte leicht auf C# �bertragbar
- [Geoprocessing with Python](https://learning.oreilly.com/library/view/geoprocessing-with-python/9781617292149/)
  - gut um Konzepte in OGR zu verstehen. Praktische Implementierung jedoch f�r Python
  - nur mit SLUB-Account

### Geometrie
- Noch nicht ganz klar, wie B�gengeometrien verarbeitet werden?
- Methoden sowohl f�r Ausgabe der Geometrie als lineare Approximation als auch mit B�gen verf�gbar
- Multipolygone k�nnen gelesen werden (ALKIS)

## Geodaten

### ALKIS
- Einlesen mit [OGR NAS-Driver](https://gdal.org/drivers/vector/nas.html#vector-nas)
- Geometrie und Sachdaten k�nnen gelesen werden --> kompletter Re-write ?

### INSPIRE Parcel-Data
- Einelesen mit [OGR GMLAS-Driver](https://gdal.org/drivers/vector/gmlas.html#vector-gmlas)?
- Vorteil: Flurst�cksdaten f�r ganz Europa?

### X-Planung
- Einelesen mit [OGR GMLAS-Driver](https://gdal.org/drivers/vector/gmlas.html#vector-gmlas)?
- Geometrie und Sachdaten k�nnen gelesen werden --> kompletter Re-write ?
- Welche Objekte sind wichtig? 


## Revit

### Site Subregion
- Performance sehr schlecht, wenn mehr als ca. 20 Subregions pro TopographySurface definiert werden!
```C#
	SiteSubRegion.Create()
```
- Noch mehr TopographySurfaces f�r Flurst�cke anlegen und diese in 10er- 20er Pakete erstellen?
  - Nachteil: Noch viel mehr "unn�tiges" Gel�nde in Revit-Dokument
- Anderes Revit-Bauteil verwenden? 

### Materialien
- F�r Alkis und XPlanung nach Umstrukturierung keine Materialdefinition mehr


## IFC-Export

### Umgebungsmodelle Master
- Revit Projektdateien neu aufsetzen? F�r verschiedene Rvt Versionen (2019, 2020, 2021)? --> dauert lange
- Export durchf�hren. Fehler dokumentieren


## Dokumentation
- �berarbeitung n�tig :(


## Abstandsfl�chen
- GeoOffice?
- Testdatensatz anfertigen
- Implementierung Vorschlag Zehrfeld?


## DataCat
?
