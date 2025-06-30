
# sets en Python

En Python, un **set** (o conjunto) es una **colección desordenada** de elementos **únicos** e **inmutables** (no se repiten y no se pueden modificar), aunque el set en sí **sí es mutable**, es decir, puedes agregar o eliminar elementos.


### 🔹 Características principales de los sets:

- No tienen elementos duplicados.
    
- No tienen un orden fijo.
    
- No se puede acceder a los elementos por índice.
    
- Son útiles para operaciones de conjuntos como **unión**, **intersección**, **diferencia**, etc.


## 🔸 Cómo crear un set:

```python
mi_set = {1, 2, 3, 4}
print(mi_set)  # {1, 2, 3, 4}
```

O usando el constructor:

```python
mi_set = set([1, 2, 3, 3, 4])
print(mi_set)  # {1, 2, 3, 4} (elimina duplicados)
```

> Si queremos inicializar un `set` vacío lo correcto es con el _constructor_ ya que si lo inicializamos con las llaves vacías `mi_set = { }` esto hace referencia a un diccionario no a un set
 

```python

## 🔸 Métodos útiles:

```python
s = {1, 2, 3}
s.add(4)         # Agrega un elemento
s.remove(2)      # Elimina un elemento (da error si no existe)
s.discard(10)    # Elimina sin error si no existe
s.clear()        # Vacía el set
```


```python
# add()
s = {1, 2}
s.add(3)
print(s)  # {1, 2, 3}

# update()
s.update([4, 5])
print(s)  # {1, 2, 3, 4, 5}

# remove() (da error si no existe)
s.remove(4)
print(s)  # {1, 2, 3, 5}

# discard() (no da error si no existe)
s.discard(10)  # No pasa nada

# pop() (elimina un elemento aleatorio)
elemento = s.pop()
print(f'Elemento eliminado: {elemento}')
print(s)  # El set sin ese elemento

# clear()
s.clear()
print(s)  # set()

```



## Operaciones con sets


#### Union

Podemos observar que los elementos duplicados solo se muestran una vez

```python
a = {1,2,3,4}
b = {3,4,5,6}

union = a | b
print(f'a y b: {union}') # a y b: {1, 2, 3, 4, 5, 6}
```

#### Intersección

Como vemos solo muestra los valores que coinciden de ambos sets en este caso 3 y 4 se repiten en ambos


```python
a = {1,2,3,4}
b = {3,4,5,6}
interseccion = a & b
print(f'Interseccion de a y b {interseccion}') # Interseccion de a y b {3, 4}
```


#### Diferencia

La diferencia entre dos sets **A y B** (escrita como `A - B` o `A.difference(B)`) es un nuevo set que contiene **solo los elementos que están en A pero no en B**.

>> 📌 **Importante:** El orden importa. `A - B` no es lo mismo que `B - A`.

```python
a = {1,2,3,4}
b = {3,4,5,6}
diferencia = a - b
print(f'Diferencia de a - b: {diferencia}') # Diferencia de a - b: {1, 2}
```

📌 ¿Por qué `{1, 2}`?  
Porque:

- El conjunto `A` tiene: `{1, 2, 3, 4}`
    
- El conjunto `B` tiene: `{3, 4, 5, 6}`
    

Entonces:

- 1 y 2 están solo en `A` (✅ quedan).
    
- 3 y 4 están en ambos (❌ se eliminan del resultado).
    
- 5 y 6 no importan porque están en `B`, no en `A`.

🔁 ¿Y si hacemos `B.difference(A)`?

```python
print(B.difference(A))  # {5, 6}
```

Porque ahora nos quedamos con los elementos que están en `B` pero **no** en `A`.


#### Diferencia Simétrica

La **diferencia simétrica** entre dos sets `A` y `B` es un nuevo set que contiene los elementos que están **en A o en B, pero no en ambos**.

> 🔁 Es como decir: "dame todo lo que **no está repetido** entre los dos".



```python
a = {1, 2, 3}
b = {3, 4, 5}

# diferencia simétrica
print(a.symmetric_difference(b))  # {1, 2, 4, 5}
print(a ^ b)                      # {1, 2, 4, 5}
```


