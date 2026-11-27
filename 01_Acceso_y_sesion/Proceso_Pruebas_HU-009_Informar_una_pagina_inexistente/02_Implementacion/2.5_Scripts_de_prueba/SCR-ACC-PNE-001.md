# SCR-ACC-PNE-001 · Mostrar página inexistente como visitante

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-001.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Mostrar página inexistente como visitante |
| Descripción | Verificar la respuesta de la aplicación cuando un visitante ingresa a una dirección inexistente. |
| Caso asociado | ACC-PNE-001 |
| Preparación | Tener disponible el entorno de pruebas y abrir un navegador sin sesión autenticada. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Confirmar que no existe una sesión autenticada. | El navegador se encuentra sin sesión iniciada. |
| 2 | Acción | Ingresar la dirección ficticia `/g5-pruebas/pagina-inexistente-001`. | La aplicación recibe la solicitud. |
| 3 | Verificación | Observar la respuesta presentada por la aplicación. | Se muestra «Página no encontrada» y no una pantalla en blanco. |
| 4 | Verificación | Comprobar que no se ejecute una operación del negocio. | No se crean ni modifican registros. |

## Estado final esperado

La aplicación muestra la respuesta de página no encontrada al visitante y no modifica registros.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
