# Hausaufgabe Session 1

Die Aufgaben könnt ihr in https://www.jdoodle.com/python3-programming-online/ lösen und dann auf die drei Punkte klicken und auf "Save (to local file)".

## Installieren:

- Python: https://wiki.python.org/moin/BeginnersGuide/Download
- Visual Studio Code (= VS Code): https://code.visualstudio.com/download
- VS Code Pyhton Extension: https://marketplace.visualstudio.com/items?itemName=ms-python.python

## Aufgabe 1

Schreibt eine Funktion `makeSentence`, die aus drei Strings einen Satz macht.
Die Funktion bekommt drei Argumente (die drei Strings) und gibt einen neuen String (den Satz) zurück.
Ein Aufruf der Funktion sollte also z.B. so aussehen:

```
print(makeSentence('Funktionen', 'machen', 'Freude'))
print(makeSentence('Python', 'ist', 'super'))
```
... und dabei sollte ausgegeben werden:

```
'Funktionen machen Freude.'
'Python ist super.' 
```

## Aufgabe 2

Schreibt eine Funktion `gramToKilogram`, die einen Wert von Gramm zu Kilogramm umrechnet (1000 Gramm = 1 Kilogramm).
Die Einheiten lassen wir dabei weg.
Die Funktion bekommt 1 Argument (eine Zahl, der Wert in Gramm) und gibt eine Zahl zurück (der Wert in Kilogramm).

```
print(gramToKilogram(7000))
print(gramToKilogram(1125))
```
Ausgabe:

```
7
1.125
```

## Aufgabe 3

Schreibt eine Funktion `guessMyName`, die einen String übergeben bekommt und die ...
- "Das ist mein Vorname!" mit `print` ausgibt, wenn der String euren Vornamen enthält,
- "Das ist mein Nachname!" mit `print` ausgibt, wenn der String euren Nachnamen enthält und
- "Falsch, das ist nicht mein Name!" mit `print` ausgibt, wenn der String etwas anderes enthält.
Ein Aufruf der Funktion sollte also z.B. so aussehen:

```
guessMyName("Julia")
guessMyName("Peter")
```
... und dabei sollte ausgegeben werden:

```
"Das ist mein Vorname!"
"Falsch, das ist nicht mein Name!"
```

## Aufgabe 4

Schreibt eine Funktion `upToOneHundred`, die eine Zahl übergeben bekommt und solange immer 10
dazurechnet, bis das Ergebnis größer als 100 ist, und dabei alle Zahlen dazwischen mit `print` ausgibt.

```
upToOneHundred(65)
upToOneHundred(80)
```
Ausgabe:

```
65
75
85
95

80
90
100
```

## Aufgabe 5

Schreibt eine Funktion `isBetween`, die drei Zahlen übergeben bekommt,
und `True` zurückgibt, wenn die erste Zahl zwischen der zweiten und dritten Zahl liegt, sonst `False`.

```
isBetween(65, 1, 100)
isBetween(80, 70, 75)
isBetween(80, 90, 75)
```
Ausgabe:

```
True
False
True
```


## Aufgabe 6

Schreibt eine Funktion `padString`, die einen String und eine Zahl übergeben bekommt,
und an diesen String soviele Nullen anhängt, bis er die Länge hat, die die Zahl angibt.

Hinweis: Die Länge von einem String bekommt man mithilfe von `len(myString)` heraus.

```
padString("Hallo", 10)
padString("Hi", 3)
padString("Ahoi", 4)
```
Ausgabe:

```
"Hallo00000"
"Hi0"
"Ahoi"
```

