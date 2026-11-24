# ACC-REG-019 · Completar el registro solo con teclado

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-019.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-019 |
| Nombre | Completar el registro solo con teclado |
| Descripción | Verificar que el formulario se diligencia y envía sin ratón, con foco visible y sin trampas de foco. |
| Número de orden de ejecución | 19 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · RNF-004 · Criterio: **CA-HU-001-01** |
| Escenario | ESC-ACC-REG-019 · Registro completo solo con teclado · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · recorrido de accesibilidad por teclado |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Ratón desconectado o sin uso.<br>4. El correo `kevin.arias@dsqa.test` no existe. |
| Datos de entrada | Nombre `Kevin Arias` · Correo `kevin.arias@dsqa.test` · Contraseña `Arce4Verde` · Rol `Administrador` (D-019; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Con Tab se recorren Nombre, Correo electrónico, Contraseña, Rol y el botón de envío en orden lógico; el foco es visible; el rol se elige con flechas; el envío se hace con Enter; el registro se acepta. |
| Postcondición | Existe la cuenta `kevin.arias@dsqa.test`. |
| Evidencia requerida | Video corto o capturas del foco en cada control. |
