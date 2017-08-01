# Klimaat

![](temperatuur.png){:.inline}

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die door de ECA (European Climate Assessment) [beschikbaar](http://eca.knmi.nl/dailydata/predefinedseries.php) wordt gemaakt in grote data files. We beperken ons tot data die de maximum- en minimumtemperatuur beschrijft voor elke dag in De Bilt sinds 1901.

Bestanden:

- <http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMax.txt>
- <http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMin.txt>

Download de bestanden, open ze en lees bovenin hoe de data gecodeerd is. We zien dat de maximum(minimum)-temperatuur op 1 januari 1901 -3.1(-6.8) graden Celsius was.

## Opdracht 2

We gaan de twee data bestanden analyseren en op basis van de data een aantal vragen beantwoorden. Dit alles gaan we presenteren in een IPython notebook.

## Tussenstap 1: preprocessing

## Tussenstap 2: IPython notebook intro

## Tussenstap 3: Extremen
Maak een bestand `temperatuur.py`. Wat waren de hoogste en laagste temperatuur die in De Bilt zijn gemeten sinds het begin van de 20e eeuw? Op welke dagen was dat? Zorg dat je programma de datum netjes op het scherm print. Zeg dus niet:

     Max 34.5 op 19670513

maar      

     De hoogste temperatuur was 34.5 graden Celcius, en werd gemeten op 13 mei 1967.

Tip: maak een aparte functie die een getal als `19670513` kan omzetten naar een goed leesbare beschrijving als `13 mei 1967`.

### Tussenstap 4: Vriesperiode

Print de langste periode dat het aaneengesloten heeft gevroren (maximumtemperatuur onder 0◦C). Print op de volgende regel de datum van de laatste dag van deze periode?

### Tussenstap 5: Zomerse dagen

We spreken van een zomerse dag als de maximumtemperatuur meer dan 25 graden Celcius was. Op een tropische dag is het in de Bilt zelfs 30 graden. Maak een grafiek waarin voor elk jaar het aantal zomerse dagen weergegeven wordt.

### Tussenstap 6: Eerste hittegolf

We spreken in Nederland van een hittegolf als de maximumtemperatuur ten minste vijf dagen achtereen minstens 25 graden Celsius was (zomerse dagen) waarvan ten minste op drie dagen 30 graden Celsius of meer (tropische dagen). Print het *eerste* jaartal uit de dataset waarin er sprake was van een hittegolf volgens deze regels.
