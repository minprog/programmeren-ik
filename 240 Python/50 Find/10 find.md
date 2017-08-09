# find.py

In deze opdracht ga je de find opdracht van CS50 maken in Python. We maken deze ietsje lastiger, zo moet je dit keer ook jouw eigen haystack creëren. Ook vragen we je binary search te implementeren. Sorteren mag je aan de `sorted()` functie overlaten!

## Gebruik

	python find.py
	Usage: python find.py needle haystack_size [seed]

	python find.py 3
	Usage: python find.py needle haystack_size [seed]

	python find.py hello bye
	Usage: python find.py needle haystack_size [seed]

	python find.py 3 1000
	Found the needle in the haystack!

	python find.py 3 1
	Did not find the needle in the haystack

	python find.py 3 1000 5
	Found the needle in the haystack

Houd in je achterhoofd dat de haystack random gegenereerd is, bovenstaande uitkomsten zijn dus niet altijd juist! :)

## Specificatie

* Schrijf een programma genaamd `find.py` dat je aanroept met twee of drie integer command line argument: een needle, een haystack, en eventueel een seed voor de random generator.
* Worden er minder dan 2 of meer dan 4 command line argumenten gegeven, dan moet het programma een bericht printen en stoppen.
* Is één van de argumenten geen integer, dan moet het programma een bericht printen en stoppen.
* Genereer een haystack met als grootte het commandline argument `haystack_size`. Zorg dat de haystack is gevuld met enkel psuedorandom gegenereerde positieve integers tussen de 0 en 1000 (inclusief).
* Doorzoek de haystack op zoek naar de needle d.m.v. binary search. Afhankelijk van of de needle in de haystack zit print je `"Did not find the needle in the haystack"` of `"Found the needle in the haystack"`.


## Tips

* Schrijf functies!
* Een lijst kun je in Python sorteren met de `sorted()` functie. Zo komt er uit `sorted([3,2,1])` de lijst `[1,2,3]`.
* Je zult gebruik moeten maken van de `random` module. Deze kun je importeren met `import random`. En vervolgens kun je de functies van de `random` module gebruiken door eerst de module naam te typen, en vervolgens de functie: `random.random()` genereerd bijvoorbeeld een random float tussen 0 en 1.
* Kijk goed naar welke functies de random module jou geeft, `randint` is een handige! Google maar.
* Implementeer zo snel mogelijk het `seed` argument, zo krijg je constant dezelfde haystack. Dat maakt het een stuk makkelijker om te debuggen! Je kan de random module seeden d.m.v. `random.seed(JOUW_SEED_ARGUMENT)`.
* Test jouw programma grondig, ook zonder `checkpy`. Je kan heel simpel dubbelchecken of de needle in de haystack zit d.m.v. de volgende regel python code `needle in haystack`. Dit laat Python d.m.v. linear search door de haystack gaan (als haystack een lijst is) en geeft `True` of `False` afhankelijk van of de needle in de haystack zit.


## Testen

	checkpy find
