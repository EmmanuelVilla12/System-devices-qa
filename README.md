# System-devices-qa · Diseño de pruebas por HU con Scrum

Repositorio del **Grupo 1** (ficha 3229209, SENA ADSO, competencia *Pruebas de Software y SCRUM*) para la evidencia **GA-220501096-05-EV05 – Diseño de pruebas por historia de usuario con Scrum**, sobre el proyecto **Device Systems**. Instructor y Product Owner: Carlos Enrique Navia Torres.

## Propósito

Contener el diseño de pruebas de las 7 historias de usuario del Grupo 1 (módulo `ACC` Acceso y sesión): análisis, criterios, técnicas, escenarios, plan, matriz de trazabilidad, datos, casos y scripts. La ejecución y la evaluación quedan preparadas en estado **No ejecutado** para el Tema 6.

## Enlaces

| Recurso | Enlace |
|---|---|
| Organización del equipo | `00_Organizacion/` (por completar) |
| Sprint 1 | `Sprint_1/` (por completar) |
| GitHub Project | Por completar |
| Issues | [Issues del repositorio](https://github.com/EmmanuelVilla12/System-devices-qa/issues) |
| Pull requests | [Pull requests](https://github.com/EmmanuelVilla12/System-devices-qa/pulls) |

## Índice de HU

| HU | Módulo de origen | Responsable | Revisor | Carpeta | Rama | Issue |
|---|---|---|---|---|---|---|
| HU-001 Registrar una cuenta | ACC · Acceso y sesión | @EmmanuelVilla12 | Grupo 5 (por designar) | [Proceso_Pruebas_HU-001_Registrar_una_cuenta](01_Acceso_y_sesion/Proceso_Pruebas_HU-001_Registrar_una_cuenta/) | `qa/hu-001` | Por enlazar |
| HU-002 Iniciar sesión | ACC · Acceso y sesión | @EmmanuelVilla12 | Grupo 5 (por designar) | [Proceso_Pruebas_HU-002_Iniciar_sesion](01_Acceso_y_sesion/Proceso_Pruebas_HU-002_Iniciar_sesion/) | `qa/hu-002` | Por enlazar |
| HU-003 Conservar la sesión al recargar | ACC · Acceso y sesión | @EmmanuelVilla12 | Grupo 5 (por designar) | [Proceso_Pruebas_HU-003_Conservar_la_sesion_al_recargar](01_Acceso_y_sesion/Proceso_Pruebas_HU-003_Conservar_la_sesion_al_recargar/) | `qa/hu-003` | Por enlazar |
| HU-004 Consultar el perfil | ACC · Acceso y sesión | @MaicollR33 | Grupo 5 (por designar) | [Proceso_Pruebas_HU-004_Consultar_el_perfil](01_Acceso_y_sesion/Proceso_Pruebas_HU-004_Consultar_el_perfil/) | `qa/hu-004` | Por enlazar |
| HU-005 Cerrar la sesión | ACC · Acceso y sesión | @jhoncardona-dev | Grupo 5 (por designar) | [Proceso_Pruebas_HU-005_Cerrar_la_sesion](01_Acceso_y_sesion/Proceso_Pruebas_HU-005_Cerrar_la_sesion/) | `qa/hu-005` | Por enlazar |
| HU-006 Finalizar una sesión inválida | ACC · Acceso y sesión | @emanuelcastanoespinoza-creator | Grupo 5 (por designar) | [Proceso_Pruebas_HU-006_Finalizar_una_sesion_invalida](01_Acceso_y_sesion/Proceso_Pruebas_HU-006_Finalizar_una_sesion_invalida/) | `qa/hu-006` | Por enlazar |
| HU-009 Informar una página inexistente | ACC · Acceso y sesión | @esneiderj159-ai | Grupo 5 (por designar) | [Proceso_Pruebas_HU-009_Informar_una_pagina_inexistente](01_Acceso_y_sesion/Proceso_Pruebas_HU-009_Informar_una_pagina_inexistente/) | `qa/hu-009` | Por enlazar |

Las carpetas de cada HU llegan a `main` cuando el Grupo 5 aprueba la pull request de su rama `qa/hu-NNN`. Mientras tanto se consultan en la rama correspondiente.

## Cómo se trabaja

1. Cada responsable crea su rama desde `main`: `qa/hu-NNN`.
2. Diseña solo dentro de su carpeta `01_Acceso_y_sesion/Proceso_Pruebas_HU-NNN_<Nombre>/`, con la misma estructura de la HU-001.
3. Hace tres commits: `preparacion`, `implementacion`, `ejecucion y evaluacion en estado no ejecutado`.
4. Sube la rama y abre una pull request hacia `main` enlazada a su issue.
5. El Grupo 5 revisa con la lista de `2.7_Revision_por_pares.md`; la PR se fusiona solo después de su aprobación.

## Nomenclatura del Grupo 1

| HU | Funcionalidad | Prefijo de caso |
|---|---|---|
| HU-001 | `REG` | `ACC-REG-NNN` |
| HU-002 | `ING` | `ACC-ING-NNN` |
| HU-003 | `REC` | `ACC-REC-NNN` |
| HU-004 | `PER` | `ACC-PER-NNN` |
| HU-005 | `CIE` | `ACC-CIE-NNN` |
| HU-006 | `INV` | `ACC-INV-NNN` |
| HU-009 | `PNE` | `ACC-PNE-NNN` |

Escenario `ESC-ACC-FUN-NNN` · caso `ACC-FUN-NNN` (sin prefijo «CP») · script `SCR-ACC-FUN-NNN` · dato `D-NNN[A-D]` · pregunta al PO `PA-NN` · incidencia `INC-ACC-FUN-NNN`.
