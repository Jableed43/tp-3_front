# Diagramas · trazabilidad con las sentencias

Los dos diagramas están en [`../diagramas/`](../diagramas/):

- [`flujo-r1.svg`](../diagramas/flujo-r1.svg) · Flujo 1 · Arranque ordenado de la revisión.
- [`flujo-r2.svg`](../diagramas/flujo-r2.svg) · Flujo 2 · Archivo no utilizable: explicar y pedir otro.

Cada diagrama tiene título y descripción accesibles dentro del propio SVG (`<title>` y `<desc>`).

## Cómo leer los colores

| Elemento | Qué significa |
|---|---|
| Azul claro | Datos de entrada |
| Blanco con borde oscuro | Acción del agente |
| Amarillo (rombo) | Decisión |
| Verde | Resultado o acción que produce la consecuencia de la sentencia |
| Rojo claro | Restricción (algo que **no** se debe hacer) |
| Verde azulado | Intervención de una persona |
| Violeta con borde punteado | Algo que agregó el grupo y que **no** sale de la sentencia |
| Gris con borde punteado | Aclaración sobre el paso siguiente |

## Flujo 1 · R1

> Si el archivo es accesible y su formato está admitido, el sistema inicia la revisión y registra el enlace de origen cuando está disponible.

| Parte de la sentencia | Dónde está en el diagrama |
|---|---|
| "el archivo es accesible **y** su formato está admitido" | Rombo central: *¿El archivo es accesible Y su formato está admitido?* |
| "inicia la revisión" | Caja verde *Iniciar la revisión* (rama SÍ). |
| "registra el enlace de origen **cuando está disponible**" | Segundo rombo *¿Hay enlace de origen?*: con enlace se registra; sin enlace se continúa igual. |
| Lo que la sentencia no define (la condición no se cumple) | Rama NO: *R1 no se aplica*, el caso pasa al Flujo 2. |
| **Agregado del grupo** | Verificador de archivos (herramienta) y caso límite D1 (archivo dañado = no accesible). |

## Flujo 2 · R2

> Si el archivo no puede abrirse o su formato no está admitido, el sistema explica el problema y solicita otro archivo sin emitir un resultado.

| Parte de la sentencia | Dónde está en el diagrama |
|---|---|
| "no puede abrirse **o** su formato no está admitido" | Rombo central: *¿El archivo NO se puede abrir O su formato NO está admitido?* |
| "explica el problema" | Caja *Explicar el problema*. |
| "solicita otro archivo" | Caja *Solicitar otro archivo*. |
| "sin emitir un resultado" | Caja roja *No emitir ningún resultado*. |
| Lo que la sentencia no define (el archivo es válido) | Rama NO: *R2 no se aplica*, el caso sigue por el Flujo 1. |
| **Agregado del grupo** | Lista de formatos en el mensaje (D4); ayuda de una persona tras dos fallos seguidos (D3); caso límite de doble falla. |

## Recorridos de comprobación

Los casos detallados están en [`02-propuestas.md`](02-propuestas.md). Cada flujo se recorrió con un caso que cumple la condición y otro que no:

| Flujo | Caso que cumple | Caso que no cumple |
|---|---|---|
| 1 · R1 | Imagen que se abre, formato admitido, con enlace → revisión iniciada y enlace registrado. | Documento de texto → R1 no se aplica, pasa al Flujo 2. |
| 2 · R2 | Archivo de formato no admitido → se explica, se pide otro y no hay resultado. | Imagen que se abre y de formato admitido → R2 no se aplica, sigue el Flujo 1. |
