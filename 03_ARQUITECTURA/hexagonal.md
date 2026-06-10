# Arquitectura Hexagonal - Mapeo con Django

## Principio
Separar el **dominio** (reglas de negocio) de la **infraestructura** (base de datos, framework, web).

## Mapeo de Capas

| Capa Hexagonal | Implementación Django |
|---------------|----------------------|
| **Dominio** (entidades) | Models (`blogs/models.py`) |
| **Puertos de entrada** (casos de uso) | Services (`blogs/services.py`) |
| **Puertos de salida** (repositorios) | Repositories (`blogs/repositories.py`) |
| **Adaptadores primarios** (entrada) | Vistas + URLs + Forms (`blogs/views.py`) |
| **Adaptadores secundarios** (salida) | ORM Django + SQLite |

## Flujo de una operación (ej: crear blog)

```
Navegador → Vista (adaptador entrada) → Service (puerto entrada)
  → Repository (puerto salida) → ORM (adaptador salida) → SQLite
```

## Estructura de una app Django con hexagonal

```
blogs/
  models.py         # Dominio (entidades + lógica de negocio)
  services.py       # Casos de uso (orquestan el dominio)
  repositories.py   # Acceso a datos (abstracción del ORM)
  views.py          # Adaptadores HTTP
  forms.py          # Validación de entrada
  urls.py           # Rutas
  templates/        # Vistas HTML
  tests/            # Tests
```
