# Apuntes 1ra Parcial
---
###### Emmanuel Munguia Quiroz 3D
-----
## Programacion Funcional

La programación funcional es un paradigma de programación que se basa en el concepto de funciones matemáticas puras y en el tratamiento de los programas como evaluación de funciones. En la programación funcional, los programas se construyen utilizando principalmente funciones y evitan el cambio de estado y la mutación de datos.
### Caracteristicas
Algunas de sus caracteristicas son:

###### * `Funciones puras`: Significa que para una entrada dada, siempre producirán la misma salida sin efectos secundarios observables.

###### * `Inmutabilidad`: Los datos en la programación funcional suelen ser inmutables, lo que significa que una vez que se crea un objeto de datos, no se puede cambiar.

###### * `Evaluacion Perezosa`: Significa que las expresiones se calculan solo cuando se necesitan.

###### * `Funciones de orden superior`: En la programación funcional, las funciones se pueden pasar como argumentos a otras funciones o devolver como valores de funciones

###### * `Recursion`: Las funciones se llaman a sí mismas con argumentos modificados en lugar de utilizar bucles iterativos.

###### * `Transparencia Referencial`: Significa que una expresión se puede reemplazar por su valor sin cambiar el comportamiento del programa. Esto se debe a que las funciones puras no tienen efectos secundarios observables.

###### * `Composicion de funciones`: Significa que se pueden combinar varias funciones para crear funciones más complejas. 

### Comparacion de los paradigmas de programacion
#### `Programacion Funcional`
 ```python
def suma(a, b):
 return a + b
def resta(a, b):
 return a - b
def multiplicacion(a, b):
 return a * b
def division(a, b):
 #validar el 0
 return a / b
def mi_calculadora(opcion, num1, num2):
    if opcion == '1':
        return suma(num1, num2)
    elif opcion == '2':
        return resta(num1, num2)
    elif opcion == '3':
        return multiplicacion(num1, num2)
    elif opcion == '4' and num2 != 0:
        return division(num1, num2)
    else:
        return "Opción no válida"
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
     print("¡Gracias por usar Mi Calculadora!")
     break
 elif opcion < '1' or opcion > '5':
             print("Opción no válida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
 resultado = mi_calculadora(opcion, num1, num2)
 print("Resultado:", resultado)
```
#####  En este paradigma se destaca el uso de `Funciones puras`, las cuales son suma, resta, multiplicacion, division, y mi_calculadora.   
---
#### `Programacion Estructurada`
```python
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
    print("¡Hasta luego!")
    break
 elif opcion < '1' or opcion > '5':
        print("Opcion no valida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
if opcion == '1':
    print("Resultado:", num1 + num2)
elif opcion == '2':
    print("Resultado:", num1 - num2)
elif opcion == '3':
    print("Resultado:", num1 * num2)
elif opcion == '4': 
     if num2 != 0:
        print("Resultado: ", num1 / num2)
     else:
       print("No se puede dividir entre cero")
else:
    print("¡Gracias por usar Mi Calculadora!")
```
##### En este paradigma se puede resaltar el uso de estructuras de control para que el usuario decida lo que va a realizar y el codigo lo ejecute, ademas de el ciclo while para ejcutar el programa hast que el usuario quiera.
---
#### `Programacion Orientada  a Objetos (POO)`
``` python
class MiCalculadora:
 def suma(self, a, b):
    return a + b
 def resta(self, a, b):
    return a - b
 def multiplicacion(self, a, b):
    return a * b
 def division(self, a, b):
    if b != 0:
        return a / b
    else:
        return "No se puede dividir entre cero"
calculadora = MiCalculadora()
while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")
    opcion = input("Selecciona una opción: ")
    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
    if opcion == '1':
        print("Resultado:", calculadora.suma(num1, num2))
    elif opcion == '2':
        print("Resultado:", calculadora.resta(num1, num2))
    elif opcion == '3':
        print("Resultado:", calculadora.multiplicacion(num1, num2))
    elif opcion == '4': 
        if num2 != 0:
            print("Resultado:", calculadora.division(num1, num2))
        else:
            print("No se puede dividir entre cero")
```
##### En este paradigma se utilizan las clases y objetos, en donde se encapsulan datos.
Algunas de las caracteristicas de este son:
###### * `Clase`: El código define una clase llamada MiCalculadora, La cual es una clase que se utiliza para crear objetos.
###### * `Métodos de Clase`: Dentro de la clase "MiCalculadora", se definen métodos como suma, resta, multiplicacion, y division. Estos métodos son funciones que operan en los atributos de los objetos de la clase.
###### * `Creación de Objetos`: Se crea una instancia de la clase "MiCalculadora" mediante la línea calculadora = MiCalculadora(). Aquí, calculadora se convierte en un objeto de la clase MiCalculadora, y se pueden llamar a sus métodos para realizar operaciones matemáticas.
###### * `Encapsulación`: Los métodos de la clase MiCalculadora encapsulan la lógica de las operaciones matemáticas. Esto significa que la implementación de las operaciones está oculta dentro de la clase, y el usuario solo necesita llamar a los métodos correspondientes.
###### * `Polimorfismo`: El código muestra polimorfismo, ya que se pueden llamar a métodos con el mismo nombre (suma, resta, etc.) en diferentes objetos de la clase MiCalculadora
---
### Tipos de Datos
#### `Numericos`
###### * `int (Entero)`: El tipo de dato int, que proviene de "entero", se utiliza para representar números enteros, es decir, números sin parte decimal. Los enteros pueden ser positivos o negativos. Ejemplos de enteros son -5, 0, 42, y 1000.

