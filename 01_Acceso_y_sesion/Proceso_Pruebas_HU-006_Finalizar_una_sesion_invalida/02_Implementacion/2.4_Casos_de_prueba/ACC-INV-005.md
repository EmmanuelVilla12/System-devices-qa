# ACC-INV-005 · Mensaje identificable y legible (RNF-004 y RNF-005)

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-INV-005.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-INV-005 |
| Nombre | Mensaje identificable y legible |
| Descripción | Verificar que el mensaje de necesidad de nuevo ingreso es visible, identificado y legible en computador y teléfono, y se lee con lector de pantalla. |
| Número de orden de ejecución | 5 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-006 · Condiciones de calidad · Criterio: **RNF-002, RNF-004, RNF-005** |
| Escenario | ESC-ACC-INV-005 · Mensaje identificable y legible (RNF-004 y RNF-005) · Calidad |
| Tipo de prueba y técnica | No funcional con efecto funcional · Inspección de respuesta y recorrido |
| RNF relacionado | RNF-002, RNF-004, RNF-005 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../../02_Implementacion/2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../../02_Implementacion/2.3_Datos_de_prueba.md).<br>2. El usuario ha accedido a una función protegida con sesión inválida (caso ACC-INV-001 o ACC-INV-002).<br>3. El lector de pantalla NVDA está disponible.<br>4. Se prueba en dos dispositivos: computador (1366×768) y teléfono (390×844). |
| Datos de entrada | Contexto: mensaje de sesión inválida desde ACC-INV-001 o ACC-INV-002 (D-005; ver [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md)) |
| Resultado esperado | El mensaje "Inicie sesión nuevamente" es: visible en pantalla; identificado por lector de pantalla NVDA (anuncia "iniciar sesión nuevamente"); legible en computador (1366×768) y teléfono (390×844); tiene contraste suficiente; no está cortado ni superpuesto por otros elementos. |
| Postcondición | Los mensajes de sesión permanecen en el historial de respuesta y son reproducibles en las dos configuraciones de pantalla. |
| Evidencia requerida | Capturas del mensaje en computador (1366×768) y teléfono (390×844); reporte del lector de pantalla NVDA leyendo el mensaje; verificación de contraste y tamaño de fuente. |