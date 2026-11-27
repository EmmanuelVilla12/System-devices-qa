# SCR-ACC-PNE-005 · Verificar que no se modifiquen registros

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-005.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Verificar que no se modifiquen registros |
| Descripción | Comprobar que solicitar una dirección inexistente no cree ni modifique información del sistema. |
| Caso asociado | ACC-PNE-005 |
| Preparación | Disponer del entorno de pruebas y de mecanismos autorizados para consultar los registros antes y después de la solicitud. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Consultar y registrar el estado inicial de usuarios, equipos y préstamos. | Se dispone de una referencia del estado inicial. |
| 2 | Acción | Ingresar a la dirección ficticia `/g5-pruebas/pagina-inexistente-001`. | La aplicación recibe la solicitud. |
| 3 | Verificación | Comprobar que se presenta «Página no encontrada». | Se muestra la respuesta esperada. |
| 4 | Verificación | Consultar nuevamente los registros de usuarios, equipos y préstamos. | Los registros conservan el mismo estado inicial. |

## Estado final esperado

La dirección inexistente muestra la respuesta correspondiente y no produce cambios en los registros.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
