# SCR-ACC-CIE-006 · Ingresar de nuevo con otra cuenta

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-006.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-006 |
| Descripción | Verificar que Después del cierre, un ingreso aceptado con otra cuenta establece una sesión que determina el acceso conforme a sus propios permisos. |
| Caso asociado | [ACC-CIE-006](../2.4_Casos_de_prueba/ACC-CIE-006.md) · CA-HU-005-04 |
| Preparación | Confirmar estado inicial de D-006 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Cerrar la sesión de la cuenta A de D-006. | — |
| 2 | Paso | Ingresar de nuevo con las credenciales exactas de la cuenta B de D-006. | — |
| 3 | Paso | Abrir la pantalla protegida de referencia con la nueva sesión. | — |
| 4 | Verificación | La sesión de la cuenta A termina. | La sesión de la cuenta A termina. |
| 5 | Verificación | Se acepta el ingreso con la cuenta B. | Se acepta el ingreso con la cuenta B. |
| 6 | Verificación | El acceso se determina por la nueva sesión de la cuenta B y sus permisos. | El acceso se determina por la nueva sesión de la cuenta B y sus permisos. |

**Estado final esperado:** El acceso disponible corresponde a la nueva cuenta y sus permisos, no a la cuenta cuya sesión se cerró.
