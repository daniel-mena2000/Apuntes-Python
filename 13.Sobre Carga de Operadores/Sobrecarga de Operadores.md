
# Sobrecarga de Operadores


La sobrecarga de un operador significa que un mismo operador puede comportarse de diferentes formas, por ejemplo el operador de _suma_, ya que este se comporta diferente si se trata de sumar **strings** o **numeros** en un caso suma y en otro concatena.

```python
a = 3
b = 4

print(a + b) # 7
```

```python

a = "Hola"
b = "Mundo"

print(a + b) # "Hola Mundo"
```


>Esto mismo lo podemos hacer con clases en Python, pero tenemos que agregar la sobrecarga de un método dependiendo del operador que queramos sobrecargar.


La **sobrecarga de operadores** en Python es la capacidad de darle un comportamiento especial a los operadores habituales (`+`, `-`, `*`, `<`, `==`, etc.) cuando se usan con objetos de una clase definida por ti.

En otras palabras, puedes definir cómo deben comportarse tus propios objetos cuando se les aplica un operador. Esto se logra implementando métodos especiales (también llamados **dunder methods** o **métodos mágicos**) dentro de la clase.

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    # Sobrecarga del operador +
    def __add__(self, otro):
        return Vector(self.x + otro.x, self.y + otro.y)

    # Sobrecarga del operador *
    def __mul__(self, escalar):
        return Vector(self.x * escalar, self.y * escalar)

    # Representación en string
    def __str__(self):
        return f"({self.x}, {self.y})"
```

```python
v1 = Vector(2, 3)
v2 = Vector(4, 5)

print(v1 + v2)      # (6, 8) → aquí se llama __add__
print(v1 * 3)       # (6, 9) → aquí se llama __mul__
```

