# Chuleta – Cadenas de texto en Python (strings)

## Qué es un string
- Secuencia de caracteres
- Ordenada
- Inmutable (no se puede modificar directamente)
- Usa Unicode (Python 3)

```python
text = 'Hola'
name = "Python"
empty = ''
```

---

## Crear strings

```python
s1 = 'texto con comillas simples'
s2 = "texto con comillas dobles"
```

### Comillas dentro de strings

```python
'Los "strings" son texto'
"Los 'strings' son texto"
```

---

## Strings multilínea (triples)

```python
poem = """To be, or not to be
that is the question"""
```

- Se usan sobre todo para textos largos y docstrings
- Por convención: triples comillas dobles

---

## Conversión de tipos

```python
str(10)        # '10'
str(True)      # 'True'
str(3.14)      # '3.14'
```

```python
int('10')      # 10
float('3.14')  # 3.14
```

```python
int('FF', 16)  # 255 (hexadecimal)
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
print(msg)
```

---

## Raw strings (texto en crudo)

```python
text = r'abc\ndef'
print(text)
```

- No interpreta \n, \t, etc.
- Muy usado en rutas y expresiones regulares

---

## print() avanzado

```python
print(a, b)                 # espacio por defecto
print(a, b, sep='|')        # separador personalizado
print(a, end='!!')          # sin salto de línea
```

---

## Leer datos del teclado

```python
name = input('Nombre: ')
age = input('Edad: ')
```

- input() siempre devuelve string
- No llames `input` a una variable

---

## Operaciones con strings

### Concatenar

```python
'Hola ' + 'Mundo'
```

### Repetir

```python
'Hi! ' * 3
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
word[0] = 'J'  # error (inmutable)
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

- El final no se incluye

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
'C' not in 'ATGAA'
```

---

## Limpiar strings

```python
text = '  hola \n'
text.strip()
```

```python
text.lstrip()
text.rstrip()
```

```python
text.strip('\n ')
```

---

## Buscar texto

```python
text = 'Hola mundo hola'
```

```python
text.find('hola')
text.index('hola')
```

```python
text.startswith('Hola')
text.endswith('hola')
```

```python
text.find('hola', 5)
text.find('hola', 5, 15)
```

---

## Buscar desde la derecha

```python
text.rfind('hola')
text.rindex('hola')
```

---

## Contar ocurrencias

```python
text.count('hola')
```

---

## Reemplazar texto

```python
text.replace('hola', 'hey')
```

```python
text.replace('hola', 'hey', 1)
```

---

## Mayúsculas y minúsculas

```python
s.capitalize()
s.title()
s.upper()
s.lower()
s.swapcase()
```

---

## Identificar caracteres

```python
'R2D2'.isalnum()
'ABC'.isalpha()
'123'.isdigit()
'ABC'.isupper()
'abc'.islower()
```

---

## f-strings

```python
name = 'Leia'
age = 22

f'Me llamo {name} y tengo {age}'
```

```python
f'{age * 2}'
f'{{ valor = {age} }}'
```

---

## Formateo con f-strings

```python
n = 42
f'{n:5d}'
f'{n:05d}'
```

```python
pi = 3.14159
f'{pi:.2f}'
```

```python
f'{n:x}'
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
print(f'{name!r}')
```

---

## Unicode

```python
ord('A')
chr(65)
```

```python
'\N{ROCKET}'
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
text.split(',')
```

```python
','.join(['a', 'b', 'c'])
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
