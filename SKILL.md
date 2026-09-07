---
name: viral-cover-brief
description: Convierte cualquier imagen de referencia (un post/reel viral, o una foto de un banco libre como Unsplash, Pexels o Pixabay) en un brief de portada (slide 1) reutilizable con tu propia marca — sin depender de un brand guide específico. Entrevista al usuario sobre la sensación deseada y el propósito de la pieza antes de proponer nada. Esta skill nunca escribe el prompt final de Google Flow — entrega siempre un brief (rama "sistema propio" con tratamiento y prop de marca, o rama "genérica" con descripción visual objetiva en puntos), listo para pegar junto con la instrucción maestra incluida (references/04-prompt-maestro-google-flow.md) en un asistente conversacional que arma el prompt final. Actívala cuando pegues una imagen de referencia y quieras "adaptar esto", "algo así, con mi marca", "inspirado en esta imagen", o cualquier variante de traducir una referencia ajena a tu propio sistema visual — sin copiar texto ni diseño del original, solo su mecánica de estilo.
---

# Viral Cover Brief

Traes una imagen de referencia por tu cuenta (fuera de esta skill) — de un post/reel viral, o de un banco de imágenes libres de derechos (Unsplash, Pexels, Pixabay). Esta skill traduce esa referencia a un brief de portada — con tu sistema de marca o de forma agnóstica, según respondas en el paso 0 — **sin copiar la referencia, solo su mecánica de estilo.**

**Nunca reproducir texto, sujeto ni diseño exacto de la imagen de referencia.** Se extrae el *mecanismo visual* (composición, luz, paleta, textura), no el contenido específico que la hace reconocible. El resultado es siempre una variante de inspiración — un concepto propio y distinto, nunca una copia con detalles cambiados.

## Antes de empezar — configura tu propio sistema (opcional)

Esta skill no viene con una paleta, tipografía o personaje predefinidos. Si tienes un sistema de marca fijo, prepara antes:

- Un archivo (o unas líneas) con tu paleta de colores (hex), tipografía y reglas visuales fijas.
- Si tienes un personaje/mascota de marca: su nombre, una imagen de referencia, y (opcional) un catálogo de "props" o poses por tema — puedes usar `references/00-plantilla-taxonomia-props.md` como punto de partida.
- Si no tienes nada de esto todavía, usa la rama genérica (abajo) — no bloquea el uso de la skill.

## Flujo

```
0. BIFURCAR   Preguntar: "¿Tienes un sistema de marca propio (paleta/personaje fijos) o prefieres una descripción genérica?"
              → Sistema propio: pasos 1–9 de la RAMA PROPIA.
              → Genérica: paso 1 (DESCRIBIR) y luego RAMA GENÉRICA (A1–A3).

── RAMA PROPIA (con tu sistema de marca) ──
1. INTAKE     Pega la imagen de referencia (o descríbela). Puede ser una captura de
              post/reel viral o una foto de un banco libre (Unsplash, Pexels, Pixabay).
2. ANALIZAR   Extraer solo la mecánica visual (composición, encuadre, iluminación,
              paleta dominante, texturas) — nunca el sujeto exacto ni el texto de la
              referencia. Ver references/02-mapeo-hooks-visuales.md para el mapeo a T1–T6.
3. ENTREVISTA Antes de proponer nada, preguntar (obligatorio, nunca saltarse este paso):
              - "¿Qué sensación querés que transmita tu portada?" (2-3 palabras: calma,
                urgencia, lujo, cercanía, etc.)
              - "¿Para qué es esta pieza?" (promoción, anuncio de servicio, portada de
                contenido — define el propósito, no el texto final que llevará encima)
              - "¿Hay algo del estilo de la referencia que NO querés conservar?"
4. MAPEAR     Elegir el tratamiento T1–T6 más cercano a la mecánica visual Y a las
              respuestas de la entrevista — la sensación deseada pesa más que el
              parecido literal a la referencia. Si no encaja en ninguno, márcalo como
              candidato a un tratamiento nuevo (T7+) y avísalo — no forzar el encaje.
5. PROP       Si tienes un personaje de marca, elige su prop/pose según el TEMA de la
              pieza (nunca según la imagen de referencia). Consulta tu propio catálogo
              si lo tienes (ver references/00-plantilla-taxonomia-props.md); si el tema
              no tiene prop aún, propón uno nuevo y espera aprobación antes de fijarlo.
6. BRIEF      Devolver: tratamiento elegido + por qué (citando la entrevista), prop
              elegido + por qué (si aplica), y los campos técnicos de escena/zona
              protegida/paleta/formato/luz (plantilla en references/01-plantilla-prompt-imagen.md).
              Esta skill NUNCA escribe aquí el prompt final — solo el brief. El
              resultado es siempre una variante nueva — nunca una réplica de la
              referencia, solo comparte su mecánica de estilo.
7. MAESTRO    Entregar el brief completo del paso 6 listo para pegar en un asistente
              conversacional (ChatGPT u otro LLM), junto con la instrucción de
              references/04-prompt-maestro-google-flow.md como system prompt de esa
              conversación. Ese asistente devuelve el prompt final listo para Google
              Flow — esta skill no lo genera.
8. ESPERA     Corres el prompt (ya generado por el asistente) en tu herramienta
              (Google Flow, Midjourney, etc.) y devuelves la imagen generada.
9. VERIFICAR  Checklist de references/01-plantilla-prompt-imagen.md sobre el render real —
              nunca aprobar solo sobre la descripción de la escena.
10. ENSAMBLAR La imagen entra a tu herramienta de diseño (Figma, Canva) como fondo;
              el texto va siempre como capa aparte encima, nunca horneado en la imagen.

── RAMA GENÉRICA (sin sistema de marca fijo) ──
A1. DESCRIBIR  Extraer la mecánica visual de la referencia en puntos separados
               (composición, encuadre, iluminación, colores dominantes,
               texturas, elementos gráficos) — ver references/03-descripcion-visual-generica.md.
               Sin paleta de marca — agnóstico. Un personaje/mascota es opcional acá:
               si lo pides para esta pieza, se describe como elemento gráfico libre.
A1.5 ENTREVISTA Mismas 3 preguntas del paso 3 de la rama propia (sensación deseada,
               propósito de la pieza, qué NO conservar) — obligatorio antes del brief.
A2. BRIEF      Devolver mecánica + descripción visual en puntos + respuestas de la
               entrevista. Esta skill nunca genera un prompt cerrado en esta rama
               tampoco.
A3. MAESTRO    Opcional: si quieres que un asistente arme el prompt final en vez de
               armarlo tú a mano, pega este brief junto con
               references/04-prompt-maestro-google-flow.md en un LLM conversacional.
A4. HANDOFF    Continúa con tu propio proceso de tipografía, paleta y layout.
```

