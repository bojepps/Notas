
# INGENIERIA EN COMPUTACION INTELIGENTE
---
### PROGRAMACIÓN FUNCIONAL

---
#### 2da Parcial
---
Kevin Rodriguez Buenrostro 1D

---

**Sintaxis de una Funcion**
``` python
def <function_name>([<parameters>]):
    <statement(s)>
```
Las funciones permiten modularidad, a continuacion un ejemplo de codigo sin modularidad:
```python
#Programa

#Lector de archivos csv
<sentencia 1>
<sentencia 2>

#Procesamiento
<sentencia 3>
<sentencia 4>

#Guardado de datos
<sentencia 5>
<sentencia 6>
\
```

Ahora un ejemplo de un codigo modular:
```python

# Lector de csv
def lector_file():
    <sentencia 1>
    <sentencia 2>
    
# Procesamiento
def procesado_file():
    <sentencia 3>
    <sentencia 4>
    
# Guardado de Datos
def guardado_file():
    <sentencia 5>
    <sentencia 6>

# Programa Principal
read_file()
process_file()
write_file()
```

### Caracteristicas
En Python, se define una función utilizando la palabra clave def, seguida del nombre de la función y paréntesis que pueden contener argumentos. La sintaxis general para definir una función es la siguiente:
```python
def nombre_de_la_funcion(argumento1, argumento2, ...):
    # Cuerpo de la función
    # Puede incluir una serie de instrucciones
    # que se ejecutan cuando la función es llamada
    return valor_de_retorno  # Opcional
   ```
### Llamada de Funciones
Puedes llamar a una función en Python escribiendo su nombre seguido de paréntesis y, si es necesario, proporcionando los argumentos requeridos dentro de los paréntesis. Aquí tienes un ejemplo de cómo llamar a una función:
```python
def saludar(nombre):
    mensaje = "¡Hola, " + nombre + "!"
    return mensaje
resultado = saludar("Juan")
print(resultado)  # Esto imprimirá "¡Hola, Juan!"
```
### Parametros y argumentos
En Python, a menudo se utilizan los términos "parámetros" y "argumentos" en el contexto de las funciones. Es importante comprender la diferencia entre estos dos conceptos:
Parámetros: Los parámetros son nombres de variables que se utilizan en la definición de una función. Son marcadores de posición para los valores que una función espera recibir cuando se llama. Los parámetros se definen entre paréntesis en la declaración de la función y se utilizan en el cuerpo de la función. Son variables locales que toman valores cuando se llama a la función.

Por ejemplo, en la siguiente función, nombre es un parámetro:
```python
def saludar(nombre):
    mensaje = "¡Hola, " + nombre + "!"
    return mensaje
```
En este caso, nombre es un parámetro que la función saludar espera recibir cuando se llama.

**Parametros Por Defecto**
En Python, puedes definir parámetros por defecto en una función. Los parámetros por defecto son valores que se asignan automáticamente a los parámetros de una función si no se proporcionan argumentos correspondientes al llamar a la función. Esto es útil cuando deseas que ciertos parámetros tengan valores predeterminados, pero aún quieres permitir que esos valores se anulen si es necesario. Aquí tienes un ejemplo de cómo se definen y utilizan parámetros por defecto:
Argumentos: Los argumentos son los valores reales que se pasan a una función cuando se la llama. Estos valores se utilizan para asignar a los parámetros de la función. Los argumentos se proporcionan dentro de los paréntesis cuando se llama a la función.
```python
def saludar(nombre="Invitado"):
    mensaje = "¡Hola, " + nombre + "!"
    return mensaje

# Llamamos a la función sin argumentos
saludo_predeterminado = saludar()
print(saludo_predeterminado)  # Esto imprimirá "¡Hola, Invitado!"

# Llamamos a la función con un argumento
saludo_personalizado = saludar("Juan")
print(saludo_personalizado)  # Esto imprimirá "¡Hola, Juan!"
```

Por ejemplo, en el siguiente código, "Juan" es un argumento que se pasa a la función saludar:
```python
resultado = saludar("Juan")
```
En este caso, "Juan" se pasa como argumento a la función saludar, y la función asigna ese valor al parámetro nombre.
En resumen, los parámetros son los nombres de las variables que se definen en la firma de la función, mientras que los argumentos son los valores reales que se pasan a la función cuando se llama. La función utiliza estos argumentos para ejecutar su lógica interna y puede devolver un resultado o realizar alguna acción en función de esos valores.

**Argumentos Posicionales**
Los argumentos posicionales en Python son los valores que se pasan a una función en el mismo orden en el que se definen los parámetros de la función. El primer argumento se asigna al primer parámetro, el segundo al segundo, y así sucesivamente. El orden de los argumentos debe coincidir con el orden de los parámetros en la función. Son la forma más común de pasar datos a una función en Python.
Ejemplo:

```python
def suma(a, b):
    resultado = a + b
    return resultado

# Llamamos a la función suma con argumentos posicionales
resultado_suma = suma(5, 3)
print(resultado_suma)  # Esto imprimirá 8
```
### Valores de parámetros predeterminados mutables
* Ejemplo:
```python
def my_function(my_list=[]):   #"my_list"inicilaiza como lista vacia (valor por defecto de la funcion)
    my_list.append('???')
    return my_list
my_function(["a", "b", "c"])

['a', 'b', 'c', '???']


#Si se llama sin ningún argumento
print(my_function())
print(my_function())
print(my_function())

['???', '???']
['???', '???', '???']
['???', '???', '???', '???']

```

