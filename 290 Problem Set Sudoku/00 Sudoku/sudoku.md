# Sudoku Solver
Behalve programma's ontwikkelen voor eindgebruikers kunnen we programmeren ook inzetten om problemen / puzzels op te lossen. Een klassiek voorbeeld hiervan is een sudoku solver.

Sudoku's zijn je waarschijnlijk wel bekend. Ze zien er zo uit:

![](sudoku_example.png)

Een grid met 9x9 vakjes. In elke vakje moet uiteindelijk een getal tussen de 1 t/m 9 komen te staan. Maar, er zijn drie restricties:

* elke horizontale rij mag maar één van elk getal bevatten
* elke verticale kolom mag maar één van elk getal bevatten
* elk 3x3 blok mag maar één van elk getal bevatten (zie ook de donkere lijnen op het grid)

## What to do
* Implementeer een regelgebaseerde solver
* Implementeer een iteratieve DFS solver
* Implementeer een recursieve DFS solver
* (Optioneel) Implementeer een interatieve DFS solver met Python generators

# Regelgebaseerde solver
Er zijn ontzettend [veel strategieën](http://www.sudokudragon.com/sudokustrategy.htm) om een sudoku puzzel op te lossen. Zo heb je o.a. de "Single possibility rule" die luidt als volgt: Als er maar één mogelijkheid over is voor een vakje, dan moet je deze wel invullen. Deze regel is ontzettend handig! Want zodra je dat vakje invult, kan het zomaar zijn dat er maar één optie overblijft voor een ander vakje. Die kun je vervolgens ook weer invullen. Typisch bij het oplossen van een Sudoku zul je merken dat je tegen het einde d.m.v. deze regel een heel hoop vakjes kan invullen.

We zouden een oplosser kunnen maken op basis van de "single possibility rule". Door het continue toepassen van de regel kan totdat de sudoku is opgelost. In psuedocode:

    while sudoku is not solved
        for every tile in sudoku
            if tile is empty and there is just one possibility
                fill in tile
