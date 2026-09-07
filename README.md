# Viral Cover Brief

Skill para [Claude Code](https://claude.com/claude-code) / Claude que convierte cualquier imagen de referencia — una captura de post/reel viral, o una foto de un banco libre como Unsplash, Pexels o Pixabay — en un brief de portada (slide 1). Nunca copia la referencia, solo su mecánica visual, y siempre te entrevista antes de proponer nada.

## Qué hace

- Analiza la imagen de referencia y extrae su mecánica visual (composición, luz, paleta, textura) — nunca el sujeto exacto ni el texto.
- **Te entrevista** sobre qué sensación querés transmitir y para qué es la pieza, antes de generar cualquier brief — no asume que sabés exactamente qué querés solo por la referencia que pegaste.
- La mapea a uno de 6 tratamientos visuales genéricos (tipográfico puro, backdrop + scrim, duotono, corte, marco, halo).
- Rama con sistema de marca propio: genera un prompt listo para tu herramienta de imagen IA (Google Flow, Midjourney, etc.), incluyendo a tu personaje/mascota si tienes uno.
- Rama genérica (sin sistema de marca): devuelve una descripción visual objetiva en puntos, para que armes tu propio prompt en la herramienta que uses.
- El resultado es siempre una variante de inspiración — un concepto propio, nunca una copia con los colores cambiados.

## Por qué existe

La mayoría de "clona este post viral" copia texto y diseño literal — lo cual es plagio y además no traduce bien a otra marca. Esta skill fuerza la separación entre *qué hace que el post funcione* (el mecanismo) y *cómo se ve* (el contenido específico) — y solo reutiliza lo primero.

## Instalación

Un solo comando, corre un scan de seguridad (Snyk) automático antes de traer el código a tu máquina:

```
npx skills add StefanoCoronado/viral-cover-brief
```

Se instala para Claude Code y el resto de agentes compatibles con [skills.sh](https://skills.sh). Si preferís copiarla a mano, la carpeta completa va en `.claude/skills/viral-cover-brief/`.

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

1. Activa la skill y pega la imagen de referencia (post/reel viral, o foto de Unsplash/Pexels/Pixabay).
2. Responde si tienes un sistema de marca propio (paleta/personaje) o prefieres la rama genérica.
3. Contesta la entrevista corta (sensación deseada, para qué es la pieza, qué no querés conservar del estilo de referencia).
4. Sigue el brief resultante — nunca reproduce texto, sujeto ni diseño exacto del original.

## Licencia

MIT — ver `LICENSE`.
