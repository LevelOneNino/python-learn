## Mi primer programa  
``` python
print("Hola, mundo!")
```
## Comentarios  
``` python
# Esto es un comentario de una unica linea

'''
Esto es
un comentario
multilinea
'''

"""
Esto es
otro comentario
multilinea
"""
```
## Variables  
- las variables en python no se declaran , solo se asignan.
- Solo pueden contener A-z 0-9 y _
- No puede iniciar por numero
- No puede ser una keyword
- Son sensibles a las mayus: nombre, Nombre y NOMbRE serian variables distintas
```python
numero_cero = 0
Texto = "Hola"
```
#### Asignar multiples valores a multiples variables  
```python
x, y, z = "naranja", "banana", "cereza"
# x = "naranja", y = "banana" ...
```
#### Asignar un valor a multiples variables  
```python
x = y = z = "uva"
# x = "uva", y = "uva" ...
```
#### Variables locales y globales  
```python
x = "global"
def someFunc():
    x = "local" # la variable x = "local" dentro de la funcion no es la misma x = "global"
```
Si queremos que la funcion acceda a la variable local tenemos que indicarlo
```python
x = "global"
def someFunc():
    global x
    x = "local" # ahora la variable x = "global" es x = "local"
```
#### Tipo de datos  
|grupo|tipo de dato Built-in|
|:-|:-|
|Texto|str|
|Numerico|int, float, complex|
|Sequencia|list, tuple, range|
|Mapa|dict|
|Set|set, frozenset|
|Boolean|bool|
|Binary|bytes, bytearray, memoryview|
|None|NoneType|

puedes saber el tipo de dato de una variable con type(var)
```python
var = 10
type(var) # int
```
#### Casting
Puedes especificar o conseguir el equivalente (cast) en otro tipo de dato (solo si es valido)
```python
x = 230
float(x) # 230.0
str(x) # '230'
int(x) # 230
```
### Operadores
- aritmeticos

|simbolo|descripcion|uso|
|-|-|-|
|+|Addition|x + y|
|-|Subtraction|x - y|
|*|Multiplication|x * y|
|/|Division|x / y|
|%|Modulus|x % y|
|**|Exponentiation|x ** y|
|//|Floor division|x // y|
- asignacion

|simbolo|uso|equivalente|
|-|-|-|
|=|x = 5|x = 5|
|+=|x += 3|x = x + 3|
|-=|x -= 3|x = x - 3|
|*= |x *= 3|x = x * 3|
|/=|x /= 3|x = x / 3|
|%=|x %= 3|x = x % 3|
|//|x //= 3|x = x // 3|
|**=|x **= 3| x ** 3|
|&=|x &= 3|x = x & 3|
|\|=|x \|= 3|x = x \| 3|
|^=|x ^= 3|x = x ^ 3|
|>>|x >>= 3|x = x >> 3|
|<<|x <<= 3|x = x << 3|
|:=|print(x := 3)|x = 3; print(x)|
- comparacion

|simbolo|descripcion|uso|
|-|-|-|
|==|Equal|x == y|
|!=|Not equal|x != y|
|>|Greater than|x > y|
|<|Less than|x < y|
|>=|Greater than or equal to|x >= y|
|<=|Less than or equal to|x <= y|
- logicos

|simbolo|descripcion|uso|
|-|-|-|
|and|Returns True if both statements are true|x < 5 and  x < 10|
|or|Returns True if one of the statements is true|x < 5 or x < 4|
|not|Reverse the result|not(x < 5 and x < 10)|
- comparacion entre objetos

|simbolo|descripcion|uso|
|-|-|-|
|is|Returns True if both variables are the same object|x is y|
|is not|Returns True if both variables are not the same object|x is not y|
- operaciones binarias

