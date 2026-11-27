# Nomenclatura y codificación · HU-006

[Portada](README.md) · [Flujo metodológico](00_Flujo_metodologico.md)

Esta sección explica cómo se leen y cómo se construyen los códigos del banco de pruebas de HU-006. Cada código identifica un solo artefacto y permite seguir la cadena **historia → criterio → escenario → caso → script → resultado → incidencia**.

## 1. Anatomía de un código de prueba

```text
SCR - ACC - INV - 001
     │     │     │     └── Consecutivo: tres dígitos, empieza en 001
     │     │     └────── Funcionalidad: Finalizar sesión inválida
     │     └────────────── Módulo: Acceso y sesión
     └──────────────────── Tipo de artefacto: Script
```

Un caso y su script comparten el módulo, la funcionalidad y el consecutivo. Solo cambia el prefijo:

| Artefacto | Código | Se lee |
|---|---|---|
| Escenario | `ESC-ACC-INV-001` | Escenario 1 de sesión inválida, módulo Acceso |
| Caso de prueba | `ACC-INV-001` | Caso 1 de sesión inválida, módulo Acceso |
| Script de prueba | `SCR-ACC-INV-001` | Script que ejecuta el caso ACC-INV-001 |
| Incidencia | `INC-ACC-INV-001` | Primera incidencia de sesión inválida (aún no existe ninguna) |

## 2. Códigos de los requisitos (los entrega el equipo de producto)

Estos códigos ya vienen definidos en la especificación. El banco de pruebas los conserva tal como están.

| Prefijo | Significado | Formato | Ejemplo | Dónde aparece |
|---|---|---|---|---|
| HU | Historia de usuario | `HU-NNN` | `HU-006` Finalizar una sesión inválida | Todos los artefactos |
| RF | Requisito funcional | `RF-NNN` | `RF-006` | Ficha de la historia, casos |
| RN | Regla de negocio | `RN-NNN` | `RN-001` | Análisis de la historia |
| RNF | Requisito no funcional (condición de calidad) | `RNF-NNN` | `RNF-002` | Criterios de calidad, casos no funcionales |
| CA | Criterio de aceptación | `CA-HU-NNN-NN` | `CA-HU-006-01` | Matriz, casos |

**Cómo leer `CA-HU-006-01`:** criterio de aceptación (`CA`), de la historia `HU-006`, número `01`.

## 3. Códigos del banco de pruebas (los crea el equipo de pruebas)

| Prefijo | Artefacto | Formato | Ejemplo | Regla |
|---|---|---|---|---|
| ESC | Escenario | `ESC-MOD-FUN-NNN` | `ESC-ACC-INV-001` | Un escenario por condición que cambia el resultado |
| *(sin prefijo)* | Caso de prueba | `MOD-FUN-NNN` | `ACC-INV-001` | Al menos un caso por escenario; nunca se antepone «CP» |
| SCR | Script de prueba | `SCR-MOD-FUN-NNN` | `SCR-ACC-INV-001` | Un script por caso, mismo consecutivo |
| D | Dato de prueba | `D-NNN` o `D-NNNX` | `D-001A` | `NNN` = caso que lo usa; la letra distingue varios envíos del mismo caso |
| PA | Pregunta abierta al Product Owner | `PA-NN` | `PA-01` | Se registra en el acta de refinamiento |
| C | Corrida de ejecución | `C-NNN` | `C-001` | Cada ejecución o reprueba es una corrida nueva (Tema 6) |
| INC | Incidencia o defecto | `INC-MOD-FUN-NNN` | `INC-ACC-INV-001` | Consecutivo propio, independiente del caso |

### Ejemplo de datos con letra

| Código | Caso | Significado |
|---|---|---|
| `D-001` | ACC-INV-001 | Único conjunto de datos del caso 1 |
| `D-001A` | ACC-INV-001 | Envío o variante 1 del caso 1 |

## 4. Códigos de módulo y funcionalidad

El código de **módulo** tiene tres letras y agrupa historias relacionadas. El código de **funcionalidad** tiene tres letras y nombra la acción de la historia.

### Módulos de Device Systems (Grupo 1)

| Código | Módulo | Historias del Grupo 1 |
|---|---|---|
| `ACC` | Acceso y sesión | HU-001, HU-002, HU-003, HU-004, HU-005, HU-006, HU-009 |

### Funcionalidades frecuentes (Grupo 1)

