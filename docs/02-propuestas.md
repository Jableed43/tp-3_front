# Propuestas de solución · Soulless Catcher (bloque S04-A)

El alcance es **diseñar y explicar**. Los agentes de estas propuestas son futuros: nada de lo que se describe acá se conecta ni se implementa.

---

## Propuesta 1 · Arranque ordenado de la revisión

**Corresponde a:** R1.

> Si el archivo es accesible y su formato está admitido, el sistema inicia la revisión y registra el enlace de origen cuando está disponible.

**Qué haría el futuro agente.** Recibiría el envío del usuario y consultaría una herramienta de verificación de archivos para saber si se puede abrir y qué formato tiene. Compararía ese formato con la lista de formatos admitidos. Si se cumplen las dos condiciones, iniciaría la revisión y dejaría registrado el enlace de origen, si el usuario lo aportó.

**Herramienta que consultaría.** Un verificador de archivos (acceso, apertura y formato).

**Cuándo pediría ayuda a una persona.** En este recorrido, nunca: es el camino normal.

**Resultado.** La revisión queda iniciada, con un registro que dice de dónde viene el material o que no se indicó un origen.

**Beneficio.** La revisión solo comienza con material utilizable. Cada informe queda con su origen registrado cuando existe, lo que da trazabilidad. El usuario sabe enseguida que su pedido ya está en marcha.

**Caso límite.** *Archivo válido pero sin enlace de origen.* La sentencia pide registrar el enlace "cuando está disponible", así que la revisión se inicia igual y el registro indica que no hay enlace. No se pide nada a una persona.

**Recorridos para comprobarlo**

| Caso | Datos | Se cumple la condición | Resultado |
|---|---|---|---|
| A | Imagen que se abre, formato admitido, con enlace de origen | Sí | Se inicia la revisión y se registra el enlace. |
| B | Video que se abre, formato admitido, sin enlace | Sí | Se inicia la revisión, sin enlace registrado. |
| C | Documento de texto (formato no admitido) | **No** | R1 no se aplica: el caso pasa a la Propuesta 2. |

---

## Propuesta 2 · Archivo no utilizable: explicar y pedir otro

**Corresponde a:** R2.

> Si el archivo no puede abrirse o su formato no está admitido, el sistema explica el problema y solicita otro archivo sin emitir un resultado.

**Qué haría el futuro agente.** Detectaría que el archivo no se puede abrir o que su formato no está admitido. Elegiría un mensaje según la causa: explicaría qué falló y qué formatos sirven, pediría otro archivo y **no emitiría ningún resultado**.

**Herramienta que consultaría.** El mismo verificador de archivos de la Propuesta 1.

**Cuándo pediría ayuda a una persona.** *Decisión del grupo (D3):* si el usuario envía dos archivos seguidos que fallan, ofrecería ayuda de una persona de soporte.

**Resultado.** El usuario recibe una explicación y un pedido claro, y no se genera ningún veredicto ni puntaje.

**Beneficio.** Evita informes engañosos sobre material que no se pudo ver. El usuario sabe exactamente qué corregir, en lugar de recibir un error genérico.

**Caso límite.** *El archivo falla por los dos motivos a la vez* (no se abre y, además, su formato no está admitido). El agente explica **ambos** motivos en un solo mensaje y pide un archivo nuevo. Si el segundo envío también falla, interviene la persona de soporte (D3).

**Recorridos para comprobarlo**

| Caso | Datos | Se cumple la condición | Resultado |
|---|---|---|---|
| A | Archivo con formato no admitido | Sí | Se explica el problema, se pide otro archivo y no se emite resultado. |
| B | Archivo dañado que no se abre | Sí | Igual que el caso A. |
| C | Imagen que se abre, formato admitido | **No** | R2 no se aplica: el caso sigue por la Propuesta 1. |
| D | Segundo archivo seguido que también falla | Sí | Igual que A, y además se ofrece ayuda de una persona (D3). |

---

## Qué viene de las sentencias y qué agregamos

| | Viene de la sentencia | Lo agregó el grupo |
|---|---|---|
| **Flujo 1** | Condición (accesible **y** formato admitido), iniciar la revisión, registrar el enlace solo si está disponible. | Uso de un verificador de archivos; orden de comprobación (D1); no verificar el enlace (D2); la lista de formatos como ejemplo (D5). |
| **Flujo 2** | Condición (no se abre **o** formato no admitido), explicar, pedir otro archivo, no emitir resultado. | Informar los formatos admitidos (D4); ayuda de una persona tras dos fallos (D3). |