###### * `float (Punto Flotante)`: El tipo de dato float, también conocido como punto flotante o número de coma flotante, se utiliza para representar números con decimales. Los números en punto flotante son aproximaciones racionales de números reales y pueden representar valores como 3.14 o 0.001.

###### * `complejo (Complejo)`: El tipo de dato complejo se utiliza para representar números complejos, que tienen una parte real y una parte imaginaria. Por ejemplo, un número complejo podría ser 3 + 2i, donde 3 es la parte real y 2i es la parte imaginaria.

###### * `decimal (Decimal)`: El tipo de dato decimal se utiliza para representar números decimales con precisión arbitraria. A diferencia de los números en punto flotante, los números decimales tienen una precisión exacta y se utilizan en situaciones donde la precisión es crucial, como en cálculos financieros.

###### * `científico (Notación Científica)`: La notación científica no es un tipo de dato en sí, sino una forma de representar números en notación exponencial. Se utiliza para manejar números extremadamente grandes o pequeños de manera más compacta. Por ejemplo, 1.23e6 representa 1.23 × 10^6, que es 1,230,000.

Cada uno de estos tipos de datos numéricos tiene sus propias características y limitaciones. La elección del tipo de dato numérico adecuado depende de la precisión requerida en tus cálculos y del rango de valores que necesitas representar. Es importante tener en cuenta que en muchos lenguajes de programación, como Python, se deben considerar las implicaciones de precisión al realizar cálculos con números en punto flotante, y en casos donde la precisión es crítica, se puede recurrir al uso de números decimales o técnicas específicas de manejo de errores.

#### `Logicos`
###### * `booleano (bool)`: Se utiliza para representar valores lógicos en programación, como Verdadero (True) o Falso (False). Se usa para tomar decisiones en el código y controlar el flujo de ejecución mediante operadores lógicos y estructuras de control condicionales. Es fundamental para evaluar y expresar condiciones en un programa.
###### * `string`: Abreviado como `str`, se utiliza para representar cadenas de texto en programación. Una cadena es una secuencia de caracteres, como letras, números o símbolos, y se utiliza para representar información legible por humanos en el código. Las cadenas son inmutables en muchos lenguajes, lo que significa que no pueden modificarse una vez creadas. Se utilizan en una variedad de tareas, como mostrar mensajes, procesar texto y manipular datos de texto.
---
### Operadores
#### `Operadores Aritméticos:`
###### * +: Suma
###### * -: Resta
###### * *: Multiplicación
###### * /: División
###### * //: División entera (resultado redondeado al número entero más cercano)
###### * %: Módulo (el residuo de la división)
###### * **: Potencia (por ejemplo, 2 ** 3 es igual a 2 elevado a la potencia de 3, es decir, 8)
Los operadores aritméticos se utilizan para realizar operaciones matemáticas en Python.

#### Operadores Lógicos:
###### * and: Operador lógico "y"
###### * or: Operador lógico "o"
###### * not: Operador lógico "no"
Los operadores lógicos se utilizan para combinar expresiones lógicas y evaluar condiciones en Python.

