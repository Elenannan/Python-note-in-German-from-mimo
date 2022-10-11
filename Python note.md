

## Python Grundlagen

### <u>Variablennamen</u>

##### - bestehen aus einzelnen Wörtern und enthalten keine Leerzeichen

##### - um Variablen mit mehreren Wörtern zu erstellen -> Snake-Case   "`home_city`"

##### - Hinzufügen von Zahlen (für mehrere ähnliche Variablen)   "car_1"



### <u>Variablenwerte/-Typen</u>

##### - Die Variable `"city"` speichert den Wert `"Miami"`    `city = "Miami"`

##### Typ 1 - Strings: Wörter in doppelten Anführungszeichen  `"Miami"`

##### *Strings können mehrere Buchstaben/ Symbolen entalten, einschließlich Leerzeichen    `"Winter is coming."`

##### *Zahlen haben keine doppelte Anführungszeichen um sich  `users = 5`

##### Typ 2 - Integer:  ganze Zahlen ohne Dezimalstellen wie 42

##### Typ 3 - Float/ Schwimmer: Zahlen mit einer oder mehreren Nachkommastellen   `pie = 3.14159`

##### Typ 4 -Boolean: nur zwei Sonderwerte `True` und `False` (keine doppelte Anführungszeichen um sich)



### <u>Anweisung print()</u>

##### - console/ Shell: der Bereich, der die Ausgabe anzeigt

##### - Variable in der Konsole anzeigen - erscheinen ihre Werte anstelle ihrer Namen

```python
name = "Ludwig!"
print(name)

**Ausgabe
Ludwig!
```



### <u>Variable-Status aktualisieren</u>

##### - ''= Zeichen" verwenden und der Variable einen neuen Wert geben

```python
status = "watching netflix"
status = "Relaxing at the beach"
print(status)

status = "sleeping"

**Ausgabe
Relaxing at the beach
sleeping
```



### <u>Ausdruck - Hinzufügen von String-Werten</u>

```python
label = "Posts:" + "13"
print(label)

**Ausgabe
Posts:13
```

##### **Vergleich zwischen mit/ohne doppelte Anführungszeichen

```python
number = "3" + "1"
print(number)

**Ausgabe
31
```

```python
number = 3 + 1
print(number)

**Ausgabe
4
```



### <u>Wahr und Falsch</u>

##### `True` - ideal für Situation wie Überprüfen, ob eine Funktion aktiviert ist oder ob Daten verfügbar sind

##### `False` - Ggegenteil von "True", Überprüfen, ob eine Funktion ausgeschaltet ist



### <u>Negationsoperator `not` - verwandelt Werte in ihr Gegenteil</u>

##### Der `not`-Operator vor `False` ändert seinen Wert. Wenn ein Wert nicht `False` ist, muss er `True` sein.

```python
print(not False)

**Ausgabe
True
```



### <u>Vergleichsoperator</u>

##### - nur zwei Ergebnisse: `True` oder `False`

#### 1) Gleichheitsoperator `==`

```python
print(10 == 10)

**Ausgabe
True
```

#### 2) Ungleichheitsoperator `!=`

```python
print(1 != 10)

**Ausgabe
True
```

```python
previous_leader = "Anna"
new_leader = "Jim"
leader_changed = previous_leader != new_leader
print(leader_changed)

**Ausgabe
True
```

#### 3) Kleiner-als-Operator `>`

#### 4) Größer-als-Operator `<`

#### 5) Kleiner-oder-Gleich-Operator `<=`

#### 6) Größer-oder-Gleich-Operator `>=`

```python
min = 5
max = 10
result = min <= max
print(result)

**Ausgabe
True
```

```python
points = 12
level_two = points >= 10
print("Level 2:")
print(level_two)

**Ausgabe
Level 2:
True
```





## Bedingte Anweisungen

### <u>formatierte Strings (f-strings)</u>

##### - um verschiedene Arten von Werten zusammen in einer String fehlerfrei anzuzeigen

```python
new = 5
read = 2
status = f"{new - read} unread messages"
print(status)

**Ausgabe
3 new messages
```

```python
degress = 70
print(f"Temperature: {degrees}F")

**Ausgabe
Temperature: 70F
```



### <u>If-Anweisung (Bedingungen `True/ False`)</u>

##### `if True:` - Codeblock werden ausgeführt

#####  `if False:` - Codeblock werden übersprungen

##### *Ein Codeblock kann mehrere Codezeilen erhalten und jeweils wird zwei Leerzeichen nach rechts eingerückt

```python
if True:
  print("Good morning!")
  print("You have three appointments today!")
  
**Ausgabe
Good morning!
You have three appointments today!
```

```python
is_charged = False
if is_charged:
  print("Charged")
print("Low battery")

**Ausgabe
Low battery
```

##### *Vergleichsoperatoren verwenden - um intelligentere Entscheidungen übers Code-Ausführen/ -Überspringen zu treffen

```python
answer = "Picasso"
if answer == "Picasso":
  print(answer + " is correct!")
  
**Ausgabe
Picasso is correct!
```

```python
score = 51
pass_grade = score > 50
if pass_grade:
  print(pass_grade)
  
**Ausgabe
True
```



### <u>If-else-Anweisung</u>

##### Codeblock der else-Anweisung wird für alle Fälle ausgeführt, in denen die if-Anweisung False zurückgibt

```python
number = 10
if number == 1:
  print("It's 1")
else:
  print("It' not 1")
  
**Ausgabe
It's not 1
```

```python
points = 7600
points_needed = 8000

if points >= points_needed:
  print("You're Level 2!")
else:
  left = points_needed - points
  print("Points till Level 2:")
  print(left)
  
**Ausgabe
Points till Level 2:
400
```



### <u>elif-Anweisung</u>

##### ausführen, wenn die Bedingungen davor `False` waren und ihre Bedingung `True` ist

##### Solange die elif-Anweisungen vor der else-Anweisung stehen, können wir so viele elif-Anweisungen hinzufügen, wie wir möchten.

```python
hour = 20

if hour < 12:
  print("Good morning")
elif hour < 17:
  print("Good afternoon")
elif hour < 21:
  print("Good evening")
else:
  print("Good night")
  
**Ausgabe
Good evening
```

```python
age = 16

if age <= 12:
  print("Where are your parents?")
elif age <= 16:
  print("You are too young to ride.")
else:
  print("Welcome!")
  
**Ausgabe:
You are too young to ride.
```



### <u>and-Operator</u> 

##### *zum Verknüpfen mehrerer voneinander abhängigen Bedingungen

##### - Ausführen, wenn alle Bedingungen `True` sind

##### - Überspringen, wenn eine oder mehrere Bedingungen `False` sind

```python
age = 17
has_permit = True
is_insured = True

if age > 16 and has_permit and is_insured:
  print("Can drive")
  
**Ausgabe
Can drive
```



### <u>Or-Operator</u>

##### *zum Verknüpfen alternativen voneinader unabhängigen Bedingungen

##### - Ausführen, wenn mindestens eine der Bedingungen `True` ist

##### - Überspringen, wenn alle Bedingungen `False` sind

```python
average_grade = "B"
final_score = 1400
won_competition = True

if average_grade == "A" or final_score >= 1500 or won_competition:
  print("Certificate achieved!")
  
**Ausgabe
Certificate achieved!
```





## Schleifen

### <u>Selbstzuweisung</u>

##### *Damit können wir Daten verfolgen, die sich im Laufe der Zeit ändern

