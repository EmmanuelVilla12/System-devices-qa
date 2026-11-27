# Nomenclatura y codificación · HU-005

[Portada](README.md) · [Flujo metodológico](00_Flujo_metodologico.md)

| Artefacto | Formato | Regla |
|---|---|---|
| Escenario | `ESC-ACC-CIE-NNN` | Consecutivo desde 001 |
| Caso | `ACC-CIE-NNN` | Sin prefijo CP |
| Script | `SCR-ACC-CIE-NNN` | Mismo consecutivo del caso |
| Dato | `D-NNN[A-D]` | NNN identifica el caso; letra distingue variantes |
| Pregunta al PO | `PA-NN` | Se lleva a refinamiento |
| Incidencia | `INC-ACC-CIE-NNN` | Consecutivo propio |

Se conservan los códigos oficiales HU-005, RF-005, RNF-002, RNF-004, RNF-005 y CA-HU-005-01 a 04.

## Tabla del grupo

| HU | Funcionalidad | Prefijo de caso | Carpeta |
|---|---|---|---|
| HU-001 Registrar una cuenta | REG | ACC-REG-NNN | Proceso_Pruebas_HU-001_Registrar_una_cuenta |
| HU-002 Iniciar sesión | ING | ACC-ING-NNN | Proceso_Pruebas_HU-002_Iniciar_sesion |
| HU-003 Conservar la sesión al recargar | REC | ACC-REC-NNN | Proceso_Pruebas_HU-003_Conservar_la_sesion_al_recargar |
| HU-004 Consultar el perfil | PER | ACC-PER-NNN | Proceso_Pruebas_HU-004_Consultar_el_perfil |
| HU-005 Cerrar la sesión | CIE | ACC-CIE-NNN | Proceso_Pruebas_HU-005_Cerrar_la_sesion |
| HU-006 Finalizar una sesión inválida | INV | ACC-INV-NNN | Proceso_Pruebas_HU-006_Finalizar_una_sesion_invalida |
| HU-009 Informar una página inexistente | PNE | ACC-PNE-NNN | Proceso_Pruebas_HU-009_Informar_una_pagina_inexistente |

Los códigos no se renumeran ni reutilizan. Estado de artefacto: Borrador → Revisado → Aprobado. Ejecución actual: No ejecutado.
