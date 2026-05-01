<div align="center">

# `~ $ ./bdl --hello`

> **AI Native Engineer** &nbsp;·&nbsp; harness engineering for agentic AI

```
┌──────────────────────────────────────────────────────────────────┐
│  Harness Engineering · Agentic AI · Physical AI · Edge · KB      │
└──────────────────────────────────────────────────────────────────┘
```

![Status](https://img.shields.io/badge/status-building-2ea44f?style=flat-square) ![Direction](https://img.shields.io/badge/direction-Harness%20Engineering-8957e5?style=flat-square)
![Focus](https://img.shields.io/badge/focus-Agentic%20AI-blue?style=flat-square) ![Stack](https://img.shields.io/badge/stack-ROS2%20%7C%20MCP%20%7C%20ESP32-orange?style=flat-square) ![Approach](https://img.shields.io/badge/approach-local--first-lightgrey?style=flat-square)

</div>

---

## `$ whoami`

```yaml
role:     AI Native Engineer
method:   harness engineering   # how   — build the runtime / scaffold
payload:  agentic AI            # what  — runs inside the harness
loops:
  ├── agent runtimes   ⇆  simulation feedback
  ├── local devices    ⇆  knowledge bases
  └── tools · memory · constraints
goal:     close practical engineering loops with reusable harnesses
```

---

## `~/focus`

| Track                     | Description                                                              |
| :------------------------ | :----------------------------------------------------------------------- |
| 🛠 **Harness Engineering** | Building runtimes / scaffolds that let AI iterate on real systems safely |
| 🧠 **Agentic AI**          | MCP tools, runtime feedback, hot deployment, self-iteration              |
| 🤖 **Physical AI**        | Simulation-in-the-loop runtime for repeatable robot behavior development |
| 📡 **Edge AI / HW**       | ESP32, BLE bridges, local-first device state sync                        |
| 📚 **Knowledge Eng.**     | Foundry-style semantic layer for agent-facing knowledge bases            |
| 🎓 **Learning**           | Model distillation and edge deployment                                   |

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

> Foundry-style semantic layer for agent-facing knowledge bases.

```text
  operational objects ─┐
  relationships       ├─▶ ontology-backed semantic layer ─▶ agents / apps
  actions             │
  governance rules    ┘
```

Maps domain operations into an ontology-backed interface so agents can work with business objects, relationships, actions, and governance rules instead of loose document chunks.

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
- [ ] `ontology/` — semantic layer for agent applications
- [ ] `mcp-ctrl/` — runtime control planes for tools, robots, devices

---

<div align="center">

`built in the open · iterating in small steps`

</div>
