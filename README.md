
CERP DEL SUROESTE (COLONIA)
PROGRAMACIÓN II
2026
ALUMNA: MARÍA COLLAZO
Ejercicio
Se espera que la resolución abarque la creación de un diagrama de clases de
implementación completo que cumpla con todos los requisitos especificados.
1. Identificación de Clases principales: Determine las clases fundamentales
necesarias para modelar el sistema de gestión de la biblioteca. Considere
entidades como 'Libro', 'Usuario' y 'Préstamo'.
2. Definición de atributos: Para cada clase identificada, defina los atributos
relevantes que describen sus características. Por ejemplo, un 'Libro' debe tener
título, autor y categoría. Un 'Usuario' debe tener nombre, dirección y número de
identificación. Un 'Préstamo' debe registrar la fecha de préstamo.
3. Establecimiento de relaciones: Modele las relaciones entre las clases.
Considere:
o La categorización de los libros (una relación entre 'Libro' y 'Categoría').
o La asociación de un libro a un usuario para registrar un préstamo (una
relación entre 'Usuario', 'Libro' y 'Préstamo').
o La cardinalidad de estas relaciones (por ejemplo, un usuario puede tener
múltiples préstamos, un libro solo puede ser prestado a un usuario a la
vez).
4. Inclusión de métodos: Aunque el foco es conceptual, identifique y represente
brevemente algunos métodos clave que las clases podrían soportar, como
"solicitar préstamo" en 'Usuario' o "registrar devolución" en 'Préstamo'.
5. Aplicación de restricciones: Represente en el diagrama las restricciones
mencionadas, como:
o Evitar préstamos de libros no disponibles.
o Prevenir préstamos duplicados para el mismo libro.
6. Diagrama de Clases: Elabore un diagrama de clases completo que integre todas
las clases, atributos, relaciones y restricciones identificadas. Asegúrese de que el
diagrama sea claro, coherente y cumpla con los requisitos del sistema.
Formato de respuesta esperado
La entrega debe consistir en un único archivo adjunto en formato PDF. Este archivo
debe contener:
 Portada: Con el título del trabajo, nombre del estudiante, número de matrícula,
nombre de la asignatura y fecha de entrega.
 Diagrama de Clases: El diagrama de clases debe ser el elemento central de la
entrega. Se espera que sea legible y bien estructurado. Puede ser generado
utilizando cualquier herramienta de diagramación UML compatible (ej.
Lucidchart, Draw.io, StarUML, Visual Paradigm, etc.) o dibujado a mano de
forma clara y escaneado.
 Breve descripción del Diagrama (Opcional pero recomendado): Un texto
conciso (máximo 200 palabras) explicando las decisiones clave tomadas en el
diseño del diagrama, las clases principales, las relaciones más importantes y
cómo se han representado las restricciones.
La extensión total del documento PDF no debe exceder las 5 páginas.
Estructura del Diagrama UML
Clases y atributos
 Libro
o título : String
o autor : String
o ISBN : String
o disponible : Boolean
 Categoría
o nombre : String
o descripción : String
 Usuario
o idUsuario : String
o nombre : String
o dirección : String
o tipoUsuario : Enum {Estudiante, Docente, Administrador}
 Préstamo
o idPrestamo : String
o fechaPrestamo : Date
o fechaDevolución : Date
o estado : Enum {Activo, Devuelto, Retrasado}
Relaciones y cardinalidades
 Libro – Categoría:
Una Categoría puede tener muchos Libros (1..*), cada Libro pertenece a una
Categoría (1).
 Usuario – Préstamo:
Un Usuario puede tener múltiples Préstamos (1..*), cada Préstamo pertenece a
un Usuario (1).
 Préstamo – Libro:
Un Préstamo se asocia a un único Libro (1), y un Libro puede estar en un
préstamo activo a la vez (0..1).
Métodos clave
 Usuario: solicitarPréstamo(), consultarHistorial()
 Préstamo: registrarDevolución(), calcularRetraso()
 Libro: verificarDisponibilidad(), actualizarEstado()
Restricciones representadas
 No se permite préstamo si Libro.disponible = false.
 No se permite duplicar préstamos para el mismo libro y usuario.
