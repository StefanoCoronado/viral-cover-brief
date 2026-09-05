# Plantilla — taxonomía de props para tu personaje de marca

Si tienes un personaje/mascota de marca, esta plantilla te ayuda a mantener consistencia: qué prop/pose usa según el tema de cada pieza, en vez de improvisar cada vez.

**v0.1 — plantilla vacía.** Cada fila nueva nace `[NUEVO]` hasta que se usa en una pieza real y la apruebas; recién ahí pasa a `[FIJO]`.

Un **prop** es el objeto o accesorio con el que posa tu personaje — no es el prompt completo, es el elemento visual que después se traduce en una frase dentro del prompt de imagen (ver `01-plantilla-prompt-imagen.md`).

Regla de elección: el prop responde al **tema de la pieza**, nunca al post viral de referencia. Si el viral tiene un perro, no le pones un perro a tu personaje — ves qué dice el perro del post (ej. "compañía, familiaridad") y buscas el prop que comunique lo mismo dentro de tu propio universo visual.

## Catálogo (ejemplo — reemplaza con tus propios temas)

| Estado | Tema/pilar | Prop | Por qué |
|---|---|---|---|
| NUEVO | [tu tema 1] | [prop] | [qué comunica] |
| NUEVO | [tu tema 2] | [prop] | [qué comunica] |

## Cómo agregar una fila nueva

1. Se propone dentro de un brief de esta skill, marcada `[NUEVO — sin confirmar]`.
2. La usas en una pieza real (o la descartas).
3. La registras en tu propio archivo de casos (o base de datos) — ver `evals/casos.md`.
4. Si se aprobó, esta tabla se actualiza a `FIJO`.

## Restricciones sugeridas (ajusta a tu propio personaje)

- Tu personaje no se agrega por defecto — solo si el tema realmente lo pide.
- Si aparece sobre un fondo plano/CTA: define un límite de escala razonable (ej. máximo 35% del alto del canvas), posición en borde/esquina, mirada dirigida al elemento principal.
- Evita decorativos genéricos que no correspondan a tu identidad visual (define tu propia lista de "nunca usar").
