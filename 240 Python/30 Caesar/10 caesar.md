# caesar.py

![](caesar.jpg)

In deze opdracht ga je de caesar opdracht van CS50 maken in Python.

## Gebruik

	python caesar.py 1
	plaintext:  HELLO
	ciphertext: IFMMP

	python caesar.py 13
	plaintext:  Hello, world!
	ciphertext: Uryyb, jbeyq!

	python caesar.py -1
	Whoops! Key is smaller than 0. Exiting

## Specificatie

* Schrijf een programma genaamd `caesar.py` dat je aanroept met een integer command line argument, de key.
* Als de key kleiner is dan 0, dan moet het programma een bericht printen en stoppen.
* Je mag aannemen dat de key altijd een integer is.
* De gebruiker mag een string invoeren wat ge-encrypt wordt met de key. Zo wordt met een de letter `a` met een key van 1 de letter `b`.
* Enkel letters moeten worden ge-encrypt, alle andere tekens blijven hetzelfde.
* Vergeet de loop around niet, dus de letter `z` met een key van 1 wordt de letter `a`.

## Tips

* In tegenstelling tot C zijn er in Python geen characters, maar enkel strings. Deze strings zijn meer dan een collectie van bytes, en je kan er dus niet meteen mee rekenen. Gelukkig heb je de functies `ord()` en `chr()` tot je beschikking. Zo is `ord("a")` 97, en `chr(97)` de string `"a"`, oftewel `chr(ord("a")) == "a"`.

## Testen

	checkpy caesar
