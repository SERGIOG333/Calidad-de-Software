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

### Diagrama de Flujo del Proceso
(Visualiza aquí con Mermaid – se renderiza automáticamente en GitHub. Si usas Draw.io, reemplaza con ![PNG](images/flujo-testing-integracion.png).)

```mermaid
graph TD
    A([Inicio: Preparación del Entorno]) --> B[Ejecutar Tests Unitarios<br/>- Jest para Node.js/JS (auth functions)<br/>- Flutter test para Dart (UI widgets)<br/>Métrica: Cobertura >85%]
    B --> C{Cobertura >85%?<br/>¿Tests Pasan?}
    C -->|No| D[Corregir Código<br/>- Revisar logs en repos<br/>- Actualizar Node.js/Flutter<br/>Bucle de iteración]
    D --> B
    C -->|Sí| E[Testing de Integración<br/>- Postman para API calls (ej: POST /login)<br/>- Verificar sync web-app (datos eventos)<br/>Métrica: Tiempo <2s, sin errores]
    E --> F{¿Integración Exitosa?<br/>¿Sync OK?}
    F -->|No| G[Debug API<br/>- Chequear endpoints Node.js<br/>- Ajustar HTTP client en Flutter/JS<br/>- Verificar JWT]
    G --> E
    F -->|Sí| H[Testing End-to-End<br/>- Cypress para web JS (flujo login-dashboard)<br/>- Integration_test para app Flutter (navegación móvil)<br/>Métrica: Tasa defectos <5%]
    H --> I[Generar Reporte<br/>- Logs coverage (GitHub Actions)<br/>- Actualizar doc Wiki/Trello]
    I --> J([Fin: Proceso Completado<br/>Alineado con ISO 25010 Eficiencia/Portabilidad])
    
    style A fill:#e1f5fe
    style J fill:#c8e6c9
    style C fill:#fff3e0
    style F fill:#fff3e0
    style D fill:#ffcdd2
    style G fill:#ffcdd2
    style B fill:#f3e5f5
    style E fill:#f3e5f5
    style H fill:#f3e5f5
    style I fill:#fff8e1