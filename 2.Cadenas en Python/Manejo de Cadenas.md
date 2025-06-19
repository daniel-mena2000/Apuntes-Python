
# Manejo de cadenas

```python
cadena1 = 'hola mundo'

# En este ejemplo pareciera que escribimos con un salto de linea pero NO, sigue con el mismo texto
cadena2 = "multiples lineas 1" \
"ffs"

# Si queremos escribir con un salto de linea usamos 3 comillas simples
cadena3 = '''Este ejemplo
de multiples lineas'''

print(cadena1)
print(cadena2)
print(cadena3)
```

Los caracteres de una cadena están indexados de manera secuencial.
Por lo tanto, podemos acceder a cada carácter indicando el índice del carácter que deseamos recuperar

```python
cadena1 = 'hola mundo';

primer_caracter = cadena1[0];
print(primer_caracter) # h
```

## Inmutabilidad de una cadena

Una vez que se crea una cadena, los caracteres dentro de ella no pueden ser modificados.
Si deseamos modificar una cadena, entonces tenemos que asignar directamente otro valor.

```python
cadena1 = 'hola mundo'

cadena1[0] = 'H' # ERROR
```


## Caracteres especiales

Estos caracteres se introducen usando el carácter de diagonal invertida. Ej.

- Nueva línea:  **\n** -> Inserta un salto de línea
- Tabulación: **\t** -> Inserta un tabulador horizontal, útil para alinear texto 
- Comilla simple: **\'**  -> Permite incluir comillas simples en una cadena delimitada por comillas simples
- Comilla doble: **\"**  -> Permite incluir comillas dobles en una cadena delimitada por comillas doble
- Barra invertida: **\\** -> Permite incluir una barra invertida en la cadena.

```python
print('Hola \nMundo')
print('\t\t Python es genial') #        Python es genial
print('Juan \' Perez') # Juan ' Perez
print('agregar \\ diagolan') #agregar \ diagolan

```

## Concatenación de cadenas

La concatenación es una operación que permite combinar 2 o mas cadenas.

En Python existen varias formas.

1. Usar el +
```python
variable1 = 'Hola'
variable2 = 'Mundo';
concatenacion1 = variable1 + variable2 # HolaMundo
concatenacion1 = variable1 + ' ' + variable2 # con espacio

```

2. Usar el método **''.join**

Para mandar llamar el método join iniciamos con una _cadena vacía_ que es donde se guardara la nueva cadena.

```python
concatenacion2 = ''.join([variable1, ' ', variable2]);
print(concatenacion2)
```

## Formateo de cadenas

Python ofrece varias maneras de formatear cadenas, que incluye la capacidad de concatenar texto, variables e incluso dar otro tipo de formateo, como por ejemplo indicar el número de decimales a utilizar en el formato.

- **f-string** Se agrego en Python 3.6 

```python
nombre = 'Jose';
edad = 30;

mensaje = f'Hola me llamo {nombre} y tengo {edad}'
```

- **método format** Es muy versátil y poderoso. Permite construir cadenas muy complejas. Una de la diferencias a la hora de concatenar por ejemplo, es que en las llaves no agregarnos la variable a concatenar directamente, si no que las dejamos vacías y con después en el format si agregamos la variable a unir.


```python
nombre = 'Jose';
edad = 30;

mensaje2 = 'Hola me llamo {} y tengo {} años'.format(nombre,edad);

```
