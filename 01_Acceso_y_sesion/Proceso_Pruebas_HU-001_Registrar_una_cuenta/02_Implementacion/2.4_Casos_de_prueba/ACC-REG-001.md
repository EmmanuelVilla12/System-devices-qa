# ACC-REG-001 · Registrar una cuenta válida con rol usuario

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-001.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-001 |
| Nombre | Registrar una cuenta válida con rol usuario |
| Descripción | Verificar que un registro con nombre, correo, contraseña y rol válidos crea una cuenta activa con rol usuario y muestra sus datos sin la contraseña. |
| Número de orden de ejecución | 3 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Flujo principal pasos 1–7 · Criterio: **CA-HU-001-01** |
| Escenario | ESC-ACC-REG-001 · Registro válido con rol usuario · Básico (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (todas las clases válidas) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `valentina.arango@dsqa.test` no existe en la base. |
| Datos de entrada | Nombre `Valentina Arango` · Correo `valentina.arango@dsqa.test` · Contraseña `Girasol47` · Rol `Usuario` (D-001; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se acepta el registro. Se muestran nombre `Valentina Arango`, correo `valentina.arango@dsqa.test` y rol usuario; la contraseña no aparece. La cuenta queda activa. |
| Postcondición | Existe una cuenta activa `valentina.arango@dsqa.test` con rol usuario. |
| Evidencia requerida | Captura de la confirmación con los datos mostrados; resultado de la consulta de solo lectura. |
