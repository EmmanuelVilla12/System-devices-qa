# ACC-ING-010 · Comprobar que el ingreso no otorga funciones ajenas al rol de la cuenta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-010.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-010 |
| Nombre | Comprobar que el ingreso no otorga funciones ajenas al rol de la cuenta |
| Descripción | Verificar que la sesión iniciada reconoce el rol y que el acceso a una función de otro rol se rechaza. |
| Número de orden de ejecución | 10 (independiente; requiere la respuesta de PA-04; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Regla «un ingreso no otorga funciones ajenas al rol de la cuenta» · RNF-002 · HU-008 (otro grupo) · Criterio: **CA-HU-002-01** |
| Escenario | ESC-ACC-ING-010 · Sesión limitada a las funciones del rol · Calidad |
| Tipo de prueba y técnica | No funcional (seguridad: permisos) con efecto funcional · Caja negra · partición de equivalencia (función permitida / función de otro rol) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Se conoce una pantalla o función existente restringida a un rol distinto de usuario (PA-04). |
| Datos de entrada | Credenciales `ingreso.usuario@dsqa.test` / `Llave8Norte`. Función restringida: por confirmar en PA-04 (D-010; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La sesión se inicia con rol usuario; al solicitar la función restringida se muestra Acceso denegado (tratamiento de HU-008) y la sesión sigue iniciada. |
| Postcondición | Sesión abierta; cerrarla al terminar. |
| Evidencia requerida | Captura de la respuesta de la función restringida. |
