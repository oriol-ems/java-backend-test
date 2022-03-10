<img src="https://esbladamedical.es/wp-content/uploads/2017/06/logo-esblada-medical.jpg"/>

# Prueba técnica Backend Developer

Ésta prueba técnica es un ejercicio práctico que utilizamos para evaluar a los candidatos a nuestra vacante de desarrollador back-end. Su objetivo es ayudarnos a conocer cómo piensas y el proceso que has seguido, no tanto que estén finalizados completamente todos los requisitos funcionales.

Los puntos que tendremos más en cuenta serán qué decisiones has tomado, por dónde has empezado, cómo has definido la arquitectura de la aplicación, cómo has diseñado el modelo, cómo has reflejado las reglas de negocio, cómo has hecho los tests y cómo has utilizado el control de versiones.

Para hacer la prueba proporcionamos un repositorio Git que sirve de esqueleto para empezar el proyecto. Debes hacer un fork del repositorio de la siguiente URL y hacer los commits ahí:

https://github.com/oriol-ems/java-backend-test

## Requisitos técnicos
Únicamente requerimos el uso de Java 8 o superior, y recomendamos que la lógica de negocio tenga test unitarios. Si quieres abordarlo utilizando TDD, todavía mejor :)

Para ahorrar tiempo, no es necesaria la implementación de la persistencia de datos, aunque el código debe reflejar su futura implementación.

## Requisitos funcionales
### Modelo
El doctor realiza un análisis a un paciente, la aplicación cliente envía los datos del paciente y el nombre del análisis realizado. Un doctor puede realizar un número ilimitado de análisis al paciente.

Se debe implementar un servicio que reciba estos análisis y los cree en el sistema. Este proceso puede llegar a ser lento y la respuesta al cliente no debería esperar a que éste haya terminado..

Para el diseño del modelo es recomendable seguir las premisas de diseño guiado por el
dominio (DDD).

### Funcionalidades a implementar
En la API se tienen que implementar los siguientes endpoints para estas funcionalidades:

- Crear un nuevo análisis.

  Este endpoint debe recibir el nombre y los apellidos de un paciente y el nombre del análisis realizado. La respuesta de este endpoint será el id del análisis.


- Recuperar los análisis de todos los pacientes.

  Devolver el listado completo (con todos los datos), agrupado por paciente, de análisis.


- Actualizar datos del diagnóstico.

  Dado el id de un análisis, se debe poder actualizar la malignidad de ese diagnóstico. La malignidad es un valor que puede ser verdadero o falso. Opcionalmente, se puede añadir un comentario al diagnóstico.
