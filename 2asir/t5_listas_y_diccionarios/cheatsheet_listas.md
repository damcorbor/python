# 🧠 Chuleta – Listas en Python

## Qué es una lista
- Estructura ordenada
- Permite duplicados
- Es mutable (se puede modificar)

```python
# ejemplos básicos
numbers = [1, 2, 3]
empty = []
```

---

## Crear listas
- Se usan corchetes []
- Elementos separados por comas
- Pueden mezclar tipos de datos

```python
data = ['Tenerife', 3718, {'temp': 24}]
```

---

## Convertir a lista
```python
# string a lista
list('Python')

# rango a lista
list(range(5))
```

---

## Acceder a elementos
```python
shopping = ['Agua', 'Huevos', 'Aceite']

shopping[0]     # primer elemento
shopping[-1]    # último elemento
```

⚠️ Índices fuera de rango dan error

---

## Trocear listas (slicing)
```python
# formato general
lista[inicio:fin:paso]

shopping[:3]        # primeros 3
shopping[2:4]       # del índice 2 al 3
shopping[::-1]      # invertir lista
```

📌 El slicing NO modifica la lista original

---

## Invertir una lista
```python
# sin modificar la original
shopping[::-1]

# creando nueva lista
list(reversed(shopping))
```

---

## Añadir elementos
```python
# al final (recomendado)
shopping.append('Atún')

# en una posición concreta
shopping.insert(1, 'Jamón')
```

❗ Para añadir al final usa siempre append()

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

⚠️ Ojo:
```python
shopping.append(fruitshop)  # mete la lista como sublista
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
# borrar por índice
del shopping[2]

# vaciar lista
shopping.clear()
```

---

## Buscar elementos
```python
shopping.index('Aceite')  # devuelve el índice
```

⚠️ Si no existe → error  
⚠️ Si hay varios iguales → solo devuelve el primero

---

## Comprobar pertenencia
```python
'Aceite' in shopping   # True
'Pollo' in shopping    # False
```

---

## Longitud y conteo
```python
len(shopping)              # número de elementos
shopping.count('Agua')     # cuántas veces aparece
```

---

## Strings y listas
```python
# dividir string
text.split()
text.split(',')

# unir lista en string
','.join(shopping)
```

⚠️ join() solo funciona con strings

---

## Ordenar listas
```python
sorted(shopping)                   # nueva lista
sorted(shopping, reverse=True)     # orden inverso
```

---

## Recorrer listas
```python
for item in shopping:
    print(item)
```

### Con índice
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

📌 Se para en la lista más corta

---

## Comparar listas
```python
[1, 2, 3] < [1, 2, 4]
```

Comparación elemento a elemento (como strings)

---

## Copias de listas
```python
# NO es copia
b = a

# copia real
b = a.copy()
```

---

## all() y any()
```python
all([True, True, False])   # False
any([False, False, True]) # True
```

⚠️ Lista vacía:
```python
all([])  # True
any([])  # False
```

---

## Listas por comprensión
```python
# forma corta
[int(x) for x in values.split(',')]

# con condición
[x for x in nums if x > 10]
```

---

## sys.argv
```python
import sys

sys.argv       # todos los argumentos
sys.argv[1:]   # sin el nombre del script
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

team[1][0]   # acceder a sublista
```

---

## Idea clave final
- Las listas se usan todo el rato
- Son mutables → cuidado con copias
- append, in, len y sorted son básicos