## Reglas duras

- La entrevista (paso 3 / A1.5) es obligatoria en las dos ramas — nunca generar el brief saltándosela, sin importar cuán claro parezca el pedido.
- El resultado final es siempre una **variante de inspiración**: comparte mecánica de estilo con la referencia, nunca su sujeto, composición exacta o diseño literal. Si el brief termina pareciéndose demasiado a la referencia (mismo sujeto, solo con otro color), no está terminado — hay que alejarse más.
- El prop/pose de tu personaje (si tienes uno) se elige por **tema de la pieza** (definido en la entrevista), nunca por replicar literalmente el sujeto de la imagen de referencia.
- Si la referencia no tiene personaje/mascota, no fuerces a meter el tuyo — el tratamiento puede resolver sin él (T1, T3, T4).
- Todo prop nuevo, antes de entrar a tu catálogo fijo, márcalo `[NUEVO — sin confirmar]` en el brief de salida. Pasa a fijo recién cuando lo uses en una pieza real y lo apruebes.
- La skill no genera la imagen en ninguna rama, y nunca escribe el prompt final de Google Flow ella misma — en ambas ramas entrega un brief/descripción. El prompt final sale de pegar ese brief + `references/04-prompt-maestro-google-flow.md` en un asistente conversacional (ChatGPT u otro), o de armarlo a mano si prefieres.
- El texto del slide 1 nunca se decide en la imagen generada — se decide después, en tu herramienta de diseño.

## Salida esperada (formato del brief)

Rama propia:
```
SISTEMA:      [nombre de tu sistema de marca, o "propio"]
SENSACIÓN:    [respuesta de la entrevista — ej. "lujo discreto, urgencia baja"]
PROPÓSITO:    [para qué es la pieza, de la entrevista]
TRATAMIENTO:  T2 — Backdrop + scrim
POR QUÉ:      [1–2 líneas, qué mecánica de la referencia se está adaptando y cómo
              conecta con la sensación pedida]
PROP:         [nombre del prop] — [motivo, ligado al tema] (si aplica)
CAMPOS TÉCNICOS: [escena, zona protegida, paleta, formato, luz — ver
              references/01-plantilla-prompt-imagen.md]
PENDIENTE:    [si el prop es nuevo, marcarlo aquí]
SIGUIENTE PASO: pega este brief completo + references/04-prompt-maestro-google-flow.md
              en tu asistente conversacional (ChatGPT u otro) para obtener el
              prompt final listo para Google Flow. Esta skill no lo genera.
```

Rama genérica — ver formato completo en `references/03-descripcion-visual-generica.md`.

## Registro de casos (opcional)

Si quieres calibrar tu propio catálogo de props/tratamientos con el tiempo, lleva un registro simple (una tabla en Markdown, una hoja de cálculo, o tu propia base de datos) de qué brief terminó usándose en una pieza real, con qué resultado. Esta skill no asume ninguna herramienta de registro específica — usa la que ya tengas. Una plantilla vacía está en `evals/casos.md`.
