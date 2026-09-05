# Plantilla de prompt para generación de imagen IA (Google Flow u otra herramienta)

Estructura fija para que cada prompt salga consistente y evite artefactos de costura comunes al generar directo en un formato vertical: generar directo en la proporción final (ej. 4:5), describir elementos reales en la zona superior en vez de pedir "espacio vacío", y posicionar tu personaje (si lo tienes) en el tercio inferior.

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

[FORMATO]    Proporción final exacta (ej. 4:5), generar directo en esa
             proporción — nunca recortar en post, ahí es donde aparecen
             las costuras.

[LUZ]        1 frase — dirección y calidad de luz, coherente con el
             tratamiento elegido.
```

## Ejemplo completo (placeholder — reemplaza con tu marca)

```
Escena de estudio minimalista en [tu paleta dominante], atmósfera [tono
deseado]. Zona superior con degradado suave de [color A] a [color B],
sin elementos de detalle — solo luz y color. En el tercio inferior,
[tu personaje: descripción breve y consistente] de pie, con [prop
elegido], mirada hacia arriba-centro. Paleta: [colores hex de tu
marca]. Formato vertical 4:5, generado directo en esa proporción. Luz
suave y cálida desde atrás del personaje, sin sombras duras.
```

## Checklist antes de generar

- [ ] No pide "espacio vacío" ni "fondo en blanco" en ningún punto
- [ ] Formato final pedido explícitamente, no recorte posterior
- [ ] Prop viene de tu taxonomía (o está marcado NUEVO y aprobado)
- [ ] Paleta mencionada son colores reales de tu marca, no genéricos
- [ ] Zona superior descrita como baja frecuencia, no detallada
