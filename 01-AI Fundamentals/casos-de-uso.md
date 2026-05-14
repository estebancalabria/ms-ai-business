# AI en la Empresa — Parte 2: Casos de Uso
## Chevron · Audiencia ejecutiva y de negocios

> Este documento cubre la segunda parte de la charla de AI empresarial, organizada en cuatro secciones según el nivel de madurez tecnológica y el perfil del usuario. Todos los casos de uso están orientados al contexto de Chevron y la industria de oil & gas.

---

## Tabla de contenidos

1. [Power Users con M365 Copilot](#1-power-users-con-m365-copilot)
2. [Herramientas No-Code: Power Platform + Copilot Studio](#2-herramientas-no-code-power-platform--copilot-studio)
3. [Azure AI Foundry: Soluciones a medida con LLMs](#3-azure-ai-foundry-soluciones-a-medida-con-llms)
4. [Machine Learning: Modelos predictivos y de optimización](#4-machine-learning-modelos-predictivos-y-de-optimización)
5. [Referencias](#referencias)

---

## 1. Power Users con M365 Copilot

**Perfil:** Ingenieros, analistas, equipos legales, operaciones.  
**Stack:** Microsoft 365 Copilot (Word, Excel, Teams, Power BI).  
**Valor:** Productividad individual y de equipos técnicos sin cambiar las herramientas existentes.

### Caso 1.1 — Síntesis de reportes técnicos de pozo

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot en Word |
| **Usuario** | Ingenieros de perforación |
| **Situación** | Decenas de drilling reports y completion reports por pozo, en PDF y documentos dispersos |
| **Solución** | Copilot resume los reportes, extrae parámetros críticos (ROP, presiones, incidencias) y genera un resumen ejecutivo en minutos |
| **Evidencia Chevron** | Caso documentado: Chevron usaba OCR + AI para extracción de datos de drilling y completion reports en asociación con Microsoft |

**Prompt de ejemplo:**
```
Resume este drilling report destacando: profundidad alcanzada, problemas operativos, 
parámetros de perforación fuera de rango y recomendaciones del equipo.
```

---

### Caso 1.2 — Análisis de contratos y cláusulas HSE

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot en Word + Excel |
| **Usuario** | Equipo legal, contratos, procurement |
| **Situación** | Revisión manual de contratos con proveedores, identificación de cláusulas de riesgo HSE |
| **Solución** | Copilot compara versiones, detecta cláusulas de riesgo, genera tabla resumen de diferencias y redacta respuestas |
| **Evidencia Chevron** | Chevron implementó NLP + OCR para hacer más eficiente la revisión contractual y recuperación de información |

**Prompt de ejemplo:**
```
Compara estas dos versiones del contrato. Lista todas las cláusulas que cambiaron 
relacionadas con responsabilidad HSE y penalidades por incumplimiento.
```

---

### Caso 1.3 — Meeting intelligence en operaciones

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot en Microsoft Teams |
| **Usuario** | Coordinadores de operaciones, gerentes de planta |
| **Situación** | Reuniones de coordinación diarias/semanales con mucha información verbal que se pierde |
| **Solución** | Copilot transcribe, resume, genera action items automáticos y permite consultar lo decidido post-reunión con lenguaje natural |
| **Impacto** | Según estudio UK Gov (14.500 usuarios): ahorro promedio de 26 minutos por persona por día |

**Prompt de ejemplo:**
```
¿Qué se decidió sobre el turnaround de la Planta Oronite en la reunión de ayer?
¿Quién quedó como responsable y cuál es la fecha comprometida?
```

---

### Caso 1.4 — Dashboards de performance con lenguaje natural

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot en Power BI |
| **Usuario** | Analistas de negocio, gerentes operativos |
| **Situación** | Dependencia del equipo de BI para cualquier nueva visualización |
| **Solución** | El analista describe la visualización en lenguaje natural; Copilot genera la query DAX y el gráfico sin intervención técnica |

**Prompt de ejemplo:**
```
Mostrar producción diaria del Permian Basin comparada con el mismo período del año anterior, 
separada por tipo de pozo, con línea de tendencia.
```

---

## 2. Herramientas No-Code: Power Platform + Copilot Studio

**Perfil:** Operadores, técnicos, coordinadores, áreas de negocio.  
**Stack:** Power Apps, Power Automate, Copilot Studio, Dataverse, Teams.  
**Valor:** El negocio construye sus propias herramientas. IT habilita, no bloquea.

### Caso 2.1 — Agente de consulta sobre producción de activos

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot Studio + Dataverse + Snowflake connector |
| **Usuario** | Operadores de campo, supervisores de producción |
| **Situación** | Para saber qué pozos tuvieron más downtime se necesitaban queries SQL complejas o tickets a IT |
| **Solución** | Agente conversacional que responde preguntas en lenguaje natural sobre datos de producción |
| **Evidencia sector** | Encino Energy (O&G) implementó este patrón exacto con Copilot Studio + Dataverse + Snowflake |

**Ejemplo de interacción:**
```
Operador: ¿Qué ubicaciones tuvieron más downtime este mes y qué equipo lo causó?
Agente:    Las 3 ubicaciones con más downtime fueron: Bloque A-14 (18h), 
           Bloque C-07 (12h) y Bloque B-22 (9h). 
           En todos los casos la causa fue falla en bombas de inyección.
```

---

### Caso 2.2 — App de inspección en campo (Power Apps)

| Atributo | Detalle |
|---|---|
| **Herramienta** | Power Apps (canvas app, modo offline) |
| **Usuario** | Técnicos de campo, inspectores HSE |
| **Situación** | Inspecciones documentadas en papel, riesgo de pérdida de datos, demora en reporte de hallazgos |
| **Solución** | App móvil con checklist digital, fotos, firma y modo offline. Al volver a red sincroniza automáticamente y dispara alertas si hay hallazgo crítico |
| **Integración** | SharePoint (almacenamiento) → Power Automate (alertas) → Teams (notificación supervisor) |

**Flujo:**
```
Técnico completa checklist offline
  → Vuelve a zona con red
    → Power Apps sincroniza
      → Power Automate detecta hallazgo crítico
        → Notificación inmediata al supervisor en Teams
          → Registro en SharePoint con trazabilidad completa
```

---

### Caso 2.3 — Flujo de aprobación de órdenes de trabajo

| Atributo | Detalle |
|---|---|
| **Herramienta** | Power Automate + SAP + Dynamics 365 Field Service |
| **Usuario** | Planificadores de mantenimiento, supervisores |
| **Situación** | Aprobaciones de work orders manuales, lentas, sin trazabilidad |
| **Solución** | Flujo automatizado: trigger SAP → aprobación Teams → actualización Dynamics 365 |
| **Beneficio** | Trazable, auditable, escalable; sin código personalizado |

**Flujo:**
```
SAP genera work order
  → Power Automate notifica supervisor en Teams con botón Aprobar/Rechazar
    → Si aprueba: actualiza estado en Dynamics 365 Field Service
      → Asigna técnico disponible
        → Genera orden de compra si aplica
```

---

### Caso 2.4 — Chatbot de soporte técnico interno (HSE / Normas)

| Atributo | Detalle |
|---|---|
| **Herramienta** | Copilot Studio + SharePoint |
| **Usuario** | Todos los empleados |
| **Situación** | Consultas frecuentes sobre normas API, manuales de seguridad, procedimientos de emergencia |
| **Solución** | Agente indexa toda la documentación técnica interna y responde con cita exacta del documento fuente |
| **Diferenciador** | No alucina: siempre cita el documento. Si no lo sabe, escala a un humano |

**Ejemplo de interacción:**
```
Empleado: ¿Cuál es el procedimiento para bloqueo y etiquetado de energías peligrosas?
Agente:   Según el Manual HSE-2024, sección 4.3: [respuesta detallada]
          Fuente: HSE-Manual-2024.pdf, página 47.
```

---

## 3. Azure AI Foundry: Soluciones a medida con LLMs

**Perfil:** Equipos de IT, data, ingeniería con soporte de desarrollo.  
**Stack:** Azure OpenAI, Azure AI Search, Azure AI Foundry, Azure Maps, Content Safety.  
**Valor:** Soluciones propietarias sobre datos privados. RAG, agentes, multimodal.

### Caso 3.1 — Plataforma tipo ApEX: RAG sobre documentos geológicos

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure OpenAI + Azure AI Search (RAG) + Azure AI Foundry |
| **Usuario** | Explorationistas, geólogos, ingenieros de reservorio |
| **Situación** | Búsqueda manual en millones de archivos históricos: reportes, mapas, estudios de pozos |
| **Solución** | Sistema multi-agente que responde preguntas sobre el portafolio de exploración en segundos |
| **Evidencia Chevron** | ApEX: 4 TB de datos, 1 millón+ de archivos, múltiples agentes especializados (geoespacial, revisión de exploración, análisis de prospectos) |

**Agentes del sistema:**
```
┌─────────────────────────────────────────────┐
│              Query del explorationista       │
└────────────────────┬────────────────────────┘
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
  Agente geo-   Agente de     Agente de
  espacial      exploración   análisis de
  (mapas)       (revisión)    prospectos
        │            │            │
        └────────────┼────────────┘
                     ▼
              Respuesta integrada
              con citación de fuentes
```

**Prompt de ejemplo:**
```
¿Qué pozos exploratorios se perforaron en la Cuenca X entre 2010 y 2020 
con profundidades mayores a 4000m? ¿Cuál fue la porosidad promedio del reservorio objetivo?
```

---

### Caso 3.2 — Generación automática de estándares de ingeniería

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure OpenAI (fine-tuning o RAG) + Content Safety |
| **Usuario** | Ingenieros de confiabilidad, equipos de normas técnicas |
| **Situación** | Redacción manual de estándares, especificaciones y safety bulletins: proceso lento y dependiente de expertos |
| **Solución** | LLM entrenado sobre el corpus de normas existentes genera borradores alineados al estilo y terminología de Chevron |
| **Evidencia Chevron** | Chevron usa LLMs para generar borradores de engineering standards, specifications y safety bulletins |

**Flujo de trabajo:**
```
Ingeniero describe el estándar necesario
  → Azure OpenAI genera borrador con formato Chevron
    → Content Safety valida el contenido
      → Ingeniero revisa y aprueba
        → Publicación en SharePoint + notificación a equipos
```

---

### Caso 3.3 — Análisis sísmico con IA generativa (agente geoespacial)

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure Maps + Azure OpenAI + datos sísmicos propietarios |
| **Usuario** | Geólogos, geofísicos |
| **Situación** | Gaps en la interpolación entre pozos existentes; análisis sísmico manual consume semanas |
| **Solución** | Gen AI llena los gaps geológicos entre pozos con datos sísmicos, genera modelos de subsuelo y evalúa probabilidad de éxito del prospecto |
| **Evidencia Chevron** | Chevron trabaja con Eliis para comercializar AI propietaria de análisis sísmico; ApEX incluye agente geoespacial |

---

### Caso 3.4 — Asistente de troubleshooting para técnicos de campo

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure AI Foundry + Azure IoT + RAG sobre historial de mantenimiento |
| **Usuario** | Técnicos de campo, ingenieros de confiabilidad |
| **Situación** | Técnicos junior sin acceso a expertos para diagnóstico de fallas complejas |
| **Solución** | Agente que cruza datos del sensor + historial de mantenimiento + manuales y guía el diagnóstico paso a paso |

**Ejemplo de interacción:**
```
Técnico: La bomba B-07 tiene vibración inusual en rodamiento delantero, 
         temperatura 15°C por encima de lo normal, iniciada hace 6 horas.

Agente:  Basado en el historial de esta bomba y patrones similares:
         1. Verificar lubricación del rodamiento delantero (último cambio: 847 horas)
         2. Revisar alineación del eje (probable causa: 78% según histórico)
         3. Si persiste, programar parada preventiva en las próximas 48h
         Documento de referencia: Manual B-Series, sección 7.2.3
```

---

## 4. Machine Learning: Modelos predictivos y de optimización

**Perfil:** Equipos de data science, ingeniería de confiabilidad, operaciones avanzadas.  
**Stack:** Azure Machine Learning, Azure IoT Hub, Azure Digital Twins, Microsoft Fabric.  
**Valor:** Pasar de mantenimiento reactivo a predictivo. Optimización de operaciones con datos.

### Caso 4.1 — Mantenimiento predictivo de equipos críticos

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure IoT Hub + Azure ML + Power BI |
| **Usuario** | Ingenieros de confiabilidad, planificadores de mantenimiento |
| **Situación** | Mantenimiento basado en tiempo o reacción a fallas; downtime no planificado costoso |
| **Solución** | Modelos ML entrenados sobre datos de sensores (temperatura, vibración, presión, caudal) predicen fallas antes de que ocurran |
| **Evidencia Chevron** | Chevron conectó miles de equipos con sensores hacia Azure; planta Oronite: **60% de reducción en turnaround time** de mantenimiento de válvulas |
| **Referencia sector** | Oil & Gas: costo de downtime no planificado ~USD 500.000/hora |

**Variables típicas de sensores:**
- Temperatura de cojinetes
- Vibración (FFT)
- Presión diferencial
- Caudal
- Corriente del motor

**Pipeline de Azure ML:**
```
Azure IoT Hub (ingesta) 
  → Azure Stream Analytics (detección de anomalías en tiempo real)
    → Azure ML (modelo de probabilidad de falla)
      → Azure Event Hubs (alertas)
        → Power BI (dashboard de salud de activos)
          → Dynamics 365 Field Service (generación automática de work order)
```

---

### Caso 4.2 — Digital twins para optimización de activos

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure Digital Twins + Azure ML + Azure IoT |
| **Usuario** | Ingenieros de proceso, operadores de planta |
| **Situación** | Cambios de parámetros operativos requieren paradas o decisiones a ciegas |
| **Solución** | Gemelo digital de la planta/equipo permite simular escenarios, evaluar impacto de cambios y detectar anomalías sin riesgo operativo |
| **Evidencia Chevron** | Chevron implementa digital twins para gestión de activos y para garantizar la integridad de proyectos de secuestro de carbono (CCS) |

**Capacidades del gemelo digital:**
```
Simulación de escenarios       → "¿Qué pasa si aumento la presión 10%?"
Detección de anomalías         → Comparación modelo ideal vs estado real
Optimización continua          → Ajuste automático de parámetros
Entrenamiento de operadores    → Simulador de condiciones extremas
```

---

### Caso 4.3 — Optimización de perforación — plataforma APOLO

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure ML + datos propietarios de pozos |
| **Usuario** | Ingenieros de perforación, empresa perforadora |
| **Situación** | Parámetros de perforación (WOB, RPM, caudal de lodo) se configuraban manualmente, subóptimos |
| **Solución** | APOLO: modelo ML entrenado sobre miles de pozos del Permian Basin que optimiza el ROP (Rate of Penetration) en tiempo real |
| **Evidencia Chevron** | APOLO es una plataforma propietaria de Chevron para drilling optimization en el Permian Basin |

**Impacto de un modelo de optimización de perforación:**
- Reducción de tiempo de perforación por pozo
- Menor desgaste de barrenas
- Reducción de eventos no productivos (NPT)
- Mejor estimación de costos de pozo

---

### Caso 4.4 — Optimización de cadena de suministro

| Atributo | Detalle |
|---|---|
| **Herramienta** | Azure ML + Microsoft Fabric + Azure Synapse Analytics |
| **Usuario** | Equipo de supply chain, logística, procurement |
| **Situación** | Datos de supply chain fragmentados, decisiones de inventario reactivas |
| **Solución** | ML para predicción de demanda de materiales, optimización de inventario de repuestos críticos y scheduling inteligente de mantenimiento |
| **Evidencia Chevron** | Chevron migró su plataforma de supply chain a Azure (con Publicis Sapient) habilitando analytics avanzado y AI |

**Casos dentro del caso:**
```
Predicción de demanda       → Reducción de stockouts de repuestos críticos
Optimización de inventario  → Menor capital inmovilizado
Scheduling de mantenimiento → Sincronización con disponibilidad de materiales
Detección de fraude         → Anomalías en órdenes de compra
```

---

## Resumen ejecutivo: Mapa de madurez

```
BAJO ─────────────────────────────────────── ALTO
 Complejidad técnica / Inversión inicial

┌─────────────┐  ┌─────────────┐  ┌──────────────┐  ┌────────────┐
│  SECCIÓN 1  │  │  SECCIÓN 2  │  │  SECCIÓN 3   │  │ SECCIÓN 4  │
│ Power Users │  │  No-Code    │  │ AI Foundry   │  │    ML      │
│             │  │             │  │              │  │            │
│ Semanas     │  │ Semanas/    │  │ Meses        │  │ Meses      │
│ para adoptar│  │ meses       │  │              │  │            │
│             │  │             │  │              │  │            │
│ ROI rápido  │  │ ROI medio   │  │ ROI alto     │  │ ROI muy    │
│             │  │             │  │              │  │ alto       │
└─────────────┘  └─────────────┘  └──────────────┘  └────────────┘
     M365             Power            Azure           Azure ML
    Copilot          Platform         OpenAI          IoT Hub
```

**Recomendación de secuencia para Chevron:**

1. **Arrancar hoy:** M365 Copilot para power users — ROI inmediato, sin fricción técnica
2. **90 días:** Piloto de Copilot Studio con un agente específico (ej: consultas de producción)
3. **6 meses:** Primer proyecto Azure AI Foundry sobre un corpus de documentos críticos
4. **12 meses:** Programa de ML para mantenimiento predictivo en activos de alta criticidad

---

## Referencias

| Fuente | Caso | URL |
|---|---|---|
| Chevron Newsroom | ApEX — plataforma de exploración con IA generativa | https://www.chevron.com/newsroom/2025/q4/a-smarter-way-to-prospect-for-oil-and-gas |
| VentureBeat | Chevron usando Gen AI para exploración y generación de estándares | https://venturebeat.com/ai/how-chevron-is-using-gen-ai-to-strike-oil |
| Klover.ai | Mantenimiento predictivo Chevron + Azure, caso planta Oronite | https://www.klover.ai/chevron-ai-strategy-analysis-of-ai-powered-dominance-in-energy/ |
| EnkiAI | APOLO (drilling optimization) y ApEX como plataformas propietarias | https://enkiai.com/chevron/chevrons-ai-strategy-2025-powering-oil-data-centers |
| Microsoft Customer Stories | Encino Energy: Copilot Studio + Dataverse para consulta de producción | https://www.microsoft.com/en/customers/story/23198-encino-energy-llc-power-apps |
| Microsoft Adoption | Escenarios de Copilot para industria energética | https://adoption.microsoft.com/en-us/scenario-library/energy-and-resources/ |
| Honeywell + Chevron | Soluciones AI para gestión de alarmas en refinación | https://www.honeywell.com/us/en/press/2024/10/honeywell-and-chevron-collaborate-on-ai-assisted-solutions-for-refining-processes |
| Emerj AI Research | Extracción de datos de drilling reports y contratos con NLP/OCR | https://emerj.com/artificial-intelligence-at-chevron/ |

---

*Preparado por: Esteban Calabria — Microsoft Certified Trainer*  
*Stack de referencia: Microsoft Azure · M365 Copilot · Power Platform · Azure AI Foundry · Azure ML*
