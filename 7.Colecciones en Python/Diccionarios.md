
# Diccionarios

### 📚 ¿Qué es un diccionario en Python?

Un **diccionario** (`dict`) es una estructura de datos que permite **almacenar pares clave:valor**. Es como una agenda donde buscas por un nombre (clave) y encuentras su número (valor).

- La **clave** (key) es única.
    
- El **valor** (value) puede ser cualquier tipo de dato (número, lista, otro diccionario, etc.).

#### Sintaxis básica: 

```python
persona = {
    "nombre": "Daniel",
    "edad": 24,
    "profesion": "Programador"
}
```


### 🔎 Acceder a valores

```python
print(persona["nombre"])  # Daniel
```

 También puedes usar `.get()` que no lanza error si la clave no existe:

```python
print(persona.get("altura"))  # None
```


### 📝 Modificar o agregar elementos

```python
persona["edad"] = 25         # Modificar
persona["ciudad"] = "CDMX"   # Agregar
```


### ❌ Eliminar elementos

```python
del persona["profesion"]      # Elimina esa clave
persona.pop("edad")           # Otra forma
```


### 🔁 Recorrer un diccionario

```python
for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

### 🧪 También puedes hacerlo así:

Este es menos legible y menos limpio

```python
pares = persona.items()

for par in pares:
    print(par)           # ('nombre', 'Daniel')
    print(par[0])        # Clave
    print(par[1])        # Valor

```


### Obtener valores y llaves:

```python
# Obtener solo los valores
print('\n Obtener solo los valores')

for valor in persona.values():
    print(valor)
```

```python
# Obtener solo las llaves:
print('Obtener solo las llaves:')

for llaves in persona.keys():
    print(llaves)
```


### 🧰 Métodos útiles

|Método|Descripción|
|---|---|
|`.keys()`|Devuelve las claves|
|`.values()`|Devuelve los valores|
|`.items()`|Devuelve pares clave:valor|
|`.get(clave)`|Obtiene un valor sin error si no existe|
|`.pop(clave)`|Elimina un elemento y devuelve su valor|
|`.clear()`|Vacía el diccionario|



### 📦 Diccionario dentro de otro

```python
alumnos = {
    "juan": {"edad": 20, "carrera": "Medicina"},
    "ana": {"edad": 22, "carrera": "Ingeniería"}
}
print(alumnos["juan"]["carrera"])  # Medicina

```

##### Agregar elemento de un diccionario dentro de otro

```python
alumnos['pedro'] = {"edad" = 19, 'carrera': 'Maestro'}
```


##### Eliminar elemento

```python
# Eliminar contacto 2 formas

agenda.pop('juan')

del agenda['ana']
```


##### Recorrer elementos de un diccionario dentro de otro

```python

print('\n Contacto')
for nombre, detalles in agenda.items():
    print(f'''Nombre: {nombre}
    Telefono: {detalles.get('telefono')}
    Email: {detalles.get('email')}
    Direccion: {detalles.get('direccion')}
''')
```

