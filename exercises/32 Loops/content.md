# Exercises: Loops

Deze oefening is anders dan je gewend bent van het basisboekje. Zo ga je zelf algoritmes schrijven. Hier kan je goed laten zien wat je geleerd hebt van de programmeeropdrachten die je tot nu toe hebt gemaakt.

Dit onderwerp kan je niet met het basisboek voorbereiden. Algoritmes schrijven leer je vooral door het te doen. Het is dus belangrijk om nog eens goed te kijken naar de opdrachten die je tot nu toe gemaakt hebt.

> De antwoorden op het toetsje hiervoor moet je schrijven als C-code. Hierbij hoef je niet op de puntkomma's te letten, maar het moet ook geen pseudocode zijn. Soms is het ook nodig om C-specifieke functies te gebruiken zoals `strlen()`. Schrijf dus zo netjes mogelijk C.

De onderwerpen die aan bod zullen komen:  

## Loops

* do-while: Kijk hiervoor nog eens naar de [input validatie](https://prog1.mprog.nl/problems/mario-less#specification) die je in Mario nodig had.
* for: Kijk nog eens hoe je een blok van hekjes ([mario block](https://prog1.mprog.nl/problems/mario-less#block)) en een pyramide  ([mario left pyramid](Mario-less)) hebt gemaakt.

### Oefeningen

Schrijf een loop die de variabele `n` vult met invoer van de gebruiker (\`get_int()\`). De ingevoerde waarde moet negatief zijn.

`int n;`

Print een piramide van `#`-jes van hoogte `h`. Bijvoorbeeld een piramide van hoogte 4 ziet er als volgt uit:

    #
    ##
    ###
    ####


    int h = 6;

## Strings

* strings: Oefen nog een keer met het doorlopen en selectief printen van strings zoals in [initials](https://prog1.mprog.nl/problems/initials-less).
* ascii: Zorg ervoor dat je weet hoe je ascii waardes kan manipuleren zoals in [Caesar](https://prog1.mprog.nl/problems/caesar). Het zal zeker niet zo complex worden als caesar en je hoeft ook zeker niet de ascii-tabel uit je hoofd te kennen, maar je moet wel eenvoudige op ascii gebaseerde conversies kunnen doen.

### Oefeningen

Schrijf een loop die van alle woorden in de string `tale` de laatste letter uitprint.

```
string tale = "It was the best of times";
```

Schrijf een loop die van de string `bob` de hoofdletters uitprint.

```
string bob = "pRoGgRaMmInG In c";
```

Print de string `knight`, maar vervang daarbij alle letters 'a' door een 'o'.

```
string knight = "Batman";
```
