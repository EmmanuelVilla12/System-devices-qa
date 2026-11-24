# Proceso de pruebas · HU-001 Registrar una cuenta

**Empieza aquí:** [Flujo metodológico](00_Flujo_metodologico.md) · [Nomenclatura](00_Nomenclatura.md)

| Control del banco | Valor |
|---|---|
| Proyecto | Device Systems |
| Equipo | Grupo 1 · ficha 3229209 · SENA ADSO |
| Evidencia | GA-220501096-05-EV05 · Diseño de pruebas por historia de usuario con Scrum |
| Historia | HU-001 Registrar una cuenta · RF-001 · Prioridad Alta |
| Versión del banco | 1.0 |
| Versión del producto | Por confirmar antes de ejecutar |
| Responsable de elaboración | Emmanuel Villa Valencia (@EmmanuelVilla12) |
| Responsable de revisión | Por designar por el Grupo 5 |
| Última actualización | 24/11/2026 |
| Estado del artefacto | Borrador para revisión por pares |
| Estado de ejecución | No ejecutado |

## Organización del directorio

```text
Proceso_Pruebas_HU-001_Registrar_una_cuenta/
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
│   ├── 2.4_Casos_de_prueba/      00_Indice_de_casos.md · _Plantilla_Caso.md · ACC-REG-001 … 021
│   ├── 2.5_Scripts_de_prueba/    _Plantilla_Script.md · SCR-ACC-REG-001 … 021
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
| Criterios de aceptación | 7 |
| Condiciones de calidad de la ficha | 4 (RNF-001, RNF-004, RNF-005, RNF-006) |
| Escenarios | 21 |
| Casos de prueba | 21 |
| Scripts de prueba | 21 |
| Preguntas abiertas al PO | 7 |

## Convención de identificadores

| Artefacto | Formato | Significado |
|---|---|---|
| Escenario | `ESC-ACC-REG-NNN` | `ACC` = módulo Acceso y sesión · `REG` = Registro de cuenta · `NNN` = consecutivo |
| Caso | `ACC-REG-NNN` | Mismo consecutivo del escenario (sin prefijo «CP») |
| Script | `SCR-ACC-REG-NNN` | Desarrolla el caso con el mismo número |
| Dato | `D-NNN[A-D]` | Fila de la hoja de datos; la letra distingue envíos del mismo caso |
| Pregunta abierta | `PA-NN` | Duda para el Product Owner registrada en el refinamiento |
| Incidencia | `INC-ACC-REG-NNN` | Consecutivo propio (sin incidencias: no hay ejecución) |

Los códigos no se renumeran si cambia el orden de ejecución; un artefacto retirado se marca «obsoleto» y su código no se reutiliza. Los códigos oficiales HU-001, RF-001 y CA-HU-001-XX se conservan.

## Estado de los artefactos

Borrador → Revisado (tras 2.7, por el Grupo 5) → Aprobado (aceptado por el PO) → Obsoleto (si la historia cambia).

[Volver al repositorio](../../README.md)
