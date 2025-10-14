# Proyecto Final - Gobernanza en Power Platform

El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos, y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad.


## Duración aproximada:
- 30 minutos.


## Desarrollo del proyecto

Sin gobernanza el banco corre riesgos: fugas de datos por conectores inseguros, entornos no controlados y falta de trazabilidad. En esta sección se configurarán entornos, políticas DLP, roles y pipelines para asegurar control y permitir despliegues ordenados.

**Pasos que debes realizar**

1. Revisar y documentar los entornos disponibles: Dev, Test, Prod. Anotar quién es responsable de cada uno.
* **Entregable:** tabla con entornos, propósito y responsables.

2. Configurar políticas DLP (Data Loss Prevention):
* Definir grupos de conectores prohibidos/restringidos para el banco (por ejemplo: evitar conectores personales o no soportados).
* Aplicar políticas a entornos críticos (Test/Prod).
* **Entregable:** captura de la política DLP aplicada.

3. Crear un rol de seguridad en Dataverse con permisos mínimos necesarios para un aprobador y otro para un administrador (crear seguridad por capas).
* Definir permisos CRUD por entidad (Solicitud: crear/leer; Aprobación: leer/actualizar).
* **Entregable:** captura del rol y la lista de permisos asignados.

4. Monitorear salud y uso: revisar paneles de capacidad, ejecuciones de flows con mayor latencia o fallas frecuentes y consumo de capacidad de Dataverse.
* Registrar métricas clave: número de ejecuciones/día, promedio de latencia, número de aprobaciones procesadas.
* **Entregable:** captura de métricas y un pequeño análisis (1 párrafo).