<p align="center"><img src="docs/banner.svg" alt="tailscale-vllm: Tailscale-Ops: Ollama model specialized for Tailscale v2 API" width="100%"></p>

# tailscale-vllm

**Tailscale-Ops**: an Ollama model specialized for the **Tailscale v2 API**, part of git-fabric's **fabric-llm** layer (`L1 transport`).

It answers questions about its domain locally, so the fabric only escalates to Claude when it has to. See [fabric-sdk](https://github.com/git-fabric/sdk) for how requests are routed.

| | |
|---|---|
| Base model | `qwen2.5:14b` |
| Context window | 4,096 tokens |
| Temperature | 0.15 |
| MCP tools described | 17 |

## Use it

```bash
ollama create tailscale-ops -f Modelfile
ollama run tailscale-ops
```

## What's inside

A single [`Modelfile`](Modelfile): the base model, its sampling parameters, and a system prompt that teaches the model the Tailscale v2 API and the MCP tools it can call.

<!-- org-footer -->
---

<p align="center"><sub>Part of <a href="https://github.com/git-fabric">git-fabric</a> · composable fabric apps for Git-native infrastructure · built by <a href="https://github.com/ry-ops">ry-ops</a></sub></p>
