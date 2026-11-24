# SCR-ACC-ING-007 · Rechazar la sexta solicitud de ingreso dentro del mismo minuto

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-007.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-007 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que hasta 5 solicitudes de ingreso por minuto se atienden y que la sexta, en el mismo minuto, se rechaza por exceso sin iniciar sesión. |
| Caso asociado | [ACC-ING-007](../2.4_Casos_de_prueba/ACC-ING-007.md) · CA-HU-002-05 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-007A, D-007B, D-007C, D-007D, D-007E, D-007F de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios). Cerrar sesión entre envíos con la acción Cerrar sesión (HU-005); el cierre no es una solicitud de ingreso. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar el cronómetro e ingresar con D-007A. | Sesión iniciada. |
| 2 | Paso | Cerrar sesión e ingresar con D-007B. | Sesión iniciada. |
| 3 | Paso | Cerrar sesión e ingresar con D-007C. | Sesión iniciada. |
| 4 | Paso | Cerrar sesión e ingresar con D-007D. | Sesión iniciada. |
| 5 | Paso | Cerrar sesión e ingresar con D-007E (5.º, antes de 60 s). | Sesión iniciada. |
| 6 | Paso | Cerrar sesión e ingresar con D-007F antes de cumplir 60 s desde el primer envío. | La solicitud se rechaza. |
| 7 | Verificación | Leer el aviso del sexto envío. | Indica exceso de solicitudes; no lo presenta como credenciales incorrectas. |
| 8 | Verificación | Abrir la dirección de **Perfil**. | Se solicita iniciar sesión: el intento rechazado no inició sesión. |
| 9 | Paso | Esperar 65 s e ingresar de nuevo con las mismas credenciales. | Sesión iniciada: la ventana se liberó. |

**Estado final esperado:** Sin sesión al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
