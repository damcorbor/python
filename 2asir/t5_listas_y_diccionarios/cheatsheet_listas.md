# Chuleta – Listas en Python

## Que es una lista
- Estructura ordenada
- Permite duplicados
- Es mutable (se puede cambiar)

```python
numbers = [1, 2, 3]   # lista normal de numeros
empty = []            # lista vacia
```

---

## Crear listas
```python
languages = ['Python', 'Ruby', 'JavaScript']   # lista de strings

data = ['Tenerife', 3718, {'temp': 24}]        # mezcla de datos
```

---

## Convertir a lista
```python
list('Python')     # ['P','y','t','h','o','n']
list(range(5))     # [0,1,2,3,4]
```

---

## Acceder a elementos
```python
shopping = ['Agua', 'Huevos', 'Aceite']

shopping[0]     # primer elemento
shopping[1]     # segundo
shopping[-1]    # ultimo
```

---

## Trocear listas (slicing)
```python
shopping = ['Agua', 'Huevos', 'Aceite', 'Sal', 'Limon']

shopping[:3]        # primeros 3
shopping[2:4]       # del indice 2 al 3
shopping[::-1]      # lista al reves
```

---

## Invertir una lista
```python
shopping[::-1]           # devuelve la lista invertida
list(reversed(shopping)) # lo mismo pero con reversed
```

---

## Anadir elementos
```python
shopping.append('Atun')      # anade al final
shopping.insert(1, 'Jamon')  # mete en una posicion concreta
```

---

## Repetir listas
```python
shopping * 3   # repite la lista 3 veces
```

---

## Combinar listas
```python
shopping + fruitshop   # une dos listas y crea una nueva
```

```python
shopping.append(fruitshop)
# mete la lista entera como un solo elemento (ojo)
```

---

## Modificar elementos
```python
shopping[0] = 'Jugo'   # cambia el primer elemento
```

---

## Modificar por trozos
```python
shopping[1:4] = ['Atun', 'Pasta']
# cambia varios valores de golpe
```

---

## Borrar elementos
```python
del shopping[2]    # borra el elemento del indice 2
shopping.clear()   # vacia toda la lista
```

---

## Buscar elementos
```python
shopping.index('Aceite')
# devuelve el indice donde esta
```

---

## Comprobar si existe
```python
'Aceite' in shopping   # True
'Pollo' in shopping    # False
```

---

## Longitud y conteo
```python
len(shopping)              # numero de elementos
shopping.count('Agua')     # cuantas veces aparece
```

---

## Strings y listas
```python
text.split()        # separa por espacios
text.split(',')     # separa por comas
```

```python
','.join(shopping)  # une la lista en un string
```

---

## Ordenar listas
```python
sorted(shopping)                 # orden normal
sorted(shopping, reverse=True)   # orden inverso
```

---

## Recorrer listas
```python
for item in shopping:
    print(item)
# recorre uno a uno
```

```python
for i, item in enumerate(shopping):
    print(i, item)
# muestra indice y valor
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
# True porque 3 es menor que 4
```

---

## Copias de listas
```python
b = a
# no copia, apuntan a la misma lista
```

```python
b = a.copy()
# copia real
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

## Listas por comprension
```python
[int(x) for x in values.split(',')]
# convierte todo a int
```

```python
[x for x in nums if x > 10]
# solo coge los mayores de 10
```

---

## sys.argv
```python
import sys

sys.argv
# argumentos del programa
```

```python
sys.argv[1:]
# sin el nombre del script
```

---

## Funciones matematicas
```python
sum(lista)   # suma
max(lista)   # maximo
min(lista)   # minimo
```

---

## Listas de listas
```python
team = [goalkeeper, defenders, midfielders]

team[1][0]
# accede a una sublista
```
