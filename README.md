# FarmHack 

[FarmHack](farmhack.nl) mobiliseert coders, creatieven en domeinexperts op vraagstukken van de boer.

## Bodemhack 2018

In drinkwatergebied ’t Klooster in de Achterhoek levert de bodem een dubbele prestatie; een productief gewas aan de bovenkant, en drinkwater aan de onderkant. Hoe zorgen we goed voor deze bodem? De centrale vraag van deze data-gedreven hackathon, georganiseerd door FarmHackNL, is:

Wat zijn bepalende factoren voor de bodemkwaliteit ten behoeve van grondwaterkwaliteit en landbouwproductie?

De drie initiatiefnemers Vitens, Provincie Gelderland en WUR stellen data beschikbaar waardoor unieke combinaties mogelijk worden.  Er zijn data op het gebied van bodem, agrarisch gebruik, (grond)waterkwaliteit en -kwantiteit.

## Data

### De Marke

Tijdens de hackathon zal data beschikbaar zijn over 

- [Weersgegevens 1994 - 2015](https://github.com/FarmHackNL/Bodemhack-2018/tree/master/data/Weersgegevens) (CSV)
- N balans per perceel (CSV)
- P balans per perceel (CSV)
- Bodemanalyses (CSV)
- Beregeningsdata - gegevens over de beregeningsregime van de percelen voor de jaren 1994 - 2017

### Provincie Gelderland

- [open data gelderland](https://opendata.gelderland.nl) (WMS/WFS) - een overzicht van alle beschikbare en herbruikbare vrije data van de provincie Gelderland
- [Geodata van Provincie Gelderland](http://geoserver.prvgld.nl/geoserver/web/?wicket:bookmarkablePage=:org.geoserver.web.demo.MapPreviewPage) (WMS/WFS). Data uit deze lijst die betrekking heeft op bodem en water zal tijdens de hackathon op een harde schijf beschikbaar zijn.
- RGB Luchtfoto's (WMS): `http://rasters.prvgld.nl/erdas-iws/ogc/wms/Luchtfoto_<jaar>`. Vervang `<jaar>` door 1992, 2005, 2012, 2015, 2016 of 2017 om de foto's van het desbetreffend jaar op te halen.

### Vitens

- [vitens.lizard.net](vitens.lizard.net) - grondwaterkwantiteitsgegevens en de locaties van de meetpunten
- Export uit DATALAB voor februari 2018 - grondwaterkwaliteitsgegevens per puilbuis en pompput (inclusief historie). Zie `data/Vitens/DATALAB documentatie.pptx` voor een overzicht van de beschikbare gegevens. De dataset wordt tijdens hackathon beschikbaar gemaakt. 

### WUR 

- [AgroDataCube](http://agrodatacube.wur.nl) (RESTful API) - A Big Open Data collection for Agri-Food Applications. De Cube bevat o.a. de volgende datasets:
  - Gewasregistratie van Nederland, 2012 – 2017.
  - Dagelijks weer van 50 KNMI meteostations, 01-01-1950 – 31-01-2018.
  - AHN2 data voor Nederland.
  - Per gewasperceel opvraagbaar:
    - AHN2 statistische informatie: count, sum, mean, stddev, min, max.
    - NDVI tijdserie (gemiddelde NDVI waarde per perceel, ongeveer 50 waarden per jaar), 2013 – 2017.
  - Bodemtypes 1:50.000, bepaald uit intersect van perceel met de Bodemkaart 1:50.000 uit 2014.
  - Info over de 50 KNMI meteostations, incl. locatie.
  - Administratieve grenzen van provincies, gemeente, postcodegebieden uit 2015.
  - Volledige lijst met gewascodes (van de gewasregistratie).
  - Volledige lijst met bodemtypes en bodemcodes (van de bodemkaart 1:50.000).
 - [NDVI](https://github.com/FarmHackNL/Bodemhack-2018/tree/master/data/NDVI) (GeoTIFF) - speciaal voor deze hackathon heeft [@robknapen](https://github.com/robknapen) een uitsnede gemaakt van de landelijke Normalized Difference Vegetation Index voor het gebied rondom "De Marke".
 
### Waterschap Rijn en IJssel

- [waterdata.wrij.nl](http://waterdata.wrij.nl) (CSV) - meetgegevens en -informatie over a) **waterhoeveelheden**: waterstanden en afvoeren van oppervlaktewateren, grondwaterstanden en neerslag en b) **waterkwaliteit**: chemische en ecologische kwaliteit van oppervlaktewateren
 
 
### Dirksen Management Support 

Voor deze hackathon maakt [DMS](https://www.dmsadvies.nl) de volgende datasets voor "De Marke" beschikbaar

- Gewas monsters - gegevens over o.a. Kalium, Nitraat, Calcium en vele andere gehaaltes in het gewas rondom "De Marke"
- Bodem monsters - gegevens over o.a. Kalium, pH, stikstof en vele andere gehaaltes in de bodem rondom "De Marke" 
- [Kringloopwijzer](https://www.verantwoordeveehouderij.nl/nl/mijnkringloopwijzer/KringloopWijzer-6.htm) gegevens voor de jaren 2015, 2016 en 2017

### Overige bronnen

- [Het Nationaal Georegister](http://nationaalgeoregister.nl) - de vindplaats van geo-informatie van Nederland.
- [Publieke Dienstverlening Op de Kaart](https://www.pdok.nl/nl/pdok-producten) - digitale geo-informatie van de overheid

## Challenges

### 1. Data crunching

Praktijkcentrum de Marke van WUR is een melkveebedrijf en de grootste landeigenaar binnen het pilotgebied. Er zijn veel data beschikbaar over bv gewasrotatie, mest en kunstmestgebruik, specifieke teelthandelingen inclusief middelengebruik, veebezetting, opbrengsten etc. 


**Kernvragen**: Wat levert het op als we deze data combineren met gedetailleerde bodemkwaliteit- en (grond)waterkwaliteitsdata van Vitens? Wat leren we eruit voor beter bodemmanagement?

### 2. Waterbeschikbaarheid

In droge periodes lijdt landbouwproductie in het gebied onder watertekorten. Toch zijn er percelen die dan opvallend beter presteren dan andere, dit is te zien op satellietbeelden. Soms zijn verschillen niet direct verklaarbaar door voordehandliggende kenmerken als hoogte of bodemsoort. Het vermoeden is dat dit te maken heeft met organische stofgehalte van de bodem, of het moeilijker te duiden begrip ‘vitaler’ bodems. 

**Kernvragen**: Is op basis van data (gewashistorie, bodemanalyses) vast te stellen welke factoren deze verschillen beinvloeden? Volgen hieruit handelingsperspectieven voor bodemmanagement?

### 3. Perceelprestatie

De bodem vervult vele functies, van landbouwproductie tot talloze ecosysteemdiensten. Soms zijn de diverse functies van de bodem gebaat bij dezelfde zorg voor de bodem; zo is waterbergend vermogen goed voor boer én drinkwaterbedrijf. Maar wanneer teveel de nadruk gelegd wordt op één van deze functies, komt de ander in het gedrang. Terwijl binnen de afzonderlijke functies goed gemonitord wordt, is het geheel van prestaties van de bodem niet voor iedereen inzichtelijk.

Een moeilijkheid daarbij is de verschillende schaalnivo’s. Landbouwdata zijn gerangschikt op perceelsnivo; ook eventuele aanpassingen in management worden per perceel gedaan.

**Kernvragen**: Kun je de relatieve bijdrage van een perceel aan de drinkwaterfunctie bepalen? Hoe kun je het geheel van prestaties dat een perceel levert zichtbaar maken? En vervolgens: Hoe kun je die totale PerceelsPrestatie optimaliseren? Is inzichtelijk(er) te maken wat landgebruik op een specifiek perceel bijdraagt aan drinkwatervoorziening?

### 4. Gebiedsarrangement

[MaxiMi](https://www.farmhack.nl/winnaar-maximi-op-weg-naar-nieuw-mineralenbeleid/) is het resultaat van een eerdere FarmHack hackathon. Het is een gebiedsarrangement waarbij de kwaliteit van het oppervlaktewater sturend is voor het agrarisch management. MaxiMi is door het Ministerie van LNV onderkend als een waardevolle benadering voor de toekomst. 

**Kernvraag**: Er worden pilots voorbereid. Wat kan de MaxiMi-aanpak betekenen voor de Achterhoek?