```python
cards = 3
cards = cards - 1
cards = cards + 4
print(cards)

**Ausgabe
6
```

##### -> vereinfacht - muss den Namen der Variablen nicht nochmal umschreiben

##### `+=` Operatur: eine Zahl vom Wert einer Variablen addieren

```python
sales = 5
sales += 1
print(sales)

**Ausgabe
6
```

##### `-=` Operatur: eine Zahl vom Wert einer Variablen subtrahieren 

```python
sales = 5
sales -= 3
print(sales)

**Ausgabe
2
```



### <u>While-Schleife</u>

##### - Wiederholen von Codezeilen, solange ihre Bedingung `True` ist

##### - die Bedingung bleibt immer True -> die Schleife wiederholt sich ewig und bringt das Programm zum Absturz

```python
while True:
  print("and again")
  
**Ausgabe
and again
and again
and again
...
Looks like your code runs forever. It may be that an infinite loop exists in your code.
```



### <u>Schleife stoppen</u>

##### - Variable `keep_going = True/ False` - entscheidet, ob die Schleife ihren Codeblock ausführen soll oder nicht

##### - Verhindern, dass die Schleife endlos wiederholt  -> `keep_going = False` innerhalb des Codeblocks aktualisieren

```python
keep_going = True

while keep_going == True:
  print("and again")
  keep_going = False
  
**Ausgabe
and again
```



### <u>Zähler-Variable</u>

##### `counter += 1`   -> erhöht den `counter` jedes Mal um eins, wenn die Schleife ihren Codeblock ausführt

##### *zeige 1(einschließlich) bis 4     ->   zuerst  `print(counter)`, dann `counter += 1`

```python
counter = 1

while counter < 5:
  print(counter)
  counter += 1
  
**Ausgabe
1
2
3
4
```

##### *zeige 1(ausschließlich) bis 4       ->   zuerst   `counter += 1`, dann   `print(counter)`

```python
counter = 1

while counter < 5:
  counter += 1
  print(counter)
  
**Ausgabe
2
3
4
```

##### *List_number

```python
list_number = 1

while list_number < 11:
  print("Add entry..")
  list_number += 1
  
**Ausgabe
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
Add entry..
```



### <u>for-Schleifen</u>

##### *Programme mit viel weniger Code schreiben und leichter verständlicher machen

##### `range(x)`   ->   Loop-Over x mal    von 0 ~ x-1

```python
for i in range(4):
  print("Round:")
  print(i)
  
**Ausgabe
Round:
0
Round:
1
Round:
2
Round:
3
```

```python
for i in range(2):
  print("We will")
  
print("Rock you!")

**Ausgabe
We will
We will
Rock you!
```

##### *Amerika-Flagge

```python
for i in range(3):
  print("**********---------")
  
for i in range(3):
  print("-------------------")
  
**Ausgabe
**********---------
**********---------
**********---------
-------------------
-------------------
-------------------
```





## Daten organisieren

### <u>Daten-Gruppierung in Listen</u>

##### Mit "`[`" und "`]`" können wir die verwandten Daten in einer Liste sammeln

##### Daten-Werte innerhalb der Liste     ->    Elemente  `"Read", "Workout", "Code"`

```python
todo = ["Read", "Workout", "Code"]
print(todo)

**Ausgabe
['Read','Workout','Code']
```



### <u>Daten-Ändern in Listen</u>

##### - Listen können jedes Datenelement speichern (String, Boolean, Float, Integer)

##### - Index (eng. Indices) -> nummerierte Position eines Elements in einer Liste `[0, 1, 2, 3, 4 ...]` (beginnt bei Null)

```python
items = ["milk", "tomato", "apple"]
print(items[1])

**Ausgabe
tomato
```

##### - Werte aktualisieren -> auf den Wert über seinen Index zugreifen und dann einen anderen Wert zuweisen

```python
temperatures = [17, 20, 26, 24]
temperatures[3] = 25

print(temperatures)

**Ausgabe
[17, 20, 25, 24]
```



### <u>Daten-Hinzufügen in Listen</u>

##### `Listenname.append("")`      -> jeweils nur einen Wert am Ende der Liste hinzufügen

##### `Listenname.insert(index,"")`       -> jeweils nur einen Wert einem bestimmten Index hinzufügen

```python
shopping = ["kiwis", "peas"]
shopping.append("lemon")
shopping.insert(0,"chocolate")
print(shopping)

**Ausgabe
['chocolate', 'kiwis', 'peas', 'lemon']
```



### <u>Daten-Entfernen in Listen</u>

##### `Listenname.pop()`       -> jeweils nur einen Wert am Ende der Liste entfernen

##### `Listenname.pop(index)`     ->  jeweils nur einen Wert einem bestimmten Index entfernen

```python
todo = ["call mom", "dishes", "homework", "chat"]
todo.pop()
todo.pop(0)
print(todo)

**Ausgabe
['dishes', 'homework']
```

##### `removed = Listenname.pop()`  -> den von `Listenname.pop()` entfernten Wert in einer Variable speichern

```python
todo = ["call mom", "dishes", "painting"]
removed = todo.pop(0)
print(removed)

**Ausgabe
call mom
```



### <u>Durchlaufen von Listen</u>

##### Alle Elemente von der Liste mit einer `for`-Schleife zu Schleife durchlaufen

```python
student_grades = ["A", "A-", "C"]

for grade in student_grades:
  print(grade)
  
**Ausgabe
A
A-
C
```

```python
data_points = [96, 97, 98, 99]

for data in data_points:
  print(data + 1)
  
**Ausgabe
97
98
99
100
```





### <u>Mit listen entscheiden</u>

##### `len(Listenname)` Anweisung -> um die Anzahl der Elemente in einer Liste zu erhalten       leere Liste -> zeigt 0

```python
users = ["Sarah", "Mike", "Ella"]
number_of_users = len(users)
print(number_of_users)

**Ausgabe
3
```

##### `len(Listenname) > 0`  ->  um bedingte Anweisungen basierend auf der Anzahl der Elemente zu erstellen

```python
tasks = ["dishes", "windows", "vacuum"]
if len(tasks) > 0:
  print("Ugh, more work!")
  
**Ausgabe
Ugh, more work!
```





## Verwendung von Listen

### <u>Extreme Daten finden</u>

##### `max(Listenname)` -> um Maximum (größte Zahl in einer Liste) zu finden

##### `min(Listenname)` -> um Minimum (kleinste Zahl in einer Liste) zu finden

##### Wiederverwendung der Ergebnisse von `max(Listenname)` und `min(Listenname)` und Speichern in neuen Variablen

```python
scores = [3, 6, 1, 12]
min_score = min(scores)
max_score = max(scores)

print(max_score)
print(min_score)

**Ausgabe
12
1
```



### <u>Daten sortieren</u>

##### `Listenname.sort()`   -> um die Werte einer Liste zu sortieren

##### - für neg. und pos. Zahlen (Float und Integer)   -> in aufsteigender numerischer Reihenfolge     `-2, 0, 0.5, 1, 4`

##### - für Strings  -> in alphabetischer Reihenfolge      `A, B, C ... Z`

```python
temperatures = [-1, 4, 0, -3.5, 2, 6.5]
temperatures.sort()
print(temperatures)

**Ausgabe
[-3.5, -1, 0, 2, 4, 6.5]
```

```python
destinations = ["Germany", "Italy", "Austria"]
destinations.sort()
print(destinations)

**Ausgabe
['Austria', 'Germany', 'Italy']
```



