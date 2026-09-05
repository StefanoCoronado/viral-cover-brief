# Viral Cover Brief

Skill para [Claude Code](https://claude.com/claude-code) / Claude que convierte la captura de un post o reel viral en un brief de portada (slide 1) — sin copiar el post original, solo su mecánica visual.

## Qué hace

- Analiza una captura de referencia y separa la mecánica del *hook* (texto) de la mecánica *visual* (composición).
- La mapea a uno de 6 tratamientos visuales genéricos (tipográfico puro, backdrop + scrim, duotono, corte, marco, halo).
- Rama con sistema de marca propio: genera un prompt listo para tu herramienta de imagen IA (Google Flow, Midjourney, etc.), incluyendo a tu personaje/mascota si tienes uno.
- Rama genérica (sin sistema de marca): devuelve una descripción visual objetiva en puntos, para que armes tu propio prompt en la herramienta que uses.

## Por qué existe

La mayoría de "clona este post viral" copia texto y diseño literal — lo cual es plagio y además no traduce bien a otra marca. Esta skill fuerza la separación entre *qué hace que el post funcione* (el mecanismo) y *cómo se ve* (el contenido específico) — y solo reutiliza lo primero.

## Instalación

Copia esta carpeta a tu directorio de skills de Claude Code (`.claude/skills/viral-cover-brief/`), o instálala vía tu gestor de skills si la publicas como repo (ej. `npx skills add <owner>/<repo>`).

## Estructura

```
SKILL.md                                      Flujo principal
references/00-plantilla-taxonomia-props.md    Plantilla para el catálogo de props de tu personaje
references/01-plantilla-prompt-imagen.md      Plantilla del prompt de imagen IA
references/02-mapeo-hooks-visuales.md         Tabla de mapeo mecánica → tratamiento T1-T6
references/03-descripcion-visual-generica.md  Estructura de la rama sin sistema de marca
evals/casos.md                                Plantilla vacía para tu propio registro de casos
```

## Uso

1. Activa la skill y pega la captura del post/reel viral de referencia.
2. Responde si tienes un sistema de marca propio (paleta/personaje) o prefieres la rama genérica.
3. Sigue el brief resultante — nunca reproduce texto ni diseño del original.

## Licencia

MIT — ver `LICENSE`.
