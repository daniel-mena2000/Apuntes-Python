
# Argumentos Variables

# **`*args`**

En Python, **los argumentos variables** son una forma de permitir que una función reciba una cantidad **indefinida de argumentos**. 

Puedes usar cualquier nombre (`*args` es una convención, no obligatorio), pero el asterisco es lo importante.

En este ejemplo podemos ver que es necesario colocar **args** al final de los parámetros para que sea valido y estos se imprimirán en forma de tupla.

```python
def super_superpoderes(superheroe, nombre, *args): # <----------------------
    print(f'Superheroe: {superheroe} - {nombre} - {args}')

super_superpoderes('Spiderman', 'Peter Parker', 'Instinto aracnido', 'Telaraña')
```

salida:

``Superheroe: Spiderman - Peter Parker - ('Instinto aracnido', 'Telaraña')``


Podemos Iterar solamente estos argumentos:

```python
def super_superpoderes(superheroe, nombre, *args):
    print(f'Superheroe: {superheroe} - {nombre} - {args}')
    # Iterando argumentos
    for poderes in args:
        print(f'Poderes: {poderes}')
super_superpoderes('Spiderman', 'Peter Parker', 'Instinto aracnido', 'Telaraña')
```

salida:

``Superheroe: Spiderman - Peter Parker - ('Instinto aracnido', 'Telaraña')
``Poderes: Instinto aracnido``
``Poderes: Telaraña``


> Si no pasamos los argumentos de la variable se imprimirá la tupla vacía


# **`**kwargs`**

Se usa para recibir una cantidad indefinida de **argumentos nombrados (por nombre)**.


Si combinamos, primero deben ir los ``parametros posicionales``, luego los ``args`` y al final los ``kwargs``

Igualmente si no se le pasan argumentos al parámetro este se imprime vacío

```python
def super_superpoderes(nombre, *args, **kwargs):
    print(f'Superheroe: {nombre} - {args} - Mas info: {kwargs}')


super_superpoderes('Spiderman', 'instinto Aracnido', edad=17, empresa='Marvel')
```

salida:

``Superheroe: Spiderman - ('instinto Aracnido',) - Mas info: {'edad': 17, 'empresa': 'Marvel'}``



### Ejemplo 2:

```python
def mostrar_info(**datos):
    for clave, valor in datos.items():
        print(f'{clave}: {valor}')

```


```python
mostrar_info(nombre="Juan", edad=30, ciudad="México")
# Salida:
# nombre: Juan
# edad: 30
# ciudad: México
```

- Internamente, `datos` es un **diccionario** con las claves y valores.