

| Campo | ¿Identifica directamente? | ¿Puede contribuir a identificar? | ¿Requiere protección? | Justificación |
| ----- | ----- | ----- | ----- | ----- |
| id | No | Sí | No | Un ID como tal no identifica directamente  a la persona, se necesitan más datos. |
| nombre | Sí | Sí | No | Si bien ayuda a identificar directamente a la persona, no es necesario ocultar el nombre como tal. |
| correo | Sí | Sí | Sí | Al ser un dato personal, debe ser protegido. |
| telefono | Sí | Sí | Sí | Al ser un dato personal, debe ser protegido. |
| rfc | Sí | Sí | Sí | Al ser un dato personal de nivel legal, debe ser protegido. |
| edad | No | Sí | En algunos casos. | Podría protegerse al agregarse un rango de edad en lugar de mostrar la edad directamente. |
| ciudad | No | Sí | No | Al ser un dato que puede ser utilizado con fines de segmentación, no es estrictamente necesario protegerse. |
| codigo\_postal | No | Sí | Sí | Al ser un dato personal de ubicación, debe protegerse. |
| fecha\_alta | No | No | No | No es un dato que realmente requiera medidas estrictas de protección. |

1. **¿Qué campos identifican directamente a una persona?** Los datos de nombre, correo, teléfono y RFC.  
2. **¿Qué campos no identifican por sí solos pero podrían contribuir a hacerlo?** Los datos de ID, nombre, correo, teléfono, RFC, edad, ciudad y código postal.  
3. **¿Qué combinación de campos podría incrementar el riesgo de reidentificación?** Directamente cualquier combinación de datos entre los datos de contacto y el nombre o el ID puede incrementar el riesgo de identificación.  
4. **¿Todos los datos que deben protegerse son necesariamente datos personales sensibles desde el punto de vista jurídico?** No, hay casos en los que algunos datos que, si bien no se consideran datos personales desde un punto de vista jurídico, deben protegerse para disminuir el riesgo de identificación.

Enmascaramiento

Mecanismo utilizado con el fin de ocultar visualmente información hacia el área de soporte. Se ocultaron datos sensibles como los datos de contacto. Esto con el fin de que los datos no se expusieran de manera visual hacia personal no autorizado, y con el objetivo de proteger la integridad de los datos incluso con personal fuera del área de trabajo, como en este caso fue de soporte.

Seudonimización

Los tokens se generan a partir del ID de los clientes, donde oculta directamente el nombre del cliente para evitar que se vea a simple vista pero evitando que falte en el análisis de datos por parte de los analistas. Se separaron los permisos para tener un mayor control sobre quién debería acceder a cierto contenido, como las tablas clientes que mostraba directamente toda la información. Los analistas deberían poder acceder solo a la tabla con los tokens donde no aparece directamente los nombres de los clientes.

Anonimización

Aquí directamente todos los datos personales, a diferencia de la edad y región, fueron eliminados, donde estos últimos se generalizaron en grupos para tener una segmentación de los datos sin mostrar explícitamente los datos. En la última instancia, todos los grupos fueron suprimidos, pero aún existe riesgo de reidentificación al poder combinar esos datos, aunque el riesgo sea mínimo.

Retención 

Aquí se utilizó el criterio de 5 años para retener información. Como dicho en el informe de la actividad en específico, dependerá de la solicitud de retención por parte del área de trabajo para justificar el porqué esos datos solicitados deberían ser retenidos. Podría eliminarse toda aquella información que no sea requerida con anterioridad. Sin embargo, si es necesario, se debe solicitar acceso a un respaldo anterior o una snapshot para recuperar datos previamente eliminados. Estos, de manera clara, ya creados previa a la eliminación de los registros.