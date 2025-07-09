
# Funciones recursivas

### ✅ ¿Qué es una función recursiva?

Una **función recursiva** es una función **que se llama a sí misma** para resolver un problema.

Se utiliza cuando un problema puede dividirse en subproblemas más pequeños del mismo tipo.

### 🧠 Reglas básicas de una función recursiva:

1. **Caso base**: condición que detiene la recursión (evita que sea infinita).
	Es la **condición que detiene la recursión**.  
	Sin esto, la función **se llamaría a sí misma infinitamente**, causando un error.

	📌 **Objetivo del caso base**:  
	Evitar que la función siga llamándose para siempre.

	📌 **Se coloca generalmente con un `if`** que revisa cuándo **ya no hay más trabajo por hacer**.
    
2. **Caso recursivo**: cuando la función se llama a sí misma.
	Es la **condición que detiene la recursión**.  
	Sin esto, la función **se llamaría a sí misma infinitamente**, causando un error.

	📌 **Objetivo del caso base**:  
	Evitar que la función siga llamándose para siempre.

	📌 **Se coloca generalmente con un `if`** que revisa cuándo **ya no hay más trabajo por hacer**.



#### Ejemplo: Imprimir del 1 al 5 de forma recursiva

El caso base es que si el numero es igual a 1, significa que hemos terminado de imprimir los números y ya no es necesario volver a llamar de nueva cuenta la función de forma recursiva.

En caso de que no entre en el if se dice que es el "caso recursivo".

 El numero 5 es donde empiezan cada una de las revisiones y es el ultimo numero que se manda a imprimir

Empieza en 5 como no es igual a 1 entra en la llamada recursiva y a ese 5 se le resta 1, y asi sucesivamente gasta que el numero sea 1 que es el fin



```python
def funcion_recursiva(numero):
    #caso base
    if numero == 1:
        print(numero, end=' ')
    else: # caso recursivo
        print(numero, end=' ')
        funcion_recursiva(numero - 1)


funcion_recursiva(5)
```

Salida:

``5 4 3 2 1 ``


