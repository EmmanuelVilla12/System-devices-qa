# ACC-INV-001 · Sesión caducada — happy path

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-INV-001.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-INV-001 |
| Nombre | Sesión caducada — happy path |
| Descripción | Verificar que un registro con nombre, correo, contraseña y rol válidos crea una cuenta activa con rol usuario y muestra sus datos sin la contraseña. |
| Número de orden de ejecución | 1 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-006 · Flujo principal pasos 1–4 · Criterio: **CA-HU-006-01** |
| Escenario | ESC-ACC-INV-001 · Sesión caducada — happy path · Básico (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (estado sesión caducado) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../../02_Implementacion/2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../../02_Implementacion/2.3_Datos_de_prueba.md) con la cuenta `sesion.vigente@dsqa.test`. Navegador sin sesión iniciada.<br>2. La sesión `sesion.vigente@dsqa.test` ha expirado (TTL > 20 min inactiva).<br>3. El correo `camila.rondon@dsqa.test` no existe en la base excepto la cuenta base. |
| Datos de entrada | Nombre `Camila Rondon` · Correo `camila.rondon@dsqa.test` · Contexto: sesión caducada (D-001; ver [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se rechaza el acceso a la función protegida. Se cierra la sesión automáticamente. Se muestra el mensaje «Inicie sesión nuevamente» identificado y legible en computador y teléfono. La cuenta `sesion.vigente@dsqa.test` queda cerrada. |
| Postcondición | No existe una sesión activa. El mensaje de necesidad de nuevo ingreso está presente en la respuesta. |
| Evidencia requerida | Captura de la respuesta con el mensaje «Inicie sesión nuevamente»; resultado de la verificación de que la sesión está cerrada. |