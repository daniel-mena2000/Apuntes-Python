
# else y finally

```python
resultado = None
try:
    a = int(input('Primer número: '))
    b = int(input('Segundo número: '))
    resultado = a / b

except ZeroDivisionError as e:
    print(f'Error: {e}')
except TypeError as e:
    print(f'Error: {e}')
# else se ejecuta solo si no ocurrio ninguna excepcion
else:
    print('No se arrojo ninguna excepcion')
#Finally se va a lanzar incluso si hay una excepcion
finally:
    print('Ejecucion del bloque finally')

print(f'Resultado: {resultado}')
```