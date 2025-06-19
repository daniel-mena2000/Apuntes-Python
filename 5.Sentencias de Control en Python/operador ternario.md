
# Operador ternario

El **operador ternario** en Python es una forma **abreviada** de escribir una **estructura `if-else`** en una sola línea. Se usa para **elegir entre dos valores** dependiendo de una condición.

```python
valor_si_verdadero if condición else valor_si_falso
```

Ejemplo:

```python
edad = 18
mensaje = "Mayor de edad" if edad >= 18 else "Menor de edad"
print(mensaje)

```

Es equivalente a esto:

```python
if edad >= 18:
    mensaje = "Mayor de edad"
else:
    mensaje = "Menor de edad"

```

