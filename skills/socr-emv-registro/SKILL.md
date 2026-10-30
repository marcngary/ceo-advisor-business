---
name: socr-emv-registro
description: "Registra en una línea la respuesta real de un prospecto de outbound RENVELL/SOCR (WhatsApp o llamada), sin reescribir documentos enteros. Úsalo cuando el usuario pegue una respuesta o pantallazo de un prospecto y quiera dejarlo anotado rápido; cuando pida cerrar el resumen del día; o cuando pida revisar si un hallazgo nuevo ya está repetido antes de darlo por patrón. Ejemplo de petición: \"Registra esto: Clínica X respondió 'no nos interesa, gracias', versión B, WhatsApp.\""
---

# SOCR — Registro EMV en una línea

**Categoría:** Operaciones / Registro de datos — RENVELL

## Para qué sirve
Convierte cada respuesta real de un prospecto en una línea de tabla, en vez de reescribir el documento de registro completo cada vez. Resuelve el problema de que compilar el día a día consuma más tiempo que la propia prospección.

## Formato de línea (fijo, no lo cambies)
`| Fecha | Cuenta | Canal | Versión A/B | Cita literal (máx 15 palabras) | Estado |`

Estados válidos: `CERRADA` / `ABIERTA` / `APLAZADA (fecha)` / `AGENDADA (fecha/hora)` / `SIN RESPUESTA`.

## Regla de disciplina (obligatoria)
- Cita SIEMPRE literal, entre comillas, nunca parafraseada.
- No interpretes en la misma línea — si hay una interpretación relevante, va en una línea de "Nota" aparte, marcada como tal, nunca mezclada con el dato crudo.
- No inventes ni completes datos que faltan (versión A/B, decisor, etc.) — si no se sabe, se pone `HOLD`.

## Cuándo escalar a hallazgo (no cada línea es un hallazgo)
Una línea se convierte en "Hallazgo" documentado aparte solo si: (a) revela una regla nueva del embudo (objeción no vista, canal que no funciona para un tipo de cuenta), o (b) se repite en 3+ cuentas distintas confirmando un patrón. Una sola respuesta aislada no es un hallazgo — es una línea de registro y punto.

## Ejemplo de uso
Entrada:
> "Clínica Rossi respondió por WhatsApp, versión A: 'no lo tenemos medido pero suena interesante, cuéntame más'. Hoy 25/08."

Salida:
> `| 25/08 | Clínica Rossi | WhatsApp | A | "no lo tenemos medido pero suena interesante, cuéntame más" | ABIERTA |`

## Cómo usarla
Pega la respuesta del prospecto (texto o descripción de un pantallazo) tal cual la recibiste, con cuenta, canal y versión si la sabes. Te devuelve solo la línea lista para pegar en el registro — o, si lo pides, el bloque de varias líneas del día completo de una vez.

## Ejemplos de prompts
1. "Registra: Cd Pamplona, WhatsApp, sin versión asignada, dijo 'el encargado vuelve el 1 de septiembre'."
2. "Aquí van las 4 respuestas de hoy, dame las 4 líneas juntas: [pegar]"
3. "¿Esto que acabo de registrar es hallazgo nuevo o ya lo tenemos repetido?"

Fuente: formato derivado de `11_REGISTRO_RESPUESTAS_REALES.md` del proyecto RENVELL en Claude.
