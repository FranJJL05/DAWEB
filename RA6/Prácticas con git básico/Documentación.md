# Documentación de Código en Entornos de Desarrollo Web (Python, JavaScript, PHP)

La documentación es esencial, no solo para los usuarios finales (documentación de API), sino sobre todo para los desarrolladores.

---

## Claves de una Buena Documentación

- **Consistencia:** Usar siempre el mismo formato y estilo.  
- **Claridad:** Explicar qué hace, qué espera (parámetros) y qué devuelve el elemento.  
- **Ubicación:** Colocar el comentario inmediatamente antes o después de la definición del elemento que describe (función, clase, método, etc.).

---

## 1. Python: Usando Docstrings y Formato Google 🐍

En **Python**, la documentación se incluye en una cadena de texto de triple comilla (`"""Docstring"""`) justo después de la definición de la función o clase.

### Convención (Formato Google)
Se utiliza el formato **Google** o **reStructuredText** (compatible con **Sphinx**).  
Aquí nos enfocamos en la estructura básica de Google:

| Etiqueta   | Propósito                                    |
|------------|----------------------------------------------|
| **Resumen** | Qué hace la función (una línea).             |
| **Args:**   | Lista los parámetros y sus tipos.            |
| **Returns:**| Describe el valor de retorno y su tipo.      |

### Ejemplo Simplificado

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
