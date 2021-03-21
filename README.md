# ORIENTACIÓN A OBJETOS II (OO2) 2019 - Facultad de Informática, Universidad Nacional de La Plata (UNLP) - 3º año

## CONTENIDOS MINIMOS

- Diseño Orientado a Objetos  
- Patrones de diseño  
- Construcción de aplicaciones con frameworks orientados a objetos.  
- Refactoring. Testing. Metodologías de Diseño Ágiles.

---

## PROGRAMA ANALÍTICO
### I - Diseño Orientado a Objetos
1. La filosofía del proceso de desarrollo de software. Las etapas del proceso de desarrollo de software. Procesos de desarrollo iterativos e incrementales, basados en modelos: utilidad de los modelos. Los modelos a través del proceso de desarrollo de software. Cualidades y clasificación de los modelos.
2. UML como Lenguaje de modelado. Diagrama de clases. Diagrama de estados. Diagrama de interacción.

### II -Patrones de Diseño:
3. Introducción a Patrones. Definición de Patrón. Descripción de un patrón. Catálogo de Patrones.
4. Patrones de diseño. Definición. Descripción de un patrón de diseño. Organización del Catálogo de patrones de diseño. Utilidad de los patrones de diseño. Selección de los patrones de diseño. Uso de los patrones de diseño.
5. Patrones creacionales: Abstract Factory, Singleton.
6. Patrones estructurales: Composite, Decorador, Adapter, Proxy.
7. Patrones de comportamiento: Observer, State, Strategy, Template Method, Command.

### III - Refactoring
8. Introducción a Refactoring. Utilidad del refactoring. Técnica de aplicación del refactoring. Casos de uso. Catalogo de refactoring.
9. Manipulación de métodos largos: Extract Method. lnline Method, Replace Temp with Queries, Replace Method with Method Object. Mover aspectos entre objetos: Move Method, Move Field, Extract class. Organización de datos. Self Encapsulate Field, Replace Data Value with Objects, Replace Type Code with Class / Subclass /State- Strategy. Simplificación de invocación de métodos: Rename Method, Replace Constructor with Factory Method, Parameterize Method. Simplificación de expresiones condicionales: Replace Conditional with Polimorfism. Manipulación de la generalización: Pull Up Method. Push Down Method, Extract Subclass, Extract Superclass, Form Template Method, Replace lnheritance with Delegation.
10. Refactoring hacia patrones. Unify interfaces with Adapter. Form Template Method. Replace conditional logic with strategy. Replace State-Altering Conditionals with State. Replace Hardcoded Notifications with Observer. Move Embellishment to Decorator.

### IV -Frameworks
11. Introducción a Frameworks. Reutilización de software vs. reutilización de diseño. Clasificación de frameworks según su propósito.
12. Frameworks basados en herencia (white box frameworks). Frameworks basados en composición (black boxframeworks).
13. Elementos centrales en la implementación de un framework: Inversión de control, Hostposts, Frozenspots.
14. Las plantillas y los ganchos como generadores de hotspots e inversión de control. Su implementación con herencia y con composición.
15. Instanciación de frameworks; casos de estudio: Seaside, SUnit.
16. Diseño evolutivo de frameworks. El rol estratégico de los patrones, el refactoring, y los tests de unidad.
17. Documentación de frameworks: ejemplos, hotspot cards, y patrones

### V - Test Driven Development
18. Testing. Importancia. Tipos de tests: de unidad, de integración, de aceptación. Metodología de desarrollo ágil TDD: "Test Driven Development". Relación entre refactoring y testing.
19. Patrones de tests de unidad: familia de frameworks XUnit.
20. El framework SUnit de test de unidad en Smalltalk.

---

## Bibliografía

BIBLIOGRAFÍA OBLIGATORIA
1. Design Patterns. Elements of Reusable Objects Oriented Software. Gamma, Helm, Johnson, Vlissides, Addison-Wesley, Professional Computing Series.
2. Refactoring: lmproving the Design of Existing Code. Fowler, Martin. AddisonWesley, 1999
3. Refactoring to Patterns. Joshua Kerievsky. Addison Wesley, 2004. ISBN: 0-321-21335-1
4. Implementing Application Frameworks: Object-Oriented Frameworks at Work(Hardcover). Mohamed E. Fayad (Editor), Douglas C. Schmidt (Editor), Ralph E.Johnson (Editor).

BIBLIOGRAFÍA COMPLEMENTARIA
1. Head First Design Patterns. Elisabeth Freeman, Bert Bates, Kathy Sierra - Computers -2004 -676 pages.
2. Extreme Programming Explained. Kent Beck and Cynthia Andres. AddisonWesley, 2005.
3. Building Application Frameworks: Object-Oriented Foundations of Framework Design. Mohamed E. Fayad (Editor), Ralph E. Johnson (Author), Douglas C. Schmidt (Editor).
4. Domain-Specific Application Frameworks: Frameworks Experience by Industry (Hardcover). Mohamed E. Fayad (Editor), Ralph E. Johnson (Editor).
5. Johnson, R. E. 1997. Components, frameworks, patterns. In Proceedings of the 1997 Symposium on Software Reusability (Boston, Massachusetts, United States, May 17 - 20, 1997). M. Harandi, Ed. SSR ’97. ACM Press,New York, NY, 10-17. [PDF]
6. Designing Reusable Classes. B. Foote, R. Johnson. Journal of Object-Oriented Programming, 1998.
7. D. Roberts and R. Johnson. Evolving Frameworks: A Pattern Language for Developing Object-Oriented Frameworks. Proceedings of Pattern Languages of Programs, Allerton Park, Illinois, September 1996. [PDF]
8. Kent Beck. Simple Smalltalk Testing: With Patterns. http://www.xprogramming.com/testfram.htm
9. Stephane Ducasse. SUnit Explained. http://www.iam.unibe.ch/~ducasse/
