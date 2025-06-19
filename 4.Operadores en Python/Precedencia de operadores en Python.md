
# Precedencia de operadores en Python

La **precedencia de operadores en Python** es el orden en que se evalúan los operadores en una expresión. Cuando una expresión contiene varios operadores, Python usa reglas de precedencia para decidir qué operaciones hacer primero.

```python
### Ejemplo básico:
`resultado = 3 + 4 * 2 print(resultado)`
```

**¿Qué pasa aquí?**  
Aunque la suma está antes, Python primero hace la **multiplicación** (`4 * 2 = 8`) y luego la **suma** (`3 + 8 = 11`) porque `*` tiene mayor **precedencia** que `+`.

### 🔢 Tabla resumida de precedencia (de mayor a menor):

|Nivel|Operadores|Descripción|
|---|---|---|
|1|`()`|Paréntesis|
|2|`**`|Potencia|
|3|`+x`, `-x`, `~x`|Unarios: positivo, negativo, complemento bit a bit|
|4|`*`, `/`, `//`, `%`|Multiplicación, división, módulo|
|5|`+`, `-`|Suma y resta|
|6|`<<`, `>>`|Desplazamiento de bits|
|7|`&`|AND bit a bit|
|8|`^`|XOR bit a bit|
|9|`|`|
|10|`==`, `!=`, `>`, `<`, `>=`, `<=`, `is`, `is not`, `in`, `not in`|Comparaciones|
|11|`not`|Lógico NOT|
|12|`and`|Lógico AND|
|13|`or`|Lógico OR|
|14|`=`, `+=`, `-=`, `*=`, etc.|Asignación|


