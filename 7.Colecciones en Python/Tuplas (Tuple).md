
# Tuplas

Las tuplas son similares a las listas, ya que también son una colección de datos ordenados, pero estas son **inmutables**, lo que significa que una vez creada no es posible modificar su tamaño, ni podemos agregar más elementos, ni modificarlos ni eliminarlos.

### Características principales de una tupla:

- Se definen con **paréntesis `()`** (aunque también pueden funcionar sin ellos).
    
- Pueden contener **diferentes tipos de datos** (números, cadenas, listas, etc.).
    
- **No se pueden cambiar** (no se puede agregar, eliminar ni modificar elementos).
    
- Son **más rápidas y ligeras** que las listas.
    
- Se pueden recorrer con un `for`, acceder con índices, y se pueden usar como claves en un diccionario (si sus elementos también son inmutables).


```python
# Definición de una tupla
mi_tupla = (1, 2, 3)
print(mi_tupla)          # (1, 2, 3)

# También se puede definir sin paréntesis
otra_tupla = "hola", 10, True
print(otra_tupla)        # ('hola', 10, True)

# Acceso por índice
print(mi_tupla[1])       # 2

# Longitud de una tupla
print(len(mi_tupla))     # 3

# Desempaquetado
a, b, c = mi_tupla
print(a, b, c)           # 1 2 3

#Para que se considere una tupla es necesario la coma al final
tupla_un_elemento = 10,

```

### ❌ Lo que **no** puedes hacer con una tupla:


```python
mi_tupla = (1, 2, 3)

mi_tupla[0] = 99      # ❌ Error: las tuplas no se pueden modificar
mi_tupla.append(4)    # ❌ Error: no tienen métodos como append()

```

