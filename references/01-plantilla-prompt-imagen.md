# Plantilla de contenido del brief (no es el prompt final)

Esta skill ya no escribe el prompt final — lo escribe tu asistente de IA a partir del brief, siguiendo `04-prompt-maestro-google-flow.md`. Esta plantilla define qué campos técnicos debe cubrir el brief para que ese asistente tenga todo lo necesario, sin ambigüedad: escena, zona protegida, personaje/prop, paleta, formato y luz. Úsala al armar el brief en el paso BRIEF, no como texto final para pegar en la herramienta de imagen.

Sigue evitando los artefactos de costura comunes al generar directo en un formato vertical: pedir la proporción final (ej. 3:4, el único ratio vertical no-story que soporta Google Flow) explícitamente, describir elementos reales en la zona superior en vez de "espacio vacío", y posicionar el personaje (si lo tienes) en el tercio inferior.

Google Flow solo acepta 16:9, 4:3, 1:1, 3:4 o 9:16 — ningún otro ratio (nada de 4:5, 16:10, etc.).

## Estructura

```
[ESCENA]     Descripción del fondo/ambiente — 1-2 frases, concreta, sin
             pedir "espacio en blanco" o "vacío" (muchas herramientas
             interpretan mal esas instrucciones y generan artefactos).

[ZONA SUPERIOR]
             Elementos reales de baja frecuencia: degradado de color,
             textura suave, luz direccional. Nunca detalle fino aquí —
             es la zona protegida para el titular.

[PERSONAJE, zona inferior] (si tienes uno)
             Pose + prop elegido de tu taxonomía (00-plantilla-taxonomia-props.md).
             Mirada dirigida hacia el centro/arriba, nunca hacia afuera del canvas.
             Escala: define un límite razonable si el fondo es plano/CTA (ej. no más
             del 35% del alto total).

[PALETA]     2-4 colores concretos de tu propia marca — mencionar los
             dominantes según el tratamiento elegido.

[FORMATO]    Proporción final exacta — solo 16:9, 4:3, 1:1, 3:4 o 9:16
             (los únicos que soporta Google Flow) — generar directo en
             esa proporción, nunca recortar en post, ahí es donde
             aparecen las costuras.

[LUZ]        1 frase — dirección y calidad de luz, coherente con el
             tratamiento elegido.
```

## Ejemplo de brief completo (placeholder — reemplaza con tu marca; esto va al asistente, no directo a la herramienta de imagen)

```
Escena de estudio minimalista en [tu paleta dominante], atmósfera [tono
deseado]. Zona superior con degradado suave de [color A] a [color B],
sin elementos de detalle — solo luz y color. En el tercio inferior,
[tu personaje: descripción breve y consistente] de pie, con [prop
elegido], mirada hacia arriba-centro. Paleta: [colores hex de tu
marca]. Formato vertical 3:4, generado directo en esa proporción. Luz
suave y cálida desde atrás del personaje, sin sombras duras.
```

## Checklist antes de pasar el brief al asistente

- [ ] No pide "espacio vacío" ni "fondo en blanco" en ningún punto
- [ ] Formato final especificado explícitamente, no recorte posterior
- [ ] Prop viene de tu taxonomía (o está marcado NUEVO y aprobado)
- [ ] Paleta mencionada son colores reales de tu marca, no genéricos
- [ ] Zona superior descrita como baja frecuencia, no detallada
- [ ] Referencias visuales adjuntas (si aplica) están señaladas como fuente exacta a preservar — el asistente lo necesita para aplicar la regla 3 de `04-prompt-maestro-google-flow.md`