### <u>Daten summieren</u>

##### `sum(Listenname)` -> um die Summe einer Liste zu berechnen

##### *die Liste enthält nagitive Zahlen  -> die Summe der positiven Zahlen abzüglich der negativen Zahlen bekommen

```python
scores = [3, 6, -2, 1, 12, -4]
total = sum(scores)
print(total)

**Ausgabe
16
```



### <u>Listen zusammenführen</u>

##### mit `+` Operator    ->  um die Elemente der Listen (sogar der verschiedenen Typen) zu einer neuen Liste zu kombinieren

##### Reihenfolge nach Kombinieren  `list_1 + list_2`      ->   `list_2` wird am Ende der `list_1` angehängt

```python
dataset_1 = [1, 2, 3]
dataset_2 = [4, 5]
combined = dataset_1 + dataset_2
print(combined)

**Ausgabe
[1, 2, 3, 4, 5]
```

```python
team_1 = ["Ana", 78, "Joe", 80]
team_2 = ["Kim", 57, "Sam", 60]
all_scores = team_1 + team_2
print(all_scores)

**Ausgabe
['Ana', 78, 'Joe', 80, 'Kim', 57, 'Sam', 60]
```



### <u>Elemente zählen</u>

##### `Listenname.count(Element)`       -> zählt, wie oft ein Wert in einer Liste vorkommt

##### *Jede Art von Werten können wir mit `Listenname.count(Element)` verwenden     -> String, Boolean, Integer, Float

```python
flavors = ["vanilla", "chocolate", "strawberry", "vanilla", "vanilla"]

choco_flavor = flavors.count("chocolate")
print(choco_flavor)

print(flavors.count("vanilla"))

**Ausgabe
1
3
```

##### *Wenn der zu zählende Wert nicht existiert - gibt Null zurück

```python
grades = ['A', 'B', 'C']
print(grades.count('D'))

**Ausgabe
0
```

##### `Element in Listenname`    -> überprüft, ob eine Liste ein Element enthält      -> Ergebnis nur Boolean wie `True/ False`

```python
ingredients = ["flour", "butter", "suagr", "eggs"]

has_sugar = "sugar" in ingredients
print(has_sugar)

print("chocolate" in ingredients)

**Ausgabe
True
False
```





## Verwendung von Strings

### <u>String teilen</u>

##### `variable.split()`  -> Strings aufteilen und die einzelnen Werte in einer Liste speichern

##### Standard-String-Trennzeichen -> whitespace 空格

```python
words = "gear fault lights build-up"
word_list = words.split()
print(word_list)

**Ausgabe
['gear', 'fault', 'lights', 'build-up']
```

##### `variable.split(",")`  -> wenn String-Trennzeichen ist ","

```python
user = "Lauren,25,F,Architect"
user_1 = user.split(",")
print(user_1)

**Ausgabe
['Lauren', '25', 'F', 'Architect']
```

##### `variable.split("/")`  -> wenn String-Trennzeichen ist  "/"

```python
path = "getmimo.com/glossary/python"
path_list = path.split("/")
print(path_list)

**Ausgabe
['getmimo.com', 'glossary', 'python']
```



### <u>String aktualisieren</u>

##### `variable.replace("ursprünglich","neu")` -> einen Teil des ursprünglichen Strings durch einen neuen Wert ersetzen

```python
speical = "Today's speical is pasta"
new_special = special.replace("pasta","pizza")
print(new_special)
print(speical)

**Ausgabe
Today's special is pizza
Today's special is pasta
```

##### *mehrfaches Vorkommen eines Werts in einem String -> Alle Vorkommen des Werts wird ersetzt

```python
june = "June sales target updated. Let's rock June!"
july = june.replace("June","July")
print(july)

**Ausgabe
July sales target updated. Let's rock July!
```



## Datentypen verwalten

##### `type(Wert)`   -> den Datentyp des Werts anzeigen

```python
print(type("hello"))
print(type(10.5))
print(type(10))
print(type(True))

**Ausgabe
<class 'str'>
<class 'float'>
<class 'int'>
<class 'bool'>
```



#### <u>Typkonvertierung</u>  -> Werte von einem Typ in einen anderen ändern

##### `str()`   -> um numerische Werte in Strings zu verwenden

```python
position = 3
update = "You are now number " + str(position) + " in the queue."
print(update)

**Ausgabe
You are now number 3 in the queue.
```

##### `float()`   -> um ein String/ Ganzzahl in einen Dezimalwert zu konvertieren

```python
total = "6.50"
items = 3
average = float(total)/ items
print('The average price is' + str(average))

**Ausgabe
The average price is 2.1666666666666665
```

##### `int()`   -> um einen Dezimalwert/ String/ Boolean in eine ganze Zahl zu konvertieren

##### *für einen Dezimalwert ->  nachfolgende Dezimalkomma und Werten entfernen, anstatt runden    -> umgekehrt `float()`

```python
price = 9.99
print(int(price))

**Ausgabe
9
```

##### *für String

```python
price = 30
tip = "5"
total = price + int(tip)
print(total)

**Ausgabe
35
```

##### * für Boolean     numerische Werte -> 1 für `True`,  0 für `False`

```python
member = True
value = int(member)
print(value)

**Ausgabe
1
```

#####  -> umgekehrt   `bool()`  ->  um ein String/ Ganzzahl in Boolean zu konvertieren

```python
detail = "I like it"
response = bool(detail)
print(response)

**Ausgabe
True
```



### <u>Typkonvertierung geeigneter zusammengesetzter Datenstrukturen</u>

##### `list()`

##### `dict()`  -> eine Liste von Tupeln nehmen und daraus ein Wörterbuch erstellen

```python
users = dict([('James', 25), ('Amanda', 19), ('Mark', 33)])
print(users)

**Ausgabe
{'James': 25, 'Amanda': 19, "Mark": 33}
```

```python
user_1 = [1, 'Sara']
user_2 = [2, 'Andy']
data = dict([user_1, user_2])
print(data)

**Ausgabe
{1: 'Sara', 2: 'Andy'}
```

##### `set()`

```python
choices = ['pizza', 'kebab', 'burger', 'pizza']
unique = set(choices)
print(unique)

**Ausgabe
{'burger', 'pizza', 'kebab'}
```

##### `tuple()` -> eine Liste in ein Tupel umwandeln

```python
info = ['Male', 26, 'David']
record = tuple(info)
print(record)

**Ausgabe
('Male', 26, 'David')
```





## Funktionen

### <u>Code mit Funktionen wiederverwenden</u>

##### `def funktion_name():`   -> um zusammengehörige Code zu gruppieren und die Aufgabe an einem Ort auszuführen

```python
def greet_user():
  print("Good morning Anna")
  print("Welcome back")
  
greet_user()

**Ausgabe
Good morning Anna
Welcome back
```



### <u>Parameter erstellen</u>

##### - Parameter fungiert als spezielle Variable innerhalb der Funktion-Klammern     `funktion_name(Parameter)`

##### *mithilfe des Parameters - muss ähnliche Code nicht mehr duplizieren - sondern jedes Mal einen neuen Wert übergeben

```python
def greet(name):
  print(f"Hello, {name}")
  
greet("April")
greet("Leslie")

**Ausgabe
Hello, April
Hello, Leslie
```

##### *Vergleich: mit und ohne Parameter

```python
def user_status(status):
  print(f"Bob is {status}")
  
user_status("Active")

**Ausgabe
Bob is Active
```

