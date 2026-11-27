# SCR-ACC-PNE-003 · Solicitar inicio de sesión para una pantalla restringida

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-003.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Solicitar inicio de sesión para una pantalla restringida |
| Descripción | Comprobar que una persona sin sesión reciba la solicitud de autenticación al acceder a una pantalla existente y protegida. |
| Caso asociado | ACC-PNE-003 |
| Preparación | Disponer de una ruta existente y protegida, confirmada por el equipo responsable, y abrir el navegador sin sesión iniciada. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Confirmar que el navegador no tiene una sesión autenticada. | El usuario se encuentra sin iniciar sesión. |
| 2 | Preparación | Obtener del equipo responsable una ruta existente y protegida. | Se dispone de una ruta válida confirmada. |
| 3 | Acción | Ingresar a la ruta protegida. | La aplicación recibe la solicitud. |
| 4 | Verificación | Observar la respuesta de la aplicación. | Se solicita iniciar sesión según HU-008 y no aparece «Página no encontrada». |

## Estado final esperado

El contenido protegido permanece inaccesible y la aplicación solicita autenticación.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
