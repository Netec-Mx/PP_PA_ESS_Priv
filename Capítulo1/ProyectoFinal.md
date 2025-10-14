# Proyecto Final - Power Automate

El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos, y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad.


## Duración aproximada:
- 60 minutos.


## Desarrollo del proyecto

En el banco muchas tareas son manuales: recepción de archivos para reportes, aprobaciones de gastos/créditos, notificaciones por correo y consolidación de datos en Excel. En esta sección se automatizarán estas tareas para reducir tiempos, aumentar la trazabilidad y centralizar información en Dataverse/SharePoint.

**Pasos que debes realizar**

1. Listar los procesos concretos a automatizar (ej.: aprobación de crédito menor a X, recepción de PO y consolidación en Excel, carga de anexos para reportes).
* **Entregable:** tabla (Excel/Word) con 6–8 procesos y prioridad (Alta/Media/Baja).

2. Mapear triggers y orígenes de datos por proceso: identificar si el disparador será “archivo en SharePoint”, “registro en Dataverse”, “botón en Canvas” o “programado”.
* **Entregable:** diagrama simple (imagen) con triggers y destinos.

3. Seleccionar la plantilla/plantillas en Power Automate que más se ajusten (ej.: “When a file is created in a folder” → “Start an approval”); anotar qué modificaciones se necesitan.
* **Entregable:** lista de plantillas seleccionadas y cambios requeridos.

4. Crear un flujo automatizado desde cero para la carga de archivos:
* Crear flujo tipo Automatizado con trigger “When a file is created in SharePoint”.
* Leer contenido del archivo (si es Excel: usar conector Excel o List rows present in a table).
* Insertar/actualizar registros en Dataverse o en lista SharePoint.
* Enviar notificación (email/Teams) al responsable.
* **Entregable:** captura del diseñador del flujo + exportación del flujo como parte de la solución.

5. Crear un flujo de aprobación desde plantilla y adaptarlo para ejecutarlo desde Canvas:
* Seleccionar plantilla de aprobación.
* Agregar condiciones (por ejemplo: monto > X → aprobador A; monto ≤ X → aprobador B).
* Exponer el flujo como Instant flow (botón) o como flujo que acepta una petición HTTP si se invoca desde Power Apps.
* Validar que la respuesta de la aprobación actualice el registro en Dataverse (estado: Aprobado/Rechazado).
* **Entregable:** captura del flujo + captura del historial de ejecución de una aprobación.

6. Crear flujos programados para consolidación de reportes:
* Programar extracción diaria/semanal de datos desde Dataverse/SharePoint.
* Fusionar información en un Excel maestro en SharePoint o generar un CSV en una carpeta para Power BI.
* **Entregable:** captura del flujo programado y del archivo final generado.

7. Probar cada flujo con casos reales y casos límite: ejecutar con distintos escenarios (documento correcto, documento sin tabla, aprobaciones duplicadas) y registrar resultados.
* **Entregable:** documento corto con 3 escenarios de prueba y resultados (OK / issue).

8. Incluir manejo de errores razonable (validaciones de entrada, condiciones para datos faltantes) y logging de fallos en una tabla de errores en Dataverse.
* **Entregable:** captura de la tabla de errores y ejemplo de registro.

9. Empaquetar los flujos dentro de una solución para ALM (añadir flows a la solución, definir environment variables si aplica).
* **Entregable:** archivo .zip de la solución que incluya los flujos.
