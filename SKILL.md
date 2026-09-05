---
name: viral-cover-brief
description: Convierte la captura de un post/reel viral en un brief de portada (slide 1) reutilizable con tu propia marca — sin depender de un brand guide específico. Rama "sistema propio" (si tienes paleta, tipografía y/o un personaje de marca fijos) genera un prompt listo para Google Flow u otra herramienta de imagen IA. Rama "genérica" devuelve una descripción visual objetiva en puntos para que armes tu propio prompt en cualquier herramienta. Actívala cuando pegues una captura de Instagram/TikTok y quieras "adaptar esto", "algo así, con mi marca", o cualquier variante de traducir un post ajeno a tu propio sistema visual — sin copiar texto ni diseño del original.
---

# Viral Cover Brief

Encuentras posts/reels virales por tu cuenta (fuera de esta skill) y los traes como captura. Esta skill traduce esa referencia a un brief de portada — con tu sistema de marca o de forma agnóstica, según respondas en el paso 0 — **sin copiar el post ajeno, solo su mecánica.**

**Nunca reproducir texto ni diseño del post de referencia.** Se extrae el *mecanismo* (qué hace que alguien pare el scroll), no el contenido.

## Antes de empezar — configura tu propio sistema (opcional)

Esta skill no viene con una paleta, tipografía o personaje predefinidos. Si tienes un sistema de marca fijo, prepara antes:

- Un archivo (o unas líneas) con tu paleta de colores (hex), tipografía y reglas visuales fijas.
- Si tienes un personaje/mascota de marca: su nombre, una imagen de referencia, y (opcional) un catálogo de "props" o poses por tema — puedes usar `references/00-plantilla-taxonomia-props.md` como punto de partida.
- Si no tienes nada de esto todavía, usa la rama genérica (abajo) — no bloquea el uso de la skill.

## Flujo

```
0. BIFURCAR   Preguntar: "¿Tienes un sistema de marca propio (paleta/personaje fijos) o prefieres una descripción genérica?"
              → Sistema propio: pasos 1–8 de la RAMA PROPIA.
              → Genérica: pasos 1–2 (ANALIZAR) y luego RAMA GENÉRICA (A1–A3).

── RAMA PROPIA (con tu sistema de marca) ──
1. INTAKE     Pega la captura de referencia (o descríbela).
2. ANALIZAR   Extraer mecánica del hook (texto) y mecánica visual (composición).
              Ver references/02-mapeo-hooks-visuales.md para el mapeo a T1–T6.
3. MAPEAR     Elegir el tratamiento T1–T6 más cercano. Si no encaja en ninguno,
              márcalo como candidato a un tratamiento nuevo (T7+) y avísalo — no forzar el encaje.
4. PROP       Si tienes un personaje de marca, elige su prop/pose según el TEMA de la
              pieza (no según el post viral). Consulta tu propio catálogo si lo tienes
              (ver references/00-plantilla-taxonomia-props.md); si el tema no tiene
              prop aún, propón uno nuevo y espera aprobación antes de fijarlo.
5. BRIEF      Devolver: tratamiento elegido + por qué, prop elegido + por qué (si aplica),
              script de prompt para tu herramienta de imagen IA (plantilla en
              references/01-plantilla-prompt-imagen.md).
6. ESPERA     Corres el prompt en tu herramienta (Google Flow, Midjourney, etc.)
              y devuelves la imagen generada.
7. VERIFICAR  Checklist de references/01-plantilla-prompt-imagen.md sobre el render real —
              nunca aprobar solo sobre la descripción de la escena.
8. ENSAMBLAR  La imagen entra a tu herramienta de diseño (Figma, Canva) como fondo;
              el texto va siempre como capa aparte encima, nunca horneado en la imagen.

── RAMA GENÉRICA (sin sistema de marca fijo) ──
A1. DESCRIBIR  Extraer la mecánica visual del post en puntos separados
               (composición, encuadre, iluminación, colores dominantes,
               texturas, elementos gráficos) — ver references/03-descripcion-visual-generica.md.
               Sin paleta de marca — agnóstico. Un personaje/mascota es opcional acá:
               si lo pides para esta pieza, se describe como elemento gráfico libre.
A2. BRIEF      Devolver mecánica + descripción visual en puntos. No se genera un
               prompt cerrado — arma tu propio prompt para la herramienta que uses.
A3. HANDOFF    Continúa con tu propio proceso de tipografía, paleta y layout.
```

## Reglas duras

- El prop/pose de tu personaje (si tienes uno) se elige por **tema de la pieza**, nunca por replicar literalmente al personaje del post viral de referencia.
- Si el post viral no tiene personaje/mascota, no fuerces a meter el tuyo — el tratamiento puede resolver sin él (T1, T3, T4).
- Todo prop nuevo, antes de entrar a tu catálogo fijo, márcalo `[NUEVO — sin confirmar]` en el brief de salida. Pasa a fijo recién cuando lo uses en una pieza real y lo apruebes.
- La skill no genera la imagen en ninguna rama. Rama propia: genera el prompt, tú lo corres en tu herramienta. Rama genérica: ni siquiera genera el prompt — genera la descripción cruda, el prompt lo armas tú.
- El texto del slide 1 nunca se decide en la imagen generada — se decide después, en tu herramienta de diseño.

## Salida esperada (formato del brief)

Rama propia:
```
SISTEMA:      [nombre de tu sistema de marca, o "propio"]
TRATAMIENTO:  T2 — Backdrop + scrim
POR QUÉ:      [1–2 líneas, qué mecánica del post viral se está adaptando]
PROP:         [nombre del prop] — [motivo, ligado al tema] (si aplica)
PROMPT:       [bloque de texto, ver references/01-plantilla-prompt-imagen.md]
PENDIENTE:    [si el prop es nuevo, marcarlo aquí]
```

Rama genérica — ver formato completo en `references/03-descripcion-visual-generica.md`.

## Registro de casos (opcional)

Si quieres calibrar tu propio catálogo de props/tratamientos con el tiempo, lleva un registro simple (una tabla en Markdown, una hoja de cálculo, o tu propia base de datos) de qué brief terminó usándose en una pieza real, con qué resultado. Esta skill no asume ninguna herramienta de registro específica — usa la que ya tengas. Una plantilla vacía está en `evals/casos.md`.
