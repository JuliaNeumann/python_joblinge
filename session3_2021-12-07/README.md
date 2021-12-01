# Programmierung mit Python - Session 3

## Mit der Kommandozeile arbeiten

Siehe https://lerneprogrammieren.de/kommandozeile/.

### Python Programme mit der Kommandozeile ausführen (Windows)

- in der Kommandozeile zu dem Ordner navigieren, der die `.py` Datei (z.B. `test.py`) enthält und Folgendes ausführen:

```
C:\> py test.py
```


## Mehr zu Listen:

### Indexing

- wie beim letzten Mal bereits gesagt, kann über den Index auf Elemente in einer Liste zugreifen

```
animals = ['Katze', 'Hund', 'Elefant', 'Maus', 'Affe']
print(animals[0])  # 'Katze'
``` 
- ein negativer Index fängt von hinten an, zu zählen -> mit -1 greift man auf das letzte Element zu, mit -2 auf das vorletzte usw.
```
print(animals[-1])  # 'Affe'
print(animals[-3])  # 'Elefant'
``` 
- mit zwei Zahlen und Doppelpunkt dazwischen, kann man auf einen Teil der Liste zugreifen (man bekommt also eine neue Liste): 
vom Index vor dem Doppelpunkt bis zu Index nach dem Doppelpunkt minus eins
```
print(animals[1:3])  # ['Hund', 'Elefant']
print(animals[3:4])  # ['Maus']
```
- lässt man den Index vor dem Doppelpunkt weg, bekommt man den Teil vom Anfang der Liste bis Index nach dem Doppelpunkt minus eins;
lässt man den Index nach dem Doppelpunkt weg, bekommt man den Teil vom Index vor dem Doppelpunkt bis zum Ende der Liste
```
print(animals[:3])   # ['Katze', 'Hund', 'Elefant']
print(animals[3:])   # ['Maus', 'Affe']
```

### Übung 1
- Legt eine Liste mit 4 Namen an und gebt den Teil der Liste mit den beiden Namen in der Mitte aus.
- Was passiert, wenn man den Index vor dem Doppelpunkt UND den Index nach dem Doppelpunkt weglässt?

### Prüfen, ob Elemente in einer Liste enthalten sind

- dazu verwendet man `if ... in ...`:
```
animals = ['Katze', 'Hund', 'Elefant', 'Maus', 'Affe']
if 'Katze' in animals:
  print('Katze ist in der Liste!')
```
- will man wissen, ob ein Element nicht in der Liste enthalten ist, kann man `not in` verwenden:
```
if 'Katze' not in animals:
  print('Katze ist nicht in der Liste!')
```

### Übung 2
- Schreibt eine kleine Funktion: Sie bekommt ein Element und eine Liste übergeben, und soll 'Ja!' zurückgeben,
wenn das Element in der Liste enthalten ist, ansonsten gibt sie 'Nein!' zurück.

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

### Übung 3

```
t_shirt = {
    'farbe': 'rot',
    'preis': 9.99,
    'marke': 'H&M'
}
```

- Schreibt das T-Shirt Dict als Klasse anstatt als Dict.
- Die Klasse soll einen Konstruktor haben, über den man Farbe, Preis und Marke angeben kann.
- Die Klasse soll eine Methode haben, um den Preis für ein T-Shirt zu erhöhen.
  Die Methode soll ein Argument bekommen: Die Zahl, um wieviel der Preis erhöht werden soll.
- Erstellt damit zwei T-Shirt Objekte.
- Erhöht den Preis von beiden T-Shirts.

### Übung 4

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die einen maximalen Preis festlegt, der für alle T-Shirts gleich ist.
- Ändert die Preis-Erhöhen-Methode so, dass der Preis nur erhöht wird, wenn der neue Preis nicht höher als der maximale Preis ist.

## Übung 5

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die die Größen, in denen das T-Shirt gekauft werden kann, in einer Liste enthält.
- Fügt der T-Shirt Klasse eine Methode hinzu, der man als Argument eine Größe übergibt, und die prüft, ob diese Größe verfübgar ist.
  Die Methode soll True zurückgeben, wenn die Größe verfügbar ist, ansonsten gibt sie False zurück.

