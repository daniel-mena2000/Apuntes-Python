
# Conversión de tipos de datos

La conversión de tipos de datos, también conocida como **castinng**, es una técnica para manipular datos que no están en el tipo requerido.

```python
#Conversion de cadena a numero
numero_cadena = '10'
numero_entero = int(numero_cadena)
print(numero_entero)

#convertir de cadena a flotante
numero_cadena2 = '3.14'
numero_flotante = float(numero_cadena2);
print(numero_flotante);

#convertir de numero a cadena
numero_entero = 25
numero_cadena3 = str(numero_entero);
print(numero_cadena3)

```

### convertir a booleano
Tipo booleano es False en los siguiente casos, si es 0, cadena vacia, o None
Regresa True si es distinto de 0, cadena vacia o de None

```python

numero_entero2 = 0;
booleano1 = bool(numero_entero2);
print(booleano1) # False

numero_entero3 = 5;
booleano2 = bool(numero_entero3);
print(booleano2) # False
```


## Suma y Concatenacion

En este caso como son string simplemente los concatena

```python
numero1_cadena = '10'
numero2_cadena = '20'
resultado1 = numero1_cadena + numero2_cadena
print(resultado1) #1020
```

Los convertimos en enteros

```python
numero1_entero = int(numero1_cadena)
numero2_entero = int(numero2_cadena)
resultado2 = numero1_entero + numero2_entero
print(resultado2) # 30
```

