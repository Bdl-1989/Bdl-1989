<div align="center">

# `Bdl-1989`

```
┌──────────────────────────────────────────────────────────────┐
│  AI Agents · Physical AI · Edge Hardware · Knowledge Systems │
└──────────────────────────────────────────────────────────────┘
```

![Status](https://img.shields.io/badge/status-building-2ea44f?style=flat-square)
![Focus](https://img.shields.io/badge/focus-Physical%20AI-blue?style=flat-square)
![Stack](https://img.shields.io/badge/stack-ROS2%20%7C%20MCP%20%7C%20ESP32-orange?style=flat-square)
![Approach](https://img.shields.io/badge/approach-local--first-lightgrey?style=flat-square)

</div>

---

## `$ whoami`

```yaml
role:        Systems / AI engineer
direction:   agent runtimes  ⇆  simulation feedback
                            ⇆  local devices
                            ⇆  knowledge bases
goal:        close practical engineering loops
```

---

## `~/focus`

| Track                 | Description                                                              |
| :-------------------- | :----------------------------------------------------------------------- |
| 🤖 **Physical AI**    | Simulation-in-the-loop runtime for repeatable robot behavior development |
| 🧩 **Agent Eng.**     | MCP tools, runtime feedback, hot deployment, self-iteration              |
| 📡 **Edge AI / HW**   | ESP32, BLE bridges, local-first device state sync                        |
| 📚 **Knowledge Eng.** | Ontology-based knowledge bases for richer agent context                  |
| 🎓 **Learning**       | Model distillation and edge deployment                                   |

---

## `~/projects`

### ▍ Kongnitive Harness &nbsp;·&nbsp; [`↗`](https://github.com/Kongnitive/Kongnitive-Harness)

> Simulation-in-the-loop runtime for robot AI development.

```text
  ┌───────┐   patch    ┌──────────────┐   deploy   ┌────────────┐
  │  AI   │──────────▶ │ ROS2 Nodes   │──────────▶ │ Simulation │
  └───────┘            └──────────────┘            └─────┬──────┘
       ▲                                                  │
       └──────────── metrics · logs · traces ◀────────────┘
```

- `AI` generates or patches ROS2 behavior nodes
- `Runtime` hot-deploys nodes — no full rebuild / restart
- `Sim` emits structured metrics, logs, and failure traces
- `Loop` feeds the trace back into the next iteration

---

### ▍ Kongnitive ESP32 Harness &nbsp;·&nbsp; [`↗`](https://github.com/Kongnitive/Kongnitive-ESP32-Harness)

> MCP base layer on ESP32.

```text
  firmware (stable)  ──────────────────────────────
        │
        └── Lua runtime ◀── AI agent ──▶ logs / deps / iterate
                                         (no reflash)
```

Firmware stays stable while AI agents update device logic through Lua scripts, inspect logs, switch dependencies, and iterate hardware behavior without repeatedly reflashing firmware.

---

### ▍ Codex Buddy Bridge &nbsp;·&nbsp; [`↗`](https://github.com/Kongnitive/codex-buddy-bridge)

> Codex Desktop ⇄ ESP32 companion, over local MCP + BLE.

```text
  ┌──────────────┐   MCP    ┌────────┐   BLE    ┌───────────┐
  │ Codex Desktop│ ───────▶ │ Plugin │ ───────▶ │ ESP32 Dev │
  └──────────────┘          └────────┘          └───────────┘
```

Syncs work state, permission prompts, recent activity, and token counters.
**Local-first** — no cloud dependency.

---

### ▍ Ontology-Based Knowledge Base

> Ontology as the organizing layer for agent context.

```text
  concepts ─┐
  relations ├─▶ ontology ─▶ structured context ─▶ agent
  constraints┤                (vs. doc chunks)
  process    ┘
```

---

## `~/principles`

```diff
+ Start from the actual problem; keep the first implementation small
+ Prefer readable systems, clear boundaries, observable behavior
+ Close the loop with tests, smoke checks, logs, metrics
+ Treat agents as engineering systems: tools · feedback · memory · constraints
+ Improve incrementally; avoid broad rewrites by default
```

---

## `~/roadmap`

- [ ] `distillation/` — deployable local intelligence
- [ ] `edge-infer/` — hardware-aware deployment
- [ ] `sim2real/` — hardware-in-the-loop workflows
- [ ] `ontology/` — retrieval & domain agent memory
- [ ] `mcp-ctrl/` — runtime control planes for tools, robots, devices

---

<div align="center">

`built in the open · iterating in small steps`

</div>
