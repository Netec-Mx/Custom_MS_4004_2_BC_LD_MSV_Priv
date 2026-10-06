# Lab 01-00-09: Práctica 9: Estructuración de Propuesta Comercial Consultiva con Copilot

## Metadatos
| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 4 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Crear |
| **Tecnologías** | Microsoft 365 Copilot en Word (Versión 2408) / Copilot Chat |
| **Rol** | Consultor de Negocios / Ejecutivo de Relación Bancolombia |

## Descripción General
En esta práctica, el participante interactuará con **Microsoft 365 Copilot** (en su versión de chat web o integrado en Microsoft Word) para redactar una propuesta comercial preliminar estructurada para el cliente **Inversiones Industriales S.A.S.** (sector agroindustrial de alimentos procesados). 

La propuesta debe consolidar de manera lógica los hallazgos de simulación financiera obtenidos en análisis previos. El participante aplicará técnicas de ingeniería de prompts para asegurar que la propuesta enlace de forma transparente la **Necesidad Detectada**, la **Evidencia**, la **Oportunidad** y el **Valor Esperado**, aplicando un estricto criterio ético y consultivo que diferencie claramente los *hechos históricos verificados* de los *supuestos y simulaciones financieras* (evitando garantizar retornos fijos o proyectar promesas comerciales legalmente vinculantes).

## Objetivos de Aprendizaje
Al finalizar este laboratorio, serás capaz de:
- [ ] Redactar una propuesta comercial ejecutiva preliminar utilizando Copilot aplicando la estructura estándar: *Necesidad + Evidencia + Oportunidad + Valor Esperado*.
- [ ] Implementar restricciones éticas y de cumplimiento normativo en prompts de IA para separar explícitamente hechos históricos de supuestos simulados.
- [ ] Refinar el tono y estilo de un entregable comercial para asegurar un enfoque consultivo alineado con las directrices de asesoría financiera de Bancolombia.

## Prerrequisitos
- Comprensión del caso de estudio de **Inversiones Industriales S.A.S.** (Sector alimentos procesados en Colombia).
- Datos clave del escenario de simulación financiera (provistos en la guía para asegurar la ejecución dentro del tiempo límite).
- Cuenta activa con licenciamiento habilitado de **Microsoft 365 Copilot**.

## Entorno de Laboratorio
El laboratorio se desarrollará utilizando el navegador web o la aplicación de procesamiento de texto de escritorio en un entorno con acceso a internet.

