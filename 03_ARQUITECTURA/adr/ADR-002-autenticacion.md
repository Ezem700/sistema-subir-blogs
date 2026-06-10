# ADR-002: Autenticación de Usuarios

**Estado:** Aceptado

**Contexto:** El sistema necesita registro, inicio de sesión y roles (usuario común, administrador).

**Decisión:** Usar el sistema de autenticación incorporado de Django (django.contrib.auth).

**Consecuencias:**
- Positivas: Maneja hashing de contraseñas, sesiones, protección CSRF. Incluye decoradores @login_required y @user_passes_test para permisos.
- Negativas: No es stateless (usa sesiones del lado del servidor), pero para un monolito es lo correcto.

**Alternativas consideradas:**
- JWT: Stateless, útil para APIs REST, pero innecesario para templates Django tradicionales.
- Autenticación propia: Riesgo de seguridad, reinventar la rueda.
