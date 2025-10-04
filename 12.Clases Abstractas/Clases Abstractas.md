
# Clases Abstractas

Las **clases abstractas** en Python son un concepto de **programación orientada a objetos** que sirven como **plantillas** para otras clases.

👉 Están definidas en el módulo `abc` (**Abstract Base Classes**) y se utilizan cuando quieres que una clase base **no pueda ser instanciada directamente**, sino que obligue a sus clases hijas a implementar ciertos métodos.


### 1. ¿Por qué existen?

- Imagina que tienes una clase `Animal`, pero **no quieres** crear directamente un objeto `Animal` (porque no tendría sentido).
    
- Lo que sí quieres es que **todas las subclases** (`Perro`, `Gato`, etc.) implementen un método como `hacer_sonido()`.
    

Con una clase abstracta logras eso: defines la **estructura** pero no la implementación.

### Sintaxis básica

```python
from abc import ABC, abstractmethod

class Animal(ABC):  # Hereda de ABC para ser abstracta
    @abstractmethod
    def hacer_sonido(self):
        pass
```

Aquí:

- `Animal` es abstracta.
    
- `hacer_sonido` es un método abstracto → las clases hijas **deben** implementarlo.

### Implementación en subclases

```python
class Perro(Animal):
    def hacer_sonido(self):
        return "Guau"

class Gato(Animal):
    def hacer_sonido(self):
        return "Miau"

# Uso
perro = Perro()
gato = Gato()

print(perro.hacer_sonido())  # Guau
print(gato.hacer_sonido())   # Miau

```


> ⚠️ Si intentas hacer `animal = Animal()` → Python te lanza un error porque no se puede instanciar directamente una clase abstracta.



### Métodos abstractos + concretos

Una clase abstracta puede tener métodos **abstractos** (obligatorios en las hijas) y métodos **normales** (que sí tienen código y pueden heredarse):


```python
class Figura(ABC):
    @abstractmethod
    def area(self):
        pass

    def descripcion(self):
        return "Soy una figura geométrica"
```


### Ventajas

- Define una **interfaz común** para las subclases.
    
- Evita instanciar clases que solo sirven como "plantilla".
    
- Hace tu código más **organizado y consistente**.