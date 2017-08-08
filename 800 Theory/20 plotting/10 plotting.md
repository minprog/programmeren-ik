# Plotting

Python heeft een handige plot module genaamd `matplotlib` om makkelijk grafieken te maken. Voor je deze module kunt gebruiken zal je deze eerst moeten installeren. Dat doe je door middel van `pip`. Pip staat voor Pip Installs Python, en dit is een Python module waarmee je andere Python modules makkelijk kan downloaden en installeren. Het werkt vrij simpel. Om matplotlib te installeren voer je het volgende commando in de terminal in:

    python -m pip install matplotlib

Dit commando ziet er misschien wat ingewikkeld uit, maar het bestaat eigenlijk uit twee delen. `python -m pip` is simpelweg een manier om pip uit te voeren, je roept Python aan en verteld d.m.v. de module flag (`-m`) om de pip module uit te voeren. Dan gaan de overgebleven argumenten (dat zijn `install matplotlib`) naar de pip module. En zoals je dan verwacht, installeert pip de module matplotlib.

Nu je matplotlib hebt geïnstalleerd, kunnen we de module importeren, en kunnen we gaan plotten. Laten we met een voorbeeld beginnen:

    import matplotlib.pyplot as plt

    y_values = [3,5,8,10,12,15,18,20]
    plt.plot(y_values)
    plt.show()

Op de eerste regel wordt matplotlib geïmporteerd. Of beter gezegd, de submodule `pyplot` van `matplotlib` wordt geïmporteerd. Dat is een module die je laat plotten door een sequentie van functie aanroepen. Dit komt je misschien bekend voor als je al eens hebt gewerkt met de programmeertaal Matlab. Het is gebruikelijk dat je lange imports afkort, en `plt` is de gebruikelijke afkorting voor `matplotlib.pyplot`. Dit scheelt je enorm veel typen! Verder zie je op de regels daarop volgend een lijstje, dan wordt dat lijstje geplot, en vervolgens laten we de plot zien. Run je bovenstaande stukje code dan zie je de volgende grafiek verschijnen:

  ![](simple_graph.png)

Je kan natuurlijk veel meer dan dit. Zo kun je meerdere lijnen plotten, kiezen uit allerlei verschillende soorten grafieken, legendas en labels toevoegen, support voor 3d, etc. Houd dit in je achterhoofd wanneer je een bepaalde grafiek wil. Met een beetje goed online zoeken kan je dat uitvinden.

In plaats van een uitputtende lijst van alle mogelijkheden hier op te schrijven gaan we focussen op interessante functies voor binnen dit vak. Als allereerste wil je waarschijnlijk meer plotten dan enkel y waardes, zo kun je ook bijbehorende x waardes willen plotten. Dat doe je door meer argumenten te geven aan de `plot()` functie. Bijvoorbeeld:

    import matplotlib.pyplot as plt

    x_values = [10,20,30,40,50,60,70,80]
    y_values = [3,5,8,10,12,15,18,20]
    plt.plot(x_values, y_values)
    plt.show()

  ![](x_graph.png)
