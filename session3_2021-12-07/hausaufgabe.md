# Hausaufgabe Session 3

Diese Aufgaben sollten in VS Code in `.py` Dateien geschrieben und ausgeführt werden.


## Aufgabe 1

Schreibt eine Funktion `getListPart`, die eine Liste und zwei Zahlen bekommt, und den Teil der Liste von Zahl 1 bis inklusive Zahl 2 zurückgibt.
Wenn der Teil nicht zurückgegeben werden kann, weil die Liste zu wenig Elemente hat, soll mit `print` ausgegeben werden 'Nicht möglich!' und eine
leere Liste zurückgegeben werden.

```
myList1 = ['Katze', 'Hund', 'Elefant', 'Maus', 'Affe']
print(getListPart(myList1, 0, 2))
print(getListPart(myList1, 2, 10))
```

Ausgabe:
```
['Katze', 'Hund', 'Elefant']
'Nicht möglich!'
[]
```

## Aufgabe 2

Programmiere mit Klassen und Objekten einen kleinen "Online-Shop".

- Zuerst brauchst du eine Klasse `Product` für Produkte. Jedes Produkt hat einen Namen (String) und einen Preis (Zahl).
Den Namen und Preis soll man über einen Konstruktor angeben können. Produkte erstellen soll dann z.B. so aussehen:

```
product1 = Product('T-Shirt', 10)
product2 = Product('Apfel', 1)

print(product1.name)    # 'T-Shirt'
print(product2.price)   # 1
```

- Dann brauchst du noch eine Klasse `Basket` für den Warenkorb. Ein Warenkorb hat einen User/Benutzer (String) und eine Liste von
Produkten. Am Anfang ist diese Liste immer leer, über den Konstruktor kann man nur den Benutzer angeben.
Einen Warenkorb erstellen soll dann z.B. so aussehen:

```
basket = Basket('Julia')

print(basket.user)              # 'Julia'
print(basket.products)          # []
print(len(basket.products))     # 0
```

- Die Klasse `Basket` soll eine Methode `addProduct` haben, der man ein Produkt übergibt.
Das Produkt soll dann in der Produkt-Liste im Warenkorb gespeichert werden.

```
basket.addProduct(product1)
print(len(basket.products))     # 1
print(basket.products)          # [<__main__.Product object at 0x7f79b5febfd0>] (Zahlen/Buchstaben am Ende können anders aussehen)

basket.addProduct(product2)
print(len(basket.products))     # 2
print(basket.products)          # [<__main__.Product object at ...>, <__main__.Product object at ...>]
```

- Die Klasse `Basket` soll außerdem eine Methode `removeProduct` haben, der man ein Produkt übergibt.
Das Produkt soll dann aus der Produkt-Liste im Warenkorb entfernt werden.
Wenn das Produkt nicht in der Liste im Warenkorb enthalten ist, soll mit `print` 
die Meldung 'Das Produkt ist nicht im Warenkorb!' ausgegeben werden.

```
basket.removeProduct(product1)
print(len(basket.products))     # 1

basket.removeProduct(product1)  # 'Das Produkt ist nicht im Warenkorb!'
```


- Die Klasse `Basket` soll außerdem eine Methode `getPrice` haben, die zurückgibt,
wieviel alle Produkte im Warenkorb zusammengerechnet kosten.
Wenn man also z.B. die beiden Produkte `product1` für 9.99 und `product2` für 0.49
hinzugefügt hat, gibt die Methode 10.48 zurück.
Fügt man weitere Produkte hinzu, order entfernt sie, dann ändert sich der Gesamtpreis.

```
basket = Basket('Julia')
basket.addProduct(product1)
basket.addProduct(product2)

print(basket.getPrice())        # 11

product3 = Product('Buch', 20)
basket.addProduct(product3)
print(basket.getPrice())        # 31

basket.removeProduct(product2)
print(basket.getPrice())        # 30
```

- Ändert die `addProduct` Methode so, dass sie zusätzlich noch eine Zahl bekommt,
die angibt, wie oft das Produkt zum Warenkorb hinzugefügt wird.
Wann man also z.B. 3 Äpfel und 2 T-Shirts bestellen möchte, soll das so aussehen:

```
basket = Basket('Julia')
basket.addProduct(product2, 3)
basket.addProduct(product1, 2)

print(len(basket.products))     # 5
print(basket.getPrice())        # 23
```

- Fügt eine Methode `getProductNames` hinzu, die eine Liste der Namen der
Produkte im Warenkorb zurückgibt.

```
basket = Basket('Julia')
basket.addProduct(product2, 1)
basket.addProduct(product1, 2)

print(basket.getProductNames())     # ['Apfel', 'T-Shirt', 'T-Shirt']
```