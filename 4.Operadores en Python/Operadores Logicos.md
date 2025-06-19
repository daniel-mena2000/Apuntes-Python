
 # Operadores Lógicos

Se usan para combinar expresiones booleanas.

|Operador|Descripción|Ejemplo|
|---|---|---|
|`and`|Y lógico|`True and False` → `False`|
|`or`|O lógico|`True or False` → `True`|
|`not`|Negación lógica|`not True` → `False`|

### ✅ Tabla de verdad de `and` (A **and** B)

|A|B|A and B|
|---|---|---|
|True|True|True|
|True|False|False|
|False|True|False|
|False|False|False|

🧠 **Regla**: Solo es `True` si **ambas** son `True`.


### ✅ Tabla de verdad de `or` (A **or** B)

|A|B|A or B|
|---|---|---|
|True|True|True|
|True|False|True|
|False|True|True|
|False|False|False|

🧠 **Regla**: Es `True` si **al menos una** es `True`.


### ✅ Tabla de verdad de `not` (solo invierte)

|A|not A|
|---|---|
|True|False|
|False|True|

🧠 **Regla**: Cambia `True` a `False` y viceversa.



```python
A = True
B = False

print(A and B)  # False
print(A or B)   # True
print(not A)    # False
print(not B)    # True
```


### Ejercicio con AND

Una tienda de supermercado ofrece un descuento especial a clientes que compren 10 o mas artículos por día y además sean miembros de la tienda.

El sistema debe solicitar al cliente que indique cuantos artículos ha comprado en el día y preguntarle si cuenta con membresía de la tienda.

En caso de haber comprado 10 o mas productos y ser miembro de la tienda entonces tendrá accedo al descuento VIP

> Recordar que 'and' solo regresa verdadero si las 2 son verdadero


```PYTHON
#
print('--SISTEMA DE DESCUENTOS VIP--')

No_PRODUCTOS_DESCUENTOS = 10

No_PRODUCTOS_CLIENTE = int(input('Indique cuantos productos lleva: '));
tiene_membresia = input('Indique si tiene membresia de la tienda (Si/No)')

es_elegible_descuento = (No_PRODUCTOS_CLIENTE >= No_PRODUCTOS_DESCUENTOS and
                          tiene_membresia.strip().lower() == 'si')

print(f'Tienes acceso al descuento VIP? {es_elegible_descuento}')
```



### Ejercicio con OR

Se pide crear un sistema para una biblioteca, la cual desea prestar libros si cumple con cualquiera de las siguientes condiciones:

1. El usuario tiene credencial de estudiante.
2. El usuario vive a nos mas de 3km a la redonda.

Si cumple con cualquiera de estas condiciones se le puede prestar el libro.

```python
print('SISTEMA PRESTAMOS DE LIBROS')

DISTANCIA_PERMITIDA_KM = 3

credencial_estudiante = input('Tienes credencial de estudiante Si/No? ')
vive_cerca = int(input('A cuantos km vives de la biblioteca? '))

validacion = (credencial_estudiante.strip().lower() == 'si' or
               vive_cerca <= DISTANCIA_PERMITIDA_KM)

print(f'Se le prestara el libro: {validacion}')
```



### Ejercicio con Not

Como una cadena vacía en Python es tomada como False a la hora de invertir con _not_ pues dara True dando como resultado que nuestra variables si esta vacia.
1. 
```python
#Revisar si una variables es cadena vacia
nombre = ''
es_cadena_vacia = not nombre
print(f'El valor nombre es cadena vacia? {es_cadena_vacia}')
```

2. 
```python
# Revisar si una variables no tiene ningun valor

variable = None
es_variable_sin_valor = not variable

print(f'La variable No tiene ningun valor asignado? {es_variable_sin_valor}')
```


```python
#Revisar si una variable se encuentra dentro derango entre 1 y 10

from random import randint

datos = randint(1,20)

rango = not datos >= 10

print(f'Esta en el rango?{datos}-{rango} ')
```

