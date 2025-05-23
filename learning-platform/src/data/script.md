## Działania dostępne w języku Python

W języku Python możemy wykonywać różne operacje arytmetyczne na liczbach.

```python=
4      # => 4
2 + 2  # => 4
5 - 2  # => 3
3 * 2  # => 6
9 / 2  # => 4.5
9 // 2 # => 4 (dzielenie całkowite)
2 ** 3 # => 8 (potęgowanie)
7 % 2  # => 1 (reszta z dzielenia)
2 * 2 + 2   # => 6
2 + 2 * 2   # => 6 (Python wie, jaka jest kolejność wykonywania działań)
(2 + 2) * 2 # => 8 (umiemy wymusić kolejność wykonywania działań)
```

Znaki pomiędzy liczbami oznaczające działania nazywamy operatorami.

## Zmienne

Zmienną możemy wyobrazić sobie jako pudełko z naklejką, do którego wkładamy jakąś wartość.

Nazwa zmiennej musi być jednym ciągiem znaków (bez spacji). Nie może zawierać operatorów ani zaczynać się od liczb.

Do pudełka możemy wkładać liczby całkowite i zmiennoprzecinkowe (ułamki dziesiętne), napisy oraz prawdę lub fałsz.

Są to różne typy danych, które Python od siebie odróżnia.

```python=
jakas_zmienna = 3 # W pudełku jest liczba 3, na naklejce jest napis 'jakas_zmienna'
```

Typy mają swoje własne nazwy w Pythonie:

- Liczby całkowite - `int`
- Liczby zmiennoprzecinkowe - `float`
- Prawda lub Fałsz - `bool`
- Napisy - `string`

Typ zmiennej zależy od tego, co w niej przechowujemy.
Na liczbach możemy wykonywać wszystkie operacje arytmetyczne.
O napisach i zmiennych typu bool powiemy później.

```python=
x = 7
y = 13
x + y     # => 20
y % x     # => 6
x * 3     # => 21
x + x - y # => 1
```

W jednej zmiennej możemy przechowywać jedną wartość jednocześnie. Stara wartość jest zapominana po ponownym przypisaniu wartośći.

```python=
x = 7
x # => 7
x = 3
x # => 3
```

Instrukcje w Pythonie wykonują się linijka po linijce. Oznacza to, że nie możemy wypisać wartości zmiennej, dopóki jej nie stworzymy.

```python=
x # => 'x' is not defined
x = 3
```

### **Stringi**

Na stringach możemy wykonywać dwie operacje:

- Dodawanie dwóch stringów
- Mnożenie stringa przez liczbę

Napis to dowolny ciąg znaków w cudzysłowie (lub apostrofach - nie ma znaczenia).

```python=
"kot" # => 'kot'
"hipo" + "potam" # => "hipopotam"
"bum" * 3 # => "bumbumbum"

3 * 3 # => 9
"3" * 3 # => "333"
```

Gdy chcemy sprawdzić ilość liter (a dokładniej znaków) używamy `len()`, na przykład:

```python
len("napis") # => 5
len("python jest super!") # => 18
```

### **Boole**

Zmienna jest typu `bool` jeśli ma wartość `True` lub `False`.

```python=
x = True
x # => True

x = False
x # => False
```

## Wypisywanie i pobieranie danych w programie

### **Print**

`print()` służy do wypisywania tekstu na ekran.

```python=
print(5) # => 5
print(3 + 5) # => 8
print("smieszny napis") # => smieszny napis

x = 8
print(x) # => 8

y = "niesmieszny napis"
print(y) # => niesmieszny napis
```

### **Input**

`input()` służy do pobierania napisów podanych przez użytkownika.

```python=
x = input("Wpisz coś: ")

print(x)
print(x * 2)
```

Wartość zwrócona przez input jest zawsze traktowana jako napis, nawet jeśli wpiszemy liczbę. Żeby program zinterpretował ją jako liczbę, musimy ręcznie zmienić jej typ.

```python=
x = input("Podaj pierwszą liczbę: ") # 3
y = int(input("Podaj drugą liczbę: ")) # 4

print(x * 2) # => 33
print(y * 2) # => 8
```

## Porównywanie wartości

Mamy zestaw operatorów do porównywania wartości. Porównania zwracają wartość typu `bool` (czyli prawdę lub fałsz).

```python=
print(5 > 2) # => True
print(2 == 3) # => False
# Do sprawdzenia równości używamy dwóch znaków równości
# bo pojedynczy służy do przypisania

x = 4
print(x <= 7) # => True
print(x < 0) # => False

y = 8
print(x != y) # => True
print(x >= y) # => False

# Wyniki porówania można zapisywać do zmiennych
czyYWieksze = y >= x
print(czyYWieksze)
```

## Instrukcje warunkowe

Jeśli chcemy, żeby jakiś kod został wykonany pod pewnym warunkiem, używamy instrukcji `if`. Po warunku piszemy dwukropek, a wszystkie instrukcje, które mają się pod nim wykonać zapisujemy z wcięciem.

```python=
x = 15

if x < 0:
    print("x jest liczbą ujemną") # => nic nie wypisze

if x > 0:
    print("x jest liczbą dodatnią") # => x jest liczbą dodatnią

if x - 10 > 0:
    print("x - 10 też jest liczbą dodatnią") # => x - 10 też jest liczbą dodatnią
```

