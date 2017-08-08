# Comprehensions

In Python heb je comprehensions om op één regel een collectie aan te maken. We gaan binnen deze cursus enkel focus leggen op `list` comprehensions. Houd wel in je achterhoofd dat er meer bestaan!

Een comprehension is eigenlijk niet meer dan een for-loop op een regel om een collectie te maken. In het geval van een `list` comprehension maken we dus op één regel een `list`. Dit ziet er als volgt uit:

    some_list = [i*2 for i range(10)]

Bovenstaande creeërt een lijst met alle tweevouden van 0 t/m 18, oftewel `[0,2,4,6,8,10,12,14,16,18]`. Je leest dit als volgt: zet voor elke `i` in `range(10)` `i*2` neer in de lijst. Het is effectief een korte manier om het volgende voor elkaar te krijgen:

    some_list = []
    for i in range(10):
        some_list.append(i * 2)
