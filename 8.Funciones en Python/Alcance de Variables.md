
# Alcance de Variables


### 🔹 LEGB: Local, Enclosing, Global, Built-in

1. **Local (L)** – Dentro de una función
    
    Variables definidas **dentro de una función** solo existen en esa función.


```python
def saludar():
    mensaje = "Hola"
    print(mensaje)

saludar()
# print(mensaje)  # ❌ Error: mensaje no está definido fuera de la función

```

## **Enclosing (E)** – Función dentro de función

Es el **ámbito de una función exterior** a otra función (funciones anidadas).

```python
def exterior():
    x = "soy de exterior"

    def interior():
        print(x)  # Accede a x desde la función que lo encierra

    interior()

exterior()

```

## **Global (G)** – A nivel del archivo (fuera de funciones)

Variables definidas **fuera de cualquier función** son globales.

```python
x = "variable global"

def mostrar():
    print(x)  # Accede a la variable global

mostrar()
```

Para modificar una variable global dentro de una función, debes usar la palabra clave `global`:

```python 
contador = 0

def incrementar():
    global contador
    contador += 1

incrementar()
print(contador)  # Imprime 1

```


### **Built-in (B)** – Palabras reservadas de Python
    
    Son funciones o nombres integrados de Python, como `len()`, `print()`, `range()`, etc.
    

---

### 📌 Orden de búsqueda LEGB:

Cuando Python busca una variable, sigue este orden:

1. **Local** (en la función actual)
    
2. **Enclosing** (en funciones que encierran a la actual)
    
3. **Global** (a nivel del archivo)
    
4. **Built-in** (funciones de Python)



## Ejemplo cambio de valor de la variable global


```python
contador_global = 0  # Variable GLOBAL

def incrementar_contador():
    contador_local = 0  # Variable LOCAL (se reinicia cada vez que se llama la función)

    global contador_global  # Esto permite MODIFICAR la variable global
    contador_global += 1    # Se incrementa su valor en 1

    contador_local += 1     # También se incrementa, pero solo vive dentro de la función

    print(f'Contador local: {contador_local}')
    print(f'Contador global: {contador_global}')


incrementar_contador()
incrementar_contador()

```


Salida:

```python
Contador local: 1
Contador global: 1
Contador local: 1
Contador global: 2
```



### 🔍 Explicación:

- `contador_global` es una variable **global**, vive fuera de la función y **su valor se conserva entre llamadas** a la función.
    
- `contador_local` se define dentro de la función, así que **se reinicia cada vez que se ejecuta la función**.
    
- La línea `global contador_global` es clave: sin ella, **no podrías modificar** la variable global desde dentro de la función (solo leerla).


> ✅ **la variable global no depende de la función para existir**, pero **sí puede ser modificada desde dentro de una función** si usas la palabra clave `global`.


### 🔹 Detalles importantes:

- La variable **global vive fuera** de cualquier función y **existe mientras el programa se esté ejecutando**.
    
- Si la modificas desde dentro de una función, debes **usar `global`** para indicarle a Python que **no cree una copia local**, sino que **use la que está fuera**.