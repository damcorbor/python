# Chuleta – Listas en Python

## Qué es una lista
- Estructura ordenada
- Permite duplicados
- Es mutable

```python
numbers = [1, 2, 3]
empty = []
```

---

## Crear listas
```python
languages = ['Python', 'Ruby', 'JavaScript']

data = ['Tenerife', 3718, {'temp': 24}]
```

---

## Convertir a lista
```python
list('Python')        # ['P','y','t','h','o','n']
list(range(5))        # [0,1,2,3,4]
```

---

## Acceder a elementos
```python
shopping = ['Agua', 'Huevos', 'Aceite']

shopping[0]
shopping[1]
shopping[-1]
```

---

## Trocear listas (slicing)
```python
shopping = ['Agua', 'Huevos', 'Aceite', 'Sal', 'Limón']

shopping[:3]
shopping[2:4]
shopping[::-1]
```

---

## Invertir una lista
```python
shopping[::-1]
list(reversed(shopping))
```

---

## Añadir elementos
```python
shopping.append('Atún')        # al final
shopping.insert(1, 'Jamón')    # en posición concreta
```

---

## Repetir listas
```python
shopping * 3
```

---

## Combinar listas
```python
shopping + fruitshop
```

```python
shopping.append(fruitshop)    # añade la lista como sublista
```

---

## Modificar elementos
```python
shopping[0] = 'Jugo'
```

---

## Modificar por trozos
```python
shopping[1:4] = ['Atún', 'Pasta']
```

---

## Borrar elementos
```python
del shopping[2]
shopping.clear()
```

---

## Buscar elementos
```python
shopping.index('Aceite')
```

---

## Comprobar pertenencia
```python
'Aceite' in shopping
'Pollo' in shopping
```

---

## Longitud y conteo
```python
len(shopping)
shopping.count('Agua')
```

---

## Strings y listas
```python
text.split()
text.split(',')

','.join(shopping)
```

---

## Ordenar listas
```python
sorted(shopping)
sorted(shopping, reverse=True)
```

---

## Recorrer listas
```python
for item in shopping:
    print(item)
```

```python
for i, item in enumerate(shopping):
    print(i, item)
```

---

## Recorrer varias listas
```python
for a, b in zip(lista1, lista2):
    print(a, b)
```

---

## Comparar listas
```python
[1, 2, 3] < [1, 2, 4]
```

---

## Copias de listas
```python
b = a          # NO copia
b = a.copy()   # copia real
```

---

## all() y any()
```python
all([True, True, False])
any([False, False, True])

all([])
any([])
```

---

## Listas por comprensión
```python
[int(x) for x in values.split(',')]

[x for x in nums if x > 10]
```

---

## sys.argv
```python
import sys

sys.argv
sys.argv[1:]
```

---

## Funciones matemáticas
```python
sum(lista)
max(lista)
min(lista)
```

---

## Listas de listas
```python
team = [goalkeeper, defenders, midfielders]

team[1][0]
```
