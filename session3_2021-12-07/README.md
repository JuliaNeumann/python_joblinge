# Programmierung mit Python - Session 3

## Mit der Kommandozeile arbeiten

Siehe https://lerneprogrammieren.de/kommandozeile/.

### Python Programme mit der Kommandozeile ausführen (Windows)

- in der Kommandozeile zu dem Ordner navigieren, der die `.py` Datei (z.B. `test.py`) enthält und Folgendes ausführen:

```
C:\> py test.py
```


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

### Übung 1

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

### Übung 2

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die einen maximalen Preis festlegt, der für alle T-Shirts gleich ist.
- Ändert die Preis-Erhöhen-Methode so, dass der Preis nur erhöht wird, wenn der neue Preis nicht höher als der maximale Preis ist.

## Übung 3

- Fügt der T-Shirt Klasse eine Eigenschaft hinzu, die die Größen, in denen das T-Shirt gekauft werden kann, in einer Liste enthält.
- Fügt der T-Shirt Klasse eine Methode hinzu, der man als Argument eine Größe übergibt, und die prüft, ob diese Größe verfübgar ist.
  Die Methode soll True zurückgeben, wenn die Größe verfügbar ist, ansonsten gibt sie False zurück.

