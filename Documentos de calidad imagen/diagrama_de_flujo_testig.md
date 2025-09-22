Diagrama de Flujo del Proceso de Testing de Integración (Representación Estructurada):

- **Nodo 1 (Inicio - Óvalo Azul)**: Preparación del Entorno
  - Descripción: Instalar dependencias (npm install para Node.js, flutter pub get para app). Configurar mocks para DB/API.

- **Nodo 2 (Rectángulo Verde)**: Ejecutar Tests Unitarios
  - Descripción: Jest para funciones backend/web JS (ej.: validar auth). Flutter test para widgets Dart (ej.: UI login).
  - Métrica: Cobertura >85%.

- **Nodo 3 (Rombo Naranja)**: ¿Tests Unitarios Pasan?
  - Sí: Proceder a Integración.
  - No: Bucle a "Corregir Código" (rectángulo rojo: Revisar logs, actualizar repos).

- **Nodo 4 (Rectángulo Azul)**: Testing de Integración
  - Descripción: Postman para calls API (ej.: POST /login desde app Flutter a Node.js). Verificar sync eventos web-app.
  - Métrica: Tiempo respuesta <2s, sin errores 500.

- **Nodo 5 (Rombo Naranja)**: ¿Integración Exitosa?
  - Sí: Proceder a End-to-End.
  - No: "Debug API" (rectángulo rojo: Chequear endpoints Node.js, ajustar Flutter HTTP client).

- **Nodo 6 (Rect