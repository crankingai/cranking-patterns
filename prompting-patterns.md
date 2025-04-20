# Prompting Patterns, as might be useful for an Agent

## 🤖 Prompting Patterns Comparison: ReAct vs ReWoo vs MRKL

| Feature / Pattern              | **ReAct** (Reason + Act)                             | **ReWoo** (Reflective Workflow)                         | **MRKL** (Modular Reasoning + Knowledge + Language)         |
|-------------------------------|------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------|
| 🧠 **Core Idea**               | Interleaves reasoning (`Thought`) and tool use (`Action`) | Plans via reusable workflows with reflection at each step | Uses modular tools + LLM to answer questions compositionally |
| 🧱 **Structure**               | `Thought → Action → Observation → Thought …`         | `Plan → Execute → Reflect → Adapt → Repeat`              | `Question → Module Select → Tool Use → Combine → Answer`     |
| 🔁 **Interactivity**          | Dynamic, stateful loop with tool feedback            | Emphasizes adaptive planning over time                   | Usually stateless tool calls guided by routing logic         |
| 🧰 **Tool Use**               | Explicit via `Action:` steps                         | Through predefined or evolving workflows                 | Handled by expert modules (e.g., search, calculator, etc.)    |
| 🧩 **Modularity**             | Medium – handled inside a single prompt or agent     | High – workflows are modular and potentially nested      | High – routing layer picks between independent modules        |
| 🧭 **Agent Autonomy**         | Medium – can decide on next action per step          | High – reflects and adapts plans over time               | Low to medium – primarily executes static modules             |
| 🔎 **Transparency**           | High – `Thought` and `Observation` steps are visible | High – steps and reflections logged                      | Medium – behavior depends on routing, may feel opaque         |
| 🧪 **Best For**               | Tool-augmented reasoning and flexible task solving   | Tasks requiring adaptability, planning, and iteration    | Query answering via toolchains or hybrid LLM+search systems   |
| 📜 **Origin / Paper**         | [ReAct (Yao et al., 2022)](https://arxiv.org/abs/2210.03629) | [ReWoo (Chen et al., 2023)](https://arxiv.org/abs/2305.17141) | [MRKL (Lewis et al., 2022)](https://arxiv.org/abs/2205.00445) |
