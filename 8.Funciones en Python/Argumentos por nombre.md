
# Argumentos por nombre

En Python, **los argumentos por nombre** (también llamados **argumentos con nombre** o **keyword arguments**) son aquellos que se pasan a una función **especificando el nombre del parámetro** al que pertenecen.


```python

def imprimir_persona(nombre, apellido, edad):
    print(f'Persona: nombre = {nombre}, apellido = {apellido}, edad = {edad}')
```

##### Pasando argumentos de manera posicional:

```python
# Imprimiendo la funcion pansado argumentos de manera posicional
imprimir_persona('Daniel', 'Quintana', 18)
```

##### Pasando argumentos por nombre

Podemos pasar los argumentos de manera desordenada

```python
# Imprimiendo la funcion usando por nombre
imprimir_persona(nombre='Jose',apellido='Lopez',edad=20)
```

