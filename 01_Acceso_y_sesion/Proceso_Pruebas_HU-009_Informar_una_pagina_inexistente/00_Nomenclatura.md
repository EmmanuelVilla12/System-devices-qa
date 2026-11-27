# Nomenclatura · HU-009

## Objetivo

Definir los identificadores utilizados en los documentos de diseño de pruebas de la historia HU-009.

## Identificadores

| Elemento | Formato | Ejemplo |
|---|---|---|
| Módulo | ACC | ACC |
| Funcionalidad | PNE | PNE |
| Escenario | ESC-ACC-PNE-NNN | ESC-ACC-PNE-001 |
| Caso de prueba | ACC-PNE-NNN | ACC-PNE-001 |
| Script | SCR-ACC-PNE-NNN | SCR-ACC-PNE-001 |
| Dato de prueba | D-NNN[A-D] | D-001A |
| Pregunta abierta | PA-NN | PA-01 |
| Incidencia | INC-ACC-PNE-NNN | INC-ACC-PNE-001 |

## Reglas

- NNN representa un consecutivo de tres dígitos que inicia en 001.
- Los identificadores de casos y scripts deben coincidir en su consecutivo.
- Cada caso tendrá un único script asociado.
- Cada dato debe estar documentado en el archivo de datos de prueba.
- Las preguntas abiertas se numeran desde PA-01.
- Las incidencias solo se identifican cuando exista una ejecución que permita registrarlas.
- No se deben reutilizar identificadores de otras historias de usuario.

## Estado

La nomenclatura queda definida para el diseño de pruebas de HU-009.
