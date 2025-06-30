
# Listas con Diccionarios


### 1. ✅ Lista de diccionarios

Una **lista** donde cada elemento es un **diccionario**. Se usa para manejar muchos "objetos" similares:

```python
personas = [
    {
        'nombre': 'Regina',
        'apellido': 'Flores',
        'edad': 21
    },
    {
        'nombre': 'Alejandro',
        'apellido': 'Reyes',
        'edad': 32
    }
]
```

#### Acceder a un diccionario desde una lista

Recordar que las listas se accede a partir de un índice, entonces accedemos al índice del diccionario que queremos y con **get** a la llave de la información que deseamos.

```python
print(f'''Nombre: {personas[0].get('nombre')}

Apellido: {personas[0].get('apellido')}

Edad: {personas[0].get('edad')}
''')
```

Salida:

Nombre: Regina
Apellido: Flores
Edad: 21
#### Recorrer los elementos de la lista

```python
for persona in personas:
    print(persona["nombre"], persona["edad"])
```

Salida:

Regina 21
Alejandro 32

#### Recorrer los elementos de la lista y listarlos

En este caso recibe otro parámetro que llamaremos _contador_ y el método _enumerate_ y le pasaremos la lista para listar sus elementos.

```python
for contador, persona in enumerate(personas):

    print(f'{contador} - Persona: {persona}')
```

Salida: 


0 - Persona: {'nombre': 'Regina', 'apellido': 'Flores', 'edad': 21}
1 - Persona: {'nombre': 'Alejandro', 'apellido': 'Reyes', 'edad': 32}


Ya dentro del recorrido igualmente podemos ver la información por separado solo accedemos con _persona_ que es el elemento actual y le pasamos la _llave_  del diccionario

```python
    print(f'Detalles: Nombre: {persona.get('nombre')} , Apellido:{persona.get('apellido')}')

```

Salida:

Detalles: Nombre: Regina , Apellido: Flores

