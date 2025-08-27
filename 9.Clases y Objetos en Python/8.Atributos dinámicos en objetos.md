
# Atributos dinámicos en objetos

En **Python**, los **atributos dinámicos** son aquellos que **puedes agregar (o quitar) a un objeto en tiempo de ejecución**, es decir, **después de haberlo creado**, aunque no estén definidos en la clase.

## Usar `setattr` para crear/modificar atributos dinámicos

`setattr(objeto, "nombre_atributo", valor)` permite **crear o modificar atributos en tiempo de ejecución** de manera programática.


```python

class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

p1 = Persona('Ana')

#Definiendo directamente
p1.edad = 25

#Definiendo con settar
setattr(p1,'edad2',23)
```

>Estos atributos de edad 1 y edad 2 solo viven en el objeto p1, por lo que si creamos p2 y accedemos estos nos marcara error ya que no están definidos como tal en la clase.



## Diferencia entre `setattr` y asignación directa

- Con `p.edad = 25` → defines directamente un atributo.
    
- Con `setattr(p, "edad", 25)` → es lo mismo, pero útil cuando **el nombre del atributo es dinámico** (por ejemplo, viene de una variable o de un input).


## 📌 También existe `getattr` y `hasattr`

- `getattr(objeto, "atributo", valor_por_defecto)` → obtener un atributo.
    
- `hasattr(objeto, "atributo")` → saber si existe un atributo.

```python
print(getattr(p, "ciudad"))          # Madrid
print(getattr(p, "altura", "N/A"))   # devuelve "N/A" si no existe
print(hasattr(p, "edad"))            # True
print(hasattr(p, "altura"))          # False
```


## Ver que atributos tiene un objeto con `__dict__`



```python
#ver que atributos tiene nuestro objeto

print(p1.__dict__) #{'nombre': 'Ana', 'edad': 25, 'edad2': 23}
```

