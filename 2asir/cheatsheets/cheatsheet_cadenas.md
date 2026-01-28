# Chuleta – Cadenas de texto en Python (strings)

## Qué es un string
- Secuencia de caracteres
- Ordenada
- Inmutable (no se puede modificar directamente)
- Usa Unicode (Python 3)

```python
text = 'Hola'        # string con texto
name = "Python"     # string con comillas dobles
empty = ''          # string vacío
```

---

## Crear strings

```python
s1 = 'texto con comillas simples'
s2 = "texto con comillas dobles"
```

### Comillas dentro de strings

```python
'Los "strings" son texto'   # comillas dobles dentro
"Los 'strings' son texto"   # comillas simples dentro
```

---

## Strings multilínea (triples)

```python
poem = """To be, or not to be
that is the question"""
```

- Se usan para textos largos
- También para docstrings
- Por convención: triples comillas dobles

---

## Conversión de tipos

```python
str(10)        # convierte a string → '10'
str(True)      # convierte a string → 'True'
str(3.14)      # convierte a string → '3.14'
```

```python
int('10')      # convierte a entero → 10
float('3.14')  # convierte a float → 3.14
```

```python
int('FF', 16)  # hexadecimal a decimal → 255
```

---

## Secuencias de escape

```python
'\n'  # salto de línea
'\t'  # tabulación
'\''  # comilla simple
'\\'  # barra invertida
```

```python
msg = 'Linea 1\nLinea 2'
print(msg)     # imprime en dos líneas
```

---

## Raw strings (texto en crudo)

```python
text = r'abc\ndef'
print(text)    # no interpreta \n
```

- No interpreta caracteres especiales
- Muy usado en rutas y regex

---

## print() avanzado

```python
print(a, b)                 # separa con espacio
print(a, b, sep='|')        # separador personalizado
print(a, end='!!')          # sin salto de línea
```

---

## Leer datos del teclado

```python
name = input('Nombre: ')    # siempre devuelve string
age = input('Edad: ')
```

- input() siempre devuelve string
- No usar input como nombre de variable

---

## Operaciones con strings

### Concatenar

```python
'Hola ' + 'Mundo'   # une strings
```

### Repetir

```python
'Hi! ' * 3          # repite el texto
```

---

## Índices

```python
word = 'Python'

word[0]   # 'P'
word[1]   # 'y'
word[-1]  # 'n'
```

```python
word[0] = 'J'  # error → string inmutable
```

---

## Trocear strings (slicing)

```python
word = 'Python'

word[0:3]   # 'Pyt'
word[:4]    # 'Pyth'
word[2:]    # 'thon'
word[::-1]  # 'nohtyP'
```

- El índice final no se incluye

---

## Longitud

```python
len('Hola')   # 4
len('')       # 0
```

---

## Comprobar pertenencia

```python
'sol' in 'girasol'      # True
'luna' in 'girasol'     # False
```

```python
'C' not in 'ATGAA'      # comprueba ausencia
```

---

## Limpiar strings

```python
text = '  hola \n'
text.strip()            # elimina espacios y saltos
```

```python
text.lstrip()           # izquierda
text.rstrip()           # derecha
```

```python
text.strip('\n ')       # elimina caracteres indicados
```

---

## Buscar texto

```python
text = 'Hola mundo hola'
```

```python
text.find('hola')       # índice o -1
text.index('hola')      # índice o error
```

```python
text.startswith('Hola') # True / False
text.endswith('hola')   # True / False
```

```python
text.find('hola', 5)
text.find('hola', 5, 15)
```

---

## Buscar desde la derecha

```python
text.rfind('hola')      # busca desde el final
text.rindex('hola')     # error si no existe
```

---

## Contar ocurrencias

```python
text.count('hola')      # número de veces
```

---

## Reemplazar texto

```python
text.replace('hola', 'hey')     # reemplaza todas
```

```python
text.replace('hola', 'hey', 1)  # solo la primera
```

---

## Mayúsculas y minúsculas

```python
s.capitalize()   # primera letra mayúscula
s.title()        # cada palabra
s.upper()        # todo mayúsculas
s.lower()        # todo minúsculas
s.swapcase()     # intercambia
```

---

## Identificar caracteres

```python
'R2D2'.isalnum()   # letras y números → True
'ABC'.isalpha()   # solo letras
'123'.isdigit()   # solo números
'ABC'.isupper()   # mayúsculas
'abc'.islower()   # minúsculas
```

---

## f-strings

```python
name = 'Leia'
age = 22

f'Me llamo {name} y tengo {age}'
```

```python
f'{age * 2}'          # evalúa expresión
f'{{ valor = {age} }}'  # llaves literales
```

---

## Formateo con f-strings

```python
n = 42
f'{n:5d}'     # ancho 5
f'{n:05d}'    # relleno con ceros
```

```python
pi = 3.14159
f'{pi:.2f}'   # dos decimales
```

```python
f'{n:x}'      # hexadecimal
```

---

## Modo debug (Python 3.8+)

```python
f'{name=}'
f'{age=}'
f'{age * 2=}'
```

---

## Representación interna (!r)

```python
name = 'Steven'
print(f'{name!r}')   # representación real
```

---

## Unicode

```python
ord('A')    # 65
chr(65)     # 'A'
```

```python
'\N{ROCKET}'  # 🚀
```

---

## Comparar strings

```python
'arca' < 'arpa'
'a' < 'antes'
'A' < 'a'
```

---

## Strings y listas

```python
text = 'uno,dos,tres'
text.split(',')   # divide en lista
```

```python
','.join(['a', 'b', 'c'])  # une lista
```

---

## Resumen rápido

```python
len(s)
'x' in s
s.strip()
s.find('x')
s.replace(a, b)
s.upper()
s.lower()
s[::-1]
```

> Los strings son inmutables: cualquier cambio crea un string nuevo
