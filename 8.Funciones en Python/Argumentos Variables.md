
# Argumentos Variables

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