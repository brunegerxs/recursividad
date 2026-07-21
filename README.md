# recursividad
## 🔢 Factorial (Explicación para Programadores)

El **factorial** de un número entero positivo $n$ (denotado como `n!`) es el producto de todos los enteros positivos desde $1$ hasta $n$.

En programación, el factorial es el ejemplo fundamental para entender conceptos clave como **iteración**, **recursividad** y la importancia del **caso base**.

---

### 💡 Ejemplo Matemático
* `5! = 5 × 4 × 3 × 2 × 1 = 120`
* `0! = 1` *(por definición)*

---

### 🛠️ Implementación en Código (Python)

#### 1. Enfoque Iterativo (Bucle)
Ideal para optimizar el rendimiento y evitar consumo excesivo de la pila de llamadas (*call stack*).

```python
def factorial_iterativo(n: int) -> int:
    if n < 0:
        raise ValueError("El factorial no está definido para números negativos.")
    
    resultado = 1
    for i in range(1, n + 1):
        resultado *= i
    return resultado
