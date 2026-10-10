# Laboratorio 4: Integrar la inteligencia de negocio con Copilot Notebooks

**Duración:** 15 min

## Descripción
Práctica 1 (8 min): Los participantes crearán un Copilot Notebook para reunir los principales resultados obtenidos mediante Investigador y Analista. Utilizarán el cuaderno como contexto delimitado para solicitar una síntesis que relacione tendencias externas, hallazgos derivados de los datos y necesidades potenciales del cliente, identificando coincidencias, diferencias y aspectos que requieren validación.

Práctica 2 (7 min): A partir del contenido incorporado al Notebook, los participantes generarán un mapa mental para organizar visualmente los principales retos, necesidades, factores externos y oportunidades identificados. Revisarán la estructura obtenida para identificar relaciones entre necesidades, hallazgos y oportunidades, y determinar cuáles ameritan continuar hacia una etapa de evaluación.

## Pasos para ejecutar la práctica

1. **Construcción de la visión integrada en Copilot Notebooks (8 min):**
   * Abre **Copilot Notebooks** (Bloc de notas de Copilot).
   * Adjunta o vincula como fuente de contexto los dos archivos creados previamente: `Reporte_Investigacion_Sector.docx` y `Hallazgos_y_Oportunidades_Cliente.docx`.
   * En el panel de instrucciones de Notebooks, envía el siguiente prompt:
     ```text
     Sintetiza la información recopilada en los dos archivos vinculados en este Notebook (Reporte_Investigacion_Sector.docx y Hallazgos_y_Oportunidades_Cliente.docx).
     
     Estructura la respuesta en:
     1. Coincidencias clave (donde las tendencias del sector confirman los datos internos del cliente).
     2. Divergencias o discrepancias entre el sector y el cliente.
     3. Lista de necesidades potenciales integradas que requieren validación urgente.
     ```

2. **Generación del Mapa Mental estructurado (7 min):**
   * En el mismo Copilot Notebook, envía la siguiente instrucción para estructurar la visualización:
     ```text
     A partir del contexto unificado de los archivos vinculados en este Notebook, genera la estructura jerárquica de un Mapa Mental de Inteligencia del Cliente.
     
     Organiza con sangría y viñetas:
     - Nodo Principal: Cliente Corporativo - Oportunidades 2026
       - Rama 1: Retos y Factores Externos (Mercado)
       - Rama 2: Hallazgos de Desempeño Interno (Datos)
       - Rama 3: Oportunidades Prioritarias
       - Rama 4: Aspectos por Validar (Incertidumbre)
     ```

## Resultado esperado
Un análisis unificado en Copilot Notebooks alimentado directamente por los archivos de los laboratorios anteriores, junto con un mapa mental jerárquico estructurado.
