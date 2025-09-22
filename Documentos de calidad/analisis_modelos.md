# Análisis de Modelos de Calidad para el Sist Control 

## Introducción
Este documento presenta un análisis comparativo de modelos de calidad de software aplicados al Sistema de Control, una solución híbrida con backend en Node.js, frontend web en JavaScript y aplicación móvil en Flutter/Dart. Repositorios: [Web](https://github.com/SERGIOG333/SIST_CONTROL_V2) | [App](https://github.com/SERGIOG333/APP_MOVIL_SIST_CONTROL). El análisis se basa en el taller del SENA y estándares como ISO 25010 y CMMI, con énfasis en seguridad, usabilidad y eficiencia cross-platform.

## 1. Objetivos de Calidad (Adaptado de Plantilla del Profesor)
- [x] Identificar modelos alineados con necesidades híbridas (web/app).
- [x] Recomendar framework para garantía de calidad en desarrollo y despliegue.
- [ ] Establecer base para métricas en actividades subsiguientes (ej.: testing).

## 2. Métricas a Medir (Derivadas del Análisis)
- Tasa de defectos: <5% en pruebas de integración API (Node.js-Flutter).
- Cobertura de testing: >85% en unitarios (Jest para JS, flutter test para Dart).
- Tiempo de respuesta: <1 segundo para endpoints críticos (medido con ISO 25010 eficiencia).

## 3. Procesos de Verificación (Basados en Modelos Recomendados)
- Revisiones de código: Pull requests en GitHub para alineación con ISO 25010 (mantenibilidad).
- Testing automatizado: CI/CD con GitHub Actions, inspirado en CMMI verificación.
- Pruebas de usabilidad: Evaluación heurística en app Flutter (navegación táctil) y web JS (responsividad).

## Análisis Detallado
### Modelos Comparados
- **ISO 25010**: Enfoque en producto (8 características). Aplicación: Evaluar portabilidad (sincronización web-app).
- **CMMI**: Enfoque en procesos (5 niveles). Aplicación: Madurez en testing de seguridad (JWT en Node.js).

### Matriz de Comparación
(Inserta la tabla de arriba aquí en Markdown para renderizado profesional)

### Recomendación
Adoptar ISO 25010 como modelo principal, complementado con CMMI Nivel 2. Beneficios: Reducción de riesgos en 20-30% para funcionalidades como autenticación y reportes.

## Conclusión y Referencias
Este análisis posiciona al Sistema de Control para una garantía de calidad robusta, alineada con normas internacionales. Próximos pasos: Integrar en documentación de repositorios.

Referencias:
- ISO/IEC 25010:2011 (iso.org/standard/35733.html).
- CMMI Institute (cmmiinstitute.com).
- Repos del Proyecto: Enlaces arriba.

Autor: sergio gomez , Fecha: 22/09/2025.