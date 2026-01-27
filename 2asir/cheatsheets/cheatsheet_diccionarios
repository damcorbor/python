# Chuleta – Diccionarios en Python

## Qué es un diccionario
- Estructura indexada por claves
- Mantiene el orden de inserción
- Es mutable (se puede cambiar)
- Las claves son únicas
- Acceso muy rápido (hash)

    rae = {
        'bifronte': 'De dos frentes o dos caras',
        'anarcoide': 'Que tiende al desorden'
    }

---

## Características importantes
- Claves: tipos inmutables (str, int, float, tuple…)
- Valores: cualquier tipo
- No permite claves duplicadas
- Internamente usa hashes

---

## Crear diccionarios

    rae = {
        'bifronte': 'De dos frentes o dos caras',
        'anarcoide': 'Que tiende al desorden',
        'montuvio': 'Campesino de la costa'
    }

    population_can = {
        2015: 2_135_209,
        2016: 2_154_924,
        2017: 2_177_048,
        2018: 2_206_901,
        2019: 2_220_270
    }

    empty_dict = {}

---

## Ejercicio típico
Crea un diccionario con 5 nombres (claves) de tu familia y sus edades (valores).

---

## Convertir a diccionario con dict()
Funciona con cualquier iterable de “pares” (2 cosas: clave y valor).

    dict(['a1', 'b2'])
    # {'a': '1', 'b': '2'}

---

## Crear diccionarios con dict() (sin llaves)

    person = dict(
        name='Guido',
        surname='van Rossum',
        job='Python creator'
    )

Ojo: las claves deben ser identificadores válidos (sin espacios).

---

## Crear con relleno (fromkeys)
Mismas claves, mismo valor inicial.

    dict.fromkeys(['portátil', 'nevera', 'ventilador', 'monitor'], 0)

Se puede aplicar sobre cualquier iterable.

---

## Obtener un elemento (acceso)
Acceder por clave con corchetes.

    rae['anarcoide']

Si la clave no existe -> KeyError

---

## Usar get() (evita KeyError)

    rae.get('bifronte')                 # si existe, devuelve valor
    rae.get('programación')             # si no existe, devuelve None
    rae.get('programación', 'No disponible')  # valor por defecto

---

## Añadir o modificar un elemento

    rae['enjuiciar'] = 'Someter una cuestión a examen, discusión y juicio'

- Si la clave existe -> modifica
- Si la clave no existe -> añade

---

## Patrón creación (empezar vacío y rellenar)

    VOWELS = 'aeiou'
    cvowels = {}

    for vowel in VOWELS:
        cvowels[vowel] = ord(vowel)

---

## Comprobar si existe una clave (pertenencia)

    'bifronte' in rae        # True / False
    'almohada' in rae        # True / False
    'montuvio' not in rae    # True / False

---

## Longitud del diccionario

    len(rae)

---

## Obtener claves, valores y pares

    rae.keys()     # claves
    rae.values()   # valores
    rae.items()    # pares (clave, valor)

---

## Iterar diccionarios

Iterar claves (por defecto):

    for word in rae:
        print(word)

Iterar claves explícito:

    for word in rae.keys():
        print(word)

Iterar valores:

    for value in rae.values():
        print(value)

Iterar claves y valores:

    for k, v in rae.items():
        print(k, v)

---

## Borrar elementos

Por clave:

    del rae['bifronte']

Borrar todo:

    rae.clear()

Borrar todo reasignando:

    rae = {}

---

## Combinar diccionarios
Regla: si una clave se repite, gana el último diccionario.

    rae1 | rae2     # devuelve uno nuevo (no modifica originales)
    rae1 |= rae2    # modifica rae1

---

## Cuidado con las copias (mutabilidad)

    copy_rae = original_rae
    # NO copia: apuntan al mismo diccionario

Copia real (copia “dura”):

    copy_rae = original_rae.copy()

---

## Diccionarios por comprensión

    words = ('sun', 'space', 'rocket', 'earth')

    words_length = {word: len(word) for word in words}

Con condición:

    words_length = {w: len(w) for w in words if w[0] not in 'aeiou'}

---

## Objetos hashables (claves válidas)
Para ser clave debe ser “hashable” (su hash no cambia).

    hash(999)
    hash(3.14)
    hash('hello')
    hash(('a', 'b', 'c'))

Listas NO (son mutables):

    hash(['a', 'b', 'c'])
    # unhashable type: 'list'

---

## Regla final
- Claves: inmutables (str, int, float, tuple, etc.)
- Valores: lo que sea
- Orden: se mantiene el de inserción
- Mutables: se pueden modificar, añadir, borrar
  
