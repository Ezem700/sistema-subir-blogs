# ADR-001: Elección del Stack Tecnológico

**Estado:** Aceptado

**Contexto:** Necesitamos elegir un stack para un sistema web de blogs educativo, que sea simple de implementar pero que permita aplicar buenas prácticas.

**Decisión:** Usar Django + SQLite + Bootstrap.

**Consecuencias:**
- Positivas: Django incluye ORM, autenticación, admin, forms. SQLite no requiere configuración de servidor. Bootstrap da interfaz responsive sin esfuerzo.
- Negativas: Menos control que un stack con frontend separado. SQLite no escala a múltiples usuarios concurrentes, pero es aceptable para un proyecto educativo.

**Alternativas consideradas:**
- Flask: Muy minimalista, requeriría agregar muchas extensiones.
- FastAPI: Excelente para APIs, pero no tiene admin ni ORM incluido.
- React + Node: Sobreingeniería para el alcance del proyecto.
