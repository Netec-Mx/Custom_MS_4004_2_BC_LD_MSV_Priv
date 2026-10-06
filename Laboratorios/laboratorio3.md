# Lab 01-00-03: Práctica 3: Análisis de Datos de Inversiones Industriales S.A.S. con Copilot Analyst

## Metadatos

| Dimensión | Detalle |
| :--- | :--- |
| **Duración** | 13 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Aplicar |

## Descripción General

En este laboratorio práctico, asumirá el rol de un consultor de negocios senior de Bancolombia que trabaja con el cliente corporativo ficticio **"Inversiones Industriales S.A.S."** (perteneciente al sector de alimentos procesados y agroindustria de mediana escala en Colombia). 

Su tarea consiste en analizar un conjunto de datos financieros estructurados distribuidos en tres pestañas críticas dentro del libro de trabajo `Datos_Cliente_Ficticio.xlsx`. Utilizando el agente especializado de IA, **Copilot Analyst en Excel**, identificará patrones financieros, aislará variaciones regionales anómalas y estructurará prompts avanzados para separar sistemáticamente los hechos comprobados (datos empíricos) de las hipótesis comerciales que requerirán una validación de campo posterior.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, el participante será capaz de:
- [ ] Analizar un dataset estructurado y multipestaña de un cliente corporativo mediante el agente especializado **Copilot Analyst** en Microsoft Excel.
- [ ] Detectar anomalías financieras, variaciones drásticas en la facturación regional y cuellos de botella en proyectos de inversión.
- [ ] Diseñar prompts complejos basados en metodologías de interrogación analítica para catalogar de forma precisa hechos contrastados versus hipótesis de negocio.
- [ ] Evaluar la resiliencia del modelo analítico de IA frente a anomalías de datos y valores faltantes (pruebas adversarias).

## Prerrequisitos

### 1. Conocimientos Necesarios
- Comprensión básica de la navegación en Microsoft Excel (creación de tablas, guardado y sincronización en la nube).
- Comprensión conceptual de los términos: *Ingresos*, *Egresos*, *Margen Operativo*, *Hecho* (dato histórico verificado) e *Hipótesis* (supuesto de negocio a validar).

### 2. Cuentas y Accesos
- Licencia activa de **Microsoft 365 Copilot Premium** asignada a su cuenta de Microsoft 365.
- Acceso a la aplicación de escritorio de **Microsoft Excel para M365** con la barra de Copilot habilitada.
- Sincronización activa de **Microsoft OneDrive para la Empresa** habilitada en el equipo local.

---

## Entorno de Laboratorio

Para garantizar la correcta ejecución del laboratorio, verifique que los recursos del sistema cumplan con las especificaciones técnicas requeridas:

### Requisitos de Hardware y Software

