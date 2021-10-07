# Oefententamen

> Regels voor oefententamen:
> 
> - Leg je collegekaart klaar op tafel (of een andere ID met foto).
> - Stilte in de zaal.
> - Er is geen pauze, maar ga gerust naar het toilet.
> - Klaar is klaar, dan kun je inleveren en weggaan.
> - Inleveren op deze pagina, uiterlijk 15 minuten voor het einde van het laptopcollege (dus bijv. om 10:45). Wij moeten de zaal vrijmaken voor de volgende gebruiker.
> - Ben je niet klaar, lever dan gewoon in. Je kunt thuis verder oefenen, maar we willen graag zien hoe veer iedereen komt.
> - Als bronnen mag je gebruiken: de lecture notes (en de rest van deze website), de CS50 Manual waarin allerlei nuttige C-functies genoemd staan, en je eigen uitwerkingen van eerdere opdrachten.
> - (Ook) voor het oefententamen is het essentieel dat je dit doet zonder verder internet of hulp van anderen. Alleen zo begrijp je waar je zelf nog vastloopt.

Hieronder vind je vier opdrachten. Op dit moment in de cursus zou je alledrie de opdrachten goed moeten kunnen maken zonder al te veel begeleiding. Het kan wel zijn dat je iets te weinig tijd hebt omdat je nu maar een goede 1,5 uur hebt.

Het doel is te demonstreren dat je zelfstandig een oplossing voor een probleem kunt ontwikkelen, en daarbij gebruik kunt maken van de basistechnieken van programmeren in C, zoals bijvoorbeeld de verschillende soorten loops, if-else-constructies, enzovoort.

Vanwege dit doel heeft het geen zin om alleen het juiste antwoord uit te printen zodat `check50` tevreden is (het zogenaamde "hardcoden"). Het is daarom ook aan te raden om zoveel mogelijk van de opdrachten te doen, mits de tijd dit toelaat. Dat geeft ruimte als je onbedoeld een antwoord hebt ge-hardcode.

De input van gebruikers hoeft alleen gecontroleerd te worden als dit duidelijk in de opdracht vermeld staat.


## Vakantie

Je wil in je eentje op vakantie naar een mooie accommodatie in Frankrijk. De kosten van de reis naar het verblijf zijn afhankelijk van het gebruikte vervoersmiddel. Met het vliegtuig kost het je 250 euro, met de trein kost het 100 euro, en met de auto kost het 150 euro. Het verblijf zelf kost 60 euro per nacht. Bovendien betaal je nog 3% servicekosten over de totale kosten (dus vermenigvuldig totaal met 0.03), afhankelijk dus van hoeveel nachten je verblijft. De servicekosten worden wel naar **beneden** afgerond op hele euro's vóórdat ze bij het totaalbedrag worden opgeteld!

Schrijf een programma dat berekent hoeveel je vakantie kost op basis van het aantal dagen dat je op vakantie gaat en met welk vervoersmiddel je gaat. Controle op (on)geldigde invoer is niet nodig.

    $ ./vakantie
    Hoe ga je reizen (v)liegtuig/(t)rein/(a)uto? v
    Hoeveel nachten ga je verblijven? 1
    Jouw vakantie kost: 319

    $ ./vakantie
    Hoe ga je reizen (v)liegtuig/(t)rein/(a)uto? t
    Hoeveel nachten ga je verblijven? 10
    Jouw vakantie kost: 721

    $ ./vakantie
    Hoe ga je reizen (v)liegtuig/(t)rein/(a)uto? a
    Hoeveel nachten ga je verblijven? 7
    Jouw vakantie kost: 587

Tip: begin altijd met het maken van een programma voor het **eerste** voorbeeld. Dit is het meest eenvoudig. Hiermee voorkom je dat je vastloopt in allerlei uitzonderingen. Zodra je programma werkt voor het eerste voorbeeld kun je gaan checken of het ook werkt voor de volgende voorbeelden, en je programma dan aanpassen.


## Caffeïne

Het internationale advies voor de maximale dagelijkse caffeïne-intake is 400mg voor een gezonde volwassene, 100mg voor iemand tussen 12 en 18 jaar oud, en helemaal geen caffeïne voor kinderen onder 12 jaar oud.

