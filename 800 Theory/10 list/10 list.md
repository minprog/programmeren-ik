# List

## Definitie
Python heeft een aantal datastructuren in de taal ingebouwd, één zo'n structuur is een `list`. Een list is een muteerbare geordende verzameling.  Laten we even goed kijken naar wat dat precies inhoud.

- Een list is muteerbaar, dat betekent dat je de verzameling kan aanpassen (muteren). Ofwel, we kunnen er elementen uit verwijderen en aan toevoegen.
- Een list is geordend, dat betekent dat de elementen in de verzameling een volgorde kennen. De volgorde waarin je elementen toevoegt aan de list maakt dus uit.

## Waarvoor / wanneer
Een list kun je heel goed gebruiken op plekken waar je arrays zou gebruiken in C. Ze zijn ook heel vergelijkbaar! Een verschil is wel, lists kun je uitbreiden. Je hoeft niet vooraf een grootte op te geven.

Lists snel O(1) in verschillende operaties zoals:

- Het ophalen van elementen op een index (welk element staat er op plek 3?)
- Het toevoegen van elementen aan het einde van de lijst
- Het verwijderen van het element op de laatste index
- Het updaten van een element op een index

En langzamer O(n) in andere operaties:

- Het opzoeken van een element (staat element E in list L?)
- Het verwijderen van elementen op basis van index (behalve de laatste index)
- Het toevoegen van een element op een andere index dan aan het einde van de list

## Code
Een list maak je zo aan:

    numbers = [1,3]
    print(numbers)

Hiervoor gebruik je in Python de blokhaken (`[]`). Wil je een lege list aanmaken, dan kan dat zo:

    numbers = []
    numbers.append(1)
    numbers.append(3)
    print(numbers)

Bovenstaande stukje code maakt een lege list en voegt de elementen 1 en 3 aan het einde van de list toe toe. Behalve toevoegen kunnen we natuurlijk ook verwijderen:

    numbers = [1,3]
    del numbers[0]
    print(numbers)

Updaten van elementen in de list gaat als volgt:

    numbers = [1,3]
    numbers[0] = 2
    numbers[1] = 4
    print(numbers)

Een list is geordend. Dat betekent dat de datastructuur een volgorde kent. Het maakt dus uit waar je elementen toevoegt, en in welke volgorde.

    numbers = []
    numbers.append(1)
    numbers.append(3)
    print(numbers)
    numbers = []
    numbers.append(3)
    numbers.append(1)
    print(numbers)
