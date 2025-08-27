
# Bubble Sort

El **algoritmo de la burbuja** (o _bubble sort_) es uno de los métodos más simples para ordenar una lista. Su idea principal es recorrer varias veces la lista comparando pares de elementos adyacentes y **"burbujeando"** los más grandes hacia el final (o los más pequeños, según el orden).

## 🔹 Explicación paso a paso:

1. Se recorre la lista desde el inicio hasta el penúltimo elemento.
    
2. En cada paso, se compara el elemento actual con el siguiente:
    
    - Si están en el orden incorrecto (por ejemplo, mayor antes que menor), **se intercambian**.
        
3. Al final de la primera pasada, el elemento más grande habrá llegado al final de la lista.
    
4. Se repite el proceso para el resto de la lista, sin incluir los elementos ya ordenados al final.
    
5. El proceso termina cuando no se hacen más intercambios o cuando ya se han realizado todas las pasadas necesarias.

![](img/burbuja.png)


En conclusión: **sí, burbuja es lento** y solo se usa con fines educativos (para aprender cómo funcionan los algoritmos de ordenamiento). En proyectos reales, **nunca se usa** porque existen algoritmos mucho más rápidos y eficientes.


```python

def buble(array):
    n = len(array)

    for i in range(n): # array para sacar posiciones
#El segundo buble se encargara de ir comparando los numeros
        for j in range(0, n-i-1):
            if array[j] > array[j+1]:
                array[j], array[j+1] = array[j+1], array[j] #Se hace el intercambio si es que j es mayor a j+1

array=[190,1200,1,2,4,55,100,6,800]

buble(array)

print('Arreglo ordenado: ')

for i in range(len(array)):
    print(array[i])
```