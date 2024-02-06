# Cuantificadores básicos 📚

Los cuantificadores básicos permiten especificar cuántas veces debe aparecer un elemento para que se produzca una coincidencia. Aquí desglosamos cada uno de ellos:

1. **`*` (Cero o más veces):**
   - Este cuantificador hace que el elemento precedente sea opcional y pueda aparecer múltiples veces.
   - Ejemplo: `ab*c` coincidirá con 'ac', 'abc', 'abbc', 'abbbc', etc.

2. **`+` (Una o más veces):**
   - Requiere que el elemento precedente aparezca al menos una vez.
   - Ejemplo: `ab+c` coincidirá con 'abc', 'abbc', 'abbbc', etc., pero no con 'ac'.

3. **`?` (Cero o una vez):**
   - Hace que el elemento precedente sea opcional, permitiendo que aparezca cero o una vez.
   - Ejemplo: `ab?c` coincidirá con 'ac' o 'abc'.

4. **`{n}` (Exactamente n veces):**
   - Especifica que el elemento precedente debe ocurrir exactamente n veces.
   - Ejemplo: `a{3}` coincidirá solo con 'aaa'.

5. **`{n,}` (n o más veces):**
   - Indica que el elemento precedente debe aparecer al menos n veces.
   - Ejemplo: `a{2,}` coincidirá con 'aa', 'aaa', 'aaaa', etc.

6. **`{n,m}` (Entre n y m veces):**
   - El elemento precedente debe ocurrir al menos n veces, pero no más de m veces.
   - Ejemplo: `a{1,3}` coincidirá con 'a', 'aa', o 'aaa'.

### Cuantificadores Perezosos y Codiciosos

Los cuantificadores desempeñan un papel crucial al determinar la cantidad de veces que un patrón debe coincidir. Entre estos, los cuantificadores perezosos y codiciosos controlan cómo se realizan estas coincidencias, especialmente en contextos donde un patrón podría coincidir de varias maneras.

**Cuantificadores Codiciosos:**
- Los cuantificadores codiciosos intentan coincidir con la mayor cantidad posible de caracteres que cumplen con el patrón. Son los cuantificadores por defecto en las expresiones regulares.
- Ejemplos incluyen `*` (cero o más veces), `+` (una o más veces), y `{n,m}` (entre n y m veces).
- **Comportamiento:** Por ejemplo, en la cadena "aaaa", el patrón `a*` (un cuantificador codicioso) coincidirá con toda la cadena "aaaa", porque intenta coincidir con tantas 'a' como sea posible.

**Cuantificadores Perezosos:**
- Los cuantificadores perezosos, por otro lado, hacen lo contrario: intentan coincidir con la menor cantidad posible de caracteres. Se indican añadiendo un `?` después del cuantificador codicioso.
- Ejemplos incluyen `*?` (cero o más veces, pero lo menos posible), `+?` (una o más veces, pero lo menos posible), y `{n,m}?` (entre n y m veces, pero lo menos posible).
- **Comportamiento:** Usando el mismo ejemplo con la cadena "aaaa", el patrón `a*?` coincidirá con una cadena vacía al principio de "aaaa", porque intenta coincidir con cero caracteres si es posible, que es la menor cantidad que puede coincidir según el patrón.

**Importancia de la Distinción:**
- La elección entre usar cuantificadores perezosos o codiciosos puede tener un gran impacto en el resultado de las coincidencias.
- **Codicioso:** Puede ser útil cuando se desea capturar tanto texto como sea posible, como en la extracción de contenido entre dos delimitadores que abarcan múltiples líneas o segmentos de texto.
- **Perezoso:** Es útil para coincidencias mínimas o cuando se desea evitar "sobrepasar" un límite deseado, especialmente en contextos donde múltiples coincidencias son posibles y solo se desea la más corta o específica.

**Ejemplo Práctico:**
- Considera la cadena "<div>Hola</div><div>Adiós</div>" y el patrón `<div>.*</div>` (codicioso). Este patrón coincidirá con todo el texto desde el primer `<div>` hasta el último `</div>`, porque extiende la coincidencia tanto como es posible.
- Cambiando el patrón a `<div>.*?</div>` (perezoso), coincidirá solo con `<div>Hola</div>`, la primera coincidencia posible, ya que se detiene en el primer `</div>` que encuentra después del `<div>` inicial.

### Uso Práctico de los Cuantificadores Básicos

- **Validación de Formatos:** Son útiles para validar entradas como números de teléfono, códigos postales, y direcciones de correo electrónico donde se requiere una cantidad específica de dígitos o caracteres.
- **Búsqueda de Patrones:** Facilitan la búsqueda de patrones específicos dentro de textos, como identificar todas las palabras que contienen al menos una 'a' o palabras que empiezan y terminan con ciertos caracteres.
- **Extracción de Datos:** Permiten extraer partes específicas de un texto, como números dentro de una cadena de caracteres o elementos específicos en un código fuente.

---

## Referencias 🌐

- [.NET - Quantifiers in Regular Expressions](https://learn.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions) - Esta página de Microsoft Learn detalla cómo los cuantificadores en las expresiones regulares definen la cantidad de veces que un carácter o grupo de caracteres debe aparecer para coincidir.
- [MDN Web Docs - Quantifiers](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Quantifiers) - MDN Web Docs ofrece una explicación sobre los cuantificadores en JavaScript, incluyendo cómo estos indican el número de caracteres o expresiones a coincidir.
- [The Java™ Tutorials - Quantifiers](https://docs.oracle.com/javase/tutorial/essential/regex/quant.html) - Los tutoriales de Oracle Java explican el uso de cuantificadores en expresiones regulares para controlar la frecuencia con la que se deben encontrar partes de una cadena para que coincida.
- [Python 3.12.1 Documentation - re — Regular expression operations](https://docs.python.org/3/library/re.html) - La documentación oficial de Python proporciona detalles sobre las operaciones con expresiones regulares, incluido el uso de cuantificadores para especificar la cantidad de coincidencias.

---

### [Ir al cuestionario 📝](../../cuestionario/03-cuantificadores-y-grupos/cuantificadores.md)

### [Ir al temario 🔍](../../readme.md)