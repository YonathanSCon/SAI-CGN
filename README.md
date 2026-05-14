# SAI-CGN — Sistema de Auditoría Inteligente

Plataforma web con Inteligencia Artificial desarrollada para la **Contraloría General de la Nación de Colombia**, orientada a modernizar los procesos de auditoría fiscal mediante detección automática de anomalías, consulta de normativa vigente y gestión integral del ciclo de vida de las auditorías.

---

## 📌 Estado del proyecto

![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-blue)
![Fase](https://img.shields.io/badge/Fase%20actual-Análisis-yellow)
![Duración](https://img.shields.io/badge/Duración-6%20meses-lightgrey)
![Versión docs](https://img.shields.io/badge/Docs-v1.0-green)

---

## 🧠 ¿Qué es SAI-CGN?

El SAI-CGN es una aplicación diseñada para asistir a los auditores de la Contraloría General de la Nación en sus procesos de fiscalización. Actualmente los auditores invierten cerca del 60% de su tiempo en recopilación manual de información; el sistema busca reducir esa carga mediante el uso de Inteligencia Artificial, permitiéndoles enfocarse en el análisis y la toma de decisiones.

El sistema se compone de ocho módulos principales:

| Módulo | Descripción |
|--------|-------------|
| M01 — Gestión de Usuarios | Control de acceso basado en roles (RBAC) e integración SSO institucional |
| M02 — Ingesta de Datos | Carga, validación y conexión automática con SECOP II, CHIP y SIRECI |
| M03 — Motor de IA | Detección de anomalías fiscales y clasificación de riesgos con Machine Learning |
| M04 — Asistente RAG | Consulta de normativa fiscal en lenguaje natural con citas de fuentes |
| M05 — Gestión de Auditorías | Ciclo de vida completo de los procesos auditores |
| M06 — Generación de Informes | Informes automáticos bajo plantillas oficiales CGN con firma digital |
| M07 — Trazabilidad y Hallazgos | Registro, seguimiento y cierre de hallazgos fiscales |
| M08 — Seguridad | Cifrado, logs de auditoría y cumplimiento del Marco de Seguridad Digital MINTIC |

---

## 🔄 Ciclo de Vida del Desarrollo

El proyecto sigue un ciclo de vida estructurado en cinco fases secuenciales. Cada fase, a excepción de la primera, requiere la aprobación formal del cliente (CGN) antes de avanzar a la siguiente.

---

### 📋 Fase 1 — Análisis ✅ Completa

Levantamiento y documentación formal de todos los requisitos del sistema. Es la base de todo el ciclo de vida; los demás documentos de las fases siguientes parten de los artefactos producidos aquí.

| # | Documento | Descripción | Versión | Estado |
|---|-----------|-------------|---------|--------|
| 1 | **ERS / SRS** | Especificación de Requisitos de Software — 36 RF y 17 RNF bajo el estándar IEEE 830-1998 | v1.0 | ✅ |
| 2 | **Acta de Levantamiento** | 4 sesiones con stakeholders CGN, hallazgos, compromisos y priorización MoSCoW | v1.0 | ✅ |
| 3 | **Historias de Usuario** | 17 HU con criterios de aceptación y Definición de Terminado (DoD) | v1.0 | ✅ |
| 4 | **Matriz de Trazabilidad** | Vínculos bidireccionales RF ↔ RNF ↔ HU ↔ Casos de prueba ↔ Sesiones | v1.0 | ✅ |
| 5 | **Gestión de Cambios** | Proceso CCB, formulario RFC, Change Log e indicadores de control | v1.0 | ✅ |

📁 Ubicación: `docs/01-analisis/`

---

### 🔧 Fase 2 — Selección de Herramientas ⏳ Pendiente

Con base en los requisitos definidos en la fase de Análisis — en particular las restricciones de soberanía de datos, la arquitectura de microservicios, las integraciones con sistemas legacy y los modelos de IA requeridos — se seleccionará el stack tecnológico del proyecto.

| Categoría | Por definir |
|-----------|-------------|
| Frontend | — |
| Backend | — |
| Base de datos | — |
| Motor de IA / ML | — |
| Modelo LLM (RAG) | — |
| Orquestación de contenedores | — |
| CI/CD | — |
| Seguridad y autenticación | — |

📁 Ubicación: `docs/02-herramientas/` *(próximamente)*

---

### 🎨 Fase 3 — Diseño ⏳ Pendiente

Elaboración de los diagramas y modelos de diseño derivados de los artefactos de la fase de Análisis. Al finalizar esta fase se presenta al cliente para su aprobación formal antes de iniciar el desarrollo.

| Diagrama / Artefacto | Descripción |
|----------------------|-------------|
| Diagrama de arquitectura del sistema | Vista general de microservicios y componentes |
| Diagrama de casos de uso | Interacciones de los 5 roles con los 8 módulos |
| Diagrama entidad-relación (ER) | Modelo de datos del sistema |
| Diagrama de clases | Estructura orientada a objetos del backend |
| Diagramas de secuencia | Flujos críticos (autenticación, detección de anomalías, generación de informes) |
| Diagrama de despliegue | Infraestructura de contenedores y servicios |
| Wireframes / Mockups | Diseño de interfaces de usuario por módulo |
| Modelo de datos de IA | Estructura de features y pipeline de ML |

📁 Ubicación: `docs/03-diseno/` *(próximamente)*

> 🔐 **Punto de aprobación del cliente:** La CGN debe aprobar formalmente los artefactos de diseño antes de iniciar la fase de Desarrollo.

---

### 💻 Fase 4 — Desarrollo ⏳ Pendiente

Construcción del software: codificación de los 8 módulos del sistema, integración entre componentes e integración con los sistemas institucionales (SECOP II, CHIP, SIRECI, LDAP). El desarrollo se ejecuta en 6 sprints de 3 semanas cada uno.

| Sprint | Período | Módulos principales |
|--------|---------|---------------------|
| Sprint 1 | May 12 – May 30 | M01 Usuarios · M08 Seguridad |
| Sprint 2 | Jun 2 – Jun 20 | M02 Ingesta · M05 Auditorías |
| Sprint 3 | Jun 23 – Jul 11 | M03 Motor IA · M04 Asistente RAG |
| Sprint 4 | Jul 14 – Aug 1 | M06 Informes · M07 Hallazgos |
| Sprint 5 | Ago 4 – Ago 22 | Integración completa · Ajustes UX |
| Sprint 6 | Ago 25 – Sep 12 | Estabilización · Preparación despliegue |

📁 Ubicación: `src/` *(próximamente)*

> 🔐 **Punto de aprobación del cliente:** La CGN debe aprobar formalmente el sistema construido antes de iniciar la fase de Pruebas.

---

### 🧪 Fase 5 — Pruebas ⏳ Pendiente

Definición, estructuración y ejecución de los documentos y casos de prueba fundamentales del proyecto. Al finalizar se presenta al cliente para su aprobación antes de pasar a producción.

| # | Documento | Descripción |
|---|-----------|-------------|
| 1 | **Plan de Pruebas** | Estrategia general, tipos de prueba, alcance y recursos |
| 2 | **Casos de Prueba** | 53 CP detallados (CP-01 a CP-36 + CP-R01 a CP-R17) |
| 3 | **Informe de Pruebas Unitarias** | Resultados de cobertura ≥ 80% por módulo |
| 4 | **Informe de Pruebas de Integración** | Validación de flujos entre módulos y sistemas externos |
| 5 | **Informe de Pruebas de Rendimiento** | Verificación de SLA (200 usuarios, tiempos de respuesta) |
| 6 | **Informe de Pentest** | Resultados de prueba de penetración externa (RNF-11) |
| 7 | **Informe de Pruebas de Aceptación (UAT)** | Validación con auditores reales de la CGN |

📁 Ubicación: `docs/05-pruebas/` *(próximamente)*

> 🔐 **Punto de aprobación del cliente:** La CGN debe aprobar formalmente los resultados de pruebas antes del despliegue en producción.

---

### 🚀 Fase 6 — Implementación ⏳ Pendiente

Despliegue del sistema en el ambiente de producción de la CGN. Esta fase toma como punto de partida los artefactos de la fase de Análisis para verificar que todo lo acordado fue implementado y está funcionando correctamente en producción.

| Actividad | Descripción |
|-----------|-------------|
| Despliegue en producción | Configuración del ambiente productivo en infraestructura CGN |
| Migración de datos | Carga inicial de datos históricos e integración con sistemas legacy |
| Capacitación de usuarios | Formación a auditores, analistas y administradores |
| Plan de rollout | Despliegue progresivo por grupos de usuarios |
| Soporte post-despliegue | Acompañamiento durante los primeros 30 días en producción |
| Acta de entrega y cierre | Documento formal de entrega del sistema a la CGN |

📁 Ubicación: `docs/06-implementacion/` *(próximamente)*

---

## 📁 Estructura completa del repositorio

SAI-CGN/
├── README.md
├── docs/
│   ├── 01-analisis/
│   │   ├── ERS_SAI-CGN.docx
│   │   ├── Acta_Levantamiento_SAI-CGN.docx
│   │   ├── Historias_Usuario_SAI-CGN.docx
│   │   ├── Matriz_Trazabilidad_SAI-CGN.docx
│   │   └── Gestion_Cambios_SAI-CGN.docx
│   ├── 02-herramientas/        ← próximamente
│   ├── 03-diseno/              ← próximamente
│   ├── 04-desarrollo/          ← próximamente
│   ├── 05-pruebas/             ← próximamente
│   └── 06-implementacion/      ← próximamente
└── src/                        ← próximamente

---

## 🏛️ Contexto institucional

- **Cliente:** Contraloría General de la Nación — Dirección de Control Fiscal
- **País:** Colombia
- **Marco normativo:** Ley 1581/2012 · Ley 594/2000 · Decreto 1008/2018 · Resolución Orgánica 7350 CGN
- **Integraciones:** SECOP II · CHIP · SIRECI · LDAP institucional · ONAC (firma digital)

---

## 👥 Equipo del proyecto

| Rol | Nombre |
|-----|--------|
| Líder de Proyecto | Mauricio Torres |
| Director de Control Fiscal CGN | Carlos Martínez |
| Subdirectora de Sistemas CGN | Laura Rodríguez |
| Auditor Líder Senior CGN | Jorge Patiño |
| Científico de Datos | Sebastián Ríos |

---

## 📋 Convenciones

| Prefijo | Significado |
|---------|-------------|
| `RF-XX` | Requisito Funcional |
| `RNF-XX` | Requisito No Funcional |
| `HU-XX` | Historia de Usuario |
| `CP-XX` | Caso de Prueba |
| `RFC-XXX` | Solicitud de Cambio de Requisito |
| `M0X` | Módulo del sistema (M01 – M08) |
| `S1–S6` | Sprints de desarrollo (3 semanas c/u) |