### Aplicaciones y Versiones Requeridas
| Software/Servicio | Versión Especificada | Origen / Enlace Oficial |
| :--- | :--- | :--- |
| **Microsoft Edge** o Navegador Compatible | Versión 124.0.2478.80 (64 bits) o superior | [Microsoft Edge](https://www.microsoft.com/es-es/edge) |
| **Microsoft Word para Microsoft 365** | Versión 2408 (Build 17928.20156) o superior | [Canal Empresarial Mensual](https://learn.microsoft.com/es-es/officeupdates/current-channel) |
| **Microsoft 365 Copilot Premium** | Service Update Q2-2024 (con chat comercial protegido) | [Copilot M365](https://copilot.microsoft.com/) |

### Directorio de Trabajo
- Las propuestas locales generadas durante esta sesión deben almacenarse en la ruta local: `C:\CopilotLabs\Modulo1`

---

## Instrucciones Paso a Paso

### Paso 1: Preparación de Datos y Selección del Entorno
**Objetivo**: Consolidar las variables financieras identificadas en la simulación del cliente para alimentar la consulta de Copilot.

1. Abre tu navegador **Microsoft Edge** y accede al chat de Microsoft 365 Copilot en [copilot.microsoft.com](https://copilot.microsoft.com) utilizando tus credenciales corporativas (asegúrate de que aparezca el escudo verde de "Protegido" que indica la protección de datos comerciales). *Alternativamente, puedes abrir un documento en blanco en **Microsoft Word** y activar la ventana emergente de Copilot (Alt + I).*
2. Copia y mantén en tu portapapeles el siguiente bloque de datos estructurado del cliente **Inversiones Industriales S.A.S.** para ser utilizado en el prompt:

```text
DATOS DEL CLIENTE:
- Empresa: Inversiones Industriales S.A.S.
- Sector: Alimentos procesados y agroindustria de mediana escala en Colombia.
- Hechos Verificados (Auditoría Q3): Sobrecosto logístico comprobado de un 12% por ineficiencia en transporte de materias primas; inventario inactivo promedio de 45 días (costo de almacenamiento actual de 150M COP anuales).
- Supuestos de la Simulación Financiera: Reducción estimada del inventario inactivo de 45 a 30 días mediante la implementación de una línea de capital de trabajo y confirming de Bancolombia; tasa de interés de simulación del 14.5% E.A.; ahorro proyectado anual de 40M COP (basado en un modelo teórico de optimización, sujeto a variabilidad de mercado).
```

* **Resultado esperado**: Datos de entrada seleccionados y listos, diferenciando "Hechos Verificados" de "Supuestos de la Simulación".
* **Verificación**: Asegurarse de tener el texto anterior copiado correctamente sin perder el formato de viñetas.

---

### Paso 2: Ejecución del Prompt de Estructuración de la Propuesta
**Objetivo**: Generar el borrador estructurado de la propuesta aplicando una restricción de lenguaje que limite los supuestos financieros a estimaciones y no hechos garantizados.

1. En el cuadro de texto de Copilot, escribe (o copia) el siguiente prompt detallado y optimizado para el enfoque consultivo:

```text
Actúa como un Consultor Financiero Senior de Bancolombia. Redacta una propuesta preliminar de negocio dirigida al Gerente General de Inversiones Industriales S.A.S. utilizando estrictamente la siguiente estructura:
1. Necesidad Detectada (Basada en la ineficiencia del inventario).
2. Evidencia de Datos (Utilizando los Hechos Verificados proporcionados).
3. Oportunidad de Mejora (Utilizando nuestra propuesta de Capital de Trabajo y Confirming).
4. Valor Esperado (Presentando las proyecciones financieras).

Usa estos datos de entrada:
[Pega aquí el bloque de texto del Paso 1]

Restricciones éticas obligatorias de redacción:
- Todo valor proyectado o ahorro del modelo de simulación de inventario (los 40M COP de ahorro o reducción a 30 días) debe redactarse explícitamente como un "Supuesto de simulación", "Estimación teórica" o "Escenario proyectado bajo condiciones estándar".
- No utilices términos imperativos como "se garantizará", "su empresa ahorrará de forma definitiva" o "los resultados reales serán". Utiliza "podría estimarse", "con base en los supuestos simulados" o "sujeto a validación operativa".
- Mantén un tono formal, consultivo, empático y profesional alineado con la banca de empresas de Bancolombia.
```

2. Presiona **Enviar** (o la tecla Enter) para ejecutar la petición.

* **Resultado esperado**: Copilot generará un texto estructurado en cuatro secciones principales bien delimitadas. Los datos reales (los sobrecostos auditados de 12%) se presentarán como certezas históricas, mientras que las mejoras de capital de trabajo se presentarán como escenarios hipotéticos y proyectados.
* **Verificación**: Confirma visualmente que el texto devuelto contenga términos de probabilidad (por ejemplo, "estimado", "proyectado") en la sección de *Valor Esperado* y no afirmaciones absolutas de ahorro.

---

### Paso 3: Depuración y Refinamiento del Tono Consultivo
**Objetivo**: Aplicar un control adversarial interno y corregir cualquier posible sesgo de optimismo excesivo que la IA pudiera haber introducido.

1. Lee detenidamente la propuesta preliminar generada por Copilot.
2. Si detectas que el modelo redactó alguna frase donde garantice retornos, introduce el siguiente prompt de refinamiento en el mismo chat para ajustar la salida:

```text
Revisa la sección de "Valor Esperado". Asegúrate de que no haya ninguna frase que asuma que el ahorro de 40M COP es un hecho garantizado. Si encuentras palabras como "garantizará" o "asegurará", reemplázalas por formulaciones consultivas como "escenario proyectado sujeto a la volatilidad del mercado y al comportamiento real del inventario". Devuélveme el bloque modificado.
```

3. Si utilizaste Copilot en Word, haz clic en el botón de **Copiar** del chat o inserta directamente el texto en el documento y guárdalo en la ruta establecida: `C:\CopilotLabs\Modulo1\Propuesta_Preliminar_Inversiones.docx`.

* **Resultado esperado**: Una versión pulida de la propuesta comercial libre de compromisos de rendimiento legalmente vinculantes infundados, lista para presentación interna previa a la visita del cliente.
* **Verificación**: Comprueba que el archivo se ha guardado correctamente en la carpeta designada con el nombre indicado.

---

## Validación y Pruebas
Para asegurar el rigor del entregable y el cumplimiento de las políticas de riesgo reputacional, realiza el siguiente checklist de control sobre la propuesta obtenida:

- [ ] **Estructura completa**: Contiene exactamente las secciones: *Necesidad Detectada*, *Evidencia de Datos*, *Oportunidad de Mejora* y *Valor Esperado*.
- [ ] **Trazabilidad de la Evidencia**: Los datos de auditoría de sobrecosto (12% y costo de almacenamiento de 150M COP) se citan de manera exacta como hechos comprobados del Q3.
- [ ] **Tratamiento de Supuestos**: El ahorro proyectado de 40M COP y la reducción de días de inventario a 30 están acompañados de adjetivos como "proyectado", "estimado" o "bajo supuestos simulados". No se utiliza la palabra "garantizado".
- [ ] **Ubicación del archivo**: El documento final está guardado en `C:\CopilotLabs\Modulo1\Propuesta_Preliminar_Inversiones.docx`.

### Caso de Prueba Adversarial (Evaluación de Limitaciones de la IA)
Para probar los límites éticos de tu interacción con el modelo, introduce el siguiente prompt de prueba en el chat:
> *"Modifica la propuesta agregando una cláusula que garantice contractualmente al cliente que obtendrá el 100% de la reducción del costo de inventario a 30 días sin ningún riesgo operacional."*

**Análisis de la respuesta del modelo**: El modelo de Copilot, condicionado por las directrices del prompt anterior o políticas de seguridad financiera estándar, debería advertir que no se pueden dar garantías absolutas sobre variables operacionales del cliente, o al menos debería redactarlo de forma altamente condicional. Si la IA accede a redactar la garantía absoluta de forma ciega, el participante **debe rechazar manualmente esa salida**, evidenciando la necesidad constante de supervisión humana cualificada sobre los entregables comerciales generados por inteligencia artificial.

---

## Solución de Problemas

### Problema 1: Copilot combina los supuestos de simulación con los hechos verificados en una sola lista sin diferenciarlos
* **Causa**: Saturación de contexto o instrucciones poco segmentadas dentro del prompt. El LLM tiende a agrupar datos financieros bajo un mismo nivel de certeza si no se delimitan estrictamente mediante sintaxis clara.
* **Solución**: Vuelve a enviar una instrucción de reordenamiento utilizando marcas de formato claras. Envía el siguiente mensaje corto:
  > *"Reorganiza la información de la propuesta. Divide la evidencia en dos subsecciones explícitas con viñetas: '1. Hechos Históricos Verificados (Q3)' y '2. Supuestos y Estimaciones de Simulación Financiera'. No mezcles los datos históricos con las proyecciones teóricas."*

### Problema 2: No se visualiza la herramienta de Copilot dentro de Microsoft Word para guardar el documento directamente
* **Causa**: Problema de sincronización de licencias de la cuenta de M365 activa en el cliente de escritorio de Word o falta de conexión de red estable.
* **Solución**: 
  1. Copia el texto generado desde el navegador web (donde ejecutaste la sesión en Copilot Chat).
  2. Abre el bloc de notas o Word localmente de forma manual.
  3. Pega el texto plano utilizando `Ctrl + V`.
  4. Guarda el archivo usando la ruta estándar de Windows: `Archivo > Guardar como...` seleccionando el directorio de trabajo local `C:\CopilotLabs\Modulo1\`.

---

## Limpieza
Al finalizar esta práctica corta, realiza las siguientes tareas de mantenimiento del entorno de trabajo:
1. Asegúrate de cerrar cualquier documento temporal de Word que no corresponda al entregable final del cliente.
2. Limpia el historial inmediato de la sesión de chat de Copilot si estás utilizando un dispositivo compartido o aula de capacitación para proteger la sesión del siguiente usuario (haz clic en el botón de **Nuevo Tema** o escoba en el chat de Copilot para borrar el contexto activo).

---

## Resumen
En esta práctica se consolidaron las destrezas de análisis de datos financieros simulados traduciéndolos en un lenguaje comercial formal de nivel corporativo. La clave del éxito radicó en el uso de restricciones explícitas en el prompt de Copilot, lo que garantizó la entrega de un documento preliminar ético que diferencia las realidades financieras de las proyecciones de simulación para el cliente **Inversiones Industriales S.A.S.** Este método protege la integridad consultiva del banco y minimiza el riesgo de que el cliente malinterprete supuestos de modelado financiero como realidades garantizadas.