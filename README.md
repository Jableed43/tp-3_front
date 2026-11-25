# Soulless Catcher · Dos flujos agénticos

TP3 de **Desarrollo de Sistemas Web Front End** · IFTS 29 · Comisión 2C26 · **Grupo 25 · BlueTech**.

Landing que propone cómo resolver con agentes dos reglas de **Soulless Catcher**, una startup creada por estudiantes del IFTS 16 que revisa imágenes y videos sospechosos de haber sido generados con IA.

| | |
|---|---|
| **Landing publicada** | _https://tp-3front.vercel.app/_ |
| **Repositorio** | _https://github.com/Jableed43/tp-3_front_ |
| **Bloque asignado** | Recepción del material (S04-A) |
| **Entrega** | 25/11/2026 |

## Integrantes y aportes

| Integrante | Aporte |
|---|---|
| **Javier Nehuén López** | Dirigió el trabajo con el agente de IA y lo hizo por etapas: análisis de las sentencias, decisiones del grupo, diagramas, landing y documentación. Revisó y probó cada etapa antes de seguir. |
| **Damián Gorosito** | Inició y creó la versión original de *Colgá tu trapo*, el otro trabajo del grupo hecho con IA (ver más abajo).  |
| **Rocío Ailen Arenas** | |
| **Facundo Sánchez** |  |

> Cada aporte describe lo que esa persona hizo. Si alguien no participó en este trabajo, no se lo incluye.

## Otro trabajo del grupo con IA: Colgá tu trapo

Además de esta landing, el grupo tiene *Colgá tu trapo*, un mural de frases con forma de bandera de tela para proyectar. Lo inició Damián Gorosito y Javier Nehuén López le sumó mejoras con Claude Code: datos guardados más seguros, proyección más cómoda, accesibilidad, fuentes y colores. Tiene su propio repositorio y su bitácora de mejoras y prompts. _[agregar enlace]_

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

Se aplicó el mismo método que en *Colgá tu trapo*: pasos chicos, un commit y una etiqueta por paso (`etapa-0` a `etapa-3`), respaldo de los archivos originales con verificación SHA-256 y prueba del resultado antes de avanzar. Así siempre se puede volver atrás.

Cada etapa registra el problema que apareció, lo que cambió, el pedido y cómo se verificó. Los pedidos son reconstrucciones, no transcripciones literales.

#### Etapa 0 · Asignación
- **Problema:** el material oficial estaba suelto y había que copiar las sentencias sin alterarlas.
- **Qué cambió:** se guardaron los datos del grupo, el logo original y un `.gitignore`.
- **Pedido:** «Copiá las sentencias R1 y R2 de la consigna sin cambiar una palabra y guardá el logo tal cual.»
- **Verificación:** el texto de R1 y R2 coincide con la consigna.

#### Etapa 1 · Fichas y propuestas
- **Problema:** las sentencias tienen términos ambiguos: «accesible», «disponible» y qué pasa si el usuario falla dos veces.
- **Qué cambió:** cada duda se resolvió como decisión del grupo (D1 a D5), separada de lo que dicen las sentencias.
- **Pedido:** «Analizá cada sentencia en condición, acción y resultado, y proponé un agente para cada una. Marcá lo que no sale de la sentencia.»
- **Verificación:** cada decisión quedó trazada a la parte de la sentencia que la motivó.

#### Etapa 2 · Diagramas
- **Problema:** los diagramas tenían que ser claros y distinguir lo que sale de la sentencia de lo que decidió el grupo.
- **Qué cambió:** dos diagramas SVG; los pasos que son decisiones del grupo tienen borde punteado y color violeta.
- **Pedido:** «Dibujá el flujo de cada regla con sus condiciones, la acción del agente y el cierre.»
- **Verificación:** se renderizó cada SVG para revisarlo antes de aceptarlo.

#### Etapa 3 · Landing y documentación
- **Problema:** la página tenía que ser accesible y simple, sin sobrecargar.
- **Qué cambió:** HTML y CSS estáticos, con texto alternativo en los diagramas, jerarquía de títulos, navegación por teclado y el detalle de cada flujo en secciones desplegables nativas.
- **Pedido:** «Armá la landing de la startup con los dos flujos y sus decisiones. No exageres.»
- **Verificación:** los enlaces internos, los diagramas y el logo cargan.

_[Agregar aquí las instrucciones literales del grupo, si las hay.]_

## Limitaciones

- Es una **propuesta de diseño**: los agentes no se ejecutan ni se conectan a servicios reales.
- Los formatos admitidos (JPG, PNG y MP4) son un ejemplo: los define la startup.
