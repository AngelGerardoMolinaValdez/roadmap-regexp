# Uso de caracteres comunes y especiales 📚

### Caracteres Comunes
   - Representan a sí mismos y no tienen un significado especial en la sintaxis de regex.
   - Ejemplos: Letras (`A`, `b`, `c`) y números (`1`, `2`, `3`).
   - En una expresión regular, estos caracteres coincidirán directamente con ellos mismos en el texto. Por ejemplo, `abc` coincidirá con la secuencia exacta 'abc'.

### Caracteres Especiales o Metacaracteres
   - Tienen un propósito específico y realizan funciones especiales en la expresión regular.
   - Ejemplos comunes incluyen:
     - `.`: Coincide con cualquier carácter excepto una nueva línea. Por ejemplo, la expresión `ventajos.s` coincidirá con "ventajosos", "ventajosas" o cualquier carácter que haya.
     - `^`: Indica el inicio de una línea. Por ejemplo, la expresión `^Hola mundo` coincidirá con "Hola mundo" pero no con "hola mundo" (y eso solo aplicara si la linea inicia con "Hola mundo")
     - `$`: Representa el final de una línea. Volviendo al ejemplo anterior si usamos la regex `mundo$` coincidirá con "Hola mundo", "Adios mundo", pero no con "Hola mundos".
     - `\`: Se utiliza como carácter de escape para dar a los metacaracteres un significado literal o para señalar secuencias especiales. Por ejemplo el regex `Hola.` coincidirá con "Hola.", "Hola?", "Holaa", "Hola!", pero con la siguiente regex `Hola\.` solo coincidirá con "Hola." porque se esta cancelando con backslash el carácter *.*.

### Secuencias Especiales
   - Representadas por un backslash seguido de otro carácter, tienen un significado especial.
   - Ejemplos:
     - `\d`: Coincide con cualquier dígito numérico (equivalente a `[0-9]`).
     - `\D`: Coincide con cualquier dígito que no sea numérico (equivalente a `[^0-9]`).
     - `\w`: Coincide con cualquier carácter alfanumérico (equivalente a `[a-zA-Z0-9_]`).
     - `\W`: Coincide con cualquier carácter que no sea alfanumérico (equivalente a `[^a-zA-Z0-9_]`).
     - `\s`: Coincide con cualquier espacio en blanco (espacios, tabulaciones, saltos de línea).
     - `\S`: Coincide con cualquier carácter que no sea espacio en blanco.
    - Los caracteres de secuencia tienen su función antagónica colocando el mismo carácter pero en mayúsculas.

### Uso de Caracteres de Escape
   - Los caracteres de escape (`\`) se utilizan para suprimir el significado especial de un metacarácter.
   - Por ejemplo, para buscar un punto en un texto, se utiliza `\.` ya que `.` solo coincidirá con cualquier carácter.

### Uso Práctico
   - Estos caracteres son fundamentales para construir patrones en expresiones regulares.
   - Permiten desde búsquedas simples (coincidir con caracteres específicos) hasta búsquedas complejas (identificar patrones como direcciones de correo electrónico, URLs, códigos postales, etc.).

---

## Referencias 🌐

- [Python 3.12.1 Documentation - Regular Expression Operations](https://docs.python.org/3/library/re.html)
- [.NET - Regular Expression Language - Quick Reference](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference)
- [Python 3.12.1 Documentation - Regular Expression HOWTO](https://docs.python.org/3/howto/regex.html)
- [MDN Web Docs - JavaScript Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

---

### [Ir al cuestionario 📝](../../cuestionario/02-caracteres-y-clases/caracteres-comunes-y-especiales.md)

### [Ir al temario 🔍](../../readme.md)