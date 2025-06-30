
En Python, **las colecciones** son **estructuras de datos** que permiten **almacenar y organizar múltiples valores** en una sola variable. Son fundamentales para manejar conjuntos de datos de manera eficiente.

Las principales colecciones en Python son:

### 1. **Listas (`list`)**

- **Ordenadas**
    
- **Mutables** (puedes modificar sus elementos)
    
- Permiten elementos duplicados
    



```python
`frutas = ["manzana", "banana", "naranja"]`
```

---

### 2. **Tuplas (`tuple`)**

- **Ordenadas**
    
- **Inmutables** (no puedes cambiar sus elementos)
    
- Permiten duplicados
    


```python
`coordenadas = (10, 20)`
```

---

### 3. **Conjuntos (`set`)**

- **Desordenados**
    
- **No permiten duplicados**
    
- No tienen índices
    



```python
`numeros = {1, 2, 3, 3, 4} # Resultado: {1, 2, 3, 4}`
```


---

### 4. **Diccionarios (`dict`)**

- Almacenan pares clave:valor
    
- **Ordenados** desde Python 3.7+
    
- Las claves son únicas
    



```python
`persona = {"nombre": "Juan", "edad": 30}`
```

---

### Ejemplo comparativo:


```python
`lista = [1, 2, 3]

tupla = (1, 2, 3)

conjunto = {1, 2, 3}

diccionario = {"a": 1, "b": 2, "c": 3}`
```