```python
def user_status():
  status = "Active"
  username = "Bob"
  print(f"{username} is {status}")
  
user_status()

**Ausgabe
Bob is Active
```





### <u>Rückgabewerte</u>

##### `return Rückgabewert`   -> um etwas von einer Funktion zurückzugeben

##### *Jeder beliebige Werttyp kann zurückgegeben - wie String, Integer, Float, Boolean

##### *wenn `return`-Anweisung nicht in der Funktion steht   -> die Funktion gibt `None` zurück

```python
def half_twice(number):
  half = number/ 2
  half_again = half/ 2
  return half_again

result = half_twice(12)
print(result)

**Ausgabe
3.0
```

```python
def age_label(age):
  label = "User age: " + age
  return label

result = age_label("29")
print(result)

**Ausgabe
User age: 29
```





### <u>Verwenden mehrere Parameter</u>

##### `Funktion_name(Parameter_1, Parameter_2, Parameter_3)`    -> um eine Funktion mehrere Parameter hinzufügen

##### *Wir übergeben Werte in der Reihenfolge, in der deren Parameter in der Funktionsdefinition platziert sind

```python
def show_winner(first, second, third):
  print("First place: " + first)
  print("Second place: " + second)
  print("Third place: " + third)
  
show_winners("Kim", "Lee", "Ava")

**Ausgabe
First place: Kim
Second place: Lee
Third place: Ava
```

```python
def create_email(name, year):
  return name + year + "@hutmail.com"

email = create_email("jo", "1998")
print(email)

**Ausgabe
jo1998@hutmail.com
```





### <u>Funktionen verstehen</u>

##### - Name soll aussagekräftig sein - um auf einen Blick zu wissen, was die Funktion macht

##### - Funktionsnamen beginnen normalerweise mit Verben     - wie  `create`   `compute`   `get`   `calculate`

```python
def display_item_price(item, price):
  print(f"{item}:{price}$")
  
display_item_price("chocolate", 3)

**Ausgabe
chocolate: 3$
```

##### - Sonderfall bei Boolean      - Verben wie `is`   `can`   `has`

```python
def is_freezing(temperature):
  return temperature < 0

freezing = is_freezing(-3)
print(freezing)

**Ausgabe
True
```

##### - Beibehaltung der gleichen Funktionsbenennung  -> das gleiche Verb verwenden, die ähnlichen Aufgaben auszuführen

```python
def calculate_sum(num_1, num_2):
  return num_1 + num_2

def calculate_difference(num_1, num_2):
  return num_1 - num_2

sum = calculate_sum(5, 3)
print(sum)

difference = calculate_difference(5, 3)
print(difference)

**Ausgabe
8
2
```



##### *Typen von der Eingabe und Ausgabe müssen nicht gleich sein        z.B. Eingabe String -> Ausgabe Boolean

```python
def is_same_world(word_1, word_2):
  print(word_1 == word_2)
  
is_same_word("dexter", "dexterous")

**Ausgabe
False
```





### <u>Variablen-Geltungsbereich</u>

##### - Innerhalb einer Funktion erstellte Variablen haben einen lokalen Geltungsbereich  -> nur innerhalb darauf zugreifen

```python
def apply_discount(price):
  discount = 20
  discount = 10
  return price - discount

final_price = apply_discount(50)
print(final_price)

**Ausgabe
40
```

##### - Außerhalb einer Funktionsblock erstellte Variablen haben einen globalen Geltungsbereich -> überall darauf zugreifen

```python
rent = 1000

def calculate_spendings(groceries):
  print(f"Total {rent + groceries}")
  
print(f"Rent {rent}")
calculate_spendings(300)

**Ausgabe
Rent 1000
Total 1300
```





### <u>Entscheiden mit Funktionen</u>

##### - Verschachteln einer Bedingung innerhalb der Funktion - zwei Leerzeichen vom Anfang der Funktion entfernt einrücken

##### - Verwendung des Parameters als Teil der Bedingung - Entscheidung-Treffen basierend auf verschiedenen Eingabewerten

##### *`if-else` Anweisung Beispiel: Versandkosten hinzufügen oder nicht - basierend auf Warenkorb-Wert

```python
def add_shipping(cart):
  if cart < 100:
    print(f"Total: {cart + 10}")
  else:
    print(f"Total: {cart}")
    
add_shipping(45)
add_shipping(200)

**Ausgabe
Total: 55
Total: 200
```

##### `elif` Anweisung

```python
def calculate(operator, x, y):
  if operator == "+":
    print(x + y)
  elif operator == "-":
    print(x - y)
  else:
    print(f"unknown: {operator}")
    
calculate("-", 30, 10)

**Ausgabe
20
```

```python
def show_score(score):
  if score < 30:
    print("Score too low")
  elif score == 100:
    print("Top score!")
  else:
    print("Onto the next level!")
    
show_score(100)

**Ausgabe
Top score!
```





### <u>Funktionen mit Listen</u>

##### Jede Art von Listenoperationen kann man innerhalb von Funktionen verwenden  `count()`   `sum()`   `len()`   `replace()`

##### `len()`

```python
def is_booked(passengers):
  print(len(passengers) > 4)
  
passengers = ["June", "Sam", "Lee"]
is_booked(passengers)

**Ausgabe
False
```

##### Daten anhand des Index aufrufen

```python
def get_winner(top_players):
  winner = top_player[0]
  print(f"Game winner: {winner}")
  
top_player = ["Jay", "Meg", "Bob"]
get_winner(top_players)

**Ausgabe
Game winner: Jay
```

##### Daten anhand des Index aktualisieren

```python
def set_initials(names, initial):
  names[0] = initial
  return(names)

author_names = ["Francis", "Scott", "Fitzgerald"]
author_names = set_initials(author_names, "F.")
print(author_names)

**Ausgabe
['F.', 'Scott', 'Fitzgerald']
```





### <u>Funktionen mit Schleifen</u>

##### `while` Schleife

```python
def onboard_passengers(bookings):
  counter = 1
  while counter <= bookings:
    print(f"Passenger {counter} on board")
    counter += 1
    
onboard_passengers(4)

**Ausgabe
Passenger 1 on board
Passenger 2 on board
Passenger 3 on board
Passenger 4 on board
```

##### `for` Schleife

```python
def display_progress(total_files):
  for i in range(total_files):
    print(f"Downloading file {i} out of {total_files}")
    
display_progress(3)

**Ausgabe
Downloading file 0 out of 3
Downloading file 1 out of 3
Downloading file 2 out of 3
```

```python
def show_next_track(playlist):
  for track in playlist:
    print(f"Next up: {track}")
    
beethoven = ["Symphony No. 1", "Symphony No. 9"]
beatles = ["Hey Jude", "Helter Skelter", "Something"]

show_next_track(beethoven)
show_next_track(beatles)

**Ausgabe
Next up: Symphony No. 1
Next up: Symphony No. 9
Next up: Hey Jude
Next up: Helter Skelter
Next up: Something
```





## Datenstrukturen - Tupel, Wörterbücher und Sets

### <u>Tupel</u>

##### `variable = ("tuple_1", "tuple_2" )`    - Gruppierung beliebig vieler eng verwandter Daten

##### *Als Sonderfall:  Tupel enden mit nur einem Wert ohnehin mit einem Komma     `user_data = ("joe_17",)`

##### - Hauptunterschied zu Listen: Werte aus Tupeln kann man nicht aktualisieren/ hinzufügen/ löschen

##### - Tupel ist unveränderlich - um Informationen/ Fakten zu speichern, die wir normalerweise nicht ändern möchten

