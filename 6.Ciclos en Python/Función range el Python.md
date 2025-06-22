
# Función range el Python

En Python, `range` se usa principalmente para **generar una secuencia de números**, y es muy común utilizarlo en los bucles `for`.

```python
range(inicio, fin, incremento)

```

>El parámetro de inicio y incremento son opcionales, el de fin si se tiene que proporcionar


- **inicio** _(opcional)_: número donde comienza la secuencia (por defecto es 0).
    
- **fin**: número donde se detiene la secuencia **(no se incluye)**.
    
- **incremento** _(opcional)_: incremento entre cada número (por defecto es 1).


Ejemplos:

1. Contar del 0 al 4:

```python
for i in range(5):
    print(i)
```

Salida: 

0
1
2
3
4

 2. Contar del 2 al 6:

```python
for i in range(2, 7):
    print(i)

```

Salida: 

2
3
4
5
6

3. Contar de 0 a 10 en pasos de 2:

```python
for i in range(0, 11, 2):
    print(i)
```

Salida:

0
2
4
6
8
10

4. Contar hacia atrás

```python
for i in range(5, 0, -1):
    print(i)
```

Salida:

5
4
3
2
1


### ¿Dónde se usa comúnmente `range`?

- Para **repetir un bloque de código** varias veces.
    
- Para **iterar por índices** en una lista o cadena.
    
- Para **generar secuencias de números** sin tener que crearlas manualmente.