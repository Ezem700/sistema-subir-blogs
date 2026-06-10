# Requisitos del Sistema - Sistema Blogs Django

## Resumen del Proyecto
Plataforma web donde usuarios registrados pueden publicar, comentar y dar like a blogs, con control de moderación para el administrador.

---

## Requisitos Funcionales

### Módulo de Autenticación
- RF-01: El sistema debe permitir el registro de nuevos usuarios con email y contraseña.
- RF-02: El sistema debe permitir el inicio de sesión de usuarios registrados.
- RF-03: El sistema debe permitir el cierre de sesión.

### Módulo de Blogs
- RF-04: El usuario autenticado debe poder crear un blog con título, contenido (texto, fotos, links) y categoría.
- RF-05: El usuario autenticado debe poder editar solo sus propios blogs.
- RF-06: El usuario autenticado debe poder eliminar solo sus propios blogs.
- RF-07: El administrador debe poder eliminar cualquier blog.
- RF-08: Cualquier visitante debe poder ver los blogs publicados.

### Módulo de Comentarios
- RF-09: Cualquier usuario autenticado debe poder comentar en cualquier blog.
- RF-10: Cualquier usuario autenticado debe poder eliminar sus propios comentarios.
- RF-11: El dueño del blog debe poder eliminar comentarios ajenos en su propio blog.
- RF-12: Debe permitirse responder comentarios (comentar a otro comentario).

### Módulo de Likes
- RF-13: El usuario autenticado debe poder dar like a un blog (un like por usuario).
- RF-14: El usuario autenticado debe poder quitar su like si lo vuelve a presionar.

### Módulo de Categorías y Etiquetas
- RF-15: El usuario debe poder crear sus propias categorías.
- RF-16: El usuario debe poder asignar etiquetas a sus blogs.

### Módulo de Perfil de Usuario
- RF-17: El usuario debe poder tener una foto de perfil.
- RF-18: El usuario debe poder tener una biografía en su perfil.
- RF-19: El perfil debe mostrar los blogs publicados por el usuario.

### Módulo de Administración
- RF-20: El administrador debe poder suspender usuarios.
- RF-21: El administrador debe poder eliminar cualquier blog o comentario inapropiado.

---

## Requisitos No Funcionales

- RNF-01: La aplicación debe ser web responsive (funcionar en desktop y mobile).
- RNF-02: La base de datos debe ser persistente (SQLite con Django).
- RNF-03: Las contraseñas deben almacenarse con hash (Django Auth).
- RNF-04: La interfaz debe ser intuitiva y simple.
- RNF-05: El sistema debe ejecutarse en un solo servidor.
