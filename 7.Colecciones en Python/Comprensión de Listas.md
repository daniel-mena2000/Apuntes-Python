
# Comprensión de Listas

```python
[expresión for elemento in iterable]
```

### 🔹 Ejemplo simple:

```python
# Crear una lista con los cuadrados de los números del 1 al 5

cuadrados = [x**2 for x in range(1, 6)]
print(cuadrados)  # Resultado: [1, 4, 9, 16, 25]
```


### 🔹 Con condicional (if):

```python
# Números pares del 1 al 10
pares = [x for x in range(1, 11) if x % 2 == 0]
print(pares)  # Resultado: [2, 4, 6, 8, 10]

```

### 🔹 Con condicional if...else:

```python
# Etiquetar números como par o impar
etiquetas = ['par' if x % 2 == 0 else 'impar' for x in range(1, 6)]
print(etiquetas)  # Resultado: ['impar', 'par', 'impar', 'par', 'impar']

```


### 🔹 Ventajas:

- Código más corto y limpio.
    
- A menudo más rápido que un bucle `for` tradicional.


### 🔹 Equivalente con bucle tradicional:


```python
# Con bucle for
cuadrados = []
for x in range(1, 6):
    cuadrados.append(x**2)

```