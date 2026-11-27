# SCR-ACC-PNE-002 · Mostrar página inexistente como usuario autenticado

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-002.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Mostrar página inexistente como usuario autenticado |
| Descripción | Verificar la respuesta de la aplicación cuando una persona autenticada ingresa a una dirección inexistente. |
| Caso asociado | ACC-PNE-002 |
| Preparación | Tener disponible el entorno de pruebas e iniciar sesión con un usuario de prueba válido. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Iniciar sesión con el usuario de prueba autorizado. | La sesión queda autenticada. |
| 2 | Acción | Ingresar la dirección ficticia `/g5-pruebas/pagina-inexistente-001`. | La aplicación recibe la solicitud. |
| 3 | Verificación | Observar la respuesta presentada. | Se muestra «Página no encontrada» y no una pantalla en blanco. |
| 4 | Verificación | Comprobar que no se ejecute una operación del negocio. | No se crean ni modifican registros. |

## Estado final esperado

La aplicación muestra la respuesta de página no encontrada aunque exista una sesión autenticada.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
