# Laboratorio 4: Integrar la inteligencia de negocio con Copilot Notebooks

**Duración:** 15 min

## Descripción
Práctica 1 (8 min): Los participantes crearán un Copilot Notebook para reunir los principales resultados obtenidos mediante Investigador y Analista. Utilizarán el cuaderno como contexto delimitado para solicitar una síntesis que relacione tendencias externas, hallazgos derivados de los datos y necesidades potenciales del cliente, identificando coincidencias, diferencias y aspectos que requieren validación.

Práctica 2 (7 min): A partir del contenido incorporado al Notebook, los participantes generarán un mapa mental para organizar visualmente los principales retos, necesidades, factores externos y oportunidades identificados. Revisarán la estructura obtenida para identificar relaciones entre necesidades, hallazgos y oportunidades, y determinar cuáles ameritan continuar hacia una etapa de evaluación.

## Pasos para ejecutar la práctica

1. **Construcción de la visión integrada en Copilot Notebooks (8 min):**
   * Abre **Copilot Notebooks** (Bloc de notas de Copilot).
   * Pega en las notas los textos obtenidos previamente con el agente Investigador (tendencias de mercado) y el agente Analista (hallazgos de datos del cliente).
   * En el panel de instrucciones de Notebooks, envía el siguiente prompt utilizando el cuaderno como contexto delimitado:
     ```text
     Sintetiza la información recopilada en este Notebook integrando el contexto externo y los datos internos del cliente.
     
     Estructura la respuesta en:
     1. Coincidencias clave (donde las tendencias de mercado confirman los hallazgos de datos del cliente).
     2. Divergencias o discrepancias (aspectos donde los datos del cliente contradicen la tendencia del sector).
     3. Lista de necesidades potenciales integradas que requieren validación urgente.
     ```

2. **Generación del Mapa Mental estructurado (7 min):**
   * En el mismo Copilot Notebook, envía la siguiente instrucción para representar visualmente el análisis:
     ```text
     A partir del contexto unificado del Notebook, genera la estructura jerárquica de un Mapa Mental de Inteligencia del Cliente.
     
     Utiliza sintaxis de texto con niveles de sangría y viñetas para organizar:
     - Nodo Principal: Cliente Corporativo - Oportunidades 2026
       - Rama 1: Retos y Factores Externos (Mercado)
       - Rama 2: Hallazgos de Desempeño Interno (Datos)
       - Rama 3: Oportunidades Prioritarias
       - Rama 4: Aspectos por Validar (Incertidumbre)
     ```

## Resultado esperado
Un documento síntesis en Copilot Notebooks que cruza tendencias externas con datos internos del cliente, complementado por un mapa mental jerárquico que prioriza visualmente los retos, hallazgos y oportunidades de negocio a evaluar.
