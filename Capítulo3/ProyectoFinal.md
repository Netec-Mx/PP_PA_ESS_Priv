# Práctica 3. Gobernanza en Power Platform

## Objetivos
Al finalizar la práctica, serás capaz de:
- Definir políticas de acceso, roles y permisos para garantizar que solo usuarios autorizados ejecuten, modifiquen o administren flujos y aplicaciones. 
- Empaquetar las soluciones en entornos de desarrollo, pruebas y producción, aplicando supervisión y monitoreo continuo para prevenir riesgos operativos.

## Duración aproximada
- 30 minutos.

## Instrucciones
El Banco Futuro busca modernizar sus procesos internos relacionados con la gestión de solicitudes de clientes y empleados, la aprobación de créditos y gastos y la gestión de accesos a aplicaciones internas. Actualmente, muchos de estos procesos se realizan manualmente con archivos de Excel, correos electrónicos y aprobaciones informales, lo que genera retrasos, errores y falta de trazabilidad. Sin gobernanza, el banco corre riesgos: fugas de datos por conectores inseguros, entornos no controlados y falta de trazabilidad. 

### Tarea 1. Configurar entornos, políticas DLP, roles y _pipelines_ para asegurar control y permitir despliegues ordenados

**Paso 1.** Revisa y documenta los entornos disponibles: Dev, Test, Prod. Anota quién es responsable de cada uno.
* **Resultado esperado:** tabla con entornos, propósito y responsables.

**Paso 2.** Configura políticas DLP (Data Loss Prevention).
* Define los grupos de conectores prohibidos y restringidos para el banco (por ejemplo: evitar conectores personales o no soportados).
* Aplica las políticas a entornos críticos (_Test/Prod_).
* **Resultado esperado:** captura de la política DLP aplicada.

**Paso 3.** Crea un rol de seguridad en Dataverse con permisos mínimos necesarios para un aprobador y otro para un administrador (crear seguridad por capas).
* Define los permisos CRUD por entidad (Solicitud: crear o leer; Aprobación: leer o actualizar).
* **Resultado esperado:** captura del rol y la lista de permisos asignados.

**Paso 4.** Monitorea la salud y el uso: revisa los paneles de capacidad, las ejecuciones de flujos con mayor latencia o fallas frecuentes y el consumo de capacidad de Dataverse.
* Registra las métricas clave: número de ejecuciones por día, promedio de latencia, total de aprobaciones procesadas.
* **Resultado esperado:** captura de métricas y un pequeño análisis (1 párrafo).


