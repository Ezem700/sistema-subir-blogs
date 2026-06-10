# Visión Arquitectónica - Sistema Blogs Django

## Visión General
Sistema web para publicación de blogs con control de usuarios, comentarios, likes y moderación administrativa. Desarrollado con Django, priorizando simplicidad y buenas prácticas.

## Principios Arquitectónicos
- **Simplicidad**: Stack minimalista (Django + SQLite + Bootstrap).
- **Separación de responsabilidades**: Dominio separado de infraestructura mediante servicios y repositorios.
- **Seguridad**: Autenticación por Django Auth, protección contra CSRF/XSS.
- **Escalabilidad educativa**: Estructura que permita agregar funcionalidades sin reescribir.

## Decisiones Estratégicas
| Decisión | Opción elegida | Alternativa descartada |
|----------|---------------|----------------------|
| Framework | Django | Flask (menos baterías incluidas) |
| Base de datos | SQLite | PostgreSQL (sobreingeniería para este alcance) |
| Frontend | Bootstrap + templates Django | React/SPA (complejidad innecesaria) |
| Autenticación | Django Auth | JWT (innecesario para monolitio) |

## Estilo Arquitectónico
Monolito modular con capas:
- **Presentación**: Templates + Bootstrap
- **Aplicación**: Vistas Django + Forms
- **Dominio**: Modelos + Servicios + Repositorios
- **Infraestructura**: ORM Django + SQLite
