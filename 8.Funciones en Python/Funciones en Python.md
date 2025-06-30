
# Funciones en Python


### ¿Qué es una función en Python?

Una **función** es un bloque de código que se puede reutilizar. Sirve para agrupar instrucciones que realizan una tarea específica.

### ✅ ¿Para qué sirven?

- Evitan repetir código
    
- Hacen el programa más ordenado y fácil de leer
    
- Permiten dividir problemas grandes en partes pequeñas


### 🔹 ¿Cómo se crea una función?

Usamos la palabra clave `def`, seguida del nombre de la función, paréntesis `()` y dos puntos `:`.

```python
def saludar():
    print("¡Hola, bienvenido!")

```

ejecutar funcion:

```python
saludar()
```


### 🔹 Funciones con parámetros

Puedes pasar datos a una función para que trabaje con ellos.

```python
def saludar(nombre):
    print(f"¡Hola, {nombre}!")

saludar("Daniel")
```


### 🔹 Funciones que devuelven un valor (`return`)

Las funciones pueden devolver datos usando `return`:

```python
def sumar(a, b):
    return a + b

resultado = sumar(5, 3)
print(resultado)  # Imprime: 8

```

### 🔹 Parámetros con valores por defecto

Si no se pasa un valor, se usa el valor por defecto

```python
def saludar(nombre="amigo"):
    print(f"¡Hola, {nombre}!")

saludar()          # Hola, amigo
saludar("María")   # Hola, María

```


### 🔹 Funciones con múltiples valores de retorno

Puedes regresar varios valores separados por comas:

```python
def operaciones(a, b):
    suma = a + b
    resta = a - b
    return suma, resta

s, r = operaciones(10, 3)
print("Suma:", s)
print("Resta:", r)

```

