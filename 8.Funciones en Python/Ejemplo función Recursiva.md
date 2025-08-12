
# Ejemplo función Recursiva


### Factorial de un Número con Recursividad


![](img/d.png)



```python
print('Factorial del número 5')

# Definimos la funcion factorial recursiva
# Definimos que el factorial de 0 y 1 sera siempre igual a 1
def factorial_recursiva(numero):
    if numero == 0 or numero == 1: # Caso Base
        print(f'Resultado factorial parcial {numero} e: 1')
        return 1
    else: # Caso recursivo
        factorial_parcial = numero * factorial_recursiva(numero - 1)
        print(f'Resultado factorial parcial {numero} es: {factorial_parcial}')
        return factorial_parcial

resultado = factorial_recursiva(5)

# Primero revisara el caso base, debido a que no es 0 ni 1 pasara al caso recursivo
# En el que numero en este caso 5 se multiplicara mandando a llamar de forma recursiva a la misma funcion y a ese 5 multiplicando y disminuyendo en 1 hasta que entre en el caso base
```

