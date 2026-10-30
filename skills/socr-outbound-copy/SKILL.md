---
name: socr-outbound-copy
description: "Redacta copy de prospección outbound (WhatsApp y llamadas) para RENVELL/SOCR, aplicando automáticamente las 5 reglas del ángulo validado con respuestas reales de clínicas dentales. Úsalo cuando el usuario pida: escribir un mensaje de WhatsApp para una clínica nueva; redactar el guion de apertura de una llamada de prospección; responder a una objeción de un prospecto (recepción, \"¿quién eres?\", \"no me gusta insistir\", \"mándame info\"); revisar si un mensaje ya escrito suena demasiado comercial. Ejemplo de petición: \"Escríbeme el WhatsApp para Clínica Dental X, decisora Dra. Fulanita, ortodoncia, Sevilla.\""
---

# SOCR — Copy de Prospección Outbound

**Categoría:** Ventas B2B / Prospección — RENVELL (grupos y clínicas dentales privadas, España)

## Para qué sirve
Genera y revisa copy de prospección (WhatsApp, apertura de llamada, respuestas a objeciones) para el producto SOCR de RENVELL, aplicando siempre las reglas ya validadas contra respuestas reales de prospectos — no reglas teóricas.

## El ángulo (obligatorio, no negociable)
No somos un proveedor que vende algo. Somos quien ya ha mirado los números del sector y ha encontrado un patrón: la mayoría de clínicas no tiene calculado cuántos presupuestos del año pasado nunca llegaron a empezar tratamiento. Esa pregunta, hecha bien, genera el interés por sí sola — no hace falta vender nada en el primer mensaje.

## Las 5 reglas (aplícalas siempre, sin excepción)
1. **El primer mensaje nunca menciona RENVELL, SOCR, ni "servicio"/"solución"/"herramienta".** Tampoco se auto-presenta el remitente de ninguna forma, ni siquiera indirecta ("trabajo con clínicas dentales" ya es auto-presentación y suena a vendedor — está prohibido).
2. **Cada fase del embudo vende solo la fase siguiente, nunca el producto final.** El WhatsApp no vende la llamada; vende que respondan la pregunta. La llamada no vende el contrato; vende los 15 minutos de diagnóstico.
3. **Lo que se ofrece es LA CIFRA (cuántos presupuestos no arrancaron), nunca "una reunión" o "una demo".**
4. **Nunca se pide acceso a datos internos ni a herramientas de gestión.** El prospecto mira su propia pantalla — nosotros no pedimos ver nada.
5. **"¿Quién eres?" es una señal de interés, no una objeción a evitar.** No se preempta explicando quién eres antes de que lo pregunten — eso mata el ángulo.

## Reglas adicionales de tono (aprendidas de respuestas reales)
- Nunca pedir perdón por escribir ("perdona el mensaje directo") — suena a alguien que sabe que está molestando.
- A recepción nunca se le pide el contacto directo del decisor — dispara un protocolo de bloqueo. Se le pide que traslade la pregunta.
- Si el prospecto plantea una objeción ética tipo "no me gusta insistir" (equipara seguimiento con presionar al paciente), no se rebate — se le da la razón y se separa "insistir a quien dijo que no" de "acompañar a quien nunca llegó a decidir". No se pide llamada de inmediato con este perfil.
- Independientes con propietario operativo → WhatsApp funciona. Grupos con estructura (varias sedes, departamentos) → WhatsApp se bloquea rápido; mejor llamada a sede concreta o LinkedIn del director.

## Plantillas base

**WhatsApp — versión A (consultiva):**
> Hola, buenas. Escribo para [decisor] — [dato verificado: especialidad / años / ciudad].
>
> Llevo meses analizando por dentro los números de clínicas dentales en España, y hay una cifra que casi ninguna tiene calculada: cuánto suman los presupuestos que se emiten y nunca llegan a empezar.
>
> ¿La tenéis vosotros?

**WhatsApp — versión B (honesta-directa):**
> Hola, buenas. Escribo para [decisor], y te aviso de entrada: esto es por trabajo, no soy paciente.
>
> Me dedico a una cosa muy concreta con clínicas dentales: los presupuestos que se hacen y luego no llegan a arrancar. Antes de proponerte nada quiero saber si os pasa.
>
> ¿Sabéis cuántos tuvisteis el año pasado?

**Apertura de llamada:**
> "Hola, buenas tardes. Antes de nada, ¿con quién hablo? ¿Tú llevas el tema de los presupuestos ahí?"
> [30 seg, sin pitch] "Te cuento por qué escribí. Trabajo con clínicas dentales en una cosa muy concreta: los presupuestos que se hacen y luego no llegan a arrancar. Casi ninguna clínica tiene calculado cuánto suma eso al año, y cuando se mira suele salir una cifra que sorprende."
> [la pregunta, y callarse] "¿Vosotros lo tenéis medido? ¿Sabéis cuántos presupuestos del año pasado se quedaron sin empezar?"

**Objeción de recepción pidiendo derivar a email o pidiendo el contacto:**
> "Entendido. ¿Le puedes trasladar la pregunta a quien lo lleve? Con que me diga el número aproximado me vale, no necesito nada más."

## Cómo usarla
Dale a Claude los datos verificados de la clínica (nombre del decisor, especialidad, ciudad, años si aplica) y el canal (WhatsApp o llamada). Si es para revisar un mensaje ya escrito, pégalo y pide que se audite contra las 5 reglas — te dirá exactamente qué regla rompe y por qué antes de corregirlo.

## Ejemplos de prompts
1. "Escríbeme el WhatsApp versión A para Clínica Dental Rossi, decisor Dr. Marco Rossi, implantología, Bilbao."
2. "Este mensaje me lo han rechazado, revísalo contra las reglas: [pegar mensaje]"
3. "La recepción me está pidiendo que le mande un email en vez de hablar con el decisor, ¿qué respondo?"

Fuente: `10_EMBUDOS_OUTBOUND_COPY.md` y `11_REGISTRO_RESPUESTAS_REALES.md` del proyecto RENVELL en Claude — estas reglas están validadas contra respuestas literales de prospectos reales, no son teoría.
