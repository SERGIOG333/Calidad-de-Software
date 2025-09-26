# Documentación del Proceso de Testing de Integración para el Sist Control 

## Introducción
Este documento detalla el proceso de testing de integración para el Sistema de Control, utilizando herramientas colaborativas en línea. El proceso verifica la interacción entre backend Node.js (API), frontend web JavaScript (dashboards) y app móvil Flutter/Dart (accesos). Alineado con ISO 25010 (eficiencia/portabilidad de Act1) y CMMI (verificación). Repos: [Web](https://github.com/SERGIOG333/SIST_CONTROL_V2) | [App](https://github.com/SERGIOG333/APP_MOVIL_SIST_CONTROL).

Este contenido está diseñado para GitHub Wiki (edición colaborativa) o Pages (sitio web). Sube a `/docs/calidad/` y activa Wiki en Settings.

## 1. Objetivos de Calidad 
- [x] Documentar pasos para testing cross-platform con cobertura >85%.
- [x] Visualizar flujo con diagrama para claridad colaborativa.
- [ ] Facilitar seguimiento de tareas vía Trello para iteraciones.

## 2. Métricas a Medir
- Cobertura de testing: >85% (Jest/flutter test).
- Tiempo de respuesta API: <2s (Postman).
- Tasa de defectos: <5% en sync web-app.

## 3. Procesos de Verificación
- Revisiones de código: Pull requests en GitHub.
- Testing automatizado: GitHub Actions (YAML para CI).
- Pruebas de usabilidad: Integradas en end-to-end.

## Descripción del Proceso
### Pasos Detallados
1. **Preparación**: Instalar dependencias (npm install, flutter pub get). Configurar entorno (env vars para API/DB).
2. **Tests Unitarios**: Jest para Node.js/JS (ej.: validar JWT auth). Flutter test para Dart (ej.: widgets login).
3. **Testing Integración**: Postman para calls (ej.: GET /events desde app a backend). Verificar sync datos.
4. **End-to-End**: Cypress para web (flujo usuario). Integration_test para app (escenarios móviles).
5. **Reporte**: Generar coverage; actualizar doc si cambios.