##### *Jedes Tupel in Klammer `()` zählt als ein Element

```python
scores = [("mia", 75), ("lee", 90)]
mia_score = scores[0]
print(mia_score)

**Ausgabe
('mia', 75)
```

##### *Jede Art von Schleife kann man verwenden, Loop-Over eine Liste von Tupeln zu durchlaufen   z.B. `for` Schleife

```python
scores = [("mia", 75), ("lee", 90)]

for user_score in scores:
  print(f"Result: {user_score}")
  
**Ausgabe
Result: ('mia', 75)
Result: ('lee', 90)
```

##### Zurückkehrende Tupel - mehrere Werte in Funktion zurückgeben     `return tutel_1,  tupel_2`

```python
def get_scores_data(score_list):
  highest_score = max(scores_list)
  lowest_score = min(scores_list)
  return highest_score, lowest_score

scores = [31, 17, 80]
data = get_scores_data(scores)

highest = data[2]
lowest = data[1]
print(f"highest score: {highest}")
print(f"lowest score: {lowest}")

**Ausgabe
highest score: 80
lowest score: 17
```

```python
def get_top_three(players):
  return players[0], players[1], players[2]

players = ["Sue", "Ed", "Ann", "Ty"]
top_three = get_top_three(players)
print(f"First: {top_three[0]}")
print(f"Second: {top_three[1]}")
print(f"Third: {top_three[2]}")

**Ausgabe
First: Sue
Second: Ed
Third: Ann
```

##### Im Vergleich zur zurückgegebenen Liste - die zurückgegebene Werte als Sammlung zu ändern

```python
def form_team(players):
  team = []
  team.append(players[0])
  team.append(players[2])
  return team

palyers = ["Sue", "Ed", "Ann", "Ty"]
team = form_team(players)
team[0] = "Chole"
print(team)

**Ausgabe
['Chole', 'Ann']
```

 

### <u>Wörterbuch</u> 

##### -> um jeden Wert einer Sammlung mit einem aussagekräftigen "Label" anstelle eines Index zu verknüpfen

##### -> bestehen aus mehreren Schlüssel-Wert-Paaren - Jedem Schlüssel ist genau ein Wert eindeutig zugeordnet

##### -> allgemein von geschweiften Klammern `{}` umgegeben,  jeweils durch Doppelpunkt `:` getrennt und  von `,` gefolgt

##### -> Schlüssel - wie beschriftete Index, die Werte zu identifizieren - Schüssel und Werte können jeden Typ sein

##### *Wörterbuch erstellen

```python
car_data = {
  "brand": "Cadillac",
  "year": 1960,
  "restoration": ["1990", "2018"],
  "rented": False
}

print(car_data)

**Ausgabe
{'brand': 'Cadillac', 'year': 1960, 'restoration': ['1990', '2018'], 'rented': False}
```

##### *Wörterbuch verwenden

##### -> ein Schlüssel-Wert aufrufen

```python
actor_bio = {
  "name": "Bill Murray",
  "known for": ["Lost in Translation", "Rushmore"]
}

actor_name = actor_bio["name"]
print(actor_name)

**Ausgabe
Bill Murray
```

##### -> alle Schlüssel-Werte mit `for` Schleife aufrufen        `for Schlüssel in Wörterbuch`

```python
contents = {
  "ch. 1": "A long-expected party",
  "ch. 2": "The shadow of the past",
  "ch. 3": "Three is company"
}

for chapter in contents:
  print(contents[chapter])
  
**Ausgabe
A long-expected party
The shadow of the past
Three is company
```

##### -> Schlüssel-Werte aktualisieren u. einen neuen Schlüssel-Wert-Paar hinzufügen  `Wörterbuch["Schlüssel"] = neu`

```python
toppings = {
  "olives": True,
  "anchovies": False,
  "cheese": True
}

topping["cheese"] = False
topping["salami"] = True

print(toppings)

**Ausgabe
{'olives': True, 'anchovies': False, 'cheese': False, 'salami': True}
```

##### -> Überprüfen, ob ein Wörterbuch einen bestimmten Schlüssel enthält      `Schlüssel in Wörterbuch`

```python
stock = {
  "S": 17,
  "M": 30,
  "L": 20
}

has_XS = "XS" in stock
print(has_XS)

**Ausgabe
False
```

##### -> ein Schlüssel-Wert-Paar entfernen      `Wörterbuch.pop("Schlüssel")`

##### *am besten vor dem Entfernen zu überprüfen, ob Schlüssel im Wörterbuch vorhanden ist ->  um Fehler zu vermeiden

```python
ticket = {
  "seat no.": 25,
  "window": True
}

if "destination" in ticket:
  ticket.pop("destination")

print(ticket)

**Ausgabe
{'seat no.': 25, 'window': True}
```

##### -> den Wert des entfernten Schlüssels zu speichern

```python
participants = {
  "Meg": True,
  "Kim": False,
  "Luis": True,
  "Luis M.": False
}

kim = participant.pop("Kim")
print(kim)

**Ausgabe
False
```



### <u>Sets</u>

##### - Sets sind Sammlung von Werten, bei denen jeder nur einmal vorkommen kann -> einzigartig, haben keine Duplikate

##### - sets erstellen - Setwerte von geschweiften Klammern `{}` umgegeben    `set_name = {"setwert_1", "setwert_2"}`

##### -> einen neuen Setwert mit `add()` Anweisung hinzufügen    `set_name.add("neu")`

##### *wenn man einen bereits vorhandenen Wert hinzufügen - das Set bleibt unverändert

```python
answers = {"yes", "no"}
answers.add("maybe")
print(answers)

**Ausgabe
{'no', 'maybe', 'yes'}
```

##### -> Sets sind ungeordnet -> Set-Elemente haben keine Index

##### *kann nur Überprüfen, ob ein Set ein Element enthält      `"set_element" in set_name`

```python
answer_options = {"yes", "no"}
print("no" in answer_options)

**Ausgabe
True
```

##### -> die Existenz mehreren Set-Elementen mit `for` Schleife überprüfen

```python
networks = {"May's", "PizzaParty5", "Wi-Free"}

for network in networks:
  print(f"Connect to: {network}")
  
**Ausgabe
Connect to: PizzaParty5
Connect to: Wi-Free
Connect to: May's
```

##### -> ein Set-Element entfernen    `set_name.remove("Set-Element")`

##### *am besten vor dem Entfernen überprüfen, ob ein Element in einem Set enthalten ist -> um Fehler zu vermeiden

```python
arrivals = {"BA1476", "DF2255", "KF3280"}

if "DF2255" in arrivals:
  arrivals.remove("DF2255")
  
print(arrivals)

**Ausgabe
{"KF3280", "BA1476"}
```

##### -> um Duplikate (doppelte Werte) aus einer Liste zu entfernen     `set(list_name)`

```python
drinks_list = ["matcha", "chai" "espresso", "americano", "chai", "matcha"]

drinks_set = set(drinks_list)
print(drinks_set)

**Ausgabe
{'chaiespresso', 'chai', 'americano', 'matcha'}
```

##### -> die Größe der Set-Mengen zu erhalten    `len(set_name)`

```python
invitations = {"Meg", "Alex", "Lee"}
print(f"{len(invitations)} invitations sent)

**Ausgabe
3 invitations sent
```

##### -> Überprüfen, ob alle Elemente der (L) Menge eine Teilmenge einer (R) anderen ist   `link_set.issubset(recht_set)`

