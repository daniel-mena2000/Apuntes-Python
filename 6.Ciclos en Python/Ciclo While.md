
# Ciclo While

Claro, Daniel. El ciclo `while` en Python se utiliza para **repetir un bloque de código mientras se cumpla una condición**. Es una estructura de control muy útil cuando **no sabes exactamente cuántas veces necesitas repetir algo**, pero **sí sabes la condición que debe cumplirse para seguir repitiendo**.

```python
contador = 1

while contador <= 5:
    print("Número:", contador)
    contador += 1

```

**¿Qué hace este código?**

- Comienza con `contador = 1`.
    
- Mientras `contador` sea menor o igual a 5, imprime el número y suma 1.
    
- Cuando `contador` llega a 6, la condición ya no se cumple y el ciclo se detiene.


![](img/ciclos.drawio.png)



### ⚠️ Importante: ¡Cuidado con los ciclos infinitos!

Si la condición **nunca se vuelve falsa**, el ciclo se ejecutará para siempre. Por ejemplo:

```python
while True:
    print("Esto nunca termina...")
```



El parámetro `end=' '` en la función `print()` sirve para cambiar lo que se imprime al final de cada línea.

```python
contador = 1
while contador <= 5:
    print(contador, end=' ')
    contador += 1
```

salida: 1 2 3 4 5

Por defecto `print` imprime:
1
2
3
4
5


## Ejercicio Suma acumulativa:

```python
print('*** Suma acumulativa ***')
# Sumar los primeros 5 numeros

MAXIMO = 5
numero = 1
acumulador_suma = 0

while numero <= MAXIMO:

    acumulador_suma += numero
    
    print(acumulador_suma) # 1 3 6 10 15
    
    numero += 1
    
print(f'Resuldato de la suma acumulativa es: {acumulador_suma}') # 15

```



