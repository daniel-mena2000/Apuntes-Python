
# Operadores en Python

En Python, **los operadores** son símbolos o palabras especiales que se utilizan para **realizar operaciones sobre variables y valores**. Se pueden agrupar en diferentes tipos según su propósito:

### 🔢 1. **Operadores aritméticos**

| Operador | Descripción      | Ejemplo (`a = 10`, `b = 3`) | Resultado  |
| -------- | ---------------- | --------------------------- | ---------- |
| `+`      | Suma             | `a + b`                     | `13`       |
| `-`      | Resta            | `a - b`                     | `7`        |
| `*`      | Multiplicación   | `a * b`                     | `30`       |
| `/`      | División         | `a / b`                     | `3.333...` |
| `//`     | División entera  | `a // b`                    | `3`        |
| `%`      | Módulo (residuo) | `a % b`                     | `1`        |
| `**`     | Potencia         | `a ** b`                    | `1000`     |


### 📦 2. **Operadores de asignación**

|Operador|Ejemplo|Equivale a|
|---|---|---|
|`=`|`a = 5`|Asigna 5 a `a`|
|`+=`|`a += 2`|`a = a + 2`|
|`-=`|`a -= 2`|`a = a - 2`|
|`*=`|`a *= 2`|`a = a * 2`|
|`/=`|`a /= 2`|`a = a / 2`|
|`//=`|`a //= 2`|`a = a // 2`|
|`%=`|`a %= 2`|`a = a % 2`|
|`**=`|`a **= 2`|`a = a ** 2`|
##### Asignación multiple

En Python también tenemos la asignación múltiple, lo que nos permite asignar valores a varias variables en una sola línea y así hacerlo mas compacto.

En este caso la _variable1_ se asigna al _valor1_ y la _variable2_ al _valor2_, siempre y cuando coincidan el numero de variables asignadas a los datos.

1. 
```python
variable1, variable2 = valor1, valor2
```
2. 
```python
a,b,c = 10, 'saludo, 14.5'
```

##### Asignación encadenada

Permite asignar el mismo valor a múltiples _variables_

En este caso _a,b,c_  tendrán el mismo valor que igual a 10

```python
a = b = c = 10

print(f'valor a= {a}, b = {b}, c = {c}');
```

##### Intercambio de valores de una variable, sin utilizar variables temporales


```python
x,y = 5,10
print(f'valores iniciales x = {x}, y = {y}') # 5,10

x,y = y,x
print(f'Invertir valores x = {x}, y = {y}') #10, 5
```


##### Recibir múltiples valores de la entrada del usuario

Para que detecte que son 2 valores y no 1, hay que separarlos con el método "split"

```python
nombre, apellido = input('Ingresa tu nombre y apellido separados por coma: ').split(',');
print(f'Nombre: {nombre}, Apellido: {apellido}')
```