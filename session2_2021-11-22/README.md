# Programmierung mit Python - Session 2

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
                    

### Übung 1

- Legt eine Liste mit 4 Namen darin an.
- Gebt den dritten Namen im Array aus.
- Was passiert, wenn man versucht auf einen Index zuzugreifen, für den es keinen Wert in der Liste gibt?


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

### Übung 2

- Schreibt eine for-Schleife, die jeden Namen aus dem Array aus Übung 1 zusammen mit einem Nachnamen ausgibt.
- Ändert den Code in der Schleife so, dass nur Namen mit 5 Buchstaben ausgegeben werden.


## Und noch mehr Daten: Dictionaries

= Container für Werte mit Namen, die zusammengehören
- Variablen für mehrere Werte (wie Listen)
- aber: jeder Wert bekommt einen Namen, über den man zugreifen kann (statt Index bei Listen)
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

### Übung 3

- Legt ein Dict für ein T-Shirt an.
- Das Dict soll Werte für Farbe, Preis und Marke enthalten.


## Eigene Daten-Typen definieren: Klassen & Objekte

- oft braucht man mehrere Variablen des gleichen Typs, die alle die gleichen Eigenschaften / Funktionalität haben,
  aber unterschiedliche Werte
- dafür kann man einen eigenen Daten-Typ als eine Klasse definieren und dann beliebig viele Objekte als Instanzen dieser Klasse anlegen

```
class Person:
  name = 'Peter'
  age = 28
  
person1 = Person()
person2 = Person()

print(person1.name) # 'Peter'
print(person2.name) # 'Peter'
```

### Objekte: Eigenschaften und Konstruktoren

- Eigenschaften = Daten im Objekt (Zahlen, Strings, Listen etc.)
- über einen Konstruktor können Eigenschaften in einem Objekt gesetzt werden


```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

person1 = Person("John", 36)
person2 = Person("Peter", 28)

print(person1.name) # 'John'
print(person2.name) # 'Peter' 
```

### Objekte: Methoden

- Methoden = Funktionen im Objekt
- Methoden können auf Eigenschaften des Objektes mithilfe von `self` zugreifen     

```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
    
  def say_hi(self):
    print("Hi, ich bin " + self.name)

person1 = Person("John", 36)
person1.say_hi() # "Hi, ich bin John"
```

### Übung 4

- Schreibt das T-Shirt Dict als Klasse anstatt als Dict.
- Die Klasse soll einen Konstruktor haben, über den man Farbe, Preis und Marke angeben kann.
- Die Klasse soll eine Methode haben, um den Preis für ein T-Shirt zu erhöhen.
  Die Methode soll ein Argument bekommen: Die Zahl, um wieviel der Preis erhöht werden soll.
- Erstellt damit zwei T-Shirt Objekte.
- Erhöht den Preis von beiden T-Shirts.

### Übung 5

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die einen maximalen Preis festlegt, der für alle T-Shirts gleich ist.
- Ändert die Preis-Erhöhen-Methode so, dass der Preis nur erhöht wird, wenn der neue Preis nicht höher als der maximale Preis ist.

## Übung 6

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die die Größen, in denen das T-Shirt gekauft werden kann, in einer Liste enthält.
- Fügt der T-Shirt Klasse eine Methode hinzu, der man als Argument eine Größe übergibt, und die prüft, ob diese Größe verfübgar ist.
  Die Methode soll True zurückgeben, wenn die Größe verfügbar ist, ansonsten gibt sie False zurück.

