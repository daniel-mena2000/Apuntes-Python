
La función **randint()**, que es parte del módulo _ramdom_, nos permite generar números aleatorios.

**randint(a, b)** devuelve un número aleatorio entre a y b, incluyendo estos valores.

Es importante importar primero el módulo de ramdom antes de usar la función randint()
Podemos importar todo el módulo o solo la función que necesitemos.

1. 
```python
import ramdom
```
2. 
```python
from random import randint
```

```python
# Generar un numero aleatorio entre 1 y 10

numero = randint(1, 10);
print(numero)
```


Si solo usamos **import ramdom** si es necesario especificar el nombre del modulo y la función a utilizar:

```python
numero = random.randint(1, 10);
print(numero)
```

