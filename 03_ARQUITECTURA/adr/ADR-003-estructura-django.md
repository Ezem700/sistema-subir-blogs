# ADR-003: Estructura de Proyecto Django

**Estado:** Aceptado

**Contexto:** Django permite organizar el código en apps. Debemos decidir cómo estructurar las apps para separar responsabilidades.

**Decisión:** Crear 3 apps Django: `accounts`, `blogs`, `core`.

**Consecuencias:**
- Positivas: Separación clara de responsabilidades. `accounts` maneja usuarios, `blogs` maneja el contenido, `core` maneja utilidades compartidas.
- Negativas: Más archivos que un proyecto con una sola app, pero más mantenible.

**Estructura propuesta:**
```
08_CODIGO_FUENTE/
  src/
    config/          # settings, urls raíz, wsgi
    accounts/        # registro, login, perfil
    blogs/           # posts, comentarios, likes, categorías
    templates/       # HTML templates
    static/          # CSS, JS, imágenes
  manage.py
```
