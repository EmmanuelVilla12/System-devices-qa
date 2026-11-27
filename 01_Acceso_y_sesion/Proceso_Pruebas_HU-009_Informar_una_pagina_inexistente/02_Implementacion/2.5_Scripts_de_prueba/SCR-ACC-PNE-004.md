# SCR-ACC-PNE-004 · Denegar acceso a una pantalla restringida

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-004.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Denegar acceso a una pantalla restringida |
| Descripción | Comprobar que una persona autenticada sin permisos reciba la respuesta de acceso denegado al intentar ingresar a una pantalla protegida. |
| Caso asociado | ACC-PNE-004 |
| Preparación | Disponer de una ruta existente y protegida, un usuario autenticado sin permisos y la configuración confirmada por el equipo responsable. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Iniciar sesión con el usuario de prueba sin permisos. | La sesión queda autenticada con el perfil indicado. |
| 2 | Preparación | Obtener una ruta existente y protegida confirmada por el equipo responsable. | Se dispone de una ruta válida. |
| 3 | Acción | Ingresar a la ruta protegida. | La aplicación recibe la solicitud. |
| 4 | Verificación | Observar la respuesta de la aplicación. | Se presenta «Acceso denegado», según HU-008, y no «Página no encontrada». |

## Estado final esperado

El usuario autenticado sin permisos no puede acceder al contenido protegido.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
