# Sintaxis Básica: Caracteres, Metacaracteres y Literales en Expresiones Regulares 📚

### Caracteres
   - En las expresiones regulares, los caracteres representan a sí mismos. Por ejemplo, `a` coincide con la letra 'a'.
   - Cualquier carácter alfanumérico (letras y números) y muchos símbolos se consideran caracteres literales.

### Metacaracteres
   - Los metacaracteres tienen un significado especial en la sintaxis de las expresiones regulares. 
   - Algunos ejemplos comunes incluyen:
     - `.`: Coincide con cualquier carácter, excepto una nueva línea.
     - `^`: Indica el inicio de una línea.
     - `$`: Indica el final de una línea.
     - `*`: Coincide con cero o más repeticiones del elemento anterior.
     - `+`: Coincide con una o más repeticiones del elemento anterior.
     - `?`: Hace que el elemento anterior sea opcional (coincide 0 o 1 vez).
     - `{n}`, `{n,}`, `{n,m}`: Cuantificadores que especifican el número de repeticiones.
     - `[...]`: Representa un conjunto de caracteres. Por ejemplo, `[abc]` coincide con 'a', 'b', o 'c'.
     - `[^...]`: Coincide con cualquier carácter que no esté en el conjunto especificado.
     - `|`: Operador de alternancia, funciona como un "OR" lógico.

### Caracteres de Escape
   - Se utilizan para darle a los metacaracteres un significado literal o para indicar un tipo especial de carácter.
   - Por ejemplo, `\` se usa para escapar metacaracteres. Si quieres buscar el carácter '.', debes usar `\.`.
   - También se utilizan para representar tipos de caracteres especiales, como `\d` para cualquier dígito, `\w` para cualquier carácter de palabra, y `\s` para cualquier espacio en blanco.

### Literales
   - Los literales son caracteres que no son metacaracteres y representan a sí mismos.
   - Por ejemplo, la expresión regular `abc` coincidirá con la secuencia exacta de caracteres 'abc'.

---

## Referencias 🌐

- [Python Official Documentation](https://docs.python.org/3/library/re.html)
- [Python Official Documentation - HOWTO](https://docs.python.org/3/howto/regex.html)
- [TutorialsTeacher](https://www.tutorialsteacher.com/regex/)

---

### [Ir al cuestionario 📝](../../cuestionario/01-introduccion/sintaxis_basica.md)

### [Ir al temario 🔍](../../readme.md)