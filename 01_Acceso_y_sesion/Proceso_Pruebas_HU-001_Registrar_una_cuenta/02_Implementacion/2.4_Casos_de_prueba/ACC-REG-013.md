# ACC-REG-013 · Rechazar contraseñas con composición incompleta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-013.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-013 |
| Nombre | Rechazar contraseñas con composición incompleta |
| Descripción | Verificar que una contraseña sin mayúscula, sin minúscula o sin número se rechaza e indica la condición que falta. |
| Número de orden de ejecución | 13 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-04 y CA-HU-001-05 · Criterio: **CA-HU-001-05** |
| Escenario | ESC-ACC-REG-013 · Contraseña sin mayúscula, sin minúscula o sin número · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (una condición incumplida por dato) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `simon.agudelo@dsqa.test` no existe. |
| Datos de entrada | `Simón Agudelo` · `simon.agudelo@dsqa.test` · Usuario con: D-013A `bosque52` · D-013B `BOSQUE52` · D-013C `BosqueAlto` (D-013A, D-013B, D-013C; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Los tres envíos se rechazan; cada uno indica la condición incumplida (mayúscula, minúscula o número); no se crea la cuenta. |
| Postcondición | No existe `simon.agudelo@dsqa.test`. |
| Evidencia requerida | Captura de cada rechazo; consulta final. |
