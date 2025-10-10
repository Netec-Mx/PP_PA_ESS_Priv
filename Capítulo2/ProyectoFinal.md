# Proyecto Final - Power Apps

El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos, y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad.


## Duración aproximada:
- 60 minutos.


## Desarrollo del proyecto

Los usuarios del banco actualmente usan Excel y correos para capturar solicitudes y hacer seguimiento. Con Power Apps se construirá una interfaz amigable para captura (Canvas) y una app Model-driven para gestión centralizada y reporting, conectadas a Dataverse/SharePoint.

**Pasos que debes realizar**

1. Definir el modelo de datos mínimo en Dataverse: entidades como Solicitud, Aprobación, Adjunto, Usuario, Log. Definir campos clave (monto, tipo, fecha, estado, aprobador).
* **Entregable:** diagrama ER simple o lista de tablas y campos.

2. Crear la app Canvas (primer prototipo):
* Crear pantalla de inicio, pantalla de creación de solicitud con formulario (campos obligatorios marcados).
* Agregar control para adjuntar archivos (guardarlos en SharePoint o en Dataverse como nota/attachment).
* Añadir botón “Enviar” que llame al flujo de aprobación (usar Power Automate como conector desde Power Apps).
* **Entregable:** diagrama simple (imagen) con triggers y destinos.

3. Conectar y validar CRUD: configurar conexiones a Dataverse/SharePoint/Excel y comprobar que crear/leer/actualizar/borrar funcionan desde la app.
* **Entregable:** breve video o secuencia de capturas demostrando CRUD.

4. Refinar la UX en Power Apps Studio: usar reglas (Visible, DisplayMode), validar entradas (IsBlank, IsNumeric) y optimizar navegación.
* **Entregable:** lista de 5 mejoras UX aplicadas y capturas.

5. Implementar la integración con el flujo de aprobación:
* Pasar parámetros necesarios (ID de solicitud, monto, aprobador) al flujo desde Power Apps.
* Manejar la respuesta del flujo para cambiar estado en Dataverse.
* **Entregable:** captura del binding del botón que llama al flujo y de la respuesta aplicada al registro.

6. Integrar IA de forma práctica (opción sencilla con AI Builder o servicio externo):
* Usar un modelo de clasificación de texto para auto-clasificar tipo de solicitud o priorización.
* Mostrar la clasificación en la app y permitir corrección manual.
* Registrar la predicción y la confianza en Dataverse para posterior evaluación.
* **Entregable:** capturas de la integración IA.

7. Crear la aplicación Model-driven para backoffice:
* Importar las tablas a la solución, diseñar vistas (Pendientes, En Proceso, Aprobadas), formularios y dashboards con charts sencillos.
* Configurar procesos de negocio (business process flows) para guiar la gestión de aprobaciones.
* **Entregable:** capturas de vistas y dashboard en la aplicación model-driven.

8. Probar el flujo completo: crear solicitud en Canvas → invocar flujo → registrar aprobación → visualizar en Model-driven → generar fila en reporte consolidado.
* **Entregable:** documento con pasos de prueba y evidencias (capturas).

9. Exportar la Canvas app y la Model-driven app dentro de la solución (agregar dependencias, environment variables) y exportar archivo .zip de la solución.
* **Entregable:** .zip de solución + breve guía de instalación (1 página).
