# Documentación de Código en Entornos de Desarrollo Web (Python, JavaScript, PHP)

La documentación es esencial, no solo para los usuarios finales, sino sobre todo para los desarrolladores.

---

## Claves de una Buena Documentación

- **Consistencia:** Usar siempre el mismo formato y estilo.  
- **Claridad:** Explicar qué hace, qué espera (parámetros) y qué devuelve el elemento.  
- **Ubicación:** Colocar el comentario inmediatamente antes o después de la definición del elemento que describe (función, clase, método, etc.).

---

## 1. Python: Usando Docstrings y Formato Google

En **Python**, la documentación se incluye en una cadena de texto de triple comilla (`"""Docstring"""`) justo después de la definición de la función o clase.

### Convención (Formato Google)
Se utiliza el formato **Google** o **reStructuredText** (compatible con **Sphinx**).  
Aquí nos enfocamos en la estructura básica de Google:

| Etiqueta     | Propósito                               |
| ------------ | --------------------------------------- |
| **Resumen**  | Qué hace la función (una línea).        |
| **Args:**    | Lista los parámetros y sus tipos.       |
| **Returns:** | Describe el valor de retorno y su tipo. |

### Ejemplo Simple

```python
def sumar(a, b):
    """
    Suma dos números enteros.

    Args:
        a (int): El primer número.
        b (int): El segundo número.

    Returns:
        int: La suma total de los dos números.
    """
    return a + b
```

## 2. JavaScript: Usando JSDoc

En **JavaScript**, la convención más popular es **JSDoc**.  
Se utiliza un comentario multilínea especial (`/** ... */`) y etiquetas con el prefijo `@` para describir tipos y elementos.  
Esto es vital para **simular el tipado** y mejorar la inteligencia de los **IDEs**.

---

### Convención
**JSDoc** es el estándar de facto.

| Etiqueta          | Propósito                        |
| ----------------- | -------------------------------- |
| `@param {tipo} n` | Describe un parámetro y su tipo. |
| `@returns {tipo}` | Describe el valor de retorno.    |

---

### Ejemplo Simple

```javascript
/**
 * Crea un saludo personalizado.
 * @param {string} nombre El nombre de la persona a saludar.
 * @returns {string} El mensaje de saludo completo.
 */
function crearSaludo(nombre) {
    return `¡Hola, ${nombre}!`;
}
```
---

## 3. PHP: Usando PHPDoc (PSR-5)

En **PHP**, el estándar es **PHPDoc**, muy similar a **JSDoc**.  
Se usa un comentario multilínea (`/** ... */`) y etiquetas.  
Es fundamental para la **generación de documentación** con herramientas como **phpDocumentor**.

---

### Convención
El estándar está definido por la **PSR-5**.

| Etiqueta             | Propósito                                  |
|----------------------|--------------------------------------------|
| `@param tipo $nombre`| Describe un parámetro y su tipo.           |
| `@return tipo`       | Describe el valor de retorno.              |

---


---

### Ejemplo Simple

```php
class Calculadora{
    /**
     * Multiplica dos números.
     *
     * @param float $num1 El primer factor.
     * @param float $num2 El segundo factor.
     * @return float El producto total.
     */
    public function multiplicar(float $num1, float $num2): float
    {
        return $num1 * $num2;
    }
}
```