# Adventure Game
Lang geleden waren text-based adventure games bijzonder populair. Dat zijn type spellen waar je tekst te zien krijgt, en door het invoeren van tekst verder komt in het spel. Eén zo'n spel is afkomstig van [William Crowther](https://en.wikipedia.org/wiki/William_Crowther_(programmer)) die in 1975 de basis legde voor text-based adventure games in zijn spel Colossal Cave, of beter bekend als Adventure.

In Adventure bevind je je in verschillende "rooms", en kan je tussen deze rooms navigeren door middel van tekst commando's. Bijvoorbeeld zo:

    You are standing at the end of a road before a small brick
    building. A small stream flows out of the building and
    down a gully to the south. A road runs up a small hill
    to the west.
    > WEST
    You are at the end of a road at the top of a small hill.
    You can see a small building in the valley to the east.
    > EAST
    Outside building.
    >

Door middel van instructies zoals West/East, maar ook bijvoorbeeld In/Out en North/South navigeer je tussen de kamers. In Adventure kan je meer dan enkel navigeren, zo kan je ten alle tijden het `HELP` commando typen voor uitleg over het spel. Het `LOOK` commando om de uitgebreide beschrijving van de kamer te zien. Zo zag je in het voorbeeld hierboven dat wanneer de kamer voor de tweede keer bezocht werd je enkel een korte beschrijving te zien kreeg. Zo je nu `LOOK` gebruiken dan gebeurt het volgende:


    > LOOK
    You are standing at the end of a road before a small brick
    building. A small stream flows out of the building and
    down a gully to the south. A road runs up a small hill
    to the west.
    >

In Adventure heb je ook objecten. Deze objecten bevinden zich in kamers en kun je als speler oppakken (`TAKE <obj>`) en laten vallen (`DROP <obj>`). Ten alle tijden kun je kijken wat je in je bezit hebt d.m.v. `INVENTORY`. Zo kom je de volgende situatie tegen in het spel:

    Inside building
    You are inside a building, a well house for a large spring.
    There is a a set of keys here
    > TAKE keys
    Taken.
    > INVENTORY
    KEYS, a set of keys
    > DROP keys
    Dropped.
    > INVENTORY
    inventory is empty.
    >

Op basis van deze objecten navigeer je op een andere manier door verschillende kamers. Heb je de sleutels in het bezit, dan kan je in de volgende kamer door de "strong steel grate", anders niet.

    You are in a 20-foot depression floored with bare dirt.
    Set into the dirt is a strong steel grate mounted in
    concrete.  A dry streambed leads into the depression from
    the north.
    > DOWN
    Beneath grate
    You are in a small chamber beneath a 3x3 steel grate to
    the surface.  A low crawl over cobbles leads inward to
    the west.
    >

# What to do

* Implementeer Crowther's Adventure
* Laad de data uit de meegeleverde bestanden in
* Start het spel, en laat de speler commando's invoeren
* Voer de commando's van de speler uit

## Om te beginnen
Bij deze opdracht leveren we data & code mee. Deze kun je [hier downloaden](https://github.com/Jelleas/adventure/archive/master.zip)

Je vindt hier 5 databestanden voor 3 versies van Adventure. `TinyRooms.txt` is de kleinste versie, dit is een spel met maar 3 kamers. Een goed punt om mee te beginnen! `SmallRooms.txt` en `SmallObjects.txt` is net ietsje groter, hier worden ook objecten bij gebruikt. Het volledige spel, de gehele dataset voor Adventure vind je in `CrowtherRooms.txt` en `CrowtherObjects.txt`.

Ook vind je 1 .py bestand genaamd `adventure.py`. Daarin vind je verschillende classes, functies en meerdere `#TODO`s. Hierin ga jij straks aan de slag!

## Stap 1: Kamers
In `TinyRooms.txt`, de kleinste instantie van het spel, vind je de volgende data:

    1
    Outside building
    You are standing at the end of a road before a small brick
    building.  A small stream flows out of the building and
    down a gully to the south.  A road runs up a small hill
    to the west.
    -----
    WEST     2
    UP       2
    NORTH    3
    IN       3

    2
    End of road
    You are at the end of a road at the top of a small hill.
    You can see a small building in the valley to the east.
    -----
    EAST     1
    DOWN     1

    3
    Inside building
    You are inside a building, a well house for a large spring.
    -----
    SOUTH     1
    OUT       1

Dit zijn de beschrijvingen van alle kamers in het spel, en hoe je van 1 kamer naar een ander komt. Elke kamer beschrijving bestaat uit 4 delen:

    <id>
    <name>
    <description>
    ----
    <routes>

Nu moeten we deze data inlezen zodat we straks in het spel tussen de verschillende kamers kunnen navigeren. Aangezien een kamer wat ingewikkelder is dan enkel een nummer of een string introduceren we hiervoor een nieuwe class genaamd `Room` in `adventure.py`. Ook introduceren we een functie genaamd `loadRooms` die verantwoordelijk is voor het inlezen van de rooms uit het bestand dat we willen inladen.

Het is aan jou om `Room` en `loadRooms` te implementeren. __Belangrijk__ negeer voor nu de routes, dit tackelen we in stap 2. Je kan je code testen door onderaan het bestand `stap 1` en de bijbehorende code te uncommenten. Je zou dan bij het runnen van de code het volgende moeten krijgen:

    stap 1
    room 1: Outside building
    room 2: End of road
    room 3: Inside building

## Stap 2: Routes
