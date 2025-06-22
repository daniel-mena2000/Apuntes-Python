
# Listas

Las **listas en Python** son un tipo de estructura de datos que permite almacenar **una colección ordenada y modificable de elementos**. Puedes pensar en ellas como una caja que guarda varios valores, y cada valor tiene una posición (índice) que empieza desde `0`.

### 🟢 Características principales de las listas:

- Son **ordenadas**: los elementos tienen un orden fijo.
    
- Son **mutables**: puedes cambiar sus elementos.
    
- Pueden contener **diferentes tipos de datos**: enteros, cadenas, otros objetos, incluso otras listas.
    
- Permiten **elementos duplicados**.


```python
mi_lista = [1, 2, 3, 4, 5]
```
También pueden tener elementos de distintos tipos:

```python
mi_lista = [1, "Hola", 3.14, True]
```


### 🔹 Acceder a elementos:


```python
print(mi_lista[0])  # Imprime el primer elemento (1)
```

### 🔹 Modificar elementos:


```python
mi_lista[1] = "Mundo"
```


### 🔹 Métodos útiles de listas:

```python
mi_lista.append(6)      # Agrega un elemento al final
mi_lista.insert(2, 99)  # Inserta 99 en la posición 2
mi_lista.remove(3.14)   # Elimina el primer valor 3.14
mi_lista.pop()          # Elimina y devuelve el último elemento
mi_lista.sort()         # Ordena la lista (si todos los elementos son comparables)

```