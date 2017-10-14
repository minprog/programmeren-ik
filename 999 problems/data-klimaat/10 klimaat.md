# Klimaat

![](temperatuur.png){:.inline}

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die door de ECA (European Climate Assessment) [beschikbaar](http://eca.knmi.nl/dailydata/predefinedseries.php) wordt gemaakt in grote data files. We beperken ons tot data die de maximum- en minimumtemperatuur beschrijft voor elke dag in De Bilt sinds 1901.

Bestanden:

<!-- TODO: nieuw bestand!!!-->
- <http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMax.txt>

Download het bestand, open ze en lees bovenin hoe de data gecodeerd is. We zien dat de maximum(minimum)-temperatuur op 1 januari 1901 -3.1(-6.8) graden Celsius was.

## Opdracht 2: Temperatuur data analyse

We gaan het data bestand analyseren en op basis van de data een aantal vragen beantwoorden. Dit alles gaan we presenteren in een Jupyter Notebook.

### Tussenstap 2: preprocessing
Zorg dat het databestand in dezelfde map staat als het net aangemaakt notebook. Dubbel check het even! Zodra je dat hebt gedaan, ga je de data preprocessen in het notebook. Maak een cell aan in het notebook dat het databestand opent, inleest, en wegschrijft als `temp.csv`. Zorg dat de eerste rij bestaat uit de kolomnamen, en de rijen daarop volgend uit alle waardes. Waardes scheid je door een komma, want anders zijn het ook geen Comma Seperated Values. Maak hierboven nog een Markdown Cell aan, en zet daarin het volgende stukje: `## preprocessing`, druk vervolgens op shift+enter. Zo krijg je een klein kopje boven jouw code, kunnen wij straks makkelijk nagaan waar alles staat!

### Tussenstap 3: Extremen
Tijd voor wat analyse! We gaan onderzoeken wat de maximale en minimale temperatuur gemeten is in De Bilt sinds het begin van de 20e eeuw. We gaan ook kijken op welke dagen dit was.

Maak weer twee nieuwe cellen aan. Zorg dat de eerste cell een markdown cell is met als kopje: extremen. Schrijf een stukje code in de tweede cell dat het databestand opent en de maximale en minimale temperatuur vind en uitprint. Dit doe je elk op een nieuwe regel, met daarnaast op welke dag deze temperatuur gemeten is. Als volgt:

    De maximale temperatuur was 34.5 graden op 13 mei 1967
    De minimale temperatuur was -1.0 graden op 7 aug 1990

Bovenstaande antwoorden zijn natuurlijk fout, je mag zelf de juiste waarden vinden. Let erop dat er twee kolommen zijn voor temperatuur in `temp.csv`! Om je wat extra uit te dagen willen we ook de datum in het bovenstaande formaat hebben, met de maanden niet in cijfers, maar in 3 letters. Het is handig om hier een functie voor te schrijven.

### Tussenstap 4: Vriesperiode

Maak twee cellen aan. Zorg dat de eerste cell een kopje is met daarin de titel vriesperiode. Zorg dat de tweede cell de lengte van de langste periode dat het aaneengesloten heeft gevroren (maximumtemperatuur onder de 0 graden Celsius) uitprint. Print daarnaast wat de laatste dag van deze vriesperiode was. Doe dit weer met de maand in 3 letters. Als volgt:

    De langste vriesperiode is 12 dagen en eindigde op 29 jun 1999.

### Tussenstap 5: Zomerse dagen

Maak twee cellen aan. Zorg dat de eerste cell een kopje is met als titel: zomerse dagen. We spreken van een zomerse dag als de maximumtemperatuur tenminste 25 graden Celcius was. Schrijf in de tweede cell een stukje code dat een grafiek maakt waarin voor elk jaar het aantal zomerse dagen weergegeven wordt. Zorg dat de jaartallen op de x-as staan, en het aantal zomerse dagen op de y-as. Vergeet geen labels langs de assen te plaatsen!

### Tussenstap 6: Eerste hittegolf

Maak twee cellen aan. Zorg dat de eerste cell een kopje is met als titel: eerste hittengolf. We spreken in Nederland van een hittegolf als de maximumtemperatuur ten minste vijf dagen achtereen minstens 25 graden Celsius was (zomerse dagen) waarvan ten minste op drie dagen 30 graden Celsius of meer (tropische dagen). Laat de tweede cell uitprinten wat het *eerste* jaartal is waarin er sprake was van een hittegolf volgens deze regels.

## Testen

Er zijn geen checkpy tests voor deze opdracht. Je zult daarom zelf nauwkeurig moeten nagaan of alle antwoorden kloppen! Vergeet niet voordat je deze opdracht inlevert even alle cells opnieuw te runnen, zo weet je zeker dat ze allemaal nog werken.
