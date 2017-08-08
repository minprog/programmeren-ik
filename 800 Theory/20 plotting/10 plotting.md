# Plotting

Python heeft een handige plot module genaamd `matplotlib` om makkelijk grafieken te maken. Voor je deze module kunt gebruiken zal je deze eerst moeten installeren. Dat doe je door middel van `pip`. Pip staat voor Pip Installs Python, en dit is een Python module waarmee je andere Python modules makkelijk kan downloaden en installeren. Het werkt vrij simpel. Om matplotlib te installeren voer je het volgende commando in de terminal in:

    python -m pip install matplotlib

Dit commando ziet er misschien wat ingewikkeld uit, maar het bestaat eigenlijk uit twee delen. `python -m pip` is simpelweg een manier om pip uit te voeren, je roept Python aan en verteld d.m.v. de module flag (`-m`) om de pip module uit te voeren. Dan gaan de overgebleven argumenten (dat zijn `install matplotlib`) naar de pip module. En zoals je dan verwacht, installeert pip de module matplotlib.

Nu je matplotlib hebt geïnstalleerd, kunnen we de module importeren, en kunnen we gaan plotten. Laten we met een voorbeeld beginnen:

{: .language-python}
    import matplotlib.pyplot as plt

    y_values = [3,5,8,10,12,15,18,20]
    plt.plot(y_values)
    plt.show()

Op de eerste regel
