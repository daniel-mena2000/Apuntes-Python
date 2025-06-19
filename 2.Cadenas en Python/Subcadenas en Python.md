
# Subcadenas en Python

Una subcadena es una parte de una cadena principal, y hay varias maneras de extraer subcadenas en Python.

Podemos extraer subcadenas, buscarlas, reemplazarlas, entre otras operaciones.

Recordar que para obtener la subcadena hay que agregar un índice mas del que estamos recorriendo en este caso hasta la "coma" del texto que es el índice 4.

```python
cadena = 'Hola, mundo!';

#Obtenemos la subcadena de hola
subcadena_hola = cadena[0:4];
print(subcadena_hola) # hola
```


### Buscar Subcadena

El método **find** devuelve el índice de la primera aparición de la subcadena, si no encuentra la subcadena, devuelve _-1_ 

```python
cadenaBuscar = 'Hola, mundo'
indice = cadena.find('mundo');
print(f'Indice donde se encontro la cadena mundo: {indice}')# 6
```

### Remplazar Subcadena

El método **replace** remplazara una subcadena por otra dentro de una cadena principal, le pasamos la palabra a remplazar a la nueva.
Recordar que no estamos modificando la cadena original, estamos creando una nueva y creando su respectivo valor

```python
cadena4 = 'Hola, mundo'

nueva_cadena = cadena.replace('mundo', 'a todos')

print(f'Nueva cadena remplazada: {nueva_cadena}') # Nueva cadena remplazada: Hola, a todos!

```



### Separando en Subcadenas

El método **split** permite dividir una cadena en una lista de subcadenas se le pasara un carácter que indique la separación en este caso cada en encuentre un _espacio en blanco_ separara en subcadenas.

>Como resultado dará una _lista_ con los elementos.

1.
```python
datos = 'texto de ejemplo'
lista = datos.split()
print(lista) # ['texto', 'de', 'ejemplo']
```

2.

En el siguiente ejemplo si le indicamos que separe con cuando encuentre una _coma_

```python
datos2 = 'juan, 30, Chile'
lista2 = datos.split(',');

print(lista2) # ['juan', ' 30', ' Chile']
```


### Multiplicando cadena

Normalmente no podemos hacer operaciones de **strings** con **numeros** pero en Python podemos hacer que un texto se multiplique equis numero de veces con el operador de multiplicación.

```python
texto = 'Hola';
veces = 5;

resultado = texto * veces

print(resultado); # HolaHolaHolaHolaHola
```

