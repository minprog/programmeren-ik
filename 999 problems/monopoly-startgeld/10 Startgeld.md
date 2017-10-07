# Monopoly: Startgeld

![](GoldenDollar.png){:.inline}{: style="width:20%"}

In een normaal potje Monopoly krijg je 1500 euro startgeld en verdien je 200 euro elke   
keer dat je start passeert. Zo'n eindige hoeveelheid startgeld heeft invloed op de snelheid 
waarmee je nieuwe straten kan kopen. In deze opdracht zoeken we uit welk effect dit precies 
heeft.


## Gebruik

	python startgeld.py
	0 euro, 2197 worpen
	500 euro, 1997 worpen
	1000 euro, 1888 worpen
	1500 euro, 1750 worpen
	2000 euro, 1560 worpen
	2500 euro, 1424 worpen

> Natuurlijk zijn ook de antwoorden hierboven fout. Het goede antwoord mag je zelf simuleren.


## Specificatie

* Schrijf een programma genaamd startgeld.py voor elke hoeveelheid startgeld van 0 t/m 2500 in stappen van 500 het aantal worpen dat nodig is om alle straten te kopen onder elkaar uitprint.
* Elke keer dat de pion start passeert krijgt de speler 200 euro extra. 
* Simuleer elke hoeveelheid een goed aantal keer, zodat het antwoord niet te veel varieert. Houd hierbij rekening met de maximaal 10 seconden die checkpy je geeft.
* Laat het programma ook een grafiek maken met op de x-as de verschillende hoeveelheden startgeld, en op de y-as het aantal worpen wanneer alles is opgekocht.
* Vergeet geen labels langs de assen van de grafiek te plaatsen.


## Tips:

* Gebruik en importeer `trump.py` d.m.v. `import trump`
*  

Maak een nieuw bestand aan genaamd startgeld.py binnen dezelfde folder als de vorige opdracht.
Simuleer nu Monopoly spellen met een variabele hoeveelheid startgeld in stappen van 500 euro, startend bij 0 euro, oplopend t/m 2500 (inclusief!).
Elke keer dat de pion start passeert krijgt de speler 200 euro extra. 
Maak een grafiek met op de x-as de verschillende hoeveelheden startgeld, en op de y-as het aantal worpen wanneer alles is opgekocht.
Draai een goed aantal simulaties per hoeveelheid startgeld, let erop dat het niet te lang duurt. Een paar seconden is prima.

Behalve de grafiek, print voor elke hoeveelheid startgeld het aantal worpen dat nodig is om alle straten te kopen onder elkaar uit.
Als volgt:

	0 euro, 155 worpen
	500 euro, 147 worpen
	1000 euro, 144 worpen
	...
	2500 euro, 132 worpen

Let op: bovenstaande aantal worpen zijn fout! Het goede antwoord mag je zelf simuleren.


## Testen

	checkpy startgeld
	