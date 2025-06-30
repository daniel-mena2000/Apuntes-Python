
# Desempaquetado de tuplas


El **desempaquetado de tuplas** en Python es una forma de **asignar los valores de una tupla a varias variables** de forma sencilla y clara.


```python
persona = ("Daniel", 24, "México")
```
```python
nombre, edad, pais = persona

print(nombre)  # Daniel
print(edad)    # 24
print(pais)    # México

```


### ✅ Reglas del desempaquetado

- El número de **variables a la izquierda** debe coincidir con el número de **elementos de la tupla**.
    
- Si no coinciden, obtendrás un error.


### 🎒 Uso con otras colecciones

También puedes desempaquetar **listas** o cualquier **secuencia**:

```python
valores = [10, 20, 30]
x, y, z = valores
```


### ⭐ Desempaquetado parcial con `*`

Puedes usar `*` para capturar el resto:

```python
numeros = (1, 2, 3, 4, 5)

a, b, *resto = numeros
print(a)      # 1
print(b)      # 2
print(resto)  # [3, 4, 5]

```

