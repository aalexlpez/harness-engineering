# AGENTS.md

## Contexto

Este repositorio utiliza un harness de desarrollo controlado. Las instrucciones globales de Codex y las skills disponibles siguen aplicándose. Este archivo añade las reglas específicas de gobierno del proyecto.

## Mapa del conocimiento

* `docs/product-specs/index.md`: definición, alcance y estado del proyecto.
* `docs/design-docs/index.md`: decisiones técnicas vigentes y propuestas pendientes.
* `ARCHITECTURE.md`: mapa de la arquitectura real y aprobada.
* `docs/BOOTSTRAP.md`: procedimiento para activar una nueva instancia y preparar sus capacidades.
* `docs/PLANS.md`: procedimiento de planificación y autorización.
* `docs/exec-plans/_template.md`: estructura mínima para crear un ExecPlan sin duplicar sus reglas.
* `docs/exec-plans/active/`: planes que todavía no han alcanzado un estado terminal.
* `docs/exec-plans/completed/`: planes cerrados como `Aceptado` o `Cancelado`.
* `docs/`: documentación específica que se consulta y completa solo cuando resulte aplicable.

Consulta únicamente los documentos relevantes para la tarea. No cargues toda la documentación por defecto.

## Autoridad

El responsable humano aprueba las decisiones técnicas, los cambios de alcance, los planes, la autorización para implementarlos, la aceptación de sus resultados, su cancelación y la activación de automatizaciones.

Una decisión técnica nueva es una elección duradera que establece o modifica el stack, la arquitectura, las dependencias relevantes, los contratos compartidos, la persistencia, la seguridad, el despliegue o los invariantes del proyecto. Los detalles locales y mecánicos cubiertos por decisiones existentes no son decisiones técnicas nuevas.

Puedes investigar, comparar alternativas y recomendar soluciones. No adoptes una decisión técnica nueva sin aprobación, aunque sea de bajo impacto o reversible, si no está cubierta por una decisión o convención previamente aprobada.

Una decisión solo está aprobada si figura expresamente con ese estado en `docs/design-docs/index.md`. Su mera presencia en la documentación no implica aprobación.

Una indicación humana expresada en una conversación, issue u otro canal debe reflejarse en el artefacto correspondiente para convertirse en estado durable. El estado actual registrado en la definición, el índice de decisiones o el ExecPlan es la fuente canónica; la conversación y el historial Git son evidencia, no sustitutos.

La autorización de un plan permite realizar sus pasos mecánicos dentro del alcance y las decisiones aprobadas. Si aparece una decisión pendiente o un cambio de alcance, detén el trabajo afectado y solicita aprobación. Puedes continuar con trabajo independiente ya autorizado.

Registra las decisiones que deban permanecer como conocimiento del proyecto. No es necesario documentar permanentemente cada elección local.

## Estado y autorización

Antes de implementar, consulta la definición del proyecto, las decisiones técnicas relevantes y el plan aplicable.

Si el proyecto está en definición, investigación o planificación, trabaja únicamente en esas actividades. No conviertas una propuesta en implementación.

Un proyecto nuevo requiere una definición aprobada, las decisiones técnicas necesarias aprobadas, un plan aprobado y autorización expresa para ejecutarlo. La ubicación o existencia de un documento no sustituye esos estados.

## Ejecución

Utiliza las instrucciones globales y las skills existentes para ejecutar, verificar y revisar el trabajo. No dupliques sus procedimientos.

Respeta las decisiones y convenciones vigentes. Si una tarea requiere cambiarlas, presenta la propuesta antes de continuar.

## Acciones externas

No configures ni actives automatizaciones por iniciativa propia.

## Mantenimiento del conocimiento

Actualiza la documentación cuando cambie la realidad que describe. Mantén este archivo como un mapa breve; coloca el conocimiento específico en los documentos correspondientes.

Si una limitación recurrente impide observar, ejecutar o verificar el sistema, trátala como una capacidad ausente: registra la evidencia y propone una herramienta, comando, prueba o documento reutilizable. No incorpores la solución sin la aprobación que corresponda.
