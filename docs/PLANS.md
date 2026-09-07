# Planificación y ejecución

## Propósito

Convertir objetivos y decisiones aprobadas en trabajo ejecutable y verificable, sin exigir un plan formal para cada tarea.

## Cuándo crear un plan

Un proyecto nuevo requiere un ExecPlan inicial aprobado y autorizado antes de comenzar a codificar.

Los trabajos amplios, arriesgados, ambiguos o que afecten varias partes del sistema deben documentarse como ExecPlans. Las tareas pequeñas y claras pueden gestionarse sin un plan persistente conforme a las instrucciones globales.

## Contenido de un plan

Un plan no trivial debe indicar:

* Responsable de aprobación.
* Fecha de creación y última actualización.
* Objetivo y resultado esperado.
* Alcance y exclusiones relevantes.
* Decisiones aprobadas que debe respetar.
* Cuestiones pendientes que bloquean o condicionan el trabajo.
* Etapas o tareas necesarias.
* Entorno y herramientas necesarios para preparar, ejecutar, observar, verificar y restablecer el sistema.
* Criterios de aceptación.
* Verificaciones previstas.
* Estado conforme al ciclo definido en este documento.
* Historial breve de los cambios de estado, con fecha y actor.

No es necesario rellenar apartados que no aporten información útil.

El ExecPlan inicial debe incluir la activación descrita en `docs/BOOTSTRAP.md`. Sus pasos de configuración o scaffolding también requieren que el plan alcance el estado `Autorizado`; preparar el entorno no autoriza por sí mismo el desarrollo posterior.

## Estados y autorización

Todo ExecPlan debe mostrar un único estado actual entre los siguientes:

1. `Borrador`: propuesta editable; no autoriza implementación.
2. `Aprobado`: el responsable acepta el plan; todavía no autoriza implementación.
3. `Autorizado`: el responsable permite comenzar su ejecución.
4. `En curso`: Codex ha comenzado a ejecutar el plan autorizado.
5. `Verificado`: el resultado se ha contrastado con los criterios de aceptación y se ha registrado la evidencia.
6. `Aceptado`: el responsable acepta el resultado verificado.
7. `Cancelado`: el responsable decide cerrar el plan sin aceptar su resultado; debe registrarse el motivo.

Codex puede crear y modificar borradores y registrar el avance a `En curso` o `Verificado` cuando exista evidencia. Solo el responsable puede aprobar un plan, autorizar su ejecución, aceptar el resultado o cancelar el plan; Codex puede reflejar esos cambios de estado después de recibir una indicación explícita.

La indicación humana puede originarse en una conversación, issue u otro canal, pero debe reflejarse en el ExecPlan con fecha y actor. El campo de estado actual del ExecPlan es la fuente canónica. No es necesario copiar la conversación ni crear un commit específico para que la transición sea válida.

La presencia de un archivo en `docs/exec-plans/active/` no implica que esté aprobado o autorizado. La aprobación tampoco implica autorización. Si aparece una decisión técnica nueva o un cambio de alcance durante la ejecución, debe solicitarse aprobación antes de continuar por ese camino.

## Progreso

Los planes que no estén `Aceptados` ni `Cancelados` se conservan en `docs/exec-plans/active/`. Deben reflejar el estado y el progreso reales, los bloqueos relevantes y los cambios aprobados.

No es necesario registrar cada acción mecánica.

No se aplica una caducidad automática. Antes de reanudar un plan cuya última actualización ya no represente claramente el estado del repositorio, comprueba que su objetivo, alcance y decisiones siguen vigentes y actualiza el plan. Si el trabajo ya no debe continuar, propone su cancelación al responsable en lugar de dejarlo indefinidamente `En curso`.

## Finalización

Un plan cumple su objetivo únicamente cuando alcanza el estado `Aceptado`. Los planes `Aceptados` y `Cancelados` están cerrados y se conservan en `docs/exec-plans/completed/`; un plan cancelado no se presenta como trabajo completado ni verificado.

Las decisiones duraderas surgidas durante el trabajo deben quedar registradas en `docs/design-docs/index.md` y, cuando necesiten desarrollo propio, documentadas en `docs/design-docs/`. La deuda técnica accionable se registra en `docs/exec-plans/tech-debt-tracker.md` cuando corresponda.

## Automatizaciones

Los procedimientos de verificación, revisión o entrega podrán automatizarse cuando el responsable lo apruebe. Este documento no autoriza su activación.
