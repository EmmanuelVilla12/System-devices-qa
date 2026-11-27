# SCR-ACC-PNE-006 · Verificar que el mensaje sea identificable

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-006.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Verificar que el mensaje sea identificable |
| Descripción | Comprobar que la respuesta permita identificar que la página solicitada no existe. |
| Caso asociado | ACC-PNE-006 |
| Preparación | Tener disponible el entorno de pruebas y abrir un navegador. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Abrir la aplicación en el entorno de pruebas. | La aplicación se encuentra disponible. |
| 2 | Acción | Ingresar a la dirección ficticia `/g5-pruebas/pagina-inexistente-001`. | La aplicación recibe la solicitud. |
| 3 | Verificación | Observar el mensaje presentado. | Se identifica «Página no encontrada». |
| 4 | Verificación | Comprobar que no se presenta una pantalla en blanco. | La respuesta permite reconocer que la dirección no corresponde a una página existente. |

## Estado final esperado

La respuesta permite identificar claramente que la página solicitada no existe.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
