
# Selection Sort

El **selection sort** (ordenamiento por selección) es otro algoritmo clásico y sencillo para ordenar listas. Igual que el burbuja, se estudia sobre todo con fines educativos, porque es **ineficiente para listas grandes**.

## 🔹 Idea principal

1. Dividimos la lista en dos partes: **ordenada** (al inicio) y **no ordenada** (el resto).
    
2. En cada iteración:
    
    - Buscamos el **mínimo** (o máximo, si ordenamos de mayor a menor) en la parte **no ordenada**.
        
    - Lo colocamos al inicio de la parte **no ordenada**, intercambiándolo con el elemento que está ahí.
        
3. Repetimos hasta que toda la lista esté ordenada.

## 🔹 Ejemplo paso a paso

Lista: `[64, 25, 12, 22, 11]`

- Primera pasada → el mínimo es `11`, lo colocamos al inicio: `[11, 25, 12, 22, 64]`
    
- Segunda pasada → el mínimo de lo que queda `[25, 12, 22, 64]` es `12`: `[11, 12, 25, 22, 64]`
    
- Tercera pasada → el mínimo de `[25, 22, 64]` es `22`: `[11, 12, 22, 25, 64]`
    
- Cuarta pasada → ya está ordenado.


👉 En resumen:

- **Más eficiente que burbuja en cuanto a intercambios** (menos swaps).
    
- **Igual de lento en comparación de tiempo total**.
    
- Se usa solo en enseñanza, no en producción.