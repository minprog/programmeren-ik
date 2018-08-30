# Python 101
Je duikt straks een nieuwe taal in. Dan zul je merken dat je eigenlijk al heel veel dingen kent, maar er in de basis een paar kleine verschillen zijn. Voornamelijk de syntax is net even anders. Daarom vind je hier de concepten die je al kent uit C, maar dan in Python. Bij elk concept staan kleine code-snippets die je kan uitvoeren in de interpreter. Dan zie je meteen hoe het werkt, en kan je er ook even mee spelen.

## Variabelen
Python is een programmeertaal met een dynamisch type systeem. Dit houdt in het geval van Python in dat variabelen niet meer zijn dan namen die je toekent aan waardes. De namen zelf kennen geen type. Waar je dus in C bij elke variabele moest aangeven van welk type die is, is dat in Python niet meer nodig / mogelijk. Probeer maar eens:

    i = 6
    s = "hello"
    i = s
    print(i)

## If statements
Python kent net zoals C (en vele andere programmeertalen) if-statements en daarbij behorende else statements. Eén klein verschil, `else if` heet in Python `elif`. Dit ziet er dan als volgt uit:

    x = 20
    if x > 30:
        print("foo")
    elif x < 10:
        print("bar")
    else:
        print("baz")

## For-loops
Python kent geen "normale" for-loop zoals C die wel kent: een for-loop met een initialisatie stap, een conditie en een update stap. In plaats daarvan kent Python enkel de zogenaamde "for each" loop. Je spreekt hem als volgt uit: voor elk element in verzameling doe iets. Daarom dus ook "for each"!

Zo'n soort loop is bijzonder handig, zo kan je bijna geen infinite loops meer schrijven. Hij ziet er als volgt uit:

    for letter in "hello":
        print(letter)

    for number in [1,2,3]:
        print(number * 2)

    for i in range(3):
        print(i)

In het stukje code wordt de `range` functie gebruikt. Dat is een functie die een reeks integer getallen genereerd. Je kan hem als volgt gebruiken:

    range(5) # genereert 0,1,2,3,4
    range(1,5) # genereert 1,2,3,4
    range(1,10,2) # genereert 1,3,5,7,9

## While-loops
De do-while loop bestaat niet in Python. Een beetje Python filosofie: "There should be one-- and preferably only one --obvious way to do it.". Daarom dus geen do-while loops. De normale while loop bestaat wel en ziet er als volgt uit:

    x = 10
    while x > 1:
        x = x / 2
        print(x)

## Functies
Functies in Python lijken heel erg op die in C. Echter, ze zijn een stuk soepeler. Je hoeft namelijk niet te specificeren wat de type van de argumenten hoeven te zijn, of welk type de functie `return`ed. Kijk maar:

    def add(a, b):
        return a + b

    x = add(3, 5)
    print(x)
    print(add("hello", "bye"))

Zo kan je dus functies schrijven die bijvoorbeeld werken op integers en floats, maar ook op strings.

## Lists
Vergeet de term array voor nu, Python heeft in plaats daarvan lists. Subtiel verschil, lists zijn precies even groot als het aantal elementen dat erin zit. Je kan ook blijven toevoegen en verwijderen. Ze schalen dus mee! Zie hier:

    items = [1,2,3]
    items.append("hello")
    del items[0]
    items.remove(2)
    print(items)
