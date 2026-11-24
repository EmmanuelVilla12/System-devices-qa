# SCR-ACC-REG-016 · Rechazar la cuarta solicitud de registro dentro del mismo minuto

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-016.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-016 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que hasta 3 solicitudes por minuto se atienden y que la cuarta, en el mismo minuto, se rechaza por exceso de solicitudes sin crear la cuenta. |
| Caso asociado | [ACC-REG-016](../2.4_Casos_de_prueba/ACC-REG-016.md) · CA-HU-001-07 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-016A, D-016B, D-016C, D-016D de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar el cronómetro y registrar D-016A. | Registro aceptado. |
| 2 | Paso | Registrar D-016B antes de 60 s. | Registro aceptado. |
| 3 | Paso | Registrar D-016C antes de 60 s. | Registro aceptado. |
| 4 | Paso | Registrar D-016D antes de cumplir 60 s desde el primer envío. | La solicitud se rechaza. |
| 5 | Verificación | Leer el aviso del cuarto envío. | Indica exceso de solicitudes; no lo presenta como dato inválido. |
| 6 | Verificación | Buscar `ventana.d@dsqa.test` mediante consulta de solo lectura a la base de ensayo (ver PA-05). | No existe. |
| 7 | Paso | Esperar 65 s. | — |
| 8 | Paso | Registrar D-016D de nuevo. | Registro aceptado: confirma que el intento rechazado no la había creado. |

**Estado final esperado:** Existen `ventana.a`, `ventana.b` y `ventana.c`; `ventana.d` solo existe después del paso de control 8.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
