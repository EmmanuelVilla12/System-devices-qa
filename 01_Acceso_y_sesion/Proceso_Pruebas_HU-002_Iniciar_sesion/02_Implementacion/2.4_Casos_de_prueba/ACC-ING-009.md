# ACC-ING-009 · Comprobar que la contraseña no queda en texto legible en los registros almacenados

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-009.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-009 |
| Nombre | Comprobar que la contraseña no queda en texto legible en los registros almacenados |
| Descripción | Verificar que, después de un ingreso, la contraseña no aparece en texto legible ni en la base ni en los registros almacenados del servicio. |
| Número de orden de ejecución | 9 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · RNF-001 «no revelar contraseñas en respuestas ni registros almacenados en texto legible» · Criterio: **CA-HU-002-06** |
| Escenario | ESC-ACC-ING-009 · Contraseña no legible en registros almacenados · Calidad |
| Tipo de prueba y técnica | No funcional (seguridad) · Caja negra · inspección de almacenamiento y registros (solo lectura) |
| RNF relacionado | RNF-001 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Acceso de solo lectura a la base y a los registros del servicio de ensayo (PA-05). |
| Datos de entrada | Correo `ingreso.soporte@dsqa.test` · Contraseña `Duna3Plata` (D-009; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La búsqueda de `Duna3Plata` en la cuenta almacenada y en los registros del servicio generados en el momento del ingreso no devuelve coincidencias. |
| Postcondición | Sin sesión al terminar. |
| Evidencia requerida | Captura de la consulta y de la búsqueda en los registros, con fecha y hora. |
