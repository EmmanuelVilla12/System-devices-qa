# Proceso de pruebas · HU-003 Conservar la sesión al recargar

**Empieza aquí:** [Flujo metodológico](00_Flujo_metodologico.md) · [Nomenclatura](00_Nomenclatura.md)

| Control del banco | Valor |
|---|---|
| Proyecto | Device Systems |
| Equipo | Grupo 1 · ficha 3229209 · SENA ADSO |
| Evidencia | GA-220501096-05-EV05 · Diseño de pruebas por historia de usuario con Scrum |
| Historia | HU-003 Conservar la sesión al recargar · RF-003 · Prioridad Alta |
| Versión del banco | 1.0 |
| Versión del producto | Por confirmar antes de ejecutar |
| Responsable de elaboración | Emmanuel Villa Valencia (@EmmanuelVilla12) |
| Responsable de revisión | Por designar por el Grupo 5 |
| Última actualización | 24/11/2026 |
| Estado del artefacto | Borrador para revisión por pares |
| Estado de ejecución | No ejecutado |

## Organización del directorio

```text
Proceso_Pruebas_HU-003_Conservar_la_sesion_al_recargar/
├── README.md
├── 00_Flujo_metodologico.md
├── 00_Nomenclatura.md
├── 01_Preparacion/
│   ├── 1.1_Analisis_de_la_HU.md
│   ├── 1.2_Criterios_de_aceptacion.md
│   ├── 1.3_Tipos_y_tecnicas_de_prueba.md
│   └── 1.4_Escenarios_de_prueba.md
├── 02_Implementacion/
│   ├── 2.1_Plan_de_pruebas.md
│   ├── 2.2_Matriz_de_trazabilidad.md
│   ├── 2.3_Datos_de_prueba.md  (+ .csv)
│   ├── 2.4_Casos_de_prueba/      00_Indice_de_casos.md · _Plantilla_Caso.md · ACC-REC-001 … 008
│   ├── 2.5_Scripts_de_prueba/    _Plantilla_Script.md · SCR-ACC-REC-001 … 008
│   ├── 2.6_Ambiente_de_pruebas.md
│   └── 2.7_Revision_por_pares.md
├── 03_Ejecucion/
│   ├── 3.1_Preparacion_de_la_ejecucion.md
│   └── 3.2_Registro_de_ejecucion.md
└── 04_Evaluacion/
    ├── 4.1_Gestion_de_incidencias.md
    ├── 4.2_Informe_de_resultados.md
    └── 4.3_Plan_de_mejora_continua.md
```

## Resumen del banco

| Elemento | Cantidad |
|---|---:|
| Criterios de aceptación | 4 |
| Condiciones de calidad de la ficha | 3 (RNF-002, RNF-004, RNF-005) |
| Escenarios | 8 |
| Casos de prueba | 8 |
| Scripts de prueba | 8 |
| Preguntas abiertas al PO | 4 |

## Convención de identificadores

| Artefacto | Formato | Significado |
|---|---|---|
| Escenario | `ESC-ACC-REC-NNN` | `ACC` = módulo Acceso y sesión · `REC` = Recarga con sesión · `NNN` = consecutivo |
| Caso | `ACC-REC-NNN` | Mismo consecutivo del escenario (sin prefijo «CP») |
| Script | `SCR-ACC-REC-NNN` | Desarrolla el caso con el mismo número |
| Dato | `D-NNN[A-D]` | Fila de la hoja de datos; la letra distingue envíos del mismo caso |
| Pregunta abierta | `PA-NN` | Duda para el Product Owner registrada en el refinamiento |
| Incidencia | `INC-ACC-REC-NNN` | Consecutivo propio (sin incidencias: no hay ejecución) |

Los códigos no se renumeran si cambia el orden de ejecución; un artefacto retirado se marca «obsoleto» y su código no se reutiliza. Los códigos oficiales HU-003, RF-003 y CA-HU-003-XX se conservan.

## Estado de los artefactos

Borrador → Revisado (tras 2.7, por el Grupo 5) → Aprobado (aceptado por el PO) → Obsoleto (si la historia cambia).

[Volver al repositorio](../../README.md)