| HU | Funcionalidad | Prefijo de caso | Carpeta de la HU |
|---|---|---|---|
| HU-001 Registrar una cuenta | `REG` | `ACC-REG-NNN` | `Proceso_Pruebas_HU-001_Registrar_una_cuenta` |
| HU-002 Iniciar sesión | `ING` | `ACC-ING-NNN` | `Proceso_Pruebas_HU-002_Iniciar_sesion` |
| HU-003 Conservar la sesión al recargar | `REC` | `ACC-REC-NNN` | `Proceso_Pruebas_HU-003_Conservar_la_sesion_al_recargar` |
| HU-004 Consultar el perfil | `PER` | `ACC-PER-NNN` | `Proceso_Pruebas_HU-004_Consultar_el_perfil` |
| HU-005 Cerrar la sesión | `CIE` | `ACC-CIE-NNN` | `Proceso_Pruebas_HU-005_Cerrar_la_sesion` |
| HU-006 Finalizar una sesión inválida | `INV` | `ACC-INV-NNN` | `Proceso_Pruebas_HU-006_Finalizar_una_sesion_invalida` |
| HU-009 Informar una página inexistente | `PNE` | `ACC-PNE-NNN` | `Proceso_Pruebas_HU-009_Informar_una_pagina_inexistente` |

**Para codificar una historia nueva:** (1) identificar el módulo; (2) elegir el verbo principal de la narrativa «quiero…»; (3) verificar que la combinación `MOD-FUN` no exista; (4) iniciar el consecutivo en `001`.

## 5. Estados

### Estado del artefacto (casos, scripts, plan)

| Estado | Significado |
|---|---|
| Borrador | En elaboración; aún no revisado |
| Revisado | Pasó la revisión por pares del Grupo 5 y se aplicaron los ajustes |
| Aprobado | Aceptado por el Product Owner como base de la prueba |
| Obsoleto | Ya no corresponde a la historia vigente; se conserva, no se borra |

### Estado de ejecución (por caso y corrida)

| Estado | Significado |
|---|---|
| No ejecutado | Aún no hay intento en la versión indicada (estado actual de todos los casos) |
| Pasó | Se observaron todos los resultados esperados |
| Falló | Al menos un resultado observado difiere del esperado |
| Bloqueado | No se pudo ejecutar por falta de precondición, ambiente, datos o permisos |

### Estado de la incidencia

`Nuevo → Abierto → Asignado → Corregido → Verificado → Cerrado`, con las salidas `Rechazado`, `Diferido` y `Reabierto`. El detalle está en [4.1 Gestión de incidencias](04_Evaluacion/4.1_Gestion_de_incidencias.md).

## 6. Clasificación de escenarios

| Tipo | Significado | Ejemplo en HU-006 |
|---|---|---|
| Básico (*happy path*) | Recorrido principal con datos válidos | ESC-ACC-INV-001 sesión caducada – happy path |
| Alterno | Variante válida del recorrido | ESC-ACC-INV-002 sesión rechazada como inválida |
| Excepción (*error path*) | El sistema debe rechazar o informar un error | ESC-ACC-INV-004 rol insuficiente con sesión válida |
| Calidad | Verifica una condición no funcional de la ficha | ESC-ACC-INV-018 comunicado de nuevo ingreso |

## 7. Nombres de carpetas y archivos

| Patrón | Significado | Ejemplo |
|---|---|---|
| `00_` | Documentos de entrada: portada, flujo, nomenclatura | `00_Flujo_metodologico.md` |
| `01_` a `04_` | Fase del proceso, en orden de elaboración | `02_Implementacion/` |
| `N.M_` | Paso `M` de la fase `N` | `2.3_Datos_de_prueba.md` |
| `<código>.md` | Un archivo por caso o por script, nombrado con su código | `ACC-INV-001.md`, `SCR-ACC-INV-001.md` |
| `_Plantilla_*.md` | Plantilla vacía para nuevos casos o scripts | `_Plantilla_Caso.md` |
| `C-<corrida>_<caso>_paso<N>.png` | Evidencia de ejecución (se crea en el Tema 6) | `C-001_ACC-INV-001_paso2.png` |

## 8. Abreviaturas

| Abreviatura | Significado |
|---|---|
| PO | Product Owner (el instructor) |
| CA | Criterio de aceptación |
| ESC | Escenario |
| SCR | Script |
| INC | Incidencia |
| PA | Pregunta abierta |
| N.º | Número |
| ✓ / ✗ | Condición cumplida / no cumplida |
| ␠ | Representa un espacio en blanco dentro de un dato |

## 9. Reglas de estabilidad

1. **No renumerar.** Si cambia el orden de ejecución, la prioridad o el nombre, el código se mantiene; el orden se anota en la ficha del caso.
2. **No reutilizar.** Un código retirado se marca como *Obsoleto* y su número no se asigna a otro artefacto.
3. **Conservar los códigos oficiales.** HU, RF, RN, RNF y CA se copian tal como vienen de la especificación.
4. **Relación uno a uno entre caso y script.** `ACC-INV-001` siempre se ejecuta con `SCR-ACC-INV-001`.
5. **Tres dígitos en el consecutivo.** `001`, no `1`, para que los archivos se ordenen correctamente.