# Ejercicio 4: Patrón State

Lea el capítulo del patrón State en el libro Design Patterns ​y responda:

1. ¿Cuándo es necesario usar el patrón State?

    State es un patrón de diseño de comportamiento que permite a un objeto alterar su comportamiento cuando su estado interno cambia.

    La idea principal es que, en cualquier momento dado, un programa puede encontrarse en un número finito de estados. Dentro de cada estado único, el programa se comporta de forma diferente y puede cambiar de un estado a otro instantáneamente. Sin embargo, dependiendo de un estado actual, el programa puede cambiar o no a otros estados. Estas normas de cambio llamadas transiciones también son finitas y predeterminadas.

2. ¿Qué representa el contexto dentro del patrón State?

    La clase Contexto almacena una referencia a uno de los objetos de estado concreto y le delega todo el trabajo específico del estado. El contexto se comunica con el objeto de estado a través de la interfaz de estado. El contexto expone un modificador (setter) para pasarle un nuevo objeto de estado.

3. ¿Puede el estado concreto acceder al contexto?

    Los objetos de estado pueden (aunque no siempre) almacenar una referencia inversa al objeto de contexto. A través de esta referencia, el estado puede extraer cualquier información requerida del objeto de contexto, así como iniciar transiciones de estado.

4. ¿Quién define las transiciones entre estados?

    Tanto el contexto como un estado concreto pueden realizar un cambio de estado del contexto, sustituyendo el objeto de estado vinculado al contexto.