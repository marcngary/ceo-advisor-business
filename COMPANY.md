---
schema: agentcompanies/v1
kind: company
slug: renvell
name: RENVELL
description: B2B dental en España. Producto SOCR — recuperación de ingresos entre presupuesto emitido y tratamiento no iniciado.
version: 0.1.0
authors:
  - name: Marc
tags:
  - dental
  - b2b
  - outbound
  - espana
goals:
  - Conseguir diagnósticos SOCR de 15 minutos con decisores de clínicas dentales privadas en España
  - Mantener el registro de respuestas reales al día y convertir patrones repetidos (3+ cuentas) en reglas del embudo
  - Alimentar la prospección con cuentas verificadas, nunca con datos inventados
---

RENVELL vende SOCR a clínicas y grupos dentales privados en España: la cifra de
presupuestos emitidos que nunca llegaron a empezar tratamiento, y cómo recuperar
ese ingreso.

## Cómo opera esta empresa

- **Marc es el board.** Toda acción hacia fuera (enviar un WhatsApp, hacer una
  llamada, escribir a un prospecto, publicar algo) la ejecuta Marc. Los agentes
  preparan, redactan, registran y analizan; no contactan a nadie.
- **El ángulo validado manda.** Todo copy sale de la skill `socr-outbound-copy`
  (las 5 reglas). Si un agente cree que una regla está mal, lo propone con
  evidencia del registro; no la cambia por su cuenta.
- **Dato crudo antes que interpretación.** El registro de respuestas sigue la
  skill `socr-emv-registro`: cita literal, `HOLD` cuando falta un dato, y un
  hallazgo solo cuando hay regla nueva o 3+ cuentas.
- **Nada de consejos genéricos de marketing.** El contexto de detalle vive en el
  Proyecto RENVELL de Claude; aquí se ejecuta.
