# Integración de Ladder con agentes en otros repos y contextos

Ladder puede utilizarse de forma automatizada desde cualquier proyecto o contexto de trabajo. A continuación se describen cuatro estrategias, ordenadas de más simple a más sofisticada.

---

## 1. CLI directo desde otro repo

Lo más básico — desde cualquier sitio, apuntas al CLI:

```bash
# Desde cualquier directorio
cd /ruta/a/tu/Ladder && bun run ladder add source --title "Bug en auth: tokens expiran antes de tiempo"
```

Un agente de Claude Code puede hacer esto con Bash desde cualquier proyecto. Para facilitarlo, se puede añadir al `CLAUDE.md` del otro repo:

```markdown
## Ladder Integration
Cuando encuentres un problema, oportunidad de mejora, o patrón interesante,
regístralo en Ladder:
  cd ~/comp/00-produccion/Ladder && bun run ladder add source --title "..."
```

**Ventaja:** Funciona hoy sin tocar nada.
**Limitación:** Requiere que el agente sepa que debe hacerlo (instrucciones explícitas).

---

## 2. Hooks de Claude Code

Automatización sin intervención manual. En el `settings.json` del proyecto:

```json
{
  "hooks": {
    "post-tool-call": [
      {
        "matcher": "Bash",
        "command": "# script que analiza el output y, si detecta algo interesante, lo manda a Ladder"
      }
    ]
  }
}
```

Cada vez que un agente ejecute un comando, un script evalúa si hay algo relevante que meter en el pipeline de Ladder.

**Ventaja:** Totalmente automático, el agente no necesita recordar nada.
**Limitación:** Requiere escribir el script de evaluación y afinar qué se considera "interesante".

---

## 3. MCP Server (la más potente)

Convertir Ladder en un **servidor MCP** que cualquier agente pueda usar como herramienta nativa. Esto expondría herramientas como `ladder_add_source`, `ladder_add_idea`, `ladder_list`, `ladder_status`, etc.

```typescript
// Tools/mcp-server.ts
// Expone: ladder_add_source, ladder_add_idea, ladder_list, ladder_status
```

Configuración en cualquier proyecto:

```json
{
  "mcpServers": {
    "ladder": {
      "command": "bun",
      "args": ["run", "/ruta/a/Ladder/Tools/mcp-server.ts"]
    }
  }
}
```

El agente tendría herramientas `ladder_add_source`, `ladder_search`, etc. disponibles **en cualquier conversación**, sin cambiar de directorio ni hacer nada especial.

**Ventaja:** Integración nativa — el agente usa Ladder como cualquier otra herramienta.
**Limitación:** Requiere construir el servidor MCP (no existe aún en el repo).

---

## 4. Subagente dedicado

Lanzar un agente en background que vigile y alimente Ladder:

```markdown
# En CLAUDE.md de tu proyecto
Cuando completes una tarea significativa, lanza un subagente que:
1. Analice qué se hizo y qué se aprendió
2. Registre hallazgos relevantes en ~/Ladder como Sources
3. Si un hallazgo sugiere una mejora, créalo también como Idea
```

**Ventaja:** Procesamiento inteligente — el subagente decide qué es relevante y cómo categorizarlo.
**Limitación:** Consume tokens adicionales por cada evaluación.

---

## Recomendación

| Situación | Estrategia recomendada |
|-----------|----------------------|
| Empezar hoy mismo | **1. CLI directo** |
| Automatizar sin desarrollo | **2. Hooks** |
| Integración a medio plazo | **3. MCP Server** |
| Máxima inteligencia | **4. Subagente dedicado** |

La opción **MCP Server** es la que más sentido tiene a medio plazo — convierte Ladder en una herramienta que cualquier agente tiene siempre disponible, sin fricción. Construirlo sería además un buen primer proyecto para alimentar el propio Ladder con su proceso de desarrollo.