### **Retorno de valores y uso de palabra clave "return"**
* Una instrucción *return* en una función de Python tiene dos propósitos:
1. Al terminar la función devuelve el control de ejecución a partir de donde se llamó.
2. Proporciona un mecanismo para regresar datos donde se llamó o asignó.
```python
def f1():             
    print("Hola")
    print("Mundo")
    return

f1()
```
Hola
Mundo
```python
def f2():             
    print("Hola")
    print("Mundo")
f2()
```
Hola
Mundo
* *return* no necesita estar al final de una función.
* Pueden aparecer en cualquier parte del cuerpo de una función
* Puede aparecer incluso varias veces 

#### Funciones sin valor de retorno (None).
* Puede usarse para la comprobación de errores

```python
def f():
    if error_cond1:
        return
    if error_cond2:
        return
    if error_cond3:
        return

    <normal processing>
```
* Cuando no se da ningún valor de retorno, una función devuelve el valor especial None
```def f():
    return


print(f())
```
None

--------------------------
#### Valor de retorno en funciones:
* Una función puede devolver cualquier tipo de objeto.
 Ejemplo: diccionario
```python
names =  dict(name_1='Hugo', name_2='Paco', name_3='Luis') #hecho en clase
names
{'name_1': 'Hugo', 'name_2': 'Paco', 'name_3': 'Luis'}
```
* Retornar listas que se pueden indizar o dividir:
``` python
names =  dict(name_1='Hugo', name_2='Paco', name_3='Luis') #hecho en clase
names
['a', 'b', 'c', 'd', 'e']
```

### Recursion
La recursión es un concepto en programación y matemáticas en el que una función se llama a sí misma para resolver un problema. Es una técnica poderosa y elegante utilizada en varios lenguajes de programación y algoritmos para resolver problemas complejos descomponiéndolos en subproblemas más pequeños y similares.

Aquí hay algunos puntos clave sobre la recursión:

Caso Base: La recursión se basa en el concepto de un caso base, que es una condición que, cuando se cumple, impide más llamadas recursivas y devuelve un resultado específico. Los casos base son esenciales para evitar la recursión infinita.

Caso Recursivo: En el caso recursivo, la función se llama a sí misma con una entrada modificada para resolver una instancia más pequeña del mismo problema. Cada llamada recursiva debe acercarse al caso base.

Pila de Llamadas: Cuando una función se llama recursivamente, cada llamada se agrega a la pila de llamadas, que lleva un registro del estado de cada llamada de función. La pila se desapila a medida que cada llamada regresa.

Eficiencia: Aunque la recursión puede ser una forma elegante de resolver problemas, no siempre es la más eficiente. La recursión excesiva puede dar lugar a un gran número de llamadas de función y consumir más memoria.

Ejemplos: Los ejemplos de problemas resueltos con recursión incluyen cálculos de factorial, búsqueda en árboles binarios, y resolución de problemas de dividir y conquistar, como el algoritmo de ordenación rápida (quicksort) o el cálculo de números de Fibonacci. La recursión es especialmente útil en situaciones en las que la estructura del problema se asemeja a una estructura en forma de árbol o grafo.

### Aplicacion de Ejemplo con guizero 
Ejemplo de un programa simple utilizando la biblioteca guizero en Python. Este programa creará una ventana con un botón, y cuando se haga clic en el botón, mostrará un cuadro de diálogo con un mensaje. A continuación, se proporciona el código con comentarios explicativos:
```python
from guizero import App, PushButton, info

# Esta función se ejecutará cuando se haga clic en el botón.
def mostrar_mensaje():
    # La función info() muestra un cuadro de diálogo con un mensaje.
    info("Mensaje", "¡Hola, mundo!")

# Crear una aplicación GUI con el título "Ejemplo guizero".
app = App("Ejemplo guizero")

# Crear un botón con el texto "Mostrar Mensaje" que llamará a la función mostrar_mensaje cuando se haga clic en él.
button = PushButton(app, text="Mostrar Mensaje", command=mostrar_mensaje)

# Iniciar la aplicación GUI.
app.display()

# La aplicación permanecerá abierta y esperando eventos (por ejemplo, clics en botones) hasta que se cierre.
```

1. Explicación por comentarios:

2. Importamos las clases App, PushButton y la función info de la biblioteca guizero.

3. Definimos una función llamada mostrar_mensaje() que se ejecutará cuando se haga clic en el botón.

4. Creamos una instancia de la aplicación GUI llamada app con el título "Ejemplo guizero".

5. Creamos un botón llamado button con el texto "Mostrar Mensaje" y especificamos que la función mostrar_mensaje se llamará cuando se haga clic en el botón mediante el parámetro command.

6. Iniciamos la aplicación GUI utilizando app.display(). Esto inicia el bucle de eventos y permite que la aplicación responda a interacciones del usuario.

7. Cuando ejecutes este código, se abrirá una ventana de GUI con un botón. Cuando hagas clic en el botón, aparecerá un cuadro de diálogo con el mensaje "¡Hola, mundo!". Puedes cerrar la ventana de la aplicación cuando hayas terminado. Este es un ejemplo simple de cómo crear una interfaz gráfica de usuario utilizando la biblioteca guizero.
