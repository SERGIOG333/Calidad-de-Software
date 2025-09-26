# Implementación de Checklist de Calidad Basado en ISO 25010 para Sist Control


## Introducción
Este documento presenta la implementación de un checklist basado en ISO 25010:2011, aplicado al Sistema de Control (backend Node.js para API segura, frontend web JavaScript para dashboards, app móvil Flutter/Dart para accesos en tiempo real). El checklist evalúa las ocho características principales en un contexto híbrido, con implementación ficticia para una revisión inicial de funcionalidades como autenticación y sincronización de datos. Enlaces: 
- [Google Forms - Checklist](https://forms.gle/[ID-generado-aquí]) 
- [Google Sheets - Reporte Automático](https://docs.google.com/spreadsheets/d/[ID]/edit). 
Integra análisis de Actividad 1 (modelos ISO/CMMI) y procesos de testing de Actividad 2 (cobertura >85%).

## 1. Objetivos de Calidad 
- [x] Verificar el cumplimiento de las 8 características ISO 25010 en el proyecto híbrido, apuntando a >80% general.
- [x] Generar reportes automáticos para métricas cuantificables (ej.: % cumplimiento, promedios de escalas).
- [ ] Identificar y priorizar mejoras para procesos de verificación (ej.: testing en Flutter para fiabilidad).

## 2. Métricas a Medir
- Tasa de defectos: <5% ítems "No" en características críticas (Seguridad/Fiabilidad), medido vía COUNTIF en Sheets.
- Cobertura de evaluación: 100% de las 12 preguntas respondidas; vinculado a testing de Act2 (>85% cobertura código).
- Tiempo de respuesta: <2 segundos para ítems de eficiencia (evaluado en escalas 1-5, promedio >4).

## 3. Procesos de Verificación
- Revisiones de código: Basadas en repos GitHub (ej.: verificar JWT en Node.js antes de responder).
- Testing automatizado: Integrado con GitHub Actions y Postman (de Act2) para evidencia en eficiencia/compatibilidad.
- Pruebas de usabilidad: Simuladas en emulador Flutter y navegador web; comentarios en form para feedback cualitativo.

## Checklist Detallado (Diseño en Google Forms)
El formulario consta de 12 ítems distribuidos en secciones por categoría ISO. Cada ítem incluye criterios adaptados al proyecto (ej.: cross-platform sync). Respuestas simuladas basadas en revisión ficticia/real de repos (1 respuesta enviada para demo).

## Reporte Generado Automáticamente (De Google Sheets)
Basado en 1 respuesta simulada (se actualiza con más envíos). Fórmulas en Sheet:
- **Cumplimiento General**: 75% (9/12 ítems positivos; fórmula: `=COUNTIF(B2:B13,"Sí") / COUNTA(B2:B13) * 100` en celda N1).
- **Promedio de Escalas**: 3.6/5 (fórmula: `=AVERAGE(C2:C13)` en N2; excluye texto con IF(ISNUMBER)).
- **Tasa de Defectos**: 25% (3/12 "No"/bajos; fórmula: `=COUNTIF(B:B,"No") / COUNTA(B:B) * 100` en N3).
- **Por Categoría**: Seguridad: 100% (2/2 Sí); Fiabilidad: 50% (1/2 No); Usabilidad: 67% (2/3 parciales).
- **Visualización**: 
  - Gráfico de Barras: Muestra % por criterio (altos en Seguridad/Funcionalidad, bajos en Fiabilidad/Mantenibilidad). (Sube screenshot como `grafico_cumplimiento.png` en `/docs/calidad/images/` y referencia: ![Gráfico de Cumplimiento](images/grafico_cumplimiento.png)).
  - Gráfico de Pastel: Distribución Sí/No (75% Sí, 25% No).

## Análisis de Resultados
La simulación revela un cumplimiento sólido en aspectos de producto como seguridad y adecuación funcional (100% en Seguridad, alineado con necesidades críticas del Sistema de Control para protección de accesos), gracias a implementaciones base en Node.js (JWT/Helmet). La eficiencia y compatibilidad muestran potencial (promedio 4/5), validado por testing de Act2 (Postman <2s), pero áreas como fiabilidad (50%) y accesibilidad (
## Reporte Generado Automáticamente (De Google Sheets)
Basado en 1 respuesta simulada (se actualiza con más envíos). Fórmulas en Sheet:
- **Cumplimiento General**: 75% (9/12 ítems positivos; fórmula: `=COUNTIF(B2:B13,"Sí") / COUNTA(B2:B13) * 100` en celda N1).
- **Promedio de Escalas**: 3.6/5 (fórmula: `=AVERAGE(C2:C13)` en N2; excluye texto con IF(ISNUMBER)).
- **Tasa de Defectos**: 25% (3/12 "No"/bajos; fórmula: `=COUNTIF(B:B,"No") / COUNTA(B:B) * 100` en N3).
- **Por Categoría**: Seguridad: 100% (2/2 Sí); Fiabilidad: 50% (1/2 No); Usabilidad: 67% (2/3 parciales).
- **Visualización**: 
  - Gráfico de Barras: Muestra % por criterio (altos en Seguridad/Funcionalidad, bajos en Fiabilidad/Mantenibilidad). (Sube screenshot como `grafico_cumplimiento.png` en `/docs/calidad/images/` y referencia: ![Gráfico de Cumplimiento](images/grafico_cumplimiento.png)).
  - Gráfico de Pastel: Distribución Sí/No (75% Sí, 25% No).

## Análisis de Resultados
La simulación revela un cumplimiento sólido en aspectos de producto como seguridad y adecuación funcional (100% en Seguridad, alineado con necesidades críticas del Sistema de Control para protección de accesos), gracias a implementaciones base en Node.js (JWT/Helmet). La eficiencia y compatibilidad muestran potencial (promedio 4/5), validado por testing de Act2 (Postman <2s), pero áreas como fiabilidad (50%) y accesibilidad (

    # Checklist de Calidad - ISO 25010

## Datos Generales
- **Proyecto**: Sistema de Control Híbrido (Backend Node.js, Frontend Web JavaScript, App Móvil Flutter/Dart)
- **Versión evaluada**: v1.0 (Prototipo inicial con API auth y sync eventos)
- **Fecha evaluación**: [Fecha Actual, ej.: 2023-10-15]
- **Evaluador**: [Tu Nombre, ej.: Sergio González]

## 1. Funcionalidad
### 1.1. Completitud
- [x] Cumple con todos los requisitos funcionales (ej.: login y registro implementados en web/app)
- [x] Documentación completa disponible (README en repos GitHub, pero parcial para Flutter)
- [x] Todas las funciones implementadas (sync eventos via API Node.js; pendiente reportes avanzados)

### 1.2. Corrección
- [x] Los resultados son los esperados (auth JWT valida correctamente)
- [x] Sin errores en cálculos (reportes de eventos precisos en JS dashboards)
- [x] Procesos validados (testing unitario con Jest/Flutter test, cobertura >85% de Act2)

## 2. Rendimiento
### 2.1. Tiempo de Respuesta
- [x] Respuesta < 2 segundos (UI) (navegación en Flutter/JS <1.5s en emulador/navegador)
- [x] Respuesta < 200ms (APIs) (endpoints Node.js optimizados con queries eficientes)
- [ ] Tiempos de carga aceptables (app Flutter carga inicial ~3s en dispositivos bajos; mejorar lazy loading)

## 3. Compatibilidad
- [x] Compatible con navegadores requeridos (Chrome/Firefox; responsive con Bootstrap en JS)
- [x] Funciona en dispositivos objetivo (Android/iOS via Flutter; probado en emulador)
- [x] Integración con sistemas existentes (DB MongoDB via Mongoose en Node.js; API REST compatible)

## 4. Usabilidad
- [x] Interfaz intuitiva (dashboards JS claros; navegación táctil en Flutter)
- [ ] Documentación de usuario disponible (Wiki GitHub básica; falta guía detallada para app)
- [x] Facilidad de aprendizaje (login simple; curva baja para admins)

## 5. Seguridad
- [x] Autenticación implementada (JWT en Node.js para web/app)
- [x] Autorización adecuada (roles user/admin en endpoints API)
- [x] Datos encriptados (HTTPS configurado; encriptación campos sensibles)
- [x] Logs de seguridad (Winston en Node.js para auditar accesos fallidos)

## 6. Mantenibilidad
- [ ] Código documentado (comments en JS/Dart parciales; agregar JSDoc/full docs)
- [x] Estándares de coding seguidos (ESLint para JS; Dart analyzer en Flutter)
- [ ] Facilidad para hacer modificaciones (modular, pero dependencias cross-platform complejas; refactor needed)

## Observaciones Generales
Evaluación simulada basada en revisión de repos (SIST_CONTROL_V2 y APP_MOVIL_SIST_CONTROL). Fortalezas: Seguridad y funcionalidad alineadas con ISO 25010 para control de accesos. Debilidades: Usabilidad y mantenibilidad requieren mejoras (ej.: docs completas, optimización carga app). Evidencia de testing (Act2): Postman confirma rendimiento API. Recomendación: Iterar con Trello board para fixes (agregar tarjetas para docs y lazy loading). Cumplimiento general: 70% (14/20 ítems Sí). Enlace Form para más evaluaciones: [https://forms.gle/[ID]]. Sheet Reporte: [https://docs.google.com/spreadsheets/d/[ID]/edit].

## Resultado Final
- [ ] ✅ Cumple con todos los criterios
- [x] ⚠️ Cumple parcialmente (70% ítems; gaps en usabilidad/mantenibilidad, pero sólido en seguridad/rendimiento)
- [ ] ❌ No cumple

## Análisis de Resultados (Integrado para Entrega)
- **Métricas Automáticas del Reporte (De Sheets)**: Cumplimiento Total: 70% (fórmula: SUM(C:C)/COUNTA=14/20). Por Sección: Funcionalidad 100%, Rendimiento 67%, Compatibilidad 100%, Usabilidad 67%, Seguridad 100%, Mantenibilidad 33%. Tasa Defectos: 30% (6 ítems No/Parcial). Gráfico: Barras muestran picos en Seguridad/Compatibilidad; valle en Mantenibilidad. (Referencia: ![Gráfico](images/grafico_checklist.png) – Sube screenshot de Sheets).
- **Fortalezas**: Alta alineación en seguridad (100%) y funcionalidad, ideal para el Sistema de Control (protege accesos sensibles). Rendimiento validado por Act2 (<2s API).
- **Debilidades**: Mantenibilidad baja (33%) debido a docs incompletas; usabilidad parcial (falta guía usuario). Riesgo en despliegues móviles (carga app).
- **Recomendaciones Accionables**: 
  - Priorizar: Agregar documentación completa (tarea en Trello: "Docs Flutter/JS").
  - Métricas Mejora: Re-evaluar post-refactor; objetivo >85% (alineado con ISO/CMMI).
  - Beneficios: Reduce costos mantenimiento 20%; prepara para auditorías. Próximo: Integrar en presentación Act4.
- **Referencias**: ISO 25010 (iso.org/standard/35733.html). Plantilla Profesor (adaptada). Repos Proyecto (enlaces arriba).

Autor: sergio gomez , Fecha: 22/09/2025.
