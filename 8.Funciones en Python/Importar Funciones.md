
# Importar Funciones


tenemos 2 archivos

1. modulo_funcion_sumar.py
2. funciones.py


En el archivo 1 tenemos el siguiente código que hace una suma

```python
def sumar(a,b):
    mi_suma = a + b
    return mi_suma
```

En el segundo archivo la mandamos a llamar y hay 2 formar de **importar** la función:

1. Una es con **import** y el nombre del archivo donde se encuentra la función

```python
import modulo_funcion_sumar
```

La llamada se vería así:

```python
print(modulo_funcion_sumar.sumar(4,4))
```


2. La segunda forma es especificando la función.

```python
from modulo_funcion_sumar import sumar
```

La llamada se vería así:

```python 
print(sumar(4,4))
```


Si por ejemplo tenemos código en el archivo **1** donde hacemos igualmente otra suma se vería así:

```python
def sumar(a,b):
    mi_suma = a + b
    return mi_suma

print(f'Resultado de la suma: {sumar(15,30)}') # <--------------------------
```

Si lo ejecutamos desde ese archivo se ve así la salida:

_Resultado de la suma: 45_

Pero si lo ejecutamos desde el archivo **2** donde tenemos solo la llamada

```python
print(f'Suma: {sumar(4,4)}')
```

salida: 

_Resultado de la suma: 45_
_Suma: 8_

>Como vemos se ejecuto el código del archivo **1** 


Para evitar esto tenemos que hacer lo siguiente:

Donde haremos un if donde si el modulo de **__name__** es igual a **__main__**, donde name va a detectar el nombre del modulo donde estamos trabajando en este momento. Si mandamos a imprimir "name" nos daremos que cuanta que imprimirá: **__main__** por ello estamos indicando, si el nombre del archivo es igual a main significa que estamos trabajando en este mismo archivo, y así evitaremos que se ejecute en otros archivos.
 
```python
def sumar(a,b):
    mi_suma = a + b
    return mi_suma

if __name__ == '__main__':
    print(f'Resultado de la suma: {sumar(15,30)}')
```