# Descripción
Como parte de los proyectos de sostenibilidad de la compañía, se está buscando una solución que permita que los empleados publiquen sus rutas de transporte e indiquen los cupos que tienen disponibles en su vehículo, la hora de salida, el lugar de origen y el destino y que permita a los demás compañeros inscribirse en alguna de las rutas

# Diagrama de arquitectura de la solución (Basada en la nube de Azure)
![Arquitectura drawio](https://user-images.githubusercontent.com/8541422/226673179-83aa4ffe-cfe8-4481-9e7c-2a3846699063.png)

# Modelo entidad relación
![Entity Relationship Diagram](https://user-images.githubusercontent.com/8541422/226685271-292c4c4f-618c-4086-8144-d8b21107260d.jpg)

# Tecnologías, lenguajes de programación y frameworks a utilizar y justificación de la selección de cada uno
- Para frontend web, implementaria la plataforma con ReactJS por la facilidad y rapidez que brinda esta libreria de JS para el desarrollo de aplicaciones web rapidas
- Para la aplicación movil, la desarrollaría con ionic Capacitor, la facilidade de desarrollo con typescript ademas de ser un framework que me genera la aplicación tanto para android como iOS
- Autenticación de usuario con B2C, ya que es un componente que nos facilita Azure para la gestion de usuarios de nuestras aplicaciones, ya sea usuarios externos o internos, completamente parametrizable
- Para el backend de la solución, me iria con .NET Core, por ser un lenguaje robusto que soportaria la logica de la solución, con la creación de microservicios alojados en contenedores docker en Azure Kubernetes services
- Para base de datos seleccionaria SQL Server o Postgresql por ser gestores de bases de datos relacionales y la simplicidad de implementación y uso

# Metodología de desarrollo
Implementaria la metodología agíl SCRUM, generando una correcta creación de cada artefacto, desde el lavantamiento de requerimientos, la creación del tablero con las Epicas, Historias de usuario y tareas, socialización del proyecto con el quipo de desarrollo, gestion de sprint planning, dailys, sprint review y sprint retrospective, de esta manera podremos tener la oportunidad de ejecutar todo el flujo de desarrollo de una manera organizada, pudiendo realizar entregas incrementales funcionales al cliente y a la vez que el equipo de desarrollo se centre especificamente en objetivos especificos en ca iteración, incluyendo pruebas.

# Descripción de las buenas prácticas metodológicas que pueden agilizar el proceso de desarrollo, para la entrega de software de calidad en los diferentes ambientes
Manejo de azure devops para el segumiento de la metodología Scrum, en el cual tenga creados los repositorios, tableros, tareas, sprint y asignaciones de cada desarrollador y tester, Segmentación de cada ambiente en devops mediante ramas, ejemplo rama master(Producción), rama dev(Desarrollo), rama qa(Pruebas), haciendo de esta manera que el ciclo correcto de desarrollo de una tarea sea generar una rama feature/#tarea sobre dev en la cual el desarrollador trabajará, una vez este completada, realizar un merge con dev, donde se realizará una revisión de calidad de codigo para así hacer un merge a qa para el proceso de pruebas, si las pruebas son exitosas, se realizará dicho merge a master con el fin de liberar esa funcionalidad, si las pruebas no son exitosas, el tester devolvera la tarea y se iniciara nuevamente el ciclo de desarrollo desde el feature corrigiendo las observaciones o no cumplimientos del entregable

# Infraestructura y plataformas necesaria para soportar el desarrollo
- Nube nativa con Azure
- WAF que me sirva de protección
- Azure B2C
- Api management services, para exponer las apis que consumirá el app web y el app movil, usa como backend un micorservicio de entrypoint
- Cluster AKS que aloja los contenedores de los microservicios
- App service para desplegar el aplicativo web
- Azure devops para el manejo de los repositorios y la metodologia Scrum
- Azure Base de datos SQL Server o postgresql
- Apis externas para el envio de sms
- Licencia y cuentas para el despliegue del app movil en la tienda playstore y en la appstore

# Posibles riesgos que pueden materializarse en la ejecución del proyecto y cómo mitigarlos
- Nuevos requerimientos no contemplados: Esto puede mitigarse verificando el impacto del nuevo requerimiento y analizando en que iteración de la metodologia puede ejecutarse
- Que se reduzca el equipo de desarrollo, por lo que se deberá mantener motivado al equipo con la finalización del proyecto y si es necesario incentivos o reconocimientos al culminar el proyecto de manera satisfactoria o al termino de cierto porcentaje de avance
- Bloqueantes tecnologicos, como un lenaguaje incompatible, se deberá analizar que otro framework nos puede brindar la misma facilidad y resultados esperados

# Otros elementos que considere necesarios para este proyecto
Se consideran necesarios un equipode desarrollo integral compuesto por 2 fullstack con conocimiento en desarrollo movil, un desarrollador backend con conocimiento en base de datos y un experto en la nube para la configuración de cada componente requerido para cada ambiente