| Componente | Especificación Mínima | Origen / Enlace Oficial |
| :--- | :--- | :--- |
| **Sistema Operativo** | Windows 11 Enterprise (Versión 23H2, arquitectura x64) | [Microsoft Windows 11 Enterprise](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise) |
| **Aplicación de Análisis** | Microsoft Excel para M365 (Canal Mensual, Versión 2408 Build 17928.20156 64-bit) | [Microsoft 365 Apps for Enterprise](https://www.microsoft.com/es-es/microsoft-365/enterprise/microsoft-365-apps-for-enterprise) |
| **Licencia de IA** | Microsoft 365 Copilot Premium (Service Update Q2-2024) | [Microsoft 365 Copilot Admin Center](https://admin.microsoft.com/) |
| **Sincronización** | Microsoft OneDrive para la Empresa (v24.161.0811.0001) | [Microsoft OneDrive Desktop](https://www.microsoft.com/es-es/microsoft-365/onedrive/download) |

### Constantes de Entorno
* **Directorio de Trabajo local:** `C:\CopilotLabs\Modulo1`
* **Nombre de Archivo:** `Datos_Cliente_Ficticio.xlsx`
* **Cliente de Referencia:** *Inversiones Industriales S.A.S.*

---

## Instrucciones Paso a Paso

### Paso 1: Configurar el Entorno de Trabajo y Generar el Dataset Corporativo

**Objetivo:** Crear de forma automatizada y estructurada el directorio de trabajo local y el archivo de datos de simulación con las tres pestañas requeridas para el análisis de Copilot.

**Instrucciones:**

1. Haga clic en el botón de Inicio de Windows, busque **PowerShell**, haga clic derecho sobre la aplicación y seleccione **Ejecutar como Administrador**.
2. Copie y pegue el siguiente bloque de comandos en la consola de PowerShell para crear automáticamente el directorio de trabajo, instanciar un objeto COM de Excel y generar el archivo `Datos_Cliente_Ficticio.xlsx` estructurado como tablas de Excel formales (las cuales son estrictamente necesarias para el correcto funcionamiento de Copilot Analyst):

```powershell
## 1. Crear el directorio de trabajo por defecto del módulo
$WorkDir = "C:\CopilotLabs\Modulo1"
if (!(Test-Path -Path $WorkDir)) {
    New-Item -ItemType Directory -Force -Path $WorkDir
}

## 2. Inicializar Excel mediante interfaz COM para crear el dataset simulado de Inversiones Industriales S.A.S.
$excel = New-Object -ComObject Excel.Application
$excel.Visible = $false
$excel.DisplayAlerts = $false
$workbook = $excel.Workbooks.Add()

## --- PESTAÑA 1: Resumen_Financiero ---
$sheet1 = $workbook.Sheets.Item(1)
$sheet1.Name = "Resumen_Financiero"
$sheet1.Cells.Item(1,1) = "Año"
$sheet1.Cells.Item(1,2) = "Ingresos_COP"
$sheet1.Cells.Item(1,3) = "Egresos_COP"
$sheet1.Cells.Item(1,4) = "Utilidad_Neta_COP"
$sheet1.Cells.Item(1,5) = "Margen_Operativo"

## Insertar registros históricos (Con anomalía marcada en 2023)
$data1 = @(
    @("2020", 14000000000, 10500000000, 3500000000, 0.25),
    @("2021", 15000000000, 11000000000, 4000000000, 0.26),
    @("2022", 18500000000, 13200000000, 5300000000, 0.28),
    @("2023", 16200000000, 14100000000, 2100000000, 0.13), # Anomalía: Ingresos caen, egresos aumentan
    @("2024", 19100000000, 14300000000, 4800000000, 0.25)
)

for ($r=0; $r -lt $data1.Length; $r++) {
    for ($c=0; $c -lt 5; $c++) {
        $sheet1.Cells.Item($r+2, $c+1) = $data1[$r][$c]
    }
}
## Formatear como Tabla de Excel (Obligatorio para Copilot)
$range1 = $sheet1.Range("A1:E6")
$tbl1 = $sheet1.ListObjects.Add(1, $range1, $null, 1)
$tbl1.Name = "TablaResumenFinanciero"

## --- PESTAÑA 2: Ventas_Regionales ---
$sheet2 = $workbook.Sheets.Add($null, $sheet1)
$sheet2.Name = "Ventas_Regionales"
$sheet2.Cells.Item(1,1) = "Region"
$sheet2.Cells.Item(1,2) = "Unidad_Negocio"
$sheet2.Cells.Item(1,3) = "Facturacion_2022"
$sheet2.Cells.Item(1,4) = "Facturacion_2023"
$sheet2.Cells.Item(1,5) = "Facturacion_2024"

$data2 = @(
    @("Andina", "Alimentos Procesados", 6000000000, 6500000000, 7100000000),
    @("Andina", "Agroindustrial", 3500000000, 3700000000, 4000000000),
    @("Caribe", "Alimentos Procesados", 4200000000, 2400000000, 3900000000), # Caída drástica del 42.8% en 2023
    @("Caribe", "Agroindustrial", 2100000000, 1100000000, 1900000000), # Caída drástica del 47.6% en 2023
    @("Pacifica", "Alimentos Procesados", 1500000000, 1600000000, 1750000000),
    @("Pacifica", "Agroindustrial", 1200000000, 900000000, 450000000)      # Caída sostenida Pacifica
)

for ($r=0; $r -lt $data2.Length; $r++) {
    for ($c=0; $c -lt 5; $c++) {
        $sheet2.Cells.Item($r+2, $c+1) = $data2[$r][$c]
    }
}
$range2 = $sheet2.Range("A1:E7")
$tbl2 = $sheet2.ListObjects.Add(1, $range2, $null, 1)
$tbl2.Name = "TablaVentasRegionales"

## --- PESTAÑA 3: Proyectos_Inversion ---
$sheet3 = $workbook.Sheets.Add($null, $sheet2)
$sheet3.Name = "Proyectos_Inversion"
$sheet3.Cells.Item(1,1) = "ID_Proyecto"
$sheet3.Cells.Item(1,2) = "Nombre_Proyecto"
$sheet3.Cells.Item(1,3) = "Presupuesto_COP"
$sheet3.Cells.Item(1,4) = "Estado"
$sheet3.Cells.Item(1,5) = "Retorno_Estimado_M365"

$data3 = @(
    @("PRJ-01", "Modernizacion Planta Caribe", 1200000000, "Demorado", 0.15),
    @("PRJ-02", "Optimizacion Cadena Andina", 800000000, "Completado", 0.22),
    @("PRJ-03", "Logistica Frio Pacifica", 1500000000, "En Ejecucion", 0.18),
    @("PRJ-04", "Cultivos Alternativos Orinoquia", 2000000000, "Planificado", 0.25),
    @("PRJ-05", "Proyecto Inyeccion Incompleto", $null, "Cancelado", $null) # Fila adversarial con nulos
)

for ($r=0; $r -lt $data3.Length; $r++) {
    for ($c=0; $c -lt 5; $c++) {
        $sheet3.Cells.Item($r+2, $c+1) = $data3[$r][$c]
    }
}
$range3 = $sheet3.Range("A1:E6")
$tbl3 = $sheet3.ListObjects.Add(1, $range3, $null, 1)
$tbl3.Name = "TablaProyectosInversion"

## Guardar y cerrar Excel de forma limpia
$FilePath = Join-Path $WorkDir "Datos_Cliente_Ficticio.xlsx"
$workbook.SaveAs($FilePath)
$workbook.Close($true)
$excel.Quit()
[System.Runtime.InteropServices.Marshal]::ReleaseComObject($excel) | Out-Null
Write-Host "Entorno configurado correctamente. Archivo de datos creado en: $FilePath" -ForegroundColor Green
```

3. Verifique el éxito del comando en la consola de PowerShell.

**Resultado esperado:** El script debe finalizar sin errores, retornando la ruta completa donde se guardó el archivo y cerrando de manera limpia los subprocesos en segundo plano del motor COM de Microsoft Excel.

**Verificación:** 
Abra el Explorador de Archivos y navegue a `C:\CopilotLabs\Modulo1\`. Asegúrese de que el archivo `Datos_Cliente_Ficticio.xlsx` exista y tenga un tamaño aproximado mayor a 10 KB.

---

### Paso 2: Análisis Inicial con el Agente Copilot Analyst en Excel

**Objetivo:** Interactuar de manera guiada con el agente integrado **Copilot Analyst** de Microsoft Excel para escanear de forma global las tendencias e identificar anomalías macroeconómicas y financieras internas de *Inversiones Industriales S.A.S.*

**Instrucciones:**

1. Con el fin de garantizar el acceso a las funciones completas de coautoría e Inteligencia Artificial en tiempo real, copie el archivo `Datos_Cliente_Ficticio.xlsx` a su carpeta sincronizada de **OneDrive para la Empresa** de Bancolombia, o bien ábralo y active el interruptor **Autoguardado** en la esquina superior izquierda de Microsoft Excel.
2. Una vez abierto el archivo desde su ubicación en la nube, navegue a la pestaña **Resumen_Financiero**.
3. Asegúrese de hacer clic en cualquier celda dentro del rango de datos formateado como tabla (por ejemplo, en la celda `B2`).
4. En la barra de herramientas principal (pestaña *Inicio*), localice y haga clic en el botón de **Copilot** (ubicado en el extremo derecho) para abrir el panel lateral del agente interactivo.

[VISUAL: 01-00-03-0001 - Ubicación del botón oficial de 'Copilot' en el menú superior derecho de Excel y apertura del panel de conversación lateral.]

5. En el cuadro de chat de Copilot, escriba la siguiente instrucción estructurada aplicando las técnicas de *grounding*:

```text
Actúa como un Analista Financiero Senior. Analiza la tendencia histórica de ingresos, egresos y margen operativo de la tabla 'TablaResumenFinanciero'. Identifica cuál fue el peor año fiscal en términos de eficiencia operativa, cuantifica la caída porcentual del margen operativo respecto al año inmediatamente anterior y genera una hipótesis preliminar de por qué se causó este comportamiento basándote exclusivamente en la relación ingresos/egresos del dataset.
```

6. Presione **Enter** para enviar el prompt al motor de IA.

**Resultado esperado:** El agente Copilot Analyst responderá analizando la tabla. Deberá destacar que el peor año fue **2023**, indicando que el margen operativo cayó de un **28% en 2022** a un **13% en 2023** (un retroceso sustancial de 15 puntos porcentuales o una caída relativa del ~53.5%), debido a que los ingresos disminuyeron en un 12.4% mientras que los egresos operativos se incrementaron en un 6.8%.

**Verificación:**
Valide que los números de la respuesta de la IA coincidan matemáticamente con los datos cargados en la pestaña. Copilot ofrecerá también la opción de "Crear una hoja de análisis", haga clic sobre esa sugerencia automática para que el agente agregue de forma automática una nueva pestaña con una gráfica de visualización del desplome operativo de 2023.

---

### Paso 3: Separación Metódica de Hechos e Hipótesis mediante Prompt Estructurado

**Objetivo:** Segmentar de manera quirúrgica y lógica los resultados del análisis en datos comprobables en el archivo (hechos empíricos) versus supuestos explicativos que dependan de factores externos del mercado de alimentos en Colombia (hipótesis).

**Instrucciones:**

1. Cambie a la pestaña **Ventas_Regionales** dentro de Excel.
2. Haga clic en una celda dentro de la tabla (rango `A1:E7`).
3. En el panel lateral del agente Copilot, ingrese el siguiente prompt avanzado estructurado bajo la técnica de *Aislamiento Epistémico*:

```text
Objetivo: Generar una matriz de diagnóstico de ventas para la junta directiva de Inversiones Industriales S.A.S.
Contexto: Necesitamos entender el desplome de ventas entre 2022 y 2023.
Instrucciones analíticas:
1. Analiza el comportamiento de la facturación en la región Caribe para las dos unidades de negocio de forma independiente.
2. Identifica el porcentaje de reducción en ambas unidades en 2023.
3. Clasifica la salida obligatoriamente en dos categorías:
   - HECHOS COMPROBADOS: Métricas exactas extraídas directamente de la tabla 'TablaVentasRegionales'.
   - HIPÓTESIS COMERCIALES: Suposiciones lógicas basadas en la naturaleza agroindustrial y de alimentos procesados en la costa colombiana que expliquen estos números pero que NO se puedan probar solo con el archivo.
Formato de salida esperado: Devuelve una tabla limpia con dos columnas: [Tipo de Hallazgo] y [Descripción detallada con cifras o supuestos].
```

[VISUAL: 01-00-03-0002 - Captura del prompt avanzado introducido en el cuadro de texto del panel Copilot Analyst, ilustrando la división clara entre Hechos e Hipótesis.]

4. Haga clic en **Enviar** y observe cómo el agente ejecuta el análisis.

**Resultado esperado:** El agente Copilot Analyst interpretará correctamente las relaciones regionales y presentará una estructura como la siguiente:
* **Hechos Comprobados:**
  * Facturación de *Alimentos Procesados* en Caribe cayó de COP 4.2B (2022) a COP 2.4B (2023) (un -42.8%).
  * Facturación de *Agroindustrial* en Caribe cayó de COP 2.1B (2022) a COP 1.1B (2023) (un -47.6%).
* **Hipótesis Comerciales:**
  * La caída drástica en Caribe podría estar asociada a fenómenos climáticos (como sequías que alteraron el suministro de materia prima agroindustrial) o demoras logísticas severas en la cadena de frío costera durante el año 2023, aspectos que requieren cruce con fuentes externas de datos meteorológicos y operativos del sector.

**Verificación:**
Haga clic en el botón "Copiar" que aparece al final de la respuesta generada por Copilot y pegue dicha matriz en la celda `G2` de la misma hoja para dejar constancia física del entregable analítico.

---

## Validación y Pruebas

Para asegurar la calidad y exactitud del proceso analítico ejecutado con Microsoft Copilot, realice las siguientes pruebas del sistema de inteligencia artificial:

### 1. Validación de Precisión Analítica (Fórmula de Control)
Realice la operación manual del desplome porcentual de la unidad *Agroindustrial* en la región Caribe para verificar la veracidad matemática de las cifras expuestas por Copilot en el Paso 3:
* **Año 2022 (Base):** COP 2.100.000.000
* **Año 2023:** COP 1.100.000.000
* **Cálculo de Variación:** 
  $$\Delta\% = \frac{1.100.000.000 - 2.100.000.000}{2.100.000.000} \times 100 \approx -47.61\%$$

*Copilot debe haber arrojado un valor redondeado a -47.6% o -48% de variación en su respuesta. Si el valor difiere sustancialmente, se ha detectado una alucinación numérica.*

### 2. Prueba Adversaria: Comportamiento ante Datos Incompletos o Nulos (Data Injection)
Con el fin de comprobar el comportamiento del agente frente a inconsistencias en los datos, navegue a la pestaña **Proyectos_Inversion**:
1. Ejecute el siguiente prompt en el chat de Copilot:
```text
Analiza la tabla de proyectos de inversión y calcula el costo promedio total de inversión planificada y ejecutada para Inversiones Industriales S.A.S. ¿Cómo afecta el proyecto 'PRJ-05' al cálculo matemático de este indicador y qué advertencia nos da el estado del proyecto 'PRJ-01'?
```
2. **Resultado Esperado de Resiliencia de IA:** El agente de IA debe identificar correctamente que:
   - El costo promedio de los proyectos con datos es:
     $$\text{Promedio} = \frac{1.2B + 0.8B + 1.5B + 2.0B}{4} = \text{COP } 1.375.000.000$$
   - Debe alertar que el registro `PRJ-05` contiene valores nulos (`NULL`) bajo la columna `Presupuesto_COP` debido a su estado "Cancelado", por lo cual se le excluye de forma segura de las sumas agregadas tradicionales.
   - Debe reportar de manera proactiva que el proyecto `PRJ-01` (*Modernización Planta Caribe*) está catalogado como "Demorado" con un presupuesto asignado considerable de COP 1.2B, lo cual apoya empíricamente la hipótesis del Paso 3 sobre las ineficiencias de entrega en la región norte.

---

## Solución de Problemas

A continuación se describen los dos errores de ejecución más comunes durante el uso de Copilot en Microsoft Excel junto con sus respectivas soluciones:

### Caso 1: El botón de "Copilot" aparece inhabilitado o en color gris en la barra superior de Excel
* **Causa raíz:** Copilot en Excel requiere estrictamente que el libro esté guardado en un entorno de almacenamiento en la nube moderno (SharePoint Online o OneDrive para la Empresa) y que el interruptor de **Autoguardado** esté activado (`ON`). Los archivos locales del disco `C:` sin sincronizar no son accesibles para la API de procesamiento seguro de Microsoft Graph en tiempo real.
* **Resolución:**
  1. Guarde una copia de su archivo directamente en su carpeta corporativa sincronizada de OneDrive local (`C:\Users\[TuUsuario]\OneDrive - Bancolombia\`).
  2. Verifique que la esquina superior izquierda del software muestre el control deslizante de **Autoguardado** en verde.
  3. Cierre y vuelva a abrir el archivo. El botón de Copilot se iluminará automáticamente.

### Caso 2: Copilot arroja el error "No puedo analizar este archivo porque no contiene datos en un formato compatible"
* **Causa raíz:** A diferencia de las herramientas genéricas de generación de texto, el agente Copilot Analyst de Excel opera de forma exclusiva sobre objetos de estructura de datos relacionales bien definidos, conocidos formalmente como **Tablas de Excel** (instanciadas internamente como `ListObjects`). Si los datos están simplemente escritos en celdas sin un encabezado estructurado o formato de tabla, el modelo de IA los rechazará.
* **Resolución:**
  1. Seleccione con el cursor el rango total de datos que desea analizar (por ejemplo, desde la celda `A1` hasta la `E6`).
  2. Presione el atajo de teclado **Ctrl + T** (o vaya a *Inicio > Dar formato como tabla*).
  3. Asegúrese de marcar la casilla *"La tabla tiene encabezados"* y haga clic en **Aceptar**.
  4. Ejecute nuevamente su consulta en el panel lateral de Copilot.

---

## Limpieza

Para restaurar de forma segura el entorno a su estado original sin perder los resultados analíticos para posibles consultas comerciales futuras del módulo:

1. Guarde y asegúrese de que el archivo final `Datos_Cliente_Ficticio.xlsx` quede debidamente sincronizado en su carpeta de OneDrive para la Empresa con el fin de evitar pérdida de progreso.
2. Cierre por completo la aplicación de escritorio de **Microsoft Excel**.
3. Abra su consola de **PowerShell** como administrador y ejecute el siguiente comando para liberar los objetos COM residentes y evitar fugas de memoria en la máquina local:
```powershell
## Detener de manera forzada instancias huérfanas de Excel generadas durante la automatización COM
Get-Process | Where-Object {$_.Name -eq "excel"} | Stop-Process -Force
Write-Host "Procesos limpiados y memoria liberada con éxito." -ForegroundColor Yellow
```

---

## Resumen

En este laboratorio práctico, ha utilizado las capacidades de **Microsoft 365 Copilot Analyst** en Excel para ejecutar una auditoría de rendimiento sobre los datos ficticios de la empresa *Inversiones Industriales S.A.S.*

**Logros Clave de Negocio:**
* **Análisis de Impacto Macro:** Detectó que el desplome financiero del cliente ocurrió en **2023**, perdiendo la mitad de su eficiencia con un margen operativo que cayó al **13%**.
* **Micro-Segmentación Regional:** Identificó que las unidades operativas más afectadas se concentraron en la región **Caribe**, donde ambas unidades productivas sufrieron contracciones cercanas al **45%**.
* **Metodología de Aislamiento:** Aprendió a construir prompts especializados para separar claramente **Hechos** (desplome del Caribe del ~42.8% y ~47.6%) de **Hipótesis** (posibles fallas climáticas, retrasos en la modernización de planta que se asocian al proyecto demorado `PRJ-01` de COP 1.2B).

Este ejercicio establece los cimientos cuantitativos empíricos para estructurar una posterior presentación ejecutiva de mitigación de riesgos dirigida a la junta directiva de su cliente corporativo.