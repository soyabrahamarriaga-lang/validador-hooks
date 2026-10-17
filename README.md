# validador-hooks

**Tu video no tiene un problema de contenido. Tiene un problema de los primeros 3 segundos.**

Si nadie se queda, nadie ve lo bueno. Puedes tener la mejor edición, la mejor idea y el mejor consejo del mundo, y si el hook es "un día conmigo"… ya perdiste.

Esta skill de Claude Code toma tu hook, te dice exactamente qué le falta y te lo devuelve armado, nivel por nivel, hasta el 5.

---

## El problema

La mayoría de los creadores escribe el hook al final, en 10 segundos, con lo primero que se le ocurre. Luego pasa 4 horas editando un video que nadie va a ver completo.

Eso está al revés. El hook es la parte con más palanca de todo el video. Si lo arreglas, todo lo demás que hiciste empieza a rendir.

## La escalera (5 niveles)

Misma idea. Mismo video. Lo único que cambia es cuánto le das al cerebro para quedarse.

| Nivel | Qué agregas | Ejemplo |
|---|---|---|
| 1 | Nada. Genérico. | "Un día conmigo" |
| 2 | Nicho + acción | "…como coach de pilates" |
| 3 | Temporalidad | "…entrenando para un Hyrox que es en dos meses" |
| 4 | Historia / tensión | "¿Se puede ser coach de pilates y entrenar para un Hyrox al mismo tiempo?" |
| 5 | Experiencia + historia + meta | "Llevo 5 años en el fitness y te enseño cómo entreno para un Hyrox que quiero hacer en menos de una hora" |

Cada escalón responde una pregunta que tu espectador se hace sin darse cuenta:

- **¿Esto es para mí?** → nicho
- **¿Qué va a pasar?** → acción
- **¿Por qué ahora?** → temporalidad
- **¿Cómo termina?** → tensión
- **¿Por qué te creo?** → experiencia
- **¿A dónde llegamos?** → meta medible

Si no contestas esas preguntas, el pulgar lo hace por ti. Y siempre contesta "siguiente".

## Qué hace la skill

Le das esto:

> valida este hook: quiero jubilar a mi novia

Y te regresa una interfaz con:

1. **Tu nivel (1–5) y puntaje (x/6).** Sin rodeos.
2. **Qué tiene y qué le falta.** Checklist de 6 puntos, cada uno con el por qué.
3. **Propuestas armadas nivel por nivel**, listas para copiar.
4. **`[DATO]` donde falta algo real.** No te inventa cifras ni credenciales. Si no sabe cuánto ganas o en cuánto tiempo, te lo pregunta. Un hook con datos falsos te cuesta más de lo que te da.
5. **El argumento en contra.** Porque más largo no siempre es mejor, y prefiero decírtelo antes de que lo descubras con 200 vistas.

## Lo que no te voy a prometer

No te prometo vistas. Nadie honesto puede.

Lo que sí: vas a dejar de publicar hooks de nivel 1 sin darte cuenta. Y eso, repetido en 100 videos, es la diferencia entre adivinar y tener un sistema.

Prueba cada versión con A/B y mira la retención a los 3 segundos. Los datos mandan, no la skill.

## Instalar

```bash
git clone https://github.com/soyabrahamarriaga-lang/validador-hooks ~/.claude/skills/validador-hooks
```

Luego en Claude Code:

> valida este hook: [tu hook]

---

Escalera basada en un reel de [@plantandofloress](https://www.instagram.com/plantandofloress/). La skill es gratis. El tiempo que pierdes publicando hooks malos, no.
