# Descripción
Como parte de los proyectos de sostenibilidad de la compañía, se está buscando una solución que permita que los empleados publiquen sus rutas de transporte e indiquen los cupos que tienen disponibles en su vehículo, la hora de salida, el lugar de origen y el destino y que permita a los demás compañeros inscribirse en alguna de las rutas

# Diagrama de arquitectura de la solución (Basada en la nube de Azure)
![Arquitectura drawio](https://user-images.githubusercontent.com/8541422/226673179-83aa4ffe-cfe8-4481-9e7c-2a3846699063.png)

# Modelo entidad relación
![Entity Relationship Diagram](https://user-images.githubusercontent.com/8541422/226685271-292c4c4f-618c-4086-8144-d8b21107260d.jpg)

# Tecnologías, lenguajes de programación y frameworks a utilizar y justificación de la selección de cada uno
- Para frontend web, implementaria la plataforma con ReactJS por la facilidad y rapidez que brinda esta libreria de JS para el desarrollo de aplicaciones web rapidas
- Para la aplicación movil, la desarrollaría con ionic Capacitor, la facilidade de desarrollo con typescript ademas de ser un framework que me genera la aplicación tanto para android como iOS
- Para el backend de la solución, me iria con .NET Core, por ser un lenguaje robusto que soportaria la logica de la solución, con la creación de microservicios alojados en contenedores docker en Azure Kubernetes services
- Para base de datos seleccionaria SQL Server o Postgresql por ser gestores de bases de datos relacionales y la simplicidad de implementación y uso

# Metodología de desarrollo
Implementaria la metodología agíl SCRUM, porque nos brinda la posibilidad de ejecutar todo el flujo de desarrollo de una manera organizada, pudiendo realizar entregas incrementales funcionales al cliente y a la vez que el equipo de desarrollo se centre especificamente en objetivos especificos en ca iteración, incluyendo pruebas.

# Descripción de las buenas prácticas metodológicas que pueden agilizar el proceso de desarrollo, para la entrega de software de calidad en los diferentes ambientes
Manejo de azure devops para el segumiento de la metodología Scrum, en el cual tenga creados los repositorios, tableros, tareas, sprint y asignaciones de cada desarrollador y tester, Segmentación de cada ambiente en devops mediante ramas, ejemplo rama master(Producción), rama dev(Desarrollo), rama qa(Pruebas), haciendo de esta manera que el ciclo correcto de desarrollo de una tarea sea generar una rama feature/#tarea sobre dev en la cual el desarrollador trabajará, una vez este completada, realizar un merge con dev, donde se realizará una revisión de calidad de codigo para así hacer un merge a qa para el proceso de pruebas, si las pruebas son exitosas, se realizará dicho merge a master con el fin de liberar esa funcionalidad, si las pruebas no son exitosas, el tester devolvera la tarea y se iniciara nuevamente el ciclo de desarrollo desde el feature corrigiendo las observaciones o no cumplimientos del entregable


