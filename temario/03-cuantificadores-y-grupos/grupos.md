# Agrupación de Patrones con Paréntesis y Uso de Grupos Capturados 📚

La agrupación de patrones con paréntesis `()` y el uso de grupos capturados son técnicas para realizar búsquedas y manipulaciones de texto más complejas.

**Agrupación de Patrones:**

- **Uso Básico:** Los paréntesis `()` se utilizan para agrupar varios caracteres como una única unidad. Esto permite aplicar cuantificadores a un grupo entero de caracteres, no solo al carácter que lo precede inmediatamente.
- **Ejemplo:** La expresión `(ab)+` coincidirá con 'ab', 'abab', 'ababab', etc., porque trata 'ab' como una unidad y busca una o más repeticiones de esta secuencia.

**Grupos Capturados:**

- **Captura:** Cuando una parte de una expresión regular está entre paréntesis, no solo define un grupo para aplicar cuantificadores, sino que también captura la subcadena de texto que coincide con esa parte de la expresión.
- **Referencia Posterior:** Puedes referirte a grupos capturados posteriormente en la expresión regular (por ejemplo, `\1`, `\2` para referirse al primer y segundo grupo capturado, respectivamente) o en operaciones de reemplazo.
- **Ejemplo de Captura y Referencia:** La expresión `(\w+)\s+\1` busca palabras que aparecen repetidas en un texto, donde `\1` hace referencia al grupo capturado que contiene la primera palabra.

**Uso Práctico de Grupos Capturados:**

- **Validación de Formatos Complejos:** Puedes utilizar grupos capturados para validar formatos complejos que tienen subpartes repetitivas o en espejo, como fechas, números de teléfono o códigos con estructuras específicas.
- **Extracción de Datos:** Son especialmente útiles para extraer subpartes específicas de un texto, como capturar áreas específicas de una URL o partes de un documento.
- **Búsqueda y Reemplazo Avanzados:** Permite realizar operaciones de búsqueda y reemplazo complejas, donde partes del texto coincidente se reutilizan o modifican en el texto de reemplazo.

**Ejemplos Avanzados:**

- **Condicionales Basados en Grupos Capturados:** Algunos motores de expresiones regulares permiten utilizar condiciones basadas en si un grupo capturado ha coincidido o no, lo que ofrece aún más flexibilidad para crear patrones complejos.

### Diferencia entre Grupos Codiciosos y No Codiciosos

La diferencia principal entre ambos radica en la cantidad de texto que intentan capturar.

**Grupos Codiciosos:**

- **Comportamiento:** Intentan coincidir con la mayor cantidad posible de texto que cumpla con el patrón especificado. Esto significa que, dada la opción, un grupo codicioso se expandirá tanto como pueda para incluir el mayor número de coincidencias.
- **Ejemplo:** Dada la cadena `"¡Hola, mundo! ¡Hola, todos!"` y el patrón `/¡Hola.*!/`, un grupo codicioso coincidiría con todo el texto desde el primer `"¡Hola"` hasta el último `"!"`, porque captura la mayor cantidad de texto posible que cumple con el patrón.

**Grupos No Codiciosos (o Perezosos):**

- **Comportamiento:** A diferencia de los grupos codiciosos, los grupos no codiciosos coinciden con la menor cantidad de texto posible. Esto se logra agregando un `?` después del cuantificador, lo que lo hace "perezoso".
- **Ejemplo:** Usando la misma cadena anterior y el patrón `/¡Hola.*?!/`, un grupo no codicioso coincidiría solo con `"¡Hola, mundo!"`, ya que se detiene en la primera coincidencia del patrón, buscando la menor expansión posible.

**Cuándo Usar Cada Uno:**

- **Grupos Codiciosos:** Son útiles cuando necesitas capturar la mayor cantidad de texto posible dentro de un patrón. Esto es especialmente útil en situaciones donde el texto objetivo está rodeado por delimitadores conocidos que no se repiten dentro del segmento de interés.
- **Grupos No Codiciosos:** Son preferibles cuando el texto que deseas capturar está seguido por un delimitador que podría aparecer varias veces en la cadena objetivo. Usar un grupo no codicioso asegura que la coincidencia se detenga en el primer delimitador que encuentre, evitando capturas excesivas.

---

## Referencias 🌐

- [.NET - Grouping Constructs in Regular Expressions](https://learn.microsoft.com/en-us/dotnet/standard/base-types/grouping-constructs-in-regular-expressions) - Esta documentación de Microsoft explica cómo se utilizan los constructos de agrupación en las expresiones regulares para capturar subcadenas de una cadena de entrada, entre otros usos.
- [MDN Web Docs - Groups and backreferences](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Groups_and_Ranges) - MDN ofrece una explicación detallada sobre los grupos y las referencias hacia atrás en JavaScript, incluyendo cómo capturar subcadenas para uso posterior.
- [Regular-Expressions.info - Capturing Groups](https://www.regular-expressions.info/refcapture.html) - Este recurso proporciona una guía completa sobre los grupos de captura en las expresiones regulares, explicando cómo se pueden utilizar para realizar operaciones más complejas.
- [Python 3.12.1 Documentation - Regular Expression HOWTO](https://docs.python.org/3/howto/regex.html) - La documentación oficial de Python ofrece una introducción práctica al uso de expresiones regulares, incluyendo detalles sobre la agrupación y captura de grupos.

---

### [Ir al cuestionario 📝](../../cuestionario/03-cuantificadores-y-grupos/grupos.md)

### [Ir al temario 🔍](../../readme.md)