```python
friends = {"Emma", "Jen", "Rob", "Ed"}
study_group = {"Emma", "Lisa"}

are_friends = study_group.issubset(friends)
print(are_friends)

**Ausgabe
False
```

##### -> die Elemente zweier Mengeen zu einer neuen Menge ohne Duplikate zu verbinden    `set_1.union(set_2)`

```python
arrivals = {"JL5273", "NH5753"}
departures = {"AA5827", "BA4616"}

all_flights = arrival.union(departures)
print(all_flights)

**Ausgabe
{'JL5273', 'BA4616', 'NH5753', 'AA5827'}
```

##### -> die identisch gleichen Elementen von zwei Mengen zu einer neuen Menge zu erstellen   `set_1.intersection(set_2)`

```python
classmates = {"Sue", "Luke", "Paul"}
friends = {"Don", "Sue", "Luke"}

common = classmates.intersection(friends)
print(f"Common: {common}")

**Ausgabe
Common: {'Sue', 'Luke'}
```

##### -> Elemente anzeigen, die in der (L) Menge vorhanden, aber in der (R) Menge fehlen   `link_set.difference(recht_set)`

```python
wishlist = {"earpods", "notebook", "handgloves"}
cart = {"cat food", "book", "earpods"}

print(wishlist.difference(cart))
print(cart.difference(wishlist))

**Ausgabe
{'notebook', 'handgloves'}
{'cat food', 'book'}
```



## Listenverständnis

###  <u>Listenverständnis verwenden</u>

##### -> zum Erstellen neuer Listen basierend auf bestehenden in wenigen Code

##### -> Listen-Abstraktion mit `for` Schleife   ->  `neu_list = [ Ausdruck for alt_Listenelement in alt_list ]`

##### *Der Ausdruck wird auf jedes Element der alten Liste angewendet und der `for` Schleife wird darauf zugegriffen

##### *Beispiel:  `halved_lc`  ist eine äquivalente, aber kompaktere Version der  `halved_loop`

```python
prices = [10, 38, 40, 58, 62]

halved_lc = [price/2 for price in prices]
print(halved_lc)

halved_loop = []
for price in prices:
  half_price = price/2
  halved_loop.append(half_price)
print(halved_loop)
  
**Ausgabe
[5.0, 19.0, 20.0, 29.0, 31.0]
[5.0, 19.0, 20.0, 29.0, 31.0]
```

##### -> Listenverständnis funktioniert mit jeder Art von Listenelementen wie Zahlen, Strings, Booleans, Tupel und mehr

```python
names = ["Smith", "Miller", "Brown"]
prefixed = ["Mr. " + name for name in names]
print(prefixed)

*Ausgabe
['Mr. Smith', 'Mr. Miller', 'Mr. Brown']
```

##### -> eine Kopie der Originalliste erstellen - Jedes Element wird ohne Änderungen kopiert

```python
meters = [100, 3800, 4000]
meters_copy = [m for m in meters]

print(meters)
print(meters_copy)

**Ausgabe
[100, 3800, 4000]
[100, 3800, 4000]
```

##### -> um das Vorkommen des Buchstabens  `"a"`  in jedem  `word`  zu zählen  `.count()`

```python
words = ["apple", "aligator", "abracadabra", "avatar"]

a_count = [word.count("a") for word in words]
print(a_count)

**Ausgabe
[1, 2, 5, 3]
```





### <u>Funktionen als Ausdruck</u>

##### -> mehrere Operationen in einer Funktion packen und als Ausdruck verwenden

##### *Wir können nur Funktionen verwenden, die eine return-Anweisung haben, da wir den zurückgegebenen Wert tatsächlich an die neue Liste anhängen. 

##### Beispiel: Halbierung des Preises nach Steuer-Entfernen

```python
prices = [10, 22, 30, 40, 58, 60]
def halve(num):
  no_tax = 0.85 * num
  return no_tax/ 2

halved = [halve(price) for price in prices]

print(halved)

**Ausgabe
[4.25, 9.35, 12.75, 17.0, 24.65, 25.5]
```

##### ->  `add_comma()` Funktion -> den Namen in einer Liste mit `split()` teilen

```python
authors = ["Virginia Wolf", "John Steinbeck"]

def add_comma(name):
  parts = name.split(" ")
  return parts[1] + ", " + parts[0]

authors_update = [add_comma(name) for name in authors]

print(authors_update)

**Ausgabe
['Wolf, Virginia', 'Steinbeck, John']
```

##### -> `passed()` Funktion   - Beispiel: ob eine Punktzahl über 90 liegt wenn 10 Bonuspunkte hinzufügt

```python
scores = [156, 70, 100]

def passed(scores):
  with_bonus = score + 10
  passed = with_bonus > 90
  return passed

passing_scores = [passed(score) for score in scores]

print(passing_scores)

**Ausgabe
[True, False, True]
```





### <u>Filtern mit if Anweisungen</u>

##### -> nach Elemente zu filtern, die eine bestimmte Bedingung erfüllen; und dann eine neue Liste erstellen

##### -> Reihenfolge: zuerst Ausdruck, gefolgt von der `for`-Schleife, endet mit einer bedingten `if`-Anweisung

```python
humidity_percent = [40, 35, 20, 70]
ideal = [level for level in humidity_percent if level >= 30 and level <= 50]
print(ideal)

**Ausgabe
{40, 35}
```

##### Beispiel: eine neue Liste mit nur französischen Websites erstellen

```python
websites = ["nytimes.com", "lemonde.fr", "economist.com"]
french = [website for website in websites if website.count(".fr") > 0]
print(french)

**Ausgabe
['lemonde.fr']
```



### <u>Negative Index</u>

##### -> negative Indizierung - ein Element vom ganz rechten Ende einer indizierbaren Objekts abzurufen   `[-n,..., -2, -1]`

##### *Alle positive oder negativen Indexwerte können wir beim Abrufen eines Listenelements innerhalb der Liste verwenden

```python
user = ("Joe", "Paris", 27)
name = user[0]
age = user[-1]
message = f"{name} {age}"
print(message)

**Ausgabe
Joe 27
```

##### -> Listenelement nach negativen Index ändern

```python
users = ["Jack", "Ahmed", "Elaine"]
users[-3] = "Jill"
print(users)

**Ausgabe
['Jill', 'Ahmed', 'Elaine']
```

##### -> Elemente innerhalb Datenstruktur nach neg. Index mit `del` Anweisung löschen - ausschließlich unveränderlich Tupel

```python
winners = ["John", "Helene", "Sigmund", "Olaf"]
del winners[-1]
print(winners)

**Ausgabe
['John', 'Helene', 'Sigmund']
```

##### -> unerwünschte Schlüssel-Wert-Paar aus dem Wörterbuch mit `del` Anweisung entfernen

```python
details = {
  "name": "Alex",
  "age": 22,
  "gender": "Female"
}

del details["gender"]
print(details)

**Ausgabe
{'name': 'Alex', 'age': 22}
```



### <u>Slice notation</u>

##### - mithilfe von Slicing - mehrere Werte aus einer Liste abrufen    `[start:stop:step]`

##### *Jeder Wert von  `start`,  `stop`  und  `step` kann positiv, negativ oder komplett weggelassen werden

#####  `start:`  -> Startposition fürs Slice         `[a:]` -> ab Listenposition `[a]` bis zum Ende der Liste

##### `:stop` -> Stopposition fürs Slice   `[:b]` -> ab Listenanfang bis zum Listenposition `[b]` (aber [b] soll nicht enthalten)

