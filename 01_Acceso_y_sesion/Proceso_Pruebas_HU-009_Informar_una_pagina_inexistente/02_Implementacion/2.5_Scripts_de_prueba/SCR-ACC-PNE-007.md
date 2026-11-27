# SCR-ACC-PNE-007 · Verificar visualización en computador y móvil

[Índice de scripts](00_Indice_de_scripts.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-PNE-007.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| Nombre | Verificar visualización en computador y móvil |
| Descripción | Comprobar que el mensaje de página inexistente sea legible y no quede cortado en diferentes tamaños de pantalla. |
| Caso asociado | ACC-PNE-007 |
| Preparación | Disponer del entorno de pruebas y de las herramientas de visualización adaptable del navegador. |

## Pasos del script

| N.º | Tipo de paso/verificación | Paso | Resultado esperado |
|---|---|---|---|
| 1 | Preparación | Abrir la aplicación en el entorno de pruebas. | La aplicación se encuentra disponible. |
| 2 | Acción | Ingresar a la dirección ficticia `/g5-pruebas/pagina-inexistente-001`. | La aplicación muestra la respuesta de página inexistente. |
| 3 | Verificación | Visualizar la respuesta con resolución 1366x768. | El mensaje se observa legible y sin texto cortado. |
| 4 | Verificación | Cambiar a resolución 390x844. | El mensaje se observa legible y sin texto cortado. |

## Estado final esperado

El mensaje de página no encontrada se visualiza correctamente en computador y móvil.

## Registro de ejecución

El resultado deberá registrarse en `03_Ejecucion/3.2_Registro_de_ejecucion.md`.

**Estado actual:** No ejecutado.
