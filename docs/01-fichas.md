# Fichas de las sentencias · Soulless Catcher (bloque S04-A)

Cada ficha desarma una sentencia: **sentencia original → datos necesarios → condición → consecuencia**. La redacción original no se modifica.

---

## Ficha R1

**Sentencia original**

> Si el archivo es accesible y su formato está admitido, el sistema inicia la revisión y registra el enlace de origen cuando está disponible.

**Datos necesarios**

| # | Dato | Para qué sirve |
|---|---|---|
| 1 | El archivo recibido | Saber si se puede acceder a él. |
| 2 | El formato del archivo | Saber de qué tipo es. |
| 3 | La lista de formatos admitidos | Comparar el formato recibido. La sentencia no la define: la fija la startup. |
| 4 | El enlace de origen (opcional) | Registrar de dónde viene el material, si el usuario lo aporta. |

**Condición**

El archivo es **accesible** **Y** su formato está **admitido**. Las dos cosas a la vez: si falla una, la condición no se cumple.

**Consecuencia**

1. El sistema **inicia la revisión**.
2. El sistema **registra el enlace de origen**, pero **solo cuando está disponible**. Es una segunda condición dentro de la consecuencia: si no hay enlace, la revisión comienza igual.

**Lo que la sentencia no dice**

- Qué pasa cuando la condición no se cumple (lo establece R2).
- Qué formatos están admitidos.
- Qué significa exactamente "disponible" para el enlace de origen.

---

## Ficha R2

**Sentencia original**

> Si el archivo no puede abrirse o su formato no está admitido, el sistema explica el problema y solicita otro archivo sin emitir un resultado.

**Datos necesarios**

| # | Dato | Para qué sirve |
|---|---|---|
| 1 | El archivo recibido | Intentar abrirlo. |
| 2 | Si el archivo puede abrirse | Detectar el primer motivo de falla. |
| 3 | El formato del archivo | Detectar el segundo motivo de falla. |
| 4 | La lista de formatos admitidos | Comparar el formato y, además, informarla al usuario. |

**Condición**

El archivo **no puede abrirse** **O** su formato **no está admitido**. Alcanza con que se cumpla **una** de las dos.

**Consecuencia**

1. El sistema **explica el problema**.
2. El sistema **solicita otro archivo**.
3. El sistema **no emite ningún resultado**. Es una prohibición: no hay veredicto ni puntaje sobre un material que no se pudo revisar.

**Lo que la sentencia no dice**

- Cuántas veces se puede reintentar.
- Si en algún momento interviene una persona.

---

## Cómo se relacionan R1 y R2

Con los símbolos A = "se puede acceder y abrir" y F = "formato admitido":

- Condición de R1: **A y F**.
- Condición de R2: **no A, o no F**.

Si "accesible" (R1) y "puede abrirse" (R2) significan lo mismo, R2 es exactamente lo contrario de R1: se complementan y cubren todos los casos sin solaparse.

**Pero las sentencias usan palabras distintas.** Eso deja un caso límite: un archivo al que se llega (accesible) pero que está dañado y no se abre, con un formato admitido. Según R1 se iniciaría la revisión; según R2 habría que explicar el problema y pedir otro archivo.

### Decisiones del grupo

Estas decisiones **no salen de las sentencias**: las agregamos nosotros para que el recorrido sea completo.

| Cód. | Decisión | Por qué |
|---|---|---|
| **D1** | "Accesible" se entiende como "se puede acceder **y abrir**". Se comprueba en este orden: acceso, apertura, formato. Si algo falla, se aplica R2. | Evita que se revise un archivo que no se pudo leer, y es coherente con "sin emitir un resultado". |
| **D2** | "Disponible" (enlace de origen) significa que **el usuario lo aportó**. El agente lo registra tal como viene, sin verificarlo. | Estas dos sentencias no piden verificar el enlace. |
| **D3** | Si el usuario envía **dos archivos seguidos** que fallan, se ofrece ayuda de **una persona de soporte**. | R2 no define reintentos; así se evita un ciclo sin salida. |
| **D4** | El mensaje de error incluye la **lista de formatos admitidos**. | Para que el usuario sepa qué enviar. |
| **D5** | Como la sentencia no los lista, los formatos admitidos son un **ejemplo**: imágenes y videos comunes (p. ej. JPG, PNG y MP4). Los define la startup. | El objetivo de la startup es revisar imágenes y videos. |