##### `::step` -> Schrittwert fürs Slice  `[::c]`      Beispiel  `[::3]`  -> jeden dritten Wert zurückgeben

##### *`step` ohne `start` oder `stop` verwenden  ->  `step` muss immer 2 vorangestellte Doppelpunkte haben

```python
letters = ["A", "B", "C", "D", "E", 'F']
print(letters[::2])

**Ausgabe
['A', 'C', 'E']
```

##### *wenn ein negativer `step` ohne `start` ohne `stop` angegeben ist - arbeitet Python automatisch am Ende einer Liste

```python
letters = ["A", "B", "C", "D", "E", 'F']
print(letters[::-3])

**Ausgabe
['F', 'C'
```

##### *`step` kann negativ sein - in dem Fall muss `start` größer als `stop` - die Reihenfolge der Elemente ist umgekehrt

```python
letters = ["A", "B", "C", "D", "E", 'F']
print(letters[3:0:-1])

**Ausgabe
['D', 'C', 'B']
```

##### *Die Angabe eines Bereichs außerhalb der Liste-Länge gibt eine leere Liste `[]` zurück und führt nicht zu einem Fehler

```python
letters = ["A", "B", "C", "D", "E", 'F']
print(letters[7:])

**Ausgabe
[]
```

##### *wenn nur ein Doppelpunkt angegeben ist - vom Anfang bis zum Ende der vollständigen Originaliste

```python
letters = ["A", "B", "C", "D", "E", 'F']
print(letters[:])

**Ausgabe
['A', 'B', 'C', 'D', 'E', 'F']
```





## Klassen

### <u>Klassen und Instanz erstellen</u>

##### - Klasse - eine Vorlage dafür, viele ähnliche, aber unterschiedliche Dinge zu erstellen      `class Klassendefinition:`

##### - Instanz von einer Klassenvorlage erstellen  `instanz = Klassendefinition()`

##### - auf eine Klassenvariable zugreifen     `instanz.klassenvariable`

```python
class Virtual_Pet:
  wagging_tail = True
  color = "brown"
  
skippy = Virtual_Pet()
print(skippy.wagging_tail)
print(skippy.color)

**Ausgabe
True
brown
```



### <u>Klassenmethode</u>

##### -`self` als erste Parameter für alle Klassenmethode verwenden, um den Gültigkeitsbereich von Klassenvariablen innerhalb einer Methode zugänglich zu machen -> damit kann man auf die Klassenvariablen innerhalb der Methode zugreifen

```python
class Virtual_Pet:
  color = "brown"
  legs = 4
  
  def bark(self):
    print("Bark")
    
  def display_color(self):
    print("I'am" + self.color)
    
  def display_legs(self):
    print(self.legs)
    
  rocky = Virtual_Pet()
  rocky.display_color()
  rocky.display_legs()
  
**Ausgabe
I am brown
4
```





### <u>Konstruktormethode</u>

##### - Zweck: um jede Instanz eines Klassenobjekts mit eindeutigen Klassenvaribalen zu konstruieren `def __init__(self):`

```python
class Flower:
  def __init__(self, kind, color):
    self.kind = kind
    self.color = color
  
  def display_color(self):
    print(self.color)
    
  rose_flower = Flower("rose", "red")
  print(rose_flower.kind)
  rose_flower.display_color()
  
  **Ausgabe
  rose
  red
```

```python
class Computer:
  def __init__(self, size, storage):
    self.size = size
    self.storage = storage
    
  def print_specs(self):
    print("Display size: " + self.size)
    print("Storage size: " + self.storage)
    
low_spec = Computer("13", "256GB")
high_spec = Computer("27", "1TB")

print("Low Spec Computer: ")
low_spec.print_specs()

print("High Spec Computer: ")
high_spec.print_specs()

**Ausgabe
Low Spec Computer:
Display size: 13
Storage size: 256GB
High Spec Computer:
Display size: 27
Storage size: 1TB
```



### <u>Funktionen innerhalb der Klassen</u>

##### - Alle grundlegende Python-Sprachfunktionen können wir innerhalb einer Klasse verwenden

```python
class Pie:
  def __init__(self, flavor, ingredients):
    self.flavor = flavor
    self.ingredients = ingredients
    
  def print_ingredients(self):
    for i in self.ingredients:
      print(i)
      
applePie = Pie('apple', ['flour', 'eggs', 'apples', 'butter'])
applePie.print_ingredients()

**Ausgabe
flour
eggs
apples
butter
```

```python
class Book_Series:
  def __init__(self, name, books):
    self.name = name
    self.books = books
    self.num_books = len(books)
    
  def print_name(self):
    print(self.name)
    
  def print_books(self):
    print(self.books)
      
hg = Book_Series("Hunger Games", ["The Hunger Games", "Catching Fire", "Mockingjay"])

hg.print_books()
print(hg.num_books)

['The Hunger Games', 'Catching Fire', 'Mockingjay']
3
```





## Objektorientierte Programmierung

##### verschiedene Programierungsstile -> Paradigmen

##### 1) funktionale Programmierung (FP): Daten und Funktionen getrennt halten -  z.B.`return` Funktion

```python
def getDistance(mph, h):
  return mph * h

mph = 60
h = 2

distance = getDistance(mph, h)
print(distance)

**Ausgabe
120
```

##### 2) Objektorientierte Programmierung (OOP): verwandte Daten und Funktionen als Eigenschaften und Methode innerhalb der selben Objekten gruppieren -> Kapselung

```python
class Piggy:
  value = 0
  def addMoney(self, amount):
    self.value = self.value + amount
    
myPiggy = Piggy()
myPiggy.addMoney(100)

print(myPiggy.value)

**Ausgabe
100
```

##### -> Umwandeln von FP in OOP

```python
def getArea(b, h):
  return b * h

base = 3
height = 4

class Rectangle:
  base = 3
  height = 4
  
  def getArea(self):
    return self.base * self.height
  
rect = Rectangle()
area = rect.getArea()
print(area)

**Ausgabe
12
```



### <u>Anwendung der Vererbung in OPP</u>

##### Vererbung - die Funktionalität einer anderen Klasse erben ->  Funktion muss nur einmal eingestellt werden -> effizienter

```python
class Parent:
  def __init__(self):
    self.eyes = "green"
    
class Child(Parent):
  def __init__(self):
    super().__init__()
    self.age = 7
    
child = Child()
print(child.eyes)
print(child.age)

**Ausgabe
green
7
```

```python
class Car:
  def start_car(self):
    print("Starting Car")
    
class Hybrid(Car):
  def charge(self):
    print("Using fuel to charge battery")
    
class Electric(Car):
  def fuel(self):
    print("No fuel necessary")
    
prius = Hybrid()
prius.start_car()
prius.charge()

electric = Electric()
electric.start_car()
electric.fuel()

**Ausgabe
Starting Car
Using fuel to charge battery
Starting Car
No fuel necessary
```

##### `super().__init__()`   -> `super` bezieht sich auf die übergeordnete Klasse

##### *`super().__init__(name, age)` -> um sicherzustellen - Student hat die gleichen Eigenschaften wie Person

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
    
  def greet(self):
    print("Hi!")
    
class Student(Person):
  def __init__(self, name, age, major):
    super().__init__(name, age)
    self.major = major
    
student = Student("Sam", 23, "chemistry")
print(student.major)
student.greet()