Hierbij een lijst met de hoeveelheid caffeïne voor één portie van verschillende dranken.

* Coffee - 90 mg
* Thee - 45 mg
* Energiedrankjes - 80 mg
* Cola - 40 mg

Schrijf een programma dat de caffeïne-inname van de gebruiker berekent en een waarschuwing print als deze te hoog is. Controle op (on)geldige invoer is niet nodig.

    $ ./caffeine 
    Hoeveel koppen koffie? 2
    Hoeveel koppen thee? 1
    Hoeveel energiedrankjes? 0
    Hoeveel glazen cola? 0
    Hoeveel jaar oud ben je? 22
    Je krijgt 225 mg caffeïne binnen.
    Dat is een veilige hoeveelheid caffeïne.

    $ ./caffeine 
    Hoeveel koppen koffie? 2
    Hoeveel koppen thee? 0
    Hoeveel energiedrankjes? 2
    Hoeveel glazen cola? 0
    Hoeveel jaar oud ben je? 17
    Je krijgt 340 mg caffeïne binnen.
    Kijk uit, dat is te veel caffeïne!

    $ ./caffeine 
    Hoeveel koppen koffie? 0
    Hoeveel koppen thee? 0
    Hoeveel energiedrankjes? 0
    Hoeveel glazen cola? 1
    Hoeveel jaar oud ben je? 10
    Je krijgt 40 mg caffeïne binnen.
    Kijk uit, dat is te veel caffeïne!

    $ ./caffeine 
    Hoeveel koppen koffie? 5
    Hoeveel koppen thee? 0
    Hoeveel energiedrankjes? 0
    Hoeveel glazen cola? 0
    Hoeveel jaar oud ben je? 38
    Je krijgt 450 mg caffeïne binnen.
    Kijk uit, dat is te veel caffeïne!


## RNA

Eiwitsynthese is het proces waarbij eiwitten worden gemaakt op basis van de informatie in het DNA. Simpel gezegd is eiwitsynthese het maken van een eiwit in een menselijke cel. De eerste stap van eiwitsynthese is de transcriptie van DNA naar RNA. (Je hoeft voorgaande niet te begrijpen.)

DNA bestaat uit verschillende moleculen, waaronder 4 nucleotiden die de DNA-code vormen: Adenine (A), Guanine (G), Cytosine (C) en Thymine (T). RNA is een zogenaamde *complementaire* transcriptie van DNA. De complementaire nucleotide van Adenine is Uracil (U), van Guanine is Cytosine, van Cysotine is Guanine en van Thymine is Adenine.

Een complementaire RNA-keten kan dus volgens een vast patroon beredeneerd worden uit de DNA-keten. Zo geeft een DNA-keten `ATGC` altijd de RNA-keten `UACG` als je bovenstaande regels toepast.

Schrijf een programma dat een keten van DNA aanneemt en de complementaire RNA-keten print. Je mag aannemen dat de DNA-keten altijd in hoofdletters wordt ingevuld. Het programma print een error message als deze een ongeldige nucleotide bevat (dus een andere letter dan A, G, C of T).

    $ ./rna
    DNA-keten: ATGC
    Dit is de bijbehorende RNA-keten: UACG

    $ ./rna
    DNA-keten: AAF
    Ongeldige DNA-keten

    $ ./rna
    DNA-keten: AAGGTTCCAA
    Dit is de bijbehorende RNA-keten: UUCCAAGGUU


## Driehoek

Schrijf een programma dat een driehoek uitprint. De gebruiker mag een hoogte opgeven. Deze hoogte mag niet kleiner dan 5 zijn en niet hoger dan 20, maar je hoeft dit **niet** te controleren!

    $ ./driehoek
    Hoe hoog moet de driehoek zijn? 5
        ##
       #  #
      #    #
     #      #
    ##########

    $ ./driehoek
    Hoe hoog moet de driehoek zijn? 15
                  ##
                 #  #
                #    #
               #      #
              #        #
             #          #
            #            #
           #              #
          #                #
         #                  #
        #                    #
       #                      #
      #                        #
     #                          #
    ##############################


## Inleveren

Heb je één van de opdrachten niet gedaan? Maak dan een leeg bestand aan met de juiste naam, en gebruik dit om hieronder in te leveren.

