# Práctica 1.3. Proyecto final: Power Automate

## Objetivos
Al finalizar la práctica, serás capaz de:
- Crear flujos que reduzcan la carga operativa en la recepción de archivos, consolidación de reportes y aprobación de solicitudes. 
- Conectar los flujos con Power Apps o Dataverse, garantizando trazabilidad y registro de errores en una solución empaquetada para despliegues controlados.

## Duración aproximada
- 60 minutos.


## Instrucciones

El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad.

### Tarea 1. Automatizar estas tareas para reducir tiempos, aumentar la trazabilidad y centralizar información en Dataverse y SharePoint

**Paso 1.** Lista los procesos concretos a automatizar (por ejemplo: aprobación de crédito menor a _x_, recepción de PO y consolidación en Excel, carga de anexos para reportes).
* **Resultado esperado:** tabla (Excel/Word) con 6–8 procesos y prioridad (Alta/Media/Baja).

**Paso 2.** Mapea triggers y orígenes de datos por proceso: identifica si el disparador será “archivo en SharePoint”, “registro en Dataverse”, “botón en Canvas” o “programado”.
* **Resultado esperado:** diagrama simple (imagen) con disparadores y destinos.

**Paso 3.** Selecciona la o las plantillas en Power Automate que más se ajusten (por ejemplo: “When a file is created in a folder” → “Start an approval”); anota qué modificaciones se necesitan.
* **Resultado esperado:** lista de plantillas seleccionadas y cambios requeridos.

**Paso 4.** Crea un flujo automatizado desde cero para la carga de archivos:
* Crear un flujo tipo automatizado con el disparador “When a file is created in SharePoint”.
* Leer el contenido del archivo (si es Excel: usar conector Excel o List rows present in a table).
* Insertar o actualizar los registros en Dataverse o en lista SharePoint.
* Enviar una notificación (e-mail/Teams) al responsable.
* **Resultado esperado:** captura del diseñador del flujo y exportación del flujo como parte de la solución.

**Paso 5.** Crea un flujo de aprobación desde plantilla y adáptalo para ejecutarlo desde Canvas:
* Seleccionar la plantilla de aprobación.
* Agregar las condiciones (por ejemplo: monto > X → aprobador A; monto ≤ X → aprobador B).
* Exponer el flujo como Instant flow (botón) o como flujo que acepta una petición HTTP si se invoca desde Power Apps.
* Validar que la respuesta de la aprobación actualice el registro en Dataverse (estado: Aprobado o Rechazado).
* **Resultado esperado:** captura del flujo y captura del historial de ejecución de una aprobación.

**Paso 6.** Crea flujos programados para la consolidación de reportes:
* Programar la extracción diaria o semanal de datos desde Dataverse o SharePoint.
* Fusionar la información en un Excel maestro en SharePoint o generar un CSV en una carpeta para Power BI.
* **Resultado esperado:** captura del flujo programado y del archivo final generado.

**Paso 7.** Prueba cada flujo con casos reales y casos límite: ejecuta con distintos escenarios (documento correcto, documento sin tabla, aprobaciones duplicadas) y registra los resultados.
* **Resultado esperado:** documento corto con tres escenarios de prueba y resultados (OK / issue).

**Paso 8.** Incluye el manejo de errores razonable (validaciones de entrada, condiciones para datos faltantes) y logging de fallos en una tabla de errores en Dataverse.
* **Resultado esperado:** captura de la tabla de errores y ejemplo de registro.

**Paso 9.** Empaqueta los flujos dentro de una solución para ALM (añade flows a la solución, define el _environment_ "variables" si aplica).
* **Resultado esperado:** archivo comprimido .zip que contenga los flujos de la solución.

