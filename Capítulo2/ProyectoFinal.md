# Práctica 2.1. Proyecto final: Power Apps

## Objetivos
Al finalizar la práctica, serás capaz de:
- Desarrollar apps que permitan a los usuarios cargar datos, consultar información y disparar aprobaciones de manera simple e intuitiva. 
- Exponer flujos de aprobación y carga de archivos dentro de la app para centralizar la operación en una sola interfaz, evitando el uso de múltiples plataformas.


## Duración aproximada
- 60 minutos.

## Instrucciones
El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad.

### Tarea 1. Con Power Apps, construir una interfaz amigable para captura (Canvas) y una app Model-Driven para la gestión centralizada y reporting, conectadas a Dataverse o SharePoint

**Paso 1.** Define el modelo de datos mínimo en Dataverse: entidades como _Solicitud_, _Aprobación_, _Adjunto_, _Usuario_, _Log_. Define los campos clave (monto, tipo, fecha, estado, aprobador).
* **Resultado esperado:** diagrama ER simple o lista de tablas y campos.

**Paso 2.** Crea la app Canvas (primer prototipo).
* Crea la pantalla de inicio: pantalla de creación de la solicitud con formulario (campos obligatorios marcados).
* Agrega el control para adjuntar archivos (guárdalos en SharePoint o en Dataverse como nota o _attachment_).
* Añade el botón “Enviar” que llame al flujo de aprobación (usa Power Automate como conector desde Power Apps).
* **Resultado esperado:** diagrama simple (imagen) con disparadores y destinos.

**Paso 3.** Conecta y valida CRUD: configura conexiones a Dataverse, SharePoint o Excel y comprueba que _Crear_, _Leer_, _Actualizar_ y _Borrar_ funcionan desde la app.
* **Resultado esperado:** breve video o secuencia de capturas demostrando CRUD.

**Paso 4.** Refina la UX en Power Apps Studio: usa reglas (Visible, DisplayMode), valida lasentradas (IsBlank, IsNumeric) y optimiza la navegación.
* **Resultado esperado:** lista de cinco mejoras UX aplicadas y capturas.

**Paso 5.** Implementa la integración con el flujo de aprobación.
* Pasa parámetros necesarios (ID de solicitud, monto, aprobador) al flujo desde Power Apps.
* Maneja la respuesta del flujo para cambiar estado en Dataverse.
* **Resultado esperado:** captura del binding del botón que llama al flujo y de la respuesta aplicada al registro.

**Paso 6.** Integra IA de forma práctica (opción sencilla con AI Builder o servicio externo).
* Usa un modelo de clasificación de texto para autoclasificar el tipo de solicitud o la priorización.
* Muestra la clasificación en la app y permite la corrección manual.
* Registra la predicción y la confianza en Dataverse para una evaluación posterior.
* **Resultado esperado:** capturas de la integración IA.

**Paso 7.** Crea la aplicación Model-Driven para Backoffice.
* Importa las tablas a la solución, diseña vistas (_Pendientes_, _En Proceso_, _Aprobadas_), formularios y _dashboards_ con _charts_ sencillos.
* Configura los procesos de negocio (_business process flows_) para guiar la gestión de aprobaciones.
* **Resultado esperado:** capturas de vistas y _dashboard_ en la aplicación Model-Driven.

**Paso 8.** Prueba el flujo completo: crea una solicitud en Canvas → invoca un flujo → registra una aprobación → visualiza en Model-Driven → genera una fila en elreporte consolidado.
* **Resultado esperado:** documento con pasos de prueba y evidencias (capturas).

**Paso 9.** Exporta la Canvas app y la Model-Driven app dentro de la solución (agregar dependencias, environment variables) y exporta el archivo .zip de la solución.
* **Resultado esperado:** .zip de solución + breve guía de instalación (1 página).