**Ausgabe
chemistry
Hi!
```





### <u>abstrakte Objekte</u>

##### - Abstraktion - Ausblenden der Details  -> hilft anderen Entwicklern, eine Klasse zu verwenden, ohne Details zu wissen

##### - Abstraktion implementieren - ein paar Kernmethoden schreiben, die Low-Level-Funktionen verarbeiten

##### - Vorteile der Abstraktion -> weniger Fehler durch Benutzerfehler

```python
class Car:
  def __init__(self):
    self.on = False
    
  def injectFuel(self):
    print('Spraying fuel')
    
  def igniteFuel(self):
    print('Boom!')
    
  def startUp(self):
    self.on = True
    while self.on:
      self.injectFuel()
      self.igniteFuel()
      
**Ausgabe
Spraying fuel
Boom!
```

```python
class Coffeemaker:
  def heatWater(self):
    print('Heating water')
    
  def brew(self):
    print('Adding water to grounds')
    
  def filterCoffee(self):
    print('Filtering coffee')
    
  def makeCoffee(self):
    self.heatWater()
    self.brew()
    self.filterCoffee()
    
  coffeMaker = Coffeemaker()
  coffeMaker.makeCoffee()
  
**Ausgabe
Heating water
Adding water to grounds
Filtering coffee
```





### <u>Polymorphe Objekte</u>

##### - Polymorphismus - Klassenverhalten unterschiedlich implementieren - aber basierend auf seiner Oberklasse

##### - Unterklasse kann die Methode überschreiben, die sie von ihrer Oberklasse erbt -> die geerbte Methode in der Unterkasse definieren und das Verhalten ändern

```python
class Feline:
  def speak(self):
    print("Meow")
    
class Cat(Feline):
  def lick(self):
    print("Licking paw")
    
class Lion(Feline):
  def prey(self):
    print("Pounces on prey")
  def speak(self):
    print("ROAR!")
    
cat = Cat()
cat.speak()
lion = Lion()
lion.speak()

**Ausgabe
Meow
ROAR!
```







## Module

##### - mit Module kann man mehr Organisationen hinzufügen     `import modul_name`

##### -> `math` Modul - Daten und Methoden für verschiedene mathematische Operationen bieten

##### -> `statistics` Modul - Methoden bieten, bei allgemeinen Statistikfunktionen helfen z.B. Mittelwert

```python
import math, statistics

print("The value of pi is")
print(math.pi)

print("Euler's number:")
print(math.e)

print("The square root of 16 is")
print(math.sqrt(16))

print("Rounded up to the nearest number")
rounded = math.ceil(22.7324)
print(rounded)

diameters = [9, 7, 4, 6]
result = statistics.mean(diameters)
print(f"Mean diameter is {result}")

**Ausgabe
The value of pi is
3.141592653589793
Euler's number:
2.718281828459045
The square root of 16 is
4.0
Rounded up to the nearest number
23
Mean diameter is 6.5
```

##### -> `from modul_name import teil_modul` -> nur bestimmte Teil der gesamten Funktionalität eines Moduls importieren

##### *Name des Moduls muss nicht mehr hinzufügt  z.B. `mean` anstelle von `statistics.mean`

```python
from statistics import mean

test_scores = [33, 7, 4, 6]
result = mean(test_scores)
print(f"Mean result is {result}")

**Ausgabe
Mean result is 12.5
```

##### -> `import alt_name as neu_name` ->  Aliasing: ein Modul umbenennen (oft längere Modulnamen kürzer zu machen)

```python
import statistics as stats

sales = [23, 43, 26, 29, 18, 24]

median = stats.median(sales)
print(median)

**Ausgabe
26
```

##### - einige Module sind online zur Verfügung gestellt - damit andere Entwickler den Code wiederverwenden können

##### *Beispiel: Diagrammmodul

```python
import pygal

pie = pygal.Pie()
pie.title = "Time Spent On Social Networks"
pie.add("Twitter", 47)
pie.add("Facebook", 23)
pie.add("Instagram", 30)

pie.render_in_browser()

**Ausgabe
![](/Users/sqm/Desktop/IMG_6016.jpg)
```

##### - `help()` Anweisung - die Funktionalität eines Moduls herausfinden

```python
import math
square = math.sqrt(16)
help(math)

**Ausgabe
Help on built-in module math:
NAME
    math  
DESCRIPTION
    This module is always available. It provides access to the mathematical functions defined by the C standard.  
FUNCTIONS
    acos(...)
        acos(x)
        Return the arc cosine (measured in radians) of X....
```





## Fehler und Ausnahmen

### <u>Fehler</u>

##### `SyntaxError` - Python kann die Code nicht verstehen -> normalerweise Tippfehler (falsch geschriebene Schlüsselwörter; Einfügen eines Schlüsselworts an der falschen Stelle; Weglassen von Symbolen wie Doppelpunkten und Klammern; unvollständige Anweisungen ausführen; eine String fälschlicherweise als Variablenname verwenden)

##### `^` Symbol -> Caret: in Fehlermeldung anzeigen, wo der Fehler im Code liegt

##### -> `IndentationError` - eine falsche oder fehlende Einrückung, zusätzliche Leerzeichen



### <u>Ausnahmen</u>

##### `ZeroDivisionError` - etwas fälschlicherweise durch Null dividiert

##### `NameError` - eine nicht existierte/ definierende Variable verwenden

##### `KeyError` - Schlüssel existiert nicht im Wörterbuch

##### `TypeError` - Zusammenfügen von verschiedenen Typen nicht unterstützen

##### `IndexError` - Index liegt außerhalb des gültigen Bereichs

##### `ValueError` - z.B. Alter kann nicht negativ sein; Alter ist zu groß 

##### `ModuleNotFoundError` - ein zu importierendes Modul mit dem angegebenen Namen nicht finden kann

##### `raise Error("optionale Nachricht")` - wenn wir in Ausgabe hervorheben möchten, dass ein Fehler aufgetreten ist

##### *`Traceback` - hilft uns, die Code zu debuggen -> Fehler zu finden (von unten nach oben zu lesen - besser zu verstehen )



### <u>Ausnahmebehandlung</u>

##### - `try` and `except` Block - wird verwendet, dass wir wissen, dass die Möglichkeit besteht, dass die Operation unmöglich ist -> damit unser Programm Fehler effektiv behandeln und weiterlaufen kann

```python
try:
  login(user)
  
except:
  print('User not known, please try again')
  
**Ausgabe
User not known, please try again
```

##### - `raise` wird normalerweise innerhalb eines `except` Codeblock verwendet

##### - `pass` - wird verwendet, wenn wir möchten, dass nichts ausgeführt wird und zum nächsten Codeblock weitergehen

##### -`else` Anweisung - wird am Ende verwendet, wenn wir Code nur ausführen möchten, wenn kein Fehler aufgetreten ist

```python
details = {
  "name": "Helena",
  "occupation": "carpenter"
  "age": 35
}

try:
  age = details["age"]
except:
  raise NameError("No age value in record")
else:
  print(f"Maximum heart rate is {220 - age}")
  
**Ausgabe
Maximum heart rate is 185
```

##### - `finally` Anweisung - wird ganz am Ende verwendet, wenn wir verwandten Code ausführen möchten, unabhängig davon, ob ein Fehler (`except`) aufgetreten ist

```python
entry = 50

try:
  result = entry * 1.5
except:
  raise ValueError("result cannot be calculated")
else:
  print(result)
finnaly:
  print("Try another value?")
  
**Ausgabe
75.0
Try another value?
```















 
