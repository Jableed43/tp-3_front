# Soulless Catcher · Dos flujos agénticos

TP3 de **Desarrollo de Sistemas Web Front End** · IFTS 29 · Comisión 2C26 · **Grupo 25 · BlueTech**.

Landing que propone cómo resolver con agentes dos reglas de **Soulless Catcher**, una startup creada por estudiantes del IFTS 16 que revisa imágenes y videos sospechosos de haber sido generados con IA.

| | |
|---|---|
| **Landing publicada** | _[completar con el enlace de Vercel]_ |
| **Repositorio** | _[completar con el enlace de GitHub]_ |
| **Bloque asignado** | Recepción del material (S04-A) |
| **Entrega** | 26/11/2026 |

## Integrantes y aportes

| Integrante | Aporte |
|---|---|
| Javier Nehuén López | Armó la landing, los diagramas y la documentación con el agente de IA, y revisó cada etapa. _[ajustar si hace falta]_ |
| Rocío Ailen Arenas | _[completar con lo que realmente aportó]_ |
| Facundo Sánchez | _[completar con lo que realmente aportó]_ |
| Damián Gorosito | _[completar con lo que realmente aportó]_ |

> Cada aporte debe describir lo que esa persona hizo. Si alguien no participó en este trabajo, no se lo incluye.

## Sentencias asignadas

> **R1.** Si el archivo es accesible y su formato está admitido, el sistema inicia la revisión y registra el enlace de origen cuando está disponible.

> **R2.** Si el archivo no puede abrirse o su formato no está admitido, el sistema explica el problema y solicita otro archivo sin emitir un resultado.

Cada una tiene su flujo, con un diagrama, las condiciones, la acción del agente, el resultado y las excepciones. Lo que no sale de las sentencias está separado como **decisiones del grupo** (D1 a D5) en la landing.

## Contenido del repositorio

```
tp-3-front/
├── index.html          la landing
├── styles.css          estilos
├── diagramas/          flujo-r1.svg y flujo-r2.svg
├── material/           logo original de la startup
├── docs/               asignación, fichas, propuestas y diagramas (trabajo previo)
└── README.md
```

La landing es HTML y CSS estáticos, sin JavaScript ni pasos de compilación. Para verla alcanza con abrir `index.html`.

## Uso de la IA

- **Herramienta:** Claude Code. **Modelo:** Claude Sonnet 5.5.
- **Qué se hizo con IA:** todo el trabajo técnico de este entregable: el análisis de las sentencias, las propuestas, los diagramas SVG, la landing y esta documentación.
- **Qué hizo el grupo:** definió el alcance, revisó cada etapa y aprobó las decisiones D1 a D5.

### Cómo se trabajó

Se trabajó por etapas, cada una con su commit y su etiqueta (`etapa-0`, `etapa-1`, `etapa-2`), para poder volver atrás.

| Etapa | Instrucción inicial | Problema o ajuste | Mejora pedida |
|---|---|---|---|
| 0 · Asignación | Leer la consigna y copiar las sentencias sin cambiarlas. | Se verificó que el texto de R1 y R2 fuera idéntico al de la consigna. | Guardar el logo original sin modificarlo. |
| 1 · Fichas y propuestas | Analizar cada sentencia: condición, acción y resultado. | Términos ambiguos, como «accesible» y «disponible». | Documentar cada duda como decisión del grupo (D1 a D5). |
| 2 · Diagramas | Dibujar el flujo de cada regla. | Se revisó el render de cada SVG antes de aceptarlo. | Distinguir con un estilo propio los pasos que son decisiones del grupo. |
| 3 · Landing | Armar la página con los dos flujos y su explicación. | Hacerla accesible: texto alternativo, jerarquía de títulos, contraste y navegación por teclado. | Mantenerla simple, sin exagerar. |

_[Agregar aquí las instrucciones literales o los ejemplos de iteración que el grupo quiera mostrar.]_

## Limitaciones

- Es una **propuesta de diseño**: los agentes no se ejecutan ni se conectan a servicios reales.
- Los formatos admitidos (JPG, PNG y MP4) son un ejemplo: los define la startup.
