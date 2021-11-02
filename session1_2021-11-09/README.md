# Programmierung mit Python - Session 1

Online mit Python arbeiten, z.B. https://www.jdoodle.com/python3-programming-online/


## Statements
- Programm = Liste von Anweisungen für den Computer
- "Anweisungen" = Statements

```
print("Hello World!")
```                   

## (Einfache) Daten
- Zahlen: 1, 10.5, ...
- Strings: 'Julia', "Hello World", ....
- Boolean: True, False

## Variablen
- speichern Daten unter einem Namen
- zum späteren Aufrufen & Manipulieren

## Variablenname
- können aus Buchstaben, Zahlen und _ bestehen
- Großbuchstaben vs. Kleinbuchstaben: `x` ist nicht die gleiche Variable wie `X`
- dürfen keine Wörter sein, die Python Befehle sind (wie z.B. `def`)
- Speichern von einem Wert in einer Variable: name = wert

```
myName = "Julia"
```   

### Aufgabe 1
- Legt eine Variable an und speichert euren Namen als String in der Variable.
- Lasst euch mit `print` den Wert der Variable ausgeben.
- Benutzt `print`, um einen Satz anzuzeigen: "Das ist mein Name: " und danach der Wert der Variable. (Hinweis: Mit + kann man 2 Strings verbinden.)

## Operatoren
- zum Kombinieren / Manipulieren von Daten
- ähnlich wie Rechenzeichen in der Mathematik

### Operatoren für Zahlen
- `+` 	Addition
- `-` 	Subtraktion
- `*` 	Multiplikation
- `/` 	Division
- ...

```
print(7 + 3)
product = 10 * 5
```    

### Aufgabe 2
- Legt zwei Variablen mit jeweils einer Zahl an.
- Speichert die Summe der beiden Zahlen in einer dritten Variable.
- Gebt diese dritte Variable in der Konsole aus.

### Operatoren für Strings
+ 	Strings kombinieren / zusammenhängen (Concatenation)

```
first_name = 'Peter'
last_name = 'Lustig'
full_name = first_name + ' ' + last_name
```
                        
### Aufgabe 3
- Legt die folgenden Variablen an und lasst sie in der Konsole ausgeben.
- Was passiert, wenn man in Python Zahlen und Strings kombiniert?

```
page = "15"
page2 = page + 1
page3 = page + "2"                            
```

### Vergleichsoperatoren
- `==` 	ist gleich
- `!=` 	ist nicht gleich
- `>` 	ist größer als
- `<` 	ist kleiner als
- `>=` 	ist größer als oder gleich
- `<=` 	ist kleiner als oder gleich

### Aufgabe 4
- Gebt das Ergebnis von einem Vergleich in der Konsole aus.
- Welche Daten-Art hat das Ergebnis?

## Bedingungen (Conditions)
- führen Code nur dann aus, wenn etwas wahr/falsch ist
- Python-Befehle: `if` / `else`
- die Einrückung ist in Python wichtig: Code innerhalb der Bedingung muss eingerückt sein (2 oder 4 Leerzeichen)

```
number = 3
if (number > 5):
  print('Yeah, number ist größer als 5!')
else:
  print('Schade, number ist kleiner als 5!')
```
                        
### Aufgabe 5
- Definiert zwei Variablen, die jeweils einen String enthalten.
- Danach soll ein `print` anzeigen, ob zweimal der gleiche String eingegeben wurde.

## Schleifen (Loops)
- führen Code mehrmals aus
- Python-Befehle: `while` / `for`

### While-Schleife
- Code wird ausgeführt, solange die Bedinung `True` ist

```
number = 3
while number < 5:
    print("immer noch kleiner... ")
    number = number + 1
print(number)
```

### Aufgabe 6
- Legt eine Variable an, die eine Zahl (größer als 0) enthält.
- Schreibt eine `while`-Schleife, die von der Variable bis 0 herunterzählt und dabei jede Zahl mit `print` ausgibt.

## Funktionen
- speichern Code unter einem Namen, damit er an verschiedenen Stellen im Programm ausgeführt werden kann
- Python-Befehl: `def`
- Wird aufgerufen mit name()

```
def sayHello():
    string1 = 'Hello'
    string2 = 'World'
    print(string1 + ' ' + string2 + '!')

sayHello()
```

### Aufgabe 7
- Schreibt eine Funktion, die das Ergebnis von 12 * 5 ausgibt.

### Argumente
= Werte, die man einer Funktion mitgibt
- sind dann wie Variablen in der Funktion

```                      
def add(number1, number2):
    print(number1 + number2)

add(1, 2)
add(3, 4)
```

### Rückgabewert
= Wert, den eine Funktion zurückgibt, damit man ihn weiter verwenden kann

```
def add(number1, number2):
    sum = number1 + number2
    return sum

sum1and2 = add(1, 2)
print(sum1and2)

sum3and4 = add(3, 4)
print(sum1and2 + sum3and4)
```

### Aufgabe 8
- Schreibt eine Funktion, die eine Zahl als Argument bekommt.
- Die Funktion soll `True` zurückgeben, wenn die Zahl größer als 10 ist. Ansonsten gibt sie `False` zurück.