|simbolo|logica|descripcion|uso|
|-|-|-|-|
|&|AND|Sets each bit to 1 if both bits are 1|x & y|
|\||OR|Sets each bit to 1 if one of two bits is 1|x \| y|
|^|XOR|Sets each bit to 1 if only one of two bits is 1|x ^ y|
|~|NOT|Inverts all the bits|~x|
|<<||Shift left by pushing zeros in from the right and let the leftmost bits fall off|x<<2|
|>>||Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off|x>>2|
### str
```python
text = "1: texto test"
    # 1: texto test

text = '2: texto\ntest'
    # 2: texto 
    # test

text = """3: texto
test"""
    # 3: texto 
    # test

text = '''4: texto test'''
    # 4: texto test
```
Los Strings son listas
```python
text = "Hello, World!"
text[0] # H
text[1] # e
text[2] # l
text[3] # l
text[4] # o
```
### bool
```python
a = True
b = False
print(5 < 3)
```
### list
- Los items de una lista son ordenados, pueden cambiarse, y permiten valores duplicados.
- Los items de una lista son indexados, el primer item tiene indice [0], el segundo tiene indice [1], etc.
```python
myList = ["apple", 15, "cherry"]
myList # ["apple", 15, "cherry"]
myList[0] # "apple"
myList[-1] # "cherry", negativos empiezan desde el ultimo hacia el primero
len(myList) # 3 (numero de items)
```
### tuple
- Los items de una tupla son ordenados, no pueden cambiarse, y permiten valores duplicados.
- Los items de una tupla son indexados, el primer item tiene indice [0], el segundo tiene indice [1], etc.
```python
myTuple = ("apple", 15, "cherry")
myTuple # ("apple", 15, "cherry")
myTuple[0] # "apple"
myTuple[-1] # "cherry", negativos empiezan desde el ultimo hacia el primero
len(myTuple) # 3 (numero de items)
```
### set
- Los items de un set no son ordenados, no pueden cambiarse, y no permiten valores duplicados.
- No puedes acceder a items de un set con un index o key, pero puedes hacer acceder a los items a traves de un loop y verificar si un item existe dentro del set
- Nota: Los valores True y 1 son considerados el mismo en sets, y son tratados como duplicados
- Nota: Los valores False y 0 son considerados el mismo en sets, y son tratados como duplicados
```python
mySet = {"apple", 15, "cherry"}
mySet # {"apple", "cherry", 15}
for item in mySet:
    print(item) # "apple"
                # "cherry"
                # 15
"apple" in mySet # True
"apple" not in mySet # False
len(mySet) # 3 (numero de items)
```
### dict
- Los diccionarios contiene data en pares key:value
- Los pares de un dict son ordenados(a partir de python 3.7), pueden cambiarse, y no permiten valores duplicados(keys).
```python
myDict = {
    "marca": "Ford",
    "modelo": "Mustang",
    "año": 1968
}
myDict
# {
#   "marca": "Ford",
#   "modelo": "Mustang",
#   "año": 1968
# }
myDict["modelo"] # "Mustang"
len(myDict) # 3 (numero de pares)
```
### Desempaquetar  
podemos extraer los valores guardados en list, tuple, set y dict
```python
paquete = [1, 2, 3] # o (1, 2, 3) o {1, 2, 3}
x, y, z = paquete
# x = 1, y = 2 ...
```
puedes desempaquetar para argumentos con * (list, tuple, set y dict keys) y ** (dict pairs)
```python
list = [1, 2, 3]
dictA = {"a": 5, "b": 10}
dictB = {"c": 15, "d": 20}
print(list) # [1, 2, 3]
print(*list) # 1 2 3
print(*dictA) # a b

# **dict extrae los pares del diccionario como "a":5 y "b":10

print({**dictA, **dictB})    # {"a": 5, "b": 10,"c": 15, "d": 20} 
```
## Condiciones y condicional if
en Python puedes usar tipicas condiciones logicas de matematicas como a > b (a mayor que b). (*ver operadores de comparacion*)
Estas condiciones pueden ser usadas en varias formas , tipicamente en loops y en condicionales **if**
```python
a = 5
b = 10
if b > a: # True
    print("b es mayor que a") # "b es mayor que a"
```
### sangrado
Python depende del sangrado(espacios) al inicio de la linea para definir como se contienen los bloques de codigo
, otros lenguajes usan { } para cumplir esto.
los **if**  requieren del sangrado para definir lo que contienen, en el ejemplo anterior print("...") tiene sangrado al inicio de la linea, indicando que hace parte del bloque del **if**
```python
a = 5
b = 10
if b > a: # True
print("b es mayor que a") # en este caso habria un error
# un condicional if no puede tener un bloque vacio
```
##### if en unica linea
Si el bloque de codigo del if es una sola linea puedes escribir todo el condicional if en una unica linea
```python
a = 5
b = 10
if b > a: print("b es mayor que a") # True -> "b es mayor que a"
```
### Elif
Los elif cumplen la idea de "si la condicion anterior no se cumple, prueba esta"
```python
a = 5
b = 5
if b > a: # False
    print("b es mayor que a")
elif b == a: # True
    print("b y a son iguales") # "b y a son iguales"
```
### Else
el bloque de codigo en un else ocurre unicamente cuando ninguna condicion anterior se cumple
```python
a = 15
b = 5
if b > a: # False
    print("b es mayor que a")
elif b == a: # False
    print("b y a son iguales")
else:
    print("b es menor que a") # "b es menor que a"
```
##### if else en unica linea
Si el bloque de codigo del if es una sola linea y el bloque del else es una sola linea puedes escribir todo el condicional if...else en una unica linea
```python
a = 10
b = 5
print("b es mayor que a") if b > a else print ("b no es mayor que a") # "b no es mayor que a"
```
### Operadores logicos
Los operadores logicos se usan para combinar y/o alterar condiciones (*Ver operadores logicos*)
```python
a = 5
b = 10
c = 15

if a < b and c > a: # True and True -> True
    print("ambas condiciones se cumplen") # "ambas condiciones se cumplen"

if a > b or c > a: # False or True -> True
    print("por lo menos una condicion se cumple") # "por lo menos una condicion se cumple"

if not a < b: # not False -> True
    print("invierte el resultado de la condicion") # "invierte el resultado de la condicion"
```
### If anidado
Puedes tener condicionales **if** dentro de otros **if**, esto se llama if anidado
```python
a = 15

if a > 10: # True
    print("a es mayor que 10") # "a es mayor que 10"
    if a > 20: # False
        print("a es mayor que 20")
    else:
        print("a es menor que 20") # "a es menor que 10"
```
### if pass
Los condicionales if no pueden estar vacios, pero si por algun motivo tienes algun if sin contenido, puedes usar **pass** para evitar errores
```python
a = 10
b = 5
if a > b:
    pass
```
## Loops
Python tiene dos loops primitivos **while** y **for**
### while
while ejecuta un bloque de codigo mientas la condicion siga siendo verdadera
```python
i = 1
while i < 6:
  print(i) # 1 2 3 4 5
  i += 1
```
### for
for se utiliza para iterar a traves de una sequencia (list, tuple, dictionary, set, string o range)
```python
myDict = {
    "nombre": "Jon",
    "Apellido": "Doe",
    "Edad": 45,
    "tez": "Morena"
}
for k in myDict
  print(myDict[k]) # "Jon" "Doe" 45 "Morena"
```
##### range()
La funcion range() retorna una secuencia de numeros, empezando desde 0(default), e incrementos de 1(default) hasta un numero indicado(no inclusivo)
``` python
for n in range(6):
    print(n) # 0 1 2 3 4 5
```
la funcion range() puede tener hasta 3 argumentos: numero inicio de la secuencia, numero limite de la secuencia y tamaño de iteraciones
``` python
for n in range(6): # 1 argumento: (numero limite)
    print(n) # 0 1 2 3 4 5

for n in range(2, 6): # 2 argumentos: (numero de inicio, numero limite)
    print(n) # 2 3 4 5

for n in range(2, 6, 3): # 3 argumentos: (numero de inicio, numero limite, tamaño de iteracion)
    print(n) # 2 5
```
### else
como en los condicionales **if**, si un loop **while** o **for** no cumple su condicion, puedes tener un bloque **else** que se ejecute una vez
```python
for x in range(6):
  print(x) # 0 1 2 3 4 5
else:
  print("Acabo el loop") # "Acabo el loop"
```




