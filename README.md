# Prompting Frameworks: CoT, ToT & GoT

**The ultimate resource for mastering advanced LLM reasoning techniques.**

![Evolution](https://via.placeholder.com/800x200/1976d2/ffffff?text=CoT+→+ToT+→+GoT)

## Overview

| Framework | Structure | Best For | Performance Gain |
|-----------|-----------|----------|------------------|
| **Chain of Thought (CoT)** | Linear | Step-by-step reasoning | Baseline |
| **Tree of Thoughts (ToT)** | Branching Tree | Exploration, planning, puzzles | + significant on search tasks |
| **Graph of Thoughts (GoT)** | Arbitrary Graph (merging, loops) | Complex synthesis, creativity | +62% on sorting vs ToT (original paper) |

## Bird's Eye View

```mermaid
flowchart TD
    A[Advanced Reasoning] --> B[CoT: Linear Chain]
    A --> C[ToT: Tree Branching]
    A --> D[GoT: Full Graph]
    
    B --> E[Sequential]
    C --> F[Parallel Exploration]
    D --> G[Merging + Refinement Loops]
    
    style A fill:#e3f2fd
    style D fill:#f3e5f5
```

## Contents
- [CoT Guide](docs/cot.md)
- [ToT Guide](docs/tot.md)
- [GoT Guide](docs/got.md)
- [Prompt Library](/prompts/)
- [Examples](/examples/)

**Star this repo if you find it useful!** 🚀