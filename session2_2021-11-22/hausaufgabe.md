# Hausaufgabe Session 2

Diese Aufgaben sollten in VS Code in `.py` Dateien geschrieben und ausgeführt werden.

## Aufgabe 1

Schreibt eine Funktion `makeSentence2`, die aus einer Liste mit beliebig vielen Strings darin einen Satz macht.
Die Funktion bekommt ein Argument (eine Liste von Strings) und gibt einen neuen String (den Satz) zurück.

```
myList1 = ['Funktionen', 'machen', 'Freude']
print(makeSentence2(myList1))
myList2 = ['Aber', 'Eis', 'essen', 'macht', 'fast', 'noch', 'mehr', 'Freude']
print(makeSentence2(myList2))
```

Ausgabe:
```
'Funktionen machen Freude.'
'Aber Eis essen macht fast noch mehr Freude.'
```

## Aufgabe 2

Schreibt eine Funktion `findMax`, die aus einer Liste von Zahlen die größte Zahl heraussucht.
Die Funktion bekommt ein Argument (die Liste von Zahlen) und gibt eine Zahl (die größte Zahl) zurück.

```
print(findMax([10, 11, 12]))
print(findMax([1, 1001, 45, 23256, 233, 9]))
```

Ausgabe:
```
12
23256
```

## Aufgabe 3

Schreibt eine Funktion `makeDict`, die aus zwei Listen ein Dict macht.
Die erste Liste soll die keys ("Namen") enthalten, die zweite die values ("Werte").

```
print(makeDict(['name', 'age', 'birthday'], ['Peter', 32, '06.06.1989']))
print(makeDict(['katze', 'hund'], ['miau', 'wuff']))
```

Ausgabe:
```
{'name': 'Peter', 'age': 32, 'birthday': '06.06.1989'}
{'katze': 'miau', 'hund': 'wuff'}
```

## Aufgabe 4

Schreibt eine Funktion `countInList`, die eine Liste und einen einzelnen Wert (kann String, Zahl, ... sein)
übergeben bekommt, und zählt, wie oft dieser Wert in der Liste vorkommt - das Ergebnis soll zurückgegeben werden.

```
print(countInList(['Julia', 'Peter', 'Emil', 'Peter'], 'Peter'))
print(countInList([12, 34, 1, 67, 23, 4], 55))
```

Ausgabe:
```
2
0
```