#### `Operadores Condicionales`:
###### * ==: Igual a
###### * !=: No igual a
###### * <: Menor que
###### * >: Mayor que
###### * <=: Menor o igual que
###### * >=: Mayor o igual que
---
### Estructuras de Datos
#### `Listas (Lists)`:
###### * Las listas son colecciones ordenadas y modificables de elementos.
###### * Los elementos pueden ser de diferentes tipos, como números, cadenas, objetos, u otras listas.
###### * Se accede a los elementos de la lista mediante índices (posiciones) y se pueden modificar.
###### * Sintaxis común en Python: mi_lista = [1, 2, 3, 'texto']

#### `Diccionarios (Dictionaries)`:
###### * Los diccionarios son colecciones de elementos que se almacenan en pares clave-valor.
###### * Se utilizan para mapear una clave a un valor asociado.
###### * Los diccionarios son desordenados, lo que significa que los elementos no tienen un orden específico.
###### * Sintaxis común en Python: mi_diccionario = {'clave1': 'valor1', 'clave2': 'valor2'}

#### `Conjuntos (Sets)`:
###### * Los conjuntos son colecciones no ordenadas y no duplicadas de elementos únicos.
###### * Se utilizan para realizar operaciones de conjunto, como unión, intersección y diferencia.
###### * Los elementos en un conjunto no tienen un orden específico.
###### * Sintaxis común en Python: mi_conjunto = {1, 2, 3, 4, 5}

#### `Tuplas (Tuples)`:

###### * Las tuplas son colecciones ordenadas e inmutables de elementos.
###### * Los elementos pueden ser de diferentes tipos, al igual que en las listas.
###### * A diferencia de las listas, una vez que se crea una tupla, no se pueden modificar.
###### * Sintaxis común en Python: mi_tupla = (1, 2, 3, 'texto')
---
#### Estructuras Condicionales:
#### `if`:

La declaración `if` se utiliza para realizar una acción si una condición es verdadera. Por ejemplo:

```python
if condicion:
    # Código a ejecutar si la condición es verdadera
```    
#### `if-else`:
La declaración if-else permite ejecutar un bloque de código si una condición es verdadera y otro bloque de código si la condición es falsa. Por ejemplo:
```python
if condicion:
    # Código a ejecutar si la condición es verdadera
else:
    # Código a ejecutar si la condición es falsa
``` 
#### `if - elif-...- else`:

##### La declaración "if-elif-...-else" permite evaluar múltiples condiciones en secuencia y ejecutar el bloque de código del primer if o elif que sea verdadero. Si ninguno es verdadero, se ejecuta el bloque else.
---
### Estructuras de Control
En programación, las estructuras de control de flujo se utilizan para determinar el orden en que se ejecutan las instrucciones en un programa. Estas estructuras permiten tomar decisiones y repetir acciones según ciertas condiciones. Las principales estructuras de control de flujo son:

#### `Estructuras de Control Condicionales`:

###### * `if`: Permite ejecutar un bloque de código si una condición es verdadera.
###### * `else`: Se utiliza en conjunto con if para ejecutar un bloque de código si la condición es falsa.
###### * `elif (abreviatura de "else if")`: Se usa para evaluar múltiples condiciones en secuencia después de un if.
``` python
if condicion:
    # Código si la condición es verdadera
else:
    # Código si la condición es falsa
```
#### `Bucles (Loops)`:

###### * `for`: Permite iterar sobre una secuencia de elementos (como una lista) y ejecutar un bloque de código para cada elemento.
###### * `while`: Permite ejecutar un bloque de código mientras una condición sea verdadera.

```python
for elemento in lista:
    # Código que se ejecuta para cada elemento

while condicion:
    # Código que se ejecuta mientras la condición sea verdadera
```
#### `Estructuras de Control de Salto`:

###### * `break`: Se utiliza para salir prematuramente de un bucle (for o while) antes de que se complete su iteración.
###### * `continue`: Se utiliza para saltar a la siguiente iteración de un bucle sin ejecutar el código restante dentro de esa iteración.
###### * `return`: Se utiliza en funciones para devolver un valor y salir de la función.

```python
for elemento in lista:
    if condicion:
        break  # Sale del bucle si la condición se cumple
    if otra_condicion:
        continue  # Salta a la siguiente iteración si la condición se cumple
def mi_funcion():
    # Código de la función
    return resultado  # Devuelve un valor y sale de la función
