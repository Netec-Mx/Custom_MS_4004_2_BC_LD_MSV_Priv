# Laboratorio 5: Evaluar una oportunidad mediante Copilot en Excel

**Duración:** 23 min

## Descripción
Práctica 1 (8 min): Los participantes seleccionarán una de las oportunidades identificadas y utilizarán Copilot en modo Plan para estructurar en un libro nuevo un instrumento de análisis con los supuestos y variables necesarias para evaluarla. Construirán distintos escenarios ilustrativos (por ejemplo, conservador, base y expansivo) utilizando exclusivamente información ficticia y supuestos explícitos.

Práctica 2 (8 min): Utilizando Copilot en modo Edición, los participantes profundizarán sobre el instrumento creado, incorporarán cálculos y comparaciones entre escenarios y generarán una visualización que permita identificar cómo cambian los resultados ante diferentes supuestos. Finalmente, solicitarán identificar qué variables tienen mayor incidencia y cuáles requieren validación antes de presentar la oportunidad al cliente.

Práctica 3 (4 min): Con los resultados obtenidos, los participantes solicitarán a Copilot estructurar una propuesta preliminar que relacione necesidad detectada + evidencia + oportunidad + valor esperado para el cliente, evitando presentar como hechos los supuestos utilizados durante el análisis.

## Pasos para ejecutar la práctica

1. **Construcción de escenarios en Excel en modo Plan:**
   * Abre un libro nuevo en **Microsoft Excel** y guarda el archivo con el nombre: `Evaluacion_Escenarios_Oportunidad.xlsx`.
   * Activa el panel de Copilot en Excel en modo **Plan** y envía:
     ```text
     Crea una tabla de evaluación financiera para una oportunidad de expansión de líneas de crédito y gestión de capital de trabajo de un cliente corporativo.
     
     Estructura las columnas con: Variable/Supuesto, Escenario Conservador, Escenario Base y Escenario Expansivo. Incluye supuestos explícitos sobre monto estimado de inversión, tasa esperada, retorno de cartera y reducción de costos operativos.
     ```

2. **Análisis, fórmulas y visualización en modo Edición:**
   * Cambia el panel de Copilot en Excel al modo **Permitir la edición** (Edición).
   * Envía la siguiente instrucción y guarda los cambios en el archivo:
     ```text
     Incorpora los cálculos necesarios para comparar el valor neto esperado entre los tres escenarios, aplica un formato condicional a los resultados y genera un gráfico comparativo de barras. Guardar la estructura en el libro.
     
     Finalmente, indícame mediante un mensaje cuál variable tiene mayor sensibilidad e incidencia en los resultados y requiere validación previa con el cliente.
     ```

3. **Definición de la Oferta de Valor E-E-O-V:**
   * Abre Copilot Chat, adjunta el archivo guardado `Evaluacion_Escenarios_Oportunidad.xlsx` y envía:
     ```text
     Con base en el análisis de escenarios del archivo adjunto Evaluacion_Escenarios_Oportunidad.xlsx, redacta la Oferta de Valor Preliminar para el cliente.
     
     Aplica el esquema:
     - Necesidad detectada
     - Evidencia de respaldo
     - Oportunidad propuesta
     - Valor esperado para el cliente (impacto)
     
     Nota: Etiqueta claramente los estimadores como "supuestos de análisis" y no como hechos consumados.
     ```

## Resultado esperado
Un modelo financiero guardado en `Evaluacion_Escenarios_Oportunidad.xlsx` con tres escenarios, cálculos automatizados y gráficos, más el enunciado formal de la oferta de valor formulado a partir del archivo.
