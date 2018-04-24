# Sudoku Solver
Behalve programma's ontwikkelen voor eindgebruikers kunnen we programmeren ook inzetten om problemen / puzzels op te lossen. Een klassiek voorbeeld hiervan is een sudoku solver.

Sudoku's zijn je waarschijnlijk wel bekend. Ze zien er zo uit:

![](sudoku_example.png)

Een grid met 9x9 vakjes. In elk vakje moet uiteindelijk een getal tussen de 1 t/m 9 komen te staan. Maar, er zijn drie restricties:

* elke horizontale rij mag maar één van elk getal bevatten
* elke verticale kolom mag maar één van elk getal bevatten
* elk 3x3 blok mag maar één van elk getal bevatten (zie ook de donkere lijnen op het grid)

## What to do
* Implementeer een regelgebaseerde solver
* Implementeer een iteratieve DFS solver
* Implementeer een recursieve DFS solver
* (Optioneel) Implementeer een interatieve DFS solver met Python generators

## Om te beginnen
Bij deze opdracht leveren we data & code mee. Deze kun je [hier downloaden](https://github.com/Jelleas/sudoku/archive/master.zip)

Je vindt hier twee mapjes: `easy` en `hard`. Met daarin, je raadt het al, makkelijke en moeilijke sudoku's. In het zelfverzonnen sudoku bestandstype. Een .sudoku ziet er zo uit:

    7,9,0,0,0,0,3,0,1
    0,0,0,0,0,6,9,0,0
    8,0,0,0,3,0,0,7,6
    0,0,0,0,0,5,0,0,2
    0,0,5,4,1,8,7,0,0
    4,0,0,7,0,0,0,0,0
    6,1,0,0,9,0,0,0,8
    0,0,2,3,0,0,0,0,0
    0,0,9,0,0,0,0,5,4

Waarin er op elke regel 9 cijfers staan. Een 0 staat voor een leeg vakje, en elk ander cijfer voor een ingevuld vakje met dat cijfer.

Ook vind je het bestand `solver.py`. Hierin ga jij straks aan de slag.

# Regelgebaseerde solver
Er zijn ontzettend [veel strategieën](http://www.sudokudragon.com/sudokustrategy.htm) om een sudoku puzzel op te lossen. Een simpele aanpak is via  de "Single possibility rule" die luidt als volgt: Als er maar één mogelijkheid over is voor een vakje, dan moet je deze wel invullen. Deze regel is ontzettend handig! Want zodra je dat vakje invult, kan het zomaar zijn dat er maar één optie overblijft voor een ander vakje. Die kun je vervolgens ook weer invullen. Typisch bij het oplossen van een Sudoku zul je merken dat je tegen het einde d.m.v. deze regel een heel hoop vakjes kan invullen.

Jij gaat straks een oplosser maken op basis van de "single possibility rule". Door het continue toepassen van de regel kan totdat de sudoku is opgelost. In psuedocode:

    while sudoku is not solved
        for every tile in sudoku
            if tile is empty and there is just one possibility
                fill in tile

Niet alle sudoku's zijn op deze manier op te lossen, zeker niet die sudoku's die als moeilijk worden bestempeld. Maar, de simpelere puzzels kunnen we d.m.v. dit algoritme wel oplossen.

## Sudoku's inladen
Implementeer allereerst de `load()` functie in `solver.py`. Deze functie accepteert een `filename` als argument en geeft de ingeladen sudoku terug. Een sudoku representeer je simpelweg met een lijst van lijsten, een 2D lijst.

Je kan jouw implementatie van `load()` in de interpreter testen:

    >>> from solver import load
    >>> load("easy/puzzle1.sudoku")
    [[7, 9, 0, 0, 0, 0, 3, 0, 1], [0, 0, 0, 0, 0, 6, 9, 0, 0], [8, 0, 0, 0, 3, 0, 0, 7, 6], [0, 0, 0, 0, 0, 5, 0, 0, 2], [0, 0, 5, 4, 1, 8, 7, 0, 0], [4, 0, 0, 7, 0, 0, 0, 0, 0], [6, 1, 0, 0, 9, 0, 0, 0, 8], [0, 0, 2, 3, 0, 0, 0, 0, 0], [0, 0, 9, 0, 0, 0, 0, 5, 4]]
    >>>

## Sudoku's printen
Het is handig om makkelijk inzicht te kunnen krijgen in wat je aan het programmeren bent. Daarom is het nu handig om de `show()` functie te implementeren. De `show()` functie print een sudoku uit als volgt:


    >>> from solver import load, show
    >>> show(load("easy/puzzle1.sudoku"))
    7 9 _   _ _ _   3 _ 1
    _ _ _   _ _ 6   9 _ _
    8 _ _   _ 3 _   _ 7 6

    _ _ _   _ _ 5   _ _ 2
    _ _ 5   4 1 8   7 _ _
    4 _ _   7 _ _   _ _ _

    6 1 _   _ 9 _   _ _ 8
    _ _ 2   3 _ _   _ _ _
    _ _ 9   _ _ _   _ 5 4
    >>>

Let op de details:
  - Eén spatie tussen elk vakje
  - Drie spaties tussen de blokken (horizontaal)
  - Eén witregel tussen de blokken (verticaal)
  - Voor de lege plekken print je een `_`

## Possibilities

## Solve_rule

## Solve_dfs_it

## Solve_dfs_rec

## (Opt) solve_dfs_gen
