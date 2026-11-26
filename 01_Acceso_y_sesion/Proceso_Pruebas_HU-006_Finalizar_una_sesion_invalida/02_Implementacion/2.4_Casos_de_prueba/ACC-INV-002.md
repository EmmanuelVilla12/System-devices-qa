# ACC-INV-002 · Sesión rechazada como inválida

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-INV-002.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-INV-002 |
| Nombre | Sesión rechazada como inválida |
| Descripción | Verificar que el servicio rechaza la sesión como inválida aunque la aplicación la tenga registrada, y la aplicación finaliza la sesión y solicita identificarme nuevamente. |
| Número de orden de ejecución | 2 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-006 · Flujo principal pasos 1–4 · Criterio: **CA-HU-006-02** |
| Escenario | ESC-ACC-INV-002 · Sesión rechazada como inválida · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (origen del rechazo) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../../02_Implementacion/2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../../02_Implementacion/2.3_Datos_de_prueba.md) con la cuenta `sesion.vigente@dsqa.test`. Navegador sin sesión iniciada.<br>2. La sesión `sesion.vigente@dsqa.test` está registrada en la aplicación pero el servicio la declara inválida.<br>3. El correo `mateo.salazar@dsqa.test` no existe en la base excepto la cuenta base. |
| Datos de entrada | Nombre `Mateo Salazar` · Correo `mateo.salazar@dsqa.test` · Contexto: sesión rechazada por servicio (D-002; ver [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md)) |
| Resultado esperado | La aplicación finaliza la sesión registrada. Se solicita al usuario que identifique nuevamente. Se muestra el mensaje «Inicie sesión nuevamente» identificado y legible en computador y teléfono. Los datos locales (carro, formulario) no se conservan. |
| Postcondición | No existe una sesión activa. Los datos locales han sido limpiados. El mensaje de necesidad de nuevo ingreso está presente en la respuesta. |
| Evidencia requerida | Captura de la respuesta con el mensaje «Inicie sesión nuevamente»; evidencia de que los datos locales no están presentes; resultado de la verificación de que la sesión está cerrada. |