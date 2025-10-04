
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
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
# Este metodo "add" se manda llamar de manera automatica cuando hacemos una suma
    def __add__(self, other):
#Aqui en este caso queremos concatenar los nombres, primero el del primer objeto y luego el segundo
        return f'{self.nombre} {other.nombre}'
        
	def __sub__(self, other):
        return self.edad - other.edad

```

```python
persona1 = Persona('Juan', 30)
persona2 = Persona('Carlos', 23)

print(persona1 + persona2) # Juan Carlos
print(persona1 - persona2) # 7
```


### 1. El parámetro `otro` o `other` en `__add__`

Cuando haces:

```python
obj1 + obj2
```

Lo anterior seria equivalente a hacer: 

```python
obj1.__add__(obj2)
```

Y como podemos ver el "obj2" seria el "other" o el otro objeto

- `self` → es `obj1` (el objeto a la izquierda del `+`)
    
- `otro` → es `obj2` (el objeto a la derecha del `+`)
    

Por eso dentro de `__add__`, `otro` representa el **segundo vector** con el que quieres sumar.




> La sobrecarga y la sobreescritura son 2 conceptos diferentes

### Métodos mágicos más comunes para sobrecargar operadores

- `__add__(self, other)` → `+`
    
- `__sub__(self, other)` → `-`
    
- `__mul__(self, other)` → `*`
    
- `__truediv__(self, other)` → `/`
    
- `__floordiv__(self, other)` → `//`
    
- `__mod__(self, other)` → `%`
    
- `__pow__(self, other)` → `**`
    
- `__eq__(self, other)` → `==`
    
- `__lt__(self, other)` → `<`
    
- `__le__(self, other)` → `<=`
    
- `__gt__(self, other)` → `>`
    
- `__ge__(self, other)` → `>=`
    
- `__str__(self)` → `str(obj)` o `print(obj)`
    
- `__repr__(self)` → representación oficial del objeto