# Ejercicio 4: Software con olores

Responda:

1. ¿Qué significa la expresión "código con mal olor" según lo visto en la teoría?

    El código con mal olor es código que presenta patrones que son indicadores de problemas de diseño:

    Los "malos olores" son:

    - **Código duplicado (Duplicated Code)**: Si encontramos la misma estructura de código en varios sitios, lo mejor es unificarla en un único punto.
    - **Método largo (Long Method)**: Los métodos pequeños son más claros en lo que hacen y permiten compartir el código y que se pueda elegir el método a llamar según el caso. La sobrecarga en la llamada a un método es casi despreciable, por lo que no debe ser excusa para usar métodos lo más pequeños posible.
    - **Clase grande (Large Class)**: Una clase que hace demasiadas cosas suele tener muchas variables de instancia y, tras ellas, suele haber código duplicado. Si una clase no utiliza todas sus variables de instancia en todo momento, las que no se usen se deberían eliminar o extraer a otra clase.
    - **Lista de parámetros larga (Long Parameter List)**: De forma distinta a lo que ocurría con tecnologías anteriores, cuando se usan objetos, no hace falta pasar a un método toda la información que necesita para su ejecución, sino sólo aquella que es imprescindible para que puede obtener todo lo que necesita.
    - **Cambio divergente (Divergent Change)**: Cuando hay que hacer un cambio, debemos ser capaces de identificar un único punto en el programa donde éste deba hacerse. Si tenemos una clase donde debamos cambiar 3 métodos por una razón y otros 4 por otra causa distinta, tal vez este objeto debería ser dividido en 2 con distintas responsabilidades.
    - **Cura de un escopetazo (Shotgun Surgery)**: Este caso es el contrario del anterior. Hay y que hacer un cambio y para ello deben modificarse varias clases desperdigadas por el código. Los métodos afectados deberían agruparse en una sola clase.
    - **Envidia de capacidades (Feature Envy)**: Si un método de una clase hace referencia más a métodos y parámetros de otra clase, tal vez sea en esa otra clase donde debería estar.
    - **Agrupaciones de datos (Data Clumps)**: Si un grupo de datos aparecen constantemente juntos y se usan siempre en los mismos momentos, estos datos deberían agruparse dentro de un objeto.
    - **Obsesión por los tipos primitivos (Primitive Obsession**): Existen ciertos datos que están mejor agrupados en pequeñas clases, en lugar de usar primitivas, aunque esto último parezca más sencillo. Usar clases para estos datos ofrece nuevas capacidades como añadir nueva funcionalidad o realizar comprobaciones de tipo de datos.
    - **Sentencias switch (Switch Statements**): A veces se encuentran las mismas sentencias switch repartidas por el código. Si se incluye un nuevo apartado clause se debe hacer para todas ellas y es fácil saltarse alguna. Normalmente esto es manejado mucho mejor a través de polimorfismo, cobre todo cuando la sentencia switch actúa en función de un valor que define el tipo de un objeto.
    - **Jerarquías paralelas de herencia (Parallel Inheritance Hierarchies)**: Esto ocurre cuando al añadir una clase en una jerarquía se hace evidente la necesidad de añadir una nueva clase en otra jerarquía distinta. Si las instancias de una jerarquía hacen referencia a las de la otra se puede eliminar una de ellas llevando sus métodos a la otra.
    - **"Clase vaga" (Lazy Class)**: Una clase que no hace nada está añadiendo una complejidad innecesaria y es mejor hacerla desaparecer.
    - **Generalización especulativa (Speculative Generality)**: Cuando se añade funcionalidad especulando sobre lo que necesitaremos en el futuro, pero que en este momento es innecesario, el resultado es código más difícil de entender y mantener. Es mejor deshacerse de ello.
    - **Campo temporal (Temporary Field)**: Si existen variables de instancia que parecen usarse sólo en algunos casos, puede ser confuso entender en cuáles. Es mejor sacar estas variables a otra clase.
    - **Cadenas de mensajes (Message Chains)**: Estas cadenas aparecen cuando un cliente pide a otro objeto un objeto y a su vez llama a éste último para obtener otro objeto. De esta menra, el cliente se acopla a toda esta estructura de navegación y cualquier cambio en ella le afectará. Es mejor recuperar otros objetos mediante un delegado que encapsule dicha navegación y abstraiga al cliente de ella.
    - **"Hombre en el medio" (Middle Man)**: El caso anterior no es necesario que se cumpla a rajatabla. A veces, si existen muchos métodos que delegan a una misma clase, es mejor quitarnos el delegado y referirnos a ella directamente.
    - **Intimidad inapropiada (Inappropiate Intimacy)**: Cuando una clase se dedica a hurgar en partes de otra clase que parecen ser privadas, ha llegado el momento de desacoplar dichas clases, por ejemplo, a través de una tercera que contenga la funcionalidad común de las dos anteriores.
    - **Clases alternativas con interfaces diferentes (Alternative Classes with Different Interfaces)**: Si tenemos dos métodos que hace los mismo pero se llaman de forma distinta, es mejor unificarlos para que se use siempre un único método.
    - **Clase de librería incompleta (Incomplete Library Class)**: A veces una clase de una librería de tercero no hace todo lo que necesitamos y debemos adaptar su uso a nuestras necesidades ya que no podemos modificarla.
    - **Clase de datos (Data Class**): Las clases que solo tienen datos getters y setters son manipuladas en gran medida por otras clases. Podemos buscar este comportamiento para llevarlo a las clases que contienen los datos.
    - **Legado rechazado (Refused Bequest)**: A veces una subclase no usa todos los métodos que hereda de su clase padre. Esto puede significar que la jerarquía no es correcta y los métodos de las clases se deben mover a donde se usan realmente.
    - **Comentarios (Comments)**: A veces los comentarios lo que están enmascarando es uno de los "malos olores" que se han visto anteriormente. Es mejor invertir el tiempo en mejorar este código que en comentarlo.

2. Encuentre tres casos de los "malos olores" explicados en la teoría en su propio código (implementacion de trabajos prácticos).

3. Basados en la bibliografía indicada en las clases teóricas de la materia, indique tres razones por las cuales es importante hacer refactoring.

- Mejora la facilidad de comprensión del mismo (legibilidad).
- Facilita el agregado de nuevas funcionalidades y reduce el costo de mantenimiento.
- Facilita la detección de bugs.