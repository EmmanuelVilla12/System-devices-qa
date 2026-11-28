# SCR-ACC-CIE-005 · Ingresar de nuevo con la misma cuenta

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-005.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-005 |
| Descripción | Verificar que Después del cierre, un ingreso aceptado con la misma cuenta establece una sesión nueva para determinar el acceso. |
| Caso asociado | [ACC-CIE-005](../2.4_Casos_de_prueba/ACC-CIE-005.md) · CA-HU-005-04 |
| Preparación | Confirmar estado inicial de D-005 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Cerrar la sesión de la cuenta A de D-005. | — |
| 2 | Paso | Ingresar de nuevo con las credenciales exactas de D-005. | — |
| 3 | Paso | Abrir la pantalla protegida de referencia con la nueva sesión. | — |
| 4 | Verificación | La sesión previa termina. | La sesión previa termina. |
| 5 | Verificación | Se acepta el nuevo ingreso con la misma cuenta. | Se acepta el nuevo ingreso con la misma cuenta. |
| 6 | Verificación | El acceso se determina por la nueva sesión y los permisos actuales de la cuenta. | El acceso se determina por la nueva sesión y los permisos actuales de la cuenta. |

**Estado final esperado:** El acceso disponible corresponde a la nueva sesión y sus permisos; el acceso anterior no se reutiliza.
