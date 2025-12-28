# Chuleta – Listas en Python

## Qué es una lista
- Estructura ordenada
- Permite duplicados
- Es mutable (se puede modificar)

```python
numbers = [1, 2, 3]     # lista de números
empty = []              # lista vacía
```

---

## Crear listas
```python
languages = ['Python', 'Ruby', 'JavaScript']   # lista de strings

data = ['Tenerife', 3718, {'temp': 24}]        # lista con tipos mezclados
```

---

## Convertir a lista
```python
list('Python')      # ['P', 'y', 't', 'h', 'o', 'n']
list(range(5))      # [0, 1, 2, 3, 4]
```

---

## Acceder a elementos
```python
shopping = ['Agua', 'Huevos', 'Aceite']

shopping[0]     # 'Agua' (primer elemento)
shopping[1]     # 'Huevos'
shopping[-1]    # 'Aceite' (último elemento)
```

---

## Trocear listas (slicing)
```python
shopping = ['Agua', 'Huevos', 'Aceite', 'Sal', 'Limón']

shopping[:3]        # ['Agua', 'Huevos', 'Aceite']
shopping[2:4]       # ['Aceite', 'Sal']
shopping[::-1]      # ['Limón', 'Sal', 'Aceite', 'Huevos', 'Agua']
```

---

## Invertir una lista
```python
shopping[::-1]              # devuelve una lista invertida
list(reversed(shopping))    # lo mismo, usando reversed()
```

---

## Añadir elementos
```python
shopping.append('Atún')     # añade al final de la lista
```

```python
shopping.insert(1, 'Jamón') # inserta 'Jamón' en el índice 1
```

---

## Repetir listas
```python
shopping * 3
# repite los elementos 3 veces
```

---

## Combinar listas
```python
shopping + fruitshop
# une dos listas y devuelve una nueva
```

```python
shopping.append(fruitshop)
# añade la lista entera como un solo elemento (sublista)
```

---

## Modificar elementos
```python
shopping[0] = 'Jugo'
# reemplaza 'Agua' por 'Jugo'
```

---

## Modificar por trozos
```python
shopping[1:4] = ['Atún', 'Pasta']
# reemplaza varios elementos de golpe
```

---

## Borrar elementos
```python
del shopping[2]
# borra el elemento del índice 2
```

```python
shopping.clear()
# vacía completamente la lista
```

---

## Buscar elementos
```python
shopping.index('Aceite')
# devuelve el índice donde está 'Aceite'
```

---

## Comprobar pertenencia
```python
'Aceite' in shopping    # True
'Pollo' in shopping     # False
```

---

## Longitud y conteo
```python
len(shopping)
# número total de elementos
```

```python
shopping.count('Agua')
# cuántas veces aparece 'Agua'
```

---

## Strings y listas
```python
text.split()
# divide el string por espacios
```

```python
text.split(',')
# divide usando la coma como separador
```

```python
','.join(shopping)
# une la lista en un string separado por comas
```

---

## Ordenar listas
```python
sorted(shopping)
# devuelve la lista ordenada alfabéticamente
```

```python
sorted(shopping, reverse=True)
# orden inverso
```

---

## Recorrer listas
```python
for item in shopping:
    print(item)
# recorre y muestra cada elemento
```

```python
for i, item in enumerate(shopping):
    print(i, item)
# muestra índice y valor
```

---

## Recorrer varias listas
```python
for a, b in zip(lista1, lista2):
    print(a, b)
# recorre dos listas a la vez
```

---

## Comparar listas
```python
[1, 2, 3] < [1, 2, 4]
# True, porque 3 < 4
```

---

## Copias de listas
```python
b = a
# NO copia, ambas variables apuntan a la misma lista
```

```python
b = a.copy()
# copia real de la lista
```

---

## all() y any()
```python
all([True, True, False])   # False
any([False, False, True]) # True
```

```python
all([])   # True
any([])   # False
```

---

## Listas por comprensión
```python
[int(x) for x in values.split(',')]
# convierte todos los valores a int
```

```python
[x for x in nums if x > 10]
# solo incluye valores mayores que 10
```

---

## sys.argv
```python
import sys

sys.argv
# lista con los argumentos del programa
```

```python
sys.argv[1:]
# argumentos sin el nombre del script
```

---

## Funciones matemáticas
```python
sum(lista)   # suma de los elementos
max(lista)   # valor máximo
min(lista)   # valor mínimo
```

---

## Listas de listas
```python
team = [goalkeeper, defenders, midfielders]

team[1][0]
# accede al primer elemento de la segunda sublista
```
