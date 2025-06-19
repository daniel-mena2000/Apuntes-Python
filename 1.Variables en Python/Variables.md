
# Variables

Una variable en Python es un nombre que almacena valor guardado en la memoria temporal de la computadora o dispositivo.

## Constantes
A diferencia de otros lenguajes de programación, en Python no existe un tipo especifico para definir una constante de manera estricta. Solo es una convención.

Python no impide cambien el valor de una variable, pero podemos seguir la siguiente convención de declarar el nombre de una variable en **mayúsculas** y con ello indicamos que el valor de esta variable NO debe modificarse una vez inicializada, es decir que esta variable se debe tratar como una **constante**.


```python
NOMBRE_CONSTANTE = valor

PI = 3.1416
```


Código:

```python
import math

#Variables en python
edad = 28;
altura = 1.65;
pais = 'México';

# Acceder a las variables
print('Edad:', edad)

# Modificar el valor de una variable
edad = 30
print('Edad modificada:', edad)

edad = 'Treinta'
print('Edad modificada a texto:', edad)

# No hay manera de definir una constante como tal, simplemente usamos MAYUSCULAS
PI = math.pi
print('PI:',PI)
```

