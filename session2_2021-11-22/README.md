# Programmierung mit Python - Session 2

## Python Programme schreiben und ausführen mit VS Code

- Python code muss in einer Datei mit der Endung `.py` gespeichert werden
- um den Code auszuführen, kann man in VS Code den grünen dreieckigen Button oben rechts verwenden

### Übung 1

- Schreibt ein Python Programm, dass "Hello World!" ausgibt, speichert es und führt es mit VS Code aus.

## Kommentare

- Anmerkungen im Code, haben keine Auswirkung auf das Programm
- z.B. für Hinweise, die helfen, den Code zu verstehen, etc.

```
# Das ist ein Kommentar in Python.
```


## Mehr Daten: Listen

= eine Liste von Daten
- Eine Variable für eine Sammlung von Werten
- in Python: `[ ]`

Anstatt als einzelne Variablen...
```
animal1 = 'Katze'
animal2 = 'Hund'
animal3 = 'Elefant'

```
... kann man Werte zusammen in einer Liste speichern:
```
animals = ['Katze', 'Hund', 'Elefant']
```                        

### Zugriff auf Werte in einer Liste

- über die Position in der Liste (= Index)
- fängt bei 0 an

``` 
print(animals[0])  # 'Katze'
print(animals[1])  # 'Hund'
```                         
                    

### Übung 2

- Legt eine Liste mit 4 Namen darin an.
- Gebt den dritten Namen im Array aus.
- Was passiert, wenn man versucht auf einen Index zuzugreifen, für den es keinen Wert in der Liste gibt?


#### Lösung:

```
names = ['Julia', 'Paul', 'Johannes', 'Sarah']
print(names[2])
print(names[6]) # Fehler: IndexError
```

## Built-In Listen-Methoden

- Listen in Python bringen eigene Funktionen (Methoden) mit, mit denen man sie z.B. verändern kann
- Bsp.: `append` fügt ein Element zur Liste hinzu:

```
animals.append('Maus')
print(animals[3])  # 'Maus'
```
- Bsp.: `remove` entfernt ein Element aus der Liste:

```
animals.remove('Maus')
print(animals[3])  # IndexError
```


## Und mehr Schleifen: for

= führt Code einmal für jedes Element in einem Array aus

```
for element in myArray:
  # code
```                        
- `element`: Variable, die im Folgenden Code jeweils den Wert von einem Element aus myArray annimmt# code
- `# code`: beliebiger Code, der für jedes Element genau einmal ausgeführt wird

Beispiel:

```
animals = ['Katze', 'Hund', 'Elefant']
for animal in animals:
  print(animal)
```

### Übung 3

- Schreibt eine for-Schleife, die jeden Namen aus dem Array aus Übung 1 zusammen mit einem Nachnamen ausgibt.
- Ändert den Code in der Schleife so, dass nur Namen mit 5 Buchstaben ausgegeben werden.

#### Lösung:

```
for name in names:
  if (len(name) == 5):
    print(name)
```

## Und noch mehr Daten: Dictionaries

= Container für Werte mit Namen, die zusammengehören
- Variablen für mehrere Werte (wie Listen)
- aber: jeder Wert (value) bekommt einen Namen (key), über den man zugreifen kann (statt Index bei Listen)
- in Python: `{ }`

```
person = {
  'name': 'Peter',
  'lastName': 'Müller',
  'age': 28
}

print(person['name']) # 'Peter'
print(person["age"])  # 28
```

- Um einen Eintrag zu einem Dict hinzuzufügen, kann man wie beim Anlegen von Variable `=` verwenden:
```
person['phone_number'] = '0123/456789'
```

### Übung 4

- Legt ein Dict für ein T-Shirt an.
- Das Dict soll Werte für Farbe, Preis und Marke enthalten.


#### Lösung:

```
t_shirt = {
  "color": "rot",
  "price": 10.00,
  "brand": "Adidas"
}
```