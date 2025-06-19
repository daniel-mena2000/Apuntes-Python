
# Entrada de datos por consola

Permite a los usuarios proporcionar valores dinámicos, en lugar de valores duros o estáticos.

En este ejemplo cuando corramos Python nos pedirá primero en consola que ingresemos el dato

```python
nombre = input('Introduce tu nombre: ');

print(f'Recibiendo el valor de nombre: {nombre}')
```

En el siguiente ejemplo nos mostrara que al pedir un dato este será un **string** por defecto y si queremos un numero como dato, tendremos que convertirlo.

```python
edad = int(input('Introduce tu edad: '))

print(f'Tu edad es: {edad}')
```


## Ejercicio 1:

Crea un programa para solicitar la informacion de un empleado, introduciendo los datos por consola: nombre empleado, edad, salario y si es jefe de departamento.

Para el salario usaremos después de la variables **:.2f**  que indica que queremos 2 dígitos después del dato y que es de tipo flotante.

```python

nombre_empleado = input('Nombre empleado: ')
edad_empleado = int(input('Edad empleado: '))
salario_empleado = float(input('Salario empleado: '))
es_jefe_departamento = input('Es jefe departamento (Si/No): ')

# Vamos a convertir a un tipo bool la variable si es jefe de departamento
# Cualquier otra cosa que escriba el usuario que no sea "si" sera false
es_jefe_departamento = es_jefe_departamento.lower() == 'si';

print(f'Nombre: {nombre_empleado}')
print(f'Edad: {edad_empleado}')
print(f'Salario: {salario_empleado:.2f}')
print(f'Es jefe de departamento: {es_jefe_departamento}');
```


## Ejercicio 2

Crea un programa para solicitar algunos valores importantes para una receta de cocina
Valores: Nombre de la receta, ingredientes, tiempo de preparación en minutos, dificultad(fácil, media, alta)


```python
nombre_receta = input('Nombre de la Receta: ')
ingredientes = input('Ingrediente: ')
tiempo_preparacion = int(input('Tiempo de preparacion: '))
dificultad = input('Dificultad: ')
```

