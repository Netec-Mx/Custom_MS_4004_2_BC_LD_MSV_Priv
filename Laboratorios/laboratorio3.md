# Laboratorio 3: Descubrir oportunidades potenciales mediante el agente Analista

**Duración:** 20 min

## Descripción
Práctica 1 (13 min): Los participantes analizarán un conjunto de datos completamente ficticios sobre el cliente corporativo del caso, relacionados con variables como evolución de ingresos, regiones, unidades de negocio, inversiones, crecimiento y otros indicadores relevantes. Utilizarán el agente Analista para identificar patrones, variaciones, relaciones entre variables y comportamientos que ameriten profundización. Solicitarán diferenciar los hallazgos sustentados por los datos de las hipótesis que requieren información adicional.

Práctica 2 (7 min): A partir de los hallazgos obtenidos, los participantes solicitarán a Copilot formular diferentes hipótesis de necesidades u oportunidades que podrían explorarse con el cliente. Cada hipótesis deberá vinculada con la evidencia que la origina, explicar qué necesidad podría existir y señalar qué información adicional debería validarse antes de convertirla en una propuesta comercial.

## Pasos para ejecutar la práctica

1. **Generación y exportación de la base de datos del cliente (0 min):**
   * En Copilot Chat, envía el siguiente prompt para crear la base de datos:
     ```text
     Genera una tabla de datos ficticios sobre el desempeño financiero de un cliente corporativo para los últimos 3 años (2023, 2024, 2025). Incluye las columnas: Año, Region, Unidad_de_Negocio, Ingresos_USD, Crecimiento_Pct, Inversion_CAPEX_USD y Margen_Operativo_Pct con 8 filas de datos con variaciones contrastantes.
     ```
   * Exporta o guarda la tabla generada en Microsoft Excel con el nombre: `Datos_Cliente_Corporativo.xlsx`.

2. **Análisis de datos con el agente Analista (13 min):**
   * Activa el agente **Analista (Analyst)** en Microsoft 365 Copilot.
   * Adjunta o selecciona el archivo `Datos_Cliente_Corporativo.xlsx` creado en el paso anterior y envía:
     ```text
     Analiza el archivo adjunto Datos_Cliente_Corporativo.xlsx sobre la evolución de ingresos, comportamiento regional, desempeño por unidad de negocio e inversiones del cliente.
     
     Identifica:
     1. Patrones anómalos, variaciones significativas y relaciones entre variables de crecimiento.
     2. Un desglose en dos secciones estrictas:
        - HALLAZGOS SUSTENTADOS (hechos probados cuantitativamente por los datos).
        - HIPÓTESIS QUE REQUIEREN PROFUNDIZACIÓN (supuestos derivados del comportamiento de los datos).
     ```

3. **Formulación de hipótesis y exportación a documento Word (7 min):**
   * En el mismo chat, envía el siguiente prompt indicando que tome los resultados del análisis realizado:
     ```text
     Con base en los hallazgos cuantitativos obtenidos del archivo Datos_Cliente_Corporativo.xlsx, formula 3 hipótesis de oportunidad de negocio estructuradas.
     
     Para cada hipótesis detalla:
     1. Evidencia origen (dato numérico exacto del archivo).
     2. Necesidad potencial del cliente.
     3. Información faltante por validar.
     ```
   * Haz clic en **Exportar a Word** y guarda este documento con el nombre: `Hallazgos_y_Oportunidades_Cliente.docx`.

## Resultado esperado
Un archivo Excel llamado `Datos_Cliente_Corporativo.xlsx` y un informe en Word llamado `Hallazgos_y_Oportunidades_Cliente.docx` con el diagnóstico de hallazgos e hipótesis sustentadas.
