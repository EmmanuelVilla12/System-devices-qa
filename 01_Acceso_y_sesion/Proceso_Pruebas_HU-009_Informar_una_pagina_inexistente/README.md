# HU-009 · Informar una página inexistente

## Información general

| Elemento | Información |
|---|---|
| Historia de usuario | HU-009 · Informar una página inexistente |
| Identificador funcional | RF-009 |
| Módulo | ACC · Acceso y sesión |
| Funcionalidad | PNE · Página no encontrada |
| Responsable | @esneiderj159-ai |
| Revisor | Por designar por el Grupo 5 |
| Versión | 1.0 |
| Estado del artefacto | Borrador para revisión por pares |
| Estado de ejecución | No ejecutado |

## Objetivo

Documentar el diseño de pruebas para verificar que la aplicación informe correctamente cuando una persona intenta ingresar a una dirección que no corresponde a una página existente.

También se comprobará que una página existente con restricciones de acceso no sea confundida con una página inexistente.

## Alcance

Este proceso contempla:

- Análisis de la historia de usuario HU-009.
- Identificación de criterios de aceptación.
- Diseño de escenarios y casos de prueba.
- Preparación de datos de prueba.
- Elaboración de scripts manuales.
- Documentación del ambiente de pruebas.
- Preparación del registro de ejecución y evaluación.

No contempla la ejecución de pruebas ni la modificación del funcionamiento de la aplicación.

## Criterios de aceptación

- CA-HU-009-01: Una dirección inexistente debe mostrar el mensaje «Página no encontrada», evitando una pantalla en blanco.
- CA-HU-009-02: La respuesta debe ser comprensible tanto para visitantes como para personas autenticadas.
- CA-HU-009-03: Una página existente con acceso restringido debe aplicar las reglas de acceso correspondientes a HU-008.
- CA-HU-009-04: La consulta de una dirección inexistente no debe crear ni modificar registros del sistema.

## Estructura documental

| Carpeta | Contenido |
|---|---|
| 01_Preparacion | Análisis, criterios, técnicas y escenarios. |
| 02_Implementacion | Plan, trazabilidad, datos, casos y scripts. |
| 03_Ejecucion | Preparación y registro de ejecución. |
| 04_Evaluacion | Incidencias, resultados y mejora continua. |

## Documentos principales

- [Flujo metodológico](00_Flujo_metodologico.md)
- [Nomenclatura](00_Nomenclatura.md)
- [Análisis de la HU](01_Preparacion/1.1_Analisis_de_la_HU.md)
- [Criterios de aceptación](01_Preparacion/1.2_Criterios_de_aceptacion.md)
- [Escenarios de prueba](01_Preparacion/1.4_Escenarios_de_prueba.md)
- [Plan de pruebas](02_Implementacion/2.1_Plan_de_pruebas.md)
- [Matriz de trazabilidad](02_Implementacion/2.2_Matriz_de_trazabilidad.md)
- [Datos de prueba](02_Implementacion/2.3_Datos_de_prueba.md)
- [Índice de casos](02_Implementacion/2.4_Casos_de_prueba/00_Indice_de_casos.md)

## Estado actual

Los documentos corresponden al diseño de pruebas. No se ha registrado ninguna ejecución, evidencia, resultado ni incidencia.

La documentación queda pendiente de revisión por pares por parte del Grupo 5.
