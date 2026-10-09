# Laboratorio 3: Descubrir oportunidades potenciales mediante el agente Analista

**Duración:** 20 min

## Descripción
Práctica 1 (13 min): Los participantes analizarán un conjunto de datos completamente ficticios sobre el cliente corporativo del caso, relacionados con variables como evolución de ingresos, regiones, unidades de negocio, inversiones, crecimiento y otros indicadores relevantes. Utilizarán el agente Analista para identificar patrones, variaciones, relaciones entre variables y comportamientos que ameriten profundización. Solicitarán diferenciar los hallazgos sustentados por los datos de las hipótesis que requieren información adicional.

Práctica 2 (7 min): A partir de los hallazgos obtenidos, los participantes solicitarán a Copilot formular diferentes hipótesis de necesidades u oportunidades que podrían explorarse con el cliente. Cada hipótesis deberá vincularse con la evidencia que la origina, explicar qué necesidad podría existir y señalar qué información adicional debería validarse antes de convertirla en una propuesta comercial.

## Pasos para ejecutar la práctica

1. **Generación del conjunto de datos ficticios del cliente:**
   * Abre Microsoft 365 Copilot Chat y envía el siguiente prompt para generar el dataset autosuficiente:
     ```text
     Genera una tabla de datos ficticios en formato Markdown sobre el desempeño financiero de un cliente corporativo para los últimos 3 años (2023, 2024, 2025).
     
     Incluye exactamente las siguientes columnas:
     | Año | Region | Unidad_de_Negocio | Ingresos_USD | Crecimiento_Pct | Inversion_CAPEX_USD | Margen_Operativo_Pct |
     
     Asegúrate de incluir 8 filas de datos mostrando variaciones contrastantes (por ejemplo: fuerte crecimiento e inversión en la Región Norte, pero caída de margen en la Región Sur e ingresos estancados en la unidad tradicional).
     ```

2. **Análisis de datos con el agente Analista (13 min):**
   * Copia la tabla de datos generada en el paso anterior.
   * Selecciona el agente **Analista (Analyst)** en Microsoft 365 Copilot.
   * Pega la tabla o envía el siguiente prompt adjuntando la información:
     ```text
     Analiza el siguiente conjunto de datos del cliente corporativo sobre la evolución de sus ingresos, comportamiento regional, desempeño por unidad de negocio e inversiones:

     [Pega aquí la tabla de datos generada en el Paso 1]
     
     Identifica:
     1. Patrones anómalos, variaciones significativas y relaciones entre variables de crecimiento.
     2. Un desglose en dos secciones estrictas:
        - HALLAZGOS SUSTENTADOS (hechos probados cuantitativamente por los datos).
        - HIPÓTESIS QUE REQUIEREN PROFUNDIZACIÓN (supuestos derivados del comportamiento de los datos).
     ```

3. **Formulación y vinculación de hipótesis de oportunidad (7 min):**
   * Copia el resultado del análisis anterior, regresa a Copilot Chat y envía el siguiente prompt:
     ```text
     Con base en los hallazgos de datos obtenidos por el Analista [Pega los hallazgos del Paso 2], formula 3 hipótesis de oportunidad de negocio estructuradas.
     
     Para cada hipótesis exige la siguiente estructura obligatoria:
     1. Evidencia origen (el dato numérico exacto que la respalda).
     2. Necesidad potencial del cliente (qué problema o reto operativo/financiero deduce).
     3. Información faltante (qué datos adicionales se deben validar obligatoriamente antes de convertirla en una propuesta comercial).
     ```

## Resultado esperado
Un conjunto de datos cuantitativos generado de forma autónoma, un diagnóstico analítico que divide hechos e hipótesis, y una matriz de 3 oportunidades comerciales fundamentadas en evidencia que identifica los datos críticos por validar.
