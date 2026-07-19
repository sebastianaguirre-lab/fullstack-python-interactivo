# Python basico

Mini guia personal de Python con ejemplos ordenados, explicacion breve y resultado esperado en consola.

> Nota: en el archivo original, la seccion de comprehensions usa `claves`, `valores` y `numeros` sin definir. En esta guia se agregan valores de ejemplo para que el codigo sea ejecutable.

## 1. `print()`

`print()` sirve para mostrar informacion en consola.

```python
print("Hola Mundo")
# Entrega Hola Mundo
```

## 2. Variables

Una variable guarda un valor para usarlo despues.

```python
nombre = "Sebastian"
edad = 30
altura = 1.76
es_programador = False

print(nombre)
print(edad)
print(altura)
print(es_programador)
```

Resultado:

```text
Sebastian
30
1.76
False
```

## 3. Tipos de datos

`type()` muestra el tipo de dato de una variable.

```python
print(type(nombre))
print(type(edad))
print(type(altura))
print(type(es_programador))
```

Resultado:

```text
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

## 4. Operaciones matematicas

Python permite hacer operaciones matematicas directamente.

```python
import math

a = 10
b = 3

print("Suma:", a + b)
print("Resta:", a - b)
print("Multiplicacion:", a * b)
print("Division:", a / b)
print("Potencia:", a ** b)
print("Raiz cuadrada:", math.sqrt(a))
print("Division entera:", a // b)
print("Modulo:", a % b)
print("Redondeo:", round(3.14159, 2))
print("Redondeo hacia arriba:", math.ceil(3.14159))
print("Redondeo hacia abajo:", math.floor(3.14159))
```

Resultado:

```text
Suma: 13
Resta: 7
Multiplicacion: 30
Division: 3.3333333333333335
Potencia: 1000
Raiz cuadrada: 3.1622776601683795
Division entera: 3
Modulo: 1
Redondeo: 3.14
Redondeo hacia arriba: 4
Redondeo hacia abajo: 3
```

## 5. Strings

Los strings son textos. Se pueden unir, transformar y medir.

```python
nombre = "Sebastian"

print("Hola " + nombre)
print(f"Hola {nombre}")
print(nombre.upper())
print(nombre.lower())
print(len(nombre))
```

Resultado:

```text
Hola Sebastian
Hola Sebastian
SEBASTIAN
sebastian
9
```

Metodos utiles de strings:

| Metodo | Para que sirve |
| --- | --- |
| `capitalize()` | Pone la primera letra en mayuscula. |
| `title()` | Pone cada palabra con inicial mayuscula. |
| `strip()` | Quita espacios al inicio y al final. |
| `replace()` | Reemplaza texto. |
| `find()` | Busca la posicion de un texto. |
| `split()` | Divide un string en una lista. |

Ejemplos parecidos en Django o ARCA:

```python
transaction.save()
serializer.is_valid()
queryset.filter(...)
```

## 6. `input()`

`input()` permite pedir informacion al usuario. En el archivo original esta comentado para que el programa no se detenga esperando una respuesta.

```python
nombre_ingresado = input("Como te llamas? ")
print(f"Hola {nombre_ingresado}")

numero_ingresado = int(input("Ingrese un numero: "))
print(numero_ingresado * 2)
```

Ejemplo de resultado si el usuario escribe `Sebastian` y luego `5`:

```text
Como te llamas? Sebastian
Hola Sebastian
Ingrese un numero: 5
10
```



## 7. Condicionales

`if`, `elif` y `else` permiten tomar decisiones.

```python
numero = 8

if numero > 0:
    print("Positivo")
elif numero == 0:
    print("Es cero")
else:
    print("Negativo")
```

Resultado:

```text
Positivo
```

Operadores de comparacion:

| Operador | Significado |
| --- | --- |
| `==` | Igual a |
| `!=` | Distinto de |
| `>` | Mayor que |
| `<` | Menor que |

Operadores logicos:

| Operador | Significado |
| --- | --- |
| `and` | Y |
| `or` | O |
| `not` | No |

## 8. `for`

`for` sirve para recorrer elementos de una secuencia.

| Si quieres... | Usa |
| --- | --- |
| Repetir hasta que ocurra algo | `while` |
| Recorrer una lista | `for elemento in lista` |
| Contar de 0 a N | `for i in range(10)` |
| Recorrer un texto letra por letra | `for letra in texto` |
| Recorrer un diccionario | `for clave, valor in persona.items()` |
| Obtener indice y valor | `enumerate()` |
| Recorrer dos listas al mismo tiempo | `zip()` |
| Salir antes de terminar | `break` |
| Saltar una iteracion | `continue` |
| Usar un bucle dentro de otro | Bucle anidado |

### `range()`

```python
for i in range(10, 1, -1):
    print(i)

"""
resultado
10
9
8
7
6
5
4
3
2
"""
```


### Recorrer un texto

```python
texto = "Hola"

for letra in texto:
    print(letra)

"""
Resultado
H
o
l
a
"""
```



### Recorrer un diccionario

```python
persona = {
    "nombre": "Sebastian",
    "edad": 30,
}

for clave, valor in persona.items():
    print(f"{clave}: {valor}")

"""
Resultado:
nombre: Sebastian
edad: 30
"""
```

### `enumerate()`

`enumerate()` entrega posicion y valor.

```python
frutas = ["Manzana", "Pera", "Kiwi"]

for posicion, fruta in enumerate(frutas):
    print(posicion, fruta)

"""
R:
0 Manzana
1 Pera
2 Kiwi
"""
```

### `zip()`

`zip()` combina listas y entrega elementos correspondientes.

```python
nombres = ["Ana", "Luis", "Pedro"]
edades = [20, 30, 40]

for nombre, edad in zip(nombres, edades):
    print(nombre, edad)

"""
R:
Ana 20
Luis 30
Pedro 40
"""
```


### `break`

`break` termina el bucle antes de tiempo.

```python
for i in range(10):
    if i == 5:
        break
    print(i)

"""
R:
0
1
2
3
4
"""
```

### `continue`

`continue` salta una iteracion y sigue con la siguiente.

```python
for i in range(10):
    if i == 5:
        continue
    print(i)

"""
R:
0
1
2
3
4
6
7
8
9
"""
```

### Bucle anidado

Un bucle anidado es un bucle dentro de otro.

```python
for fila in range(3):
    for columna in range(4):
        print(fila, columna)

"""
R:
0 0
0 1
0 2
0 3
1 0
1 1
1 2
1 3
2 0
2 1
2 2
2 3
"""
```

## Comprehensions

Las comprehensions permiten crear listas o diccionarios de forma mas corta.

### List comprehension

```python
cuadrados = []

for i in range(10):
    cuadrados.append(i ** 2)

# todo lo anterior pasa a ser:
cuadrados = [i ** 2 for i in range(10)]

print(cuadrados)

# Resultado [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### Dict comprehension

```python
claves = ["nombre", "edad", "pais"]
valores = ["Sebastian", 30, "Chile"]

diccionario = {k: v for k, v in zip(claves, valores)}

print(diccionario)

# {'nombre': 'Sebastian', 'edad': 30, 'pais': 'Chile'}
```

### Condicional dentro de una list comprehension

```python
numeros = [1, 2, 3, 4, 5, 6]

resultado = ["Par" if numero % 2 == 0 else "Impar" for numero in numeros]

print(resultado)

# Resultado ['Impar', 'Par', 'Impar', 'Par', 'Impar', 'Par']
```


### Filtrar elementos

```python
numeros = [1, 2, 3, 4, 5, 6]

pares = [numero for numero in numeros if numero % 2 == 0]

print(pares)

# Resultado [2, 4, 6]
```



## 9. `while`

`while` repite instrucciones mientras una condicion sea verdadera.

```python
contador = 1

while contador <= 3:
    print(contador)
    contador += 1
```

Resultado:

```text
1
2
3
```

## 10. Funciones

Una funcion agrupa instrucciones para reutilizarlas

```python
def sumar(x, y): # parámetros
    return x + y

a = sumar(5, 7) # Argumentos
print(a)

#R: 12
```

### Parametros nombrados

Los parametros nombrados permiten indicar que valor recibe cada parametro.

```python
def dividir(a, b):
    print(a / b)


dividir(a=10, b=2)
dividir(b=2, a=10)
# En ambas el resultado es 5.0
```

### Parametros por defecto

Un parametro puede tener un valor por defecto. Ese valor se usa si no se entrega un argumento.

```python
def saludar(nombre="Usuario"):
    print(f"Hola {nombre}")


saludar() # Hola Uusario
saludar("Sebastian") # Hola Sebastian
```

### `return`

`print()` muestra informacion en consola.

`return` devuelve un valor para poder guardarlo o usarlo despues.

Ejemplo usando `print()`:

```python
def cuadrado(x):
    print(x ** 2)


a = cuadrado(5) #25
print(a) #None
```


Ejemplo usando `return`:

```python
def cuadrado(x):
    return x ** 2


a = cuadrado(5)
print(a) #25
```

Ahora la funcion devuelve el valor y se puede guardar en la variable `resultado`.

### Multiples retornos

Una funcion puede devolver mas de un valor.

```python
def operaciones(numero):
    cuadrado = numero ** 2
    cubo = numero ** 3
    return cuadrado, cubo

c2, c3 = operaciones(4)

print(c2)#16
print(c3)#64
#
```

Esto se llama desempaquetado. Cada valor retornado se guarda en una variable.

### Funciones que reciben listas

Una funcion puede recibir una lista como argumento.

```python
def promedio(lista):
    total = sum(lista)
    cantidad = len(lista)
    return total / cantidad


notas = [6, 5, 7]
resultado = promedio(notas)

print(resultado) #6.0
```

### Funciones que reciben diccionarios

Una funcion tambien puede recibir un diccionario.

```python
def mostrar_productos(diccionario):
    for producto, precio in diccionario.items():
        print(f"{producto}: ${precio}")

productos = {
    "Pan": 1200,
    "Leche": 1000,
    "Queso": 3500
}

mostrar_productos(productos)
"""
Imprime
Pan: $1200
Leche: $1000
Queso: $3500
"""
```


### Funciones como argumentos

En Python una funcion tambien es un objeto. Por eso se puede enviar una funcion como argumento a otra funcion.

```python
def operar(lista, funcion):
    return funcion(lista)


numeros = [10, 20, 30]

print(operar(numeros, sum)) #60
print(operar(numeros, len)) #3
```

Se escribe `sum` y no `sum()` porque queremos entregar la funcion, no ejecutarla inmediatamente.

### `*args`

`*args` permite recibir una cantidad variable de argumentos.

Sirve cuando no sabemos cuantos valores se van a entregar.

```python
def sumar(*args):
    total = 0

    for numero in args:
        total += numero

    return total


print(sumar(1, 2)) #3
print(sumar(1, 2, 3, 4)) #10
```

### `**kwargs`

`**kwargs` permite recibir una cantidad variable de argumentos con nombre.

Internamente, `kwargs` es un diccionario.

```python
def crear_perfil(**kwargs):
    for clave, valor in kwargs.items():
        print(f"{clave}: {valor}")


crear_perfil(nombre="Sebastian", edad=30, ciudad="Santiago")

"""
Entrega
nombre: Sebastian
edad: 30
ciudad: Santiago
"""
```

### Variables locales y globales

El scope es el alcance de una variable. Indica donde existe y donde se puede usar.

Una variable creada dentro de una funcion es local. Solo existe dentro de esa funcion.

```python
def ejemplo():
    mensaje = "Hola"
    print(mensaje)

ejemplo() #Hola
print(mensaje) #name 'mensaje' is not defined
```

### `global`

Aunque funciona, usar `global` suele ser una mala practica porque hace que el codigo sea mas dificil de entender y mantener.

Es mejor usar `return`.

```python
def aumentar(contador):
    return contador + 1

contador = 0
contador = aumentar(contador)

print(contador) #R: 1
```

### Funciones que modifican en el lugar

Algunas funciones modifican directamente el objeto recibido y devuelven `None`.

`random.shuffle()` mezcla una lista en el lugar.

```python
import random

lista = [1, 2, 3]
random.shuffle(lista)

print(lista) # La lista queda desordenada
```

No se debe guardar el resultado de `shuffle()`.

```python
lista = random.shuffle(lista)
print(lista) #None
```

Ejemplo correcto:

```python
def shuffle_alt(pregunta):
    random.shuffle(pregunta["alternativas"])
    return pregunta["alternativas"]
```

Si se escribe:

```python
pregunta["alternativas"] = random.shuffle(pregunta["alternativas"])
```

primero se mezcla la lista, pero despues `pregunta["alternativas"]` queda valiendo `None`.

## 11. Listas

Las listas guardan varios elementos y se accede a ellos por posicion.


```python
frutas = ["Manzana", "Pera", "Naranja"]

print(frutas)
# R: ['Manzana', 'Pera', 'Naranja']

print(frutas[0])
# R: Manzana
print(frutas[-1])
# R: Naranja

frutas.append("Platano")

"""
R: 
Manzana
Pera
Naranja
Platano
"""

for fruta in frutas:
    print(fruta)

print(", ".join(frutas))
# R: Manzana, Pera, Naranja, Platano
```

Metodos y operaciones utiles:

| Ejemplo | Resultado o uso |
| --- | --- |
| `frutas[0]` | Primer elemento. |
| `frutas.append("kiwi")` | Agrega al final. |
| `frutas.insert(1, "platano")` | Agrega en la posicion 1. |
| `frutas.pop(2)` | Elimina y devuelve el elemento eliminado. |
| `frutas.remove("uva")` | Elimina ese valor. |
| `frutas.reverse()` | Invierte la lista. |
| `frutas.sort()` | Ordena la lista original. |
| `sorted(numeros)` | Devuelve una copia ordenada. |
| `frutas.index("pera")` | Devuelve la posicion. |
| `max(numeros)` | Mayor valor. |
| `min(numeros)` | Menor valor. |
| `sum(numeros)` | Suma total. |
| `[1, 2] + [3, 4]` | `[1, 2, 3, 4]` |
| `[1, 2] * 3` | `[1, 2, 1, 2, 1, 2]` |

### Argumentos desde terminal

Con `sys.argv` se pueden leer argumentos escritos al ejecutar un archivo.

```python
import sys

print(sys.argv[0])
print(sys.argv[1])

"""
Si en terminal se ejecuta:

python argumentos.py Sebastian

El resultado es:

argumentos.py
Sebastian
"""
```

## 12. Tuplas

Las tuplas se parecen a las listas, pero normalmente se usan para datos que no cambian.

```python
coordenadas = (10.0, 20.0)

print(coordenadas)
```

Resultado:

```text
(10.0, 20.0)
```

## 13. Sets

Los sets no permiten elementos duplicados.

```python
numeros = {1, 1, 2, 3, 4, 5}

print(numeros)
```

Resultado:

```text
{1, 2, 3, 4, 5}
```

## 14. Diccionarios

Los diccionarios guardan informacion usando claves.

```python
persona = {
    "nombre": "Sebastian",
    "edad": 30,
    "profesion": "Ingeniero",
}

print(persona["nombre"])
print(persona["edad"])

transaction = {
    "amount": 5000,
    "currency": "USD",
    "country": "CL",}

print(transaction)

"""
Resultados
Sebastian
30
{'amount': 5000, 'currency': 'USD', 'country': 'CL'}
"""
```

Ejemplo de lista con diccionarios:

```python
transactions = [
    transaction1,
    transaction2,
    transaction3,
]
```

Ejemplo de comprehension con diccionarios:

```python
ventas = {
    "enero": 100,
    "febrero": 250,
    "marzo": 80,
}

umbral = 100

ventas_mayores = {
    mes: monto
    for mes, monto in ventas.items()
    if monto > umbral
}

print(ventas_mayores)

# Resultado {'febrero': 250}
```


Operaciones comunes:

| Ejemplo | Uso |
| --- | --- |
| `persona["peso"] = 72` | Agrega una clave. |
| `persona["edad"] = 31` | Modifica un valor. |
| `del persona["peso"]` | Elimina una clave. |
| `persona.pop("peso")` | Elimina y devuelve el valor. |
| `a.update(b)` | Mezcla dos diccionarios. |
| `persona.keys()` | Entrega las claves. |
| `persona.values()` | Entrega los valores. |
| `persona.items()` | Entrega claves y valores. |

Uso de `get()`:

```python
persona = {
    "nombre": "Sebastian",
    "edad": 30,
}

print(persona.get("telefono"))
# Entrega None

print(persona.get("telefono", "No existe"))
# Entrena No existe
```


Idea clave:

```text
En una lista busco por posicion.
En un diccionario busco por clave.
```

## 15. Librerias

Las librerias permiten usar codigo ya hecho.

```python
import math
from math import ceil, pi, sqrt
import math as m

print(math.sqrt(25))
print(math.ceil(3.14))
print(math.pi)

ceil_value = ceil(3.14)

print(sqrt(25))
print(ceil_value)
print(pi)
print(m.sqrt(25))
```

Resultado:

```text
5.0
4
3.141592653589793
5.0
4
3.141592653589793
5.0
```

Instalacion de librerias externas:

```bash
pip install pandas
pip install numpy
```

## 16. Modularizacion

Modularizar es separar un programa en partes mas pequeñas y ordenadas.

### Importaciones

Las importaciones permiten usar codigo desde otro modulo.

`import modulo`

Importa el modulo completo.

```python
import math

print(math.sqrt(25)) #5.0
```

`import modulo as alias`

Importa el modulo con un nombre mas corto.

```python
import math as m

print(m.sqrt(25)) #5.0
```

`from modulo import funcion`

Importa solo una funcion o elemento del modulo.

```python
from math import sqrt

print(sqrt(25)) #5.0
```

### `main.py`

`main.py` normalmente es el punto de entrada del programa.

Desde ahi se coordinan los demas modulos.

```python
from calculadora import sumar

print(sumar(2, 3)) #5
```

### `if __name__ == "__main__"`

Esto evita que un modulo ejecute codigo automaticamente al importarlo.

```python
def saludar():
    print("Hola")

if __name__ == "__main__":
    saludar()
```

### Docstrings

Los docstrings son textos que documentan que hace una funcion, clase o modulo.

```python
def sumar(a, b):
    """
    Suma dos numeros.
    """
```

## Refactorizacion

Refactorizar es mejorar el codigo sin cambiar su funcionamiento.


Antes:

```python
print("Hola Ana")
print("Hola Luis")
```

Despues:

```python
for nombre in ["Ana", "Luis"]:
    print(f"Hola {nombre}")
```

## 17. Experiencia de usuario

### `time.sleep()`

`time.sleep()` pausa el programa por una cantidad de segundos.

```python
import time

print("Cargando...")
time.sleep(2)
print("Listo")
```

### Limpiar pantalla

Limpiar pantalla depende del sistema operativo.

```python
os.system("cls")
os.system("clear")
```

### `exit()`

`exit()` finaliza el programa.

```python
exit()
```
