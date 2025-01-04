### 1. siendo n un número, imprime los números desde el 1 hasta n
```python
# Resultado esperado

# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
# 11
# 12
# ... hasta llegar a n
```
### 2. Imprime los elementos de una lista
> [!NOTE]
>   Puedes usar la funcion len() para saber el número de elementos dentro de una lista

> [!WARNING]
>   si intentas acceder a un elemento que excede el rango de la lista se generara un error.
```python
nombres = ["Camilo", "Maria", "Fernando"] # indices 0 1 2 

# --- Ejemplo len() ---
len(nombres) # Devuelve 3, siendo ese el número de elementos dentro de la lista nombres

# Recuerda que puedes asignar ese valor a variable o usarlo directamente

n = len(nombres) # Ejemplo asignando el valor a n
if 5 > len(nombres): # Ejemplo usando el valor directamente para la operacion 5 > len(nombres)

# --- Ejemplo error ---
nombres[3] # Genera error al exceder el rango de la lista (indice maximo 2)
```
```python
# Resultado esperado

lista = ["elemento1","elemento2","elemento3","elemento4"]
# elemento1
# elemento2
# elemento3
# elemento4
```
### 3. Calcula el factorial de un número n
Para un número n calcular el factorial , siendo factorial la forma n! = 1 * 2 * 3 * ... * n , recuerda que si n == 0 entonces n! = 1
```python
# Ejemplos de resultados esperados

# Para n == 3, resultado -> 6
# Para n == 4, resultado -> 24
# Para n == 0, resultado -> 1
```
