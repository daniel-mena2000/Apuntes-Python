
# Break y Continúe

En Python, `break` y `continue` son **instrucciones de control de flujo** que se usan dentro de bucles (`for` o `while`) para alterar su comportamiento:

ejemplo 1 break:

```python
for numero in range(1, 10):
    if numero == 5:
        break
    print(numero)
```
salida:

1
2
3
4

> Cuando `numero == 5`, se ejecuta `break` y se termina el bucle.

ejemplo 2:

```python
for numero in range(1, 10):
    if numero % 2 == 0:
        print(numero)
        break # Salimos el ciclo despues de la primera impresion
```

salida: 
2

ejemplo 1 continue:

```python
for numero in range(1, 6):
    if numero == 3:
        continue
    print(numero)

```
salida:

1
2
4
5

>En la iteración donde `numero == 3`, el `continue` salta el `print(numero)` y sigue con el siguiente número.


ejemplo 2 continue:


 ```python
 for numero2 in range(1,10):
    if numero2 % 2 == 1: # numero impar
        continue
    print(numero2)

```
salida:

2
4
6
8

> En este caso salta los numero impares y muestra solo los pares


### 🧠 Diferencia clave:

- `break` **rompe** el bucle.
    
- `continue` **omite** lo que queda de la iteración actual y **continúa** con la siguiente.
