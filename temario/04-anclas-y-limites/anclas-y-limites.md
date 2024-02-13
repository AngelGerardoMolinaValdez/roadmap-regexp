# Anclas y Límites de Palabras en Expresiones Regulares 📚

Las anclas y los límites de palabras son metacaracteres que no coinciden con caracteres, sino con posiciones dentro de la cadena de texto. Son esenciales para realizar búsquedas basadas en la posición de los patrones. A continuación, se explica el uso de `^`, `$`, `\b`, y `\B`.

**1. `^` - Inicio de la Cadena o Línea:**
   - El metacarácter `^` se utiliza para coincidir con la posición al inicio de la cadena de texto, o al inicio de una línea si se utiliza la bandera de múltiples líneas.
   - **Ejemplo:** `^Hola` coincide con "Hola" solo si "Hola" está al inicio de la cadena de texto.

**2. `$` - Fin de la Cadena o Línea:**
   - El metacarácter `$` se utiliza para coincidir con la posición al final de la cadena de texto, o al final de una línea en el modo de múltiples líneas.
   - **Ejemplo:** `mundo$` coincide con "mundo" solo si "mundo" está al final de la cadena de texto.

**3. `\b` - Límite de Palabras:**
   - `\b` es una ancla que coincide con una posición que es un límite de palabras. Esto significa que coincide con una posición donde una palabra es seguida por un espacio, o viceversa, o al inicio o final de una cadena si esta comienza o termina con una palabra.
   - **Ejemplo:** `\bHola\b` coincidirá con "Hola" solo si "Hola" está aislada como una palabra.

**4. `\B` - No Límite de Palabras:**
   - `\B` es el opuesto de `\b`. Coincide con cualquier posición que no sea un límite de palabras.
   - **Ejemplo:** `\B...\B` buscaría coincidencias de tres caracteres que no estén al inicio ni al final de una palabra.

### Aplicaciones Prácticas

- **Validación de Formatos:** Usar `^` y `$` para asegurar que toda la cadena de texto cumpla con un patrón específico, como verificar formatos de correo electrónico o números de teléfono.
- **Búsqueda Sensible al Contexto:** Utilizar `\b` para buscar palabras específicas en un texto, asegurando que se encuentren aisladas y no como parte de otras palabras.
- **Patrones Dentro de Palabras:** `\B` permite buscar patrones que forman parte de una palabra, útil para análisis lingüísticos o búsqueda de raíces y prefijos.

---

## Referencias 🌐

- [.NET Regular Expressions - Anchors](https://learn.microsoft.com/en-us/dotnet/standard/base-types/anchors-in-regular-expressions) 
- [Regex Tutorial - \b Word Boundaries](https://www.regular-expressions.info/wordboundaries.html)

---

### [Ir al cuestionario 📝](../../cuestionario/04-anclas-y-limites/anclas-y-limites.md)

### [Ir al temario 🔍](../../readme.md)