Jeśli chcemy, żeby w przeciwnym przypadku stało się coś innego, używamy `else`.

```python=
x = -3
if x > 0:
    print("x jest liczbą dodatnią")
else:
    print("x nie jest liczbą dodatnią")
```

Jeśli chcemy rozważyć więcej niż dwa możliwe przypadki, możemy to zrobić używając `elif` (skrót od else if)

```python=
x = 5
if x > 0:
    print("x jest liczbą dodatnią")
elif x == 0:
    print("x jest zerem")
else:
    print("x jest liczbą ujemną")
```

Jeśli chcemy mieć więcej niż jeden warunek, używamy odpowiednio `and` lub `or`.
Jeśli wszystkie warunki muszą być spełnione piszemy `and`.
Jeśli przynajmniej jeden warunek musi być spełniony piszemy `or`.
Możemy w jednym warunku łączyć `or` i `and` korzystając z nawiasów. To co jest w nawiasach zostanie sprawdzone jako pierwsze.

```python=
imie = "Jan"
wiek = 23
if imie == "Jan" and wiek == 23:
    print("Nazywasz sie Jan i masz 23 lata.")

if imie == "Jan" or imie == "Robert":
    print("Nazywasz sie Jan lub Robert")

if (imie == "Jan" or imie == "Robert") and wiek == 23:
    print("Nazywasz sie Jan lub Robert i masz 23 lata")
```

## Pętle

Jeśli chcemy jakąs instrukcję wykonać kilka razy, to do tej pory napisalibyśmy ją pięć razy.

```python=
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
print("normalnie pisałbym to dziesięc razy")
```

Zamiast tego możemy użyć pętli.
Zapis pętli jest podobny do sposobu pisania instrukcji `if` (czyli dwukropek i wcięcie):

```python=
x = 1
while x <= 10:
    print("normalnie bym to dziesięc razy pisał")
    x = x + 1
```

Mamy do wyboru dwa rodzaje pętli:

### **While**

Instrukcje wewnątrz pętli `while` wykonują się dopóki warunek jest spełniony.

```python=
x = 1
while x <= 10:
    print(x)
    x = x + 1
# => 1 2 3 ... 10
```

Przy pisaniu pętli `while` musimy upewnić się, że warunek kiedyś stanie się nieprawdziwy. W przeciwnym wypadku stworzymy nieskończoną pętle - program będzie wykonywał się w nieskończoność.

```python=
x = 1
while x <= 10:
    print(x)
    x = x - 1
```

### **For**

Jeśli chcemy wykonać jakieś instrukcje konkretną liczbę razy, możemy użyć pętli `for`. Korzystając z niej, wiemy na którym powtórzeniu aktualnie jesteśmy i że skończy się w określonym przez nas momencie.

```python=
for i in range(10):
    print('to jest wykonanie numer ', i)
```

Do range'a możemy podać więcej niż jedną wartość.
Pierwsza z nich oznacza początkową wartość `i`.
Druga z nich oznacza wartość `i`, na której pętla ma się zakończyć.
Trzecia oznacza krok, czyli wartość o którą `i` zwiększa się przy każdym obrocie pętli.
Jeżeli w range'u podamy tylko jedną wartość, to początek jest ustawiany na 0, a krok na 1.

```python=
for i in range(0, 11, 2):
    print(i)
```

## Listy

Zdefiniowaliśmy wcześniej pojęcie zmiennej jako pudełka. Listę możemy sobie wyobrazić jako zestaw pudełek ustawionych obok siebie, w ustalonej kolejności.

```python=
lista = [3, 12, 23, 523]
```

Elementy, które przechowujemy w liście, nie muszą być tego samego typu, na przykład:

```python=
lista = [10, "napis", 4.20, 21.37, True]
```

Każdy element w liście jest numerowany kolejno od 0.
Jeśli chcemy wypisać konkretny element z listy, to możemy go uzyskać odwołując się do jego indeksu (miejsca, na którym jest w liście).

```python=
lista = [10, "napis", 4.20, 21.37, True]
        # 0,       1,    2,     3,    4

print(lista[1]) # możemy wypisać konkretny element listy

print(lista) # albo całą listę na raz
lista[3] = 6.9
print(lista)
```

Możemy dodawać elementy do listy używając konstrukcji `.append()`.

```python=
lista = [10, "napis", 4.20, 21.37, True]

lista.append("pan tu nie stał")

print(lista) # [10, "napis", 4.20, 21.37, True, "pan tu nie stał"]
```

Jeśli chcemy się dowiedzieć, ile jest elementów w liście używamy `len()`, tak jak przy stringach:

```python
lista = ["Ala", "ma", "kota"]

len(lista) # => 3
```

### Stringi to też takie trochę listy

Stringi (napisy) trochę przypominają listy. Tak samo jak umiemy wyciągnąć wartość z listy, to ze stringa umiemy wyciągnąć pojedynczą literę

Tak samo jak w listach, litery numerowane są od 0:

```python=
napis = "Ala ma kota"
print(napis[0]) #A
print(napis[4]) #m
print(napis[3]) #' '
```

## Środowisko programistyczne

Prawdziwych programów nie piszemy w konsoli, służy ona raczej do sprawdzania poprawności lub działania pojedynczych wyrażeń.

Programy piszemy w plikach z rozszerzeniem `.py`, a środowisko ułatwia edycję kodu i pozwala na uruchomienie programu.
