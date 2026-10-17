---
name: validador-hooks
description: Valida y mejora hooks (primeras 1-3 frases) de reels/shorts con la escalera de 5 niveles (básico → nicho+acción → temporalidad → historia → experiencia+historia+meta). Úsala cuando el usuario pida "valida este hook", "califica mi hook", "mejora el gancho", o pegue un guion/transcripción de video corto.
---

# Validador de hooks (escalera de 5 niveles)

Fuente: reel de @plantandofloress (Cris), donde la misma idea ("un día conmigo") sube de nivel. Las vistas que muestra son de **videos distintos de otros creadores**: sirven de ejemplo, no prueban causalidad. No prometas vistas.

## La escalera

| Nivel | Fórmula | Ejemplo del reel | Vistas mostradas |
|---|---|---|---|
| 1 Básico | Formato genérico | "Un día conmigo" | 1,940 |
| 2 | + nicho + acción | "...como coach de pilates" | 11 mil |
| 3 | + temporalidad | "...entrenando para un Hyrox que es en dos meses" | 77.9 mil |
| 4 | Lo conviertes en historia (tensión/pregunta) | "¿Se puede ser coach de pilates y entrenar para un Hyrox al mismo tiempo? Ahí te va cómo le hago" | 279 mil |
| 5 | Experiencia + historia + meta | "Llevo 5 años en el fitness y te voy a enseñar cómo entreno para un Hyrox que quiero hacer en menos de una hora" | 2.7 mill. |

## Checklist (1 punto c/u, máx. 6)

1. **Nicho**: ¿dice a quién o de qué específicamente? (no "un día conmigo" a secas)
2. **Acción**: ¿hay un verbo concreto de lo que pasa?
3. **Temporalidad**: ¿plazo, fecha o contador? ("en 2 meses", "día 3 de 30")
4. **Historia/tensión**: ¿pregunta, contradicción o conflicto que pida respuesta?
5. **Autoridad/experiencia**: ¿por qué escucharte? ("llevo 5 años", dato, resultado)
6. **Meta medible**: ¿destino concreto? ("en menos de una hora", "$10k", "10 kg")

Extras (no puntúan, sólo se señalan): ¿la primera frase cabe en ≤3 s / ~12 palabras? ¿el texto en pantalla refuerza el hook? ¿el video cumple lo que promete? (clickbait que no cumple = baja retención).

## Cómo responder

**Siempre muestra la interfaz**: lee `plantilla.html` (junto a este archivo), reemplaza `__DATA__` por un objeto JSON y pásalo a `show_widget` (llama antes a `read_me` con `interactive` si no lo hiciste en la sesión). Si `show_widget` no existe, da lo mismo como tabla en markdown.

```json
{"hook":"...","nivel":2,
 "checks":[{"nombre":"Nicho","ok":true,"nota":"por qué"}, ... los 6 de la checklist],
 "propuestas":[{"nivel":2,"agrega":"Nicho + acción","texto":"..."}, ... hasta nivel 5],
 "contra":"argumento en contra de la versión nivel 5"}
```

Fuera del widget, sólo 1–2 líneas de texto. Reglas para llenar los datos:

1. Cita el hook tal cual y asígnale **nivel (1–5)** y **puntaje (x/6)** con una frase de por qué en cada punto.
2. Reescribe el hook **subiendo un nivel a la vez** hasta nivel 5, usando sólo datos reales que dio el usuario. Si falta un dato (años de experiencia, meta, plazo), pon `[DATO: …]` y pregúntalo; **nunca inventes cifras ni credenciales**.
3. Da el **argumento en contra** de tu mejor versión (p. ej. demasiado largo, meta poco creíble, nicho tan cerrado que reduce alcance) y qué falta para probarlo (A/B en 2–3 posts, retención a 3 s en analytics).
4. Si el usuario pasa un video: usa la skill `watch` para obtener transcripción y texto en pantalla de los primeros ~5 s, y valida eso.

Formato breve, en español.
