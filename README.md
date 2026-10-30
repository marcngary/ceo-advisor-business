# RENVELL — empresa de agentes para Paperclip

Paquete [Agent Companies](https://github.com/paperclipai/paperclip/blob/master/docs/companies/companies-spec.md)
para importar RENVELL en [Paperclip](https://github.com/paperclipai/paperclip):
un CEO advisor y tres agentes que trabajan el embudo outbound de SOCR.

**Los agentes no contactan a nadie.** Preparan cuentas, redactan copy, registran
respuestas y proponen prioridades. Marc envía los WhatsApps y hace las llamadas.

## Organigrama

| Agente | Rol | Qué hace | Skills |
|---|---|---|---|
| `ceo` — CEO Advisor | ceo | Prioriza la semana, reparte trabajo, revisa entregas contra el ángulo | `socr-outbound-copy`, `socr-emv-registro` |
| `copy-outbound` | general | WhatsApp A/B, aperturas de llamada, objeciones, auditoría de mensajes | `socr-outbound-copy` |
| `registro-emv` | researcher | Registro de respuestas reales en una línea, detección de patrones (3+ cuentas) | `socr-emv-registro` |
| `research-cuentas` | researcher | Lotes de cuentas verificadas (decisor, especialidad, canal, fuente) | — |

## Proyecto y tareas iniciales (`projects/outbound-socr`)

| Tarea | Responsable | Tipo |
|---|---|---|
| Revisión semanal del embudo SOCR | `ceo` | Rutina, lunes 8:47 (Madrid) |
| Cierre diario del registro de respuestas | `registro-emv` | Rutina, laborables 19:43 (Madrid) |
| Primer lote de 20 cuentas verificadas | `research-cuentas` | Única |
| Auditar plantillas A/B contra el registro | `copy-outbound` | Única |

## Configuración (`.paperclip.yaml`)

- Todos los agentes con el adaptador `claude_local` (Claude Code), modelo por
  defecto de Paperclip. El directorio de trabajo (`cwd`) se elige al importar.
- Presupuesto mensual por agente: CEO 40, copy 20, research 20, registro 10
  (unidades de la moneda de tu instancia; ajústalo en Paperclip).
- Contratar agentes nuevos requiere aprobación del board (Marc).

## Importar

Necesitas Paperclip en marcha (`npx paperclipai@latest onboard --yes`, Node 24.11+)
y Claude Code instalado en esa máquina.

```sh
# Vista previa sin aplicar nada
paperclipai company import marcngary/ceo-advisor-business --dry-run

# Importar como empresa nueva
paperclipai company import marcngary/ceo-advisor-business --target new
```

Si el repo es privado, clónalo e importa desde la carpeta local:
`paperclipai company import ./ceo-advisor-business`. También funciona desde la UI:
ajustes de empresa → **Import**.

Los agentes y rutinas importados llegan **pausados**. Actívalos desde el panel
"Activate imported agents and routines" cuando estés listo.

## Mantener las skills al día

`skills/socr-outbound-copy` y `skills/socr-emv-registro` son copias de tus skills
de Claude. Si cambias las reglas en el Proyecto RENVELL, actualiza también estos
`SKILL.md` y vuelve a importar las skills.
