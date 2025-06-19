# Sentencias de decisión

Las sentencias de decisión nos permiten controlar el flujo de ejecución de un programa.

Las estructuras que podemos usar son: **if, else y elif**

En Python los bloques de código dentro del if se identifican con _tabuladores_ todo lo que este del lado derecho de la condición es un bloque de código, no es como en otros lenguajes que se usan llaves.

```python
edad = 30
if edad >= 18:
    print('Eres mayor de edad')
```

#### Diagrama de flujo:

![](img/python1.png)

#### Sentencia if else

Esta se usa para ejecutar un bloque de código cuando la condición del if es falsa

```python
# Sentencia if else
edad2 = 15
if edad >= 18:
    print(f'Eres mayor de edad. Tienes {edad2} años')
else:
    print(f'Eres menor de edad. Tienes {edad2} años')
```


#### Sentencia if elif else

La sentencia **elif** es una abreviatura de "else if" y se utiliza cuando necesitamos verificar múltiples condiciones, una tras otra.

Se pueden agregar tantas nuevas condiciones de tipo **elif** como necesitemos, pero deben después de un **if** y antes de un **else**

```python

# Sentencia elif

edad3 = 12
if edad3 >= 18:
    print(f'Eres mayor de edad. Tienes {edad2} años')
elif 13 <= edad3 < 18:
    print(f'Eres un adolecente. Tienes {edad2} años')
else:
    print(f'Eres un niño. Tienes {edad2} años')
```



![](img/python2.png)