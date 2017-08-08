# Dictionary

Python heeft een aantal datastructuren standaard in de taal gebouwd. Eén daarvan is een zogenaamde dictionary, ofwel `dict` in het kort. Een `dict` is een datastructuur die in tegenstelling tot een `list` geen indices kent. In plaats daarvan werkt een `dict` met **key-value pairs**. Je hebt sleutels die bijbehorende waarden kunnen ophalen. Laten we gelijk kijken naar een voorbeeld:

    last_names = {"Jelle" : "van Assema", "Thomas" : "Kamps", "Mike" : "Brink"}

Bovenstaande creeërt een dictionary met de speciale syntax voor dictionaries, namelijk de curly braces (ze worden toch ergens voor gebruikt in Python ;). Dan zie je drie key-value paren. De keys zijn `"Jelle"`, `"Thomas"` en `"Mike"`. De bijbehorende values zijn `"van Assema"`, `"Kamps"` en `"Brink"`. De namen zitten aan elkaar gelinkt, vul je voornaam in (de key), dan krijg je de achternaam terug (de value). In actie:


    >>> last_names["Jelle"]
    van Assema
    >>> last_names["Thomas"]
    Kamps
