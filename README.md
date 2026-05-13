# Prompting Frameworks: CoT, ToT & GoT

Comprehensive visual guide to advanced reasoning techniques for LLMs like Grok.

## Flowcharts

### 1. Chain of Thought (CoT)
```mermaid
flowchart TD
    A[Start: User Query] --> B[Understand Problem]
    B --> C[Break into Steps]
    C --> D[Reason Step 1]
    D --> E[Reason Step 2]
    E --> F[Continue All Steps]
    F --> G[Synthesize Answer]
    G --> H[Verify]
    H --> I[Final Output]
    
    style A fill:#e3f2fd
    style I fill:#e8f5e9
```

### 2. Tree of Thoughts (ToT)
```mermaid
flowchart TD
    A[Start: User Query] --> B[Decompose Problem]
    B --> C{Generate Multiple\nBranches?}
    
    C --> D1[Branch 1]
    C --> D2[Branch 2]
    C --> D3[Branch 3]
    
    D1 --> E1[Evaluate\nScore 1-10]
    D2 --> E2[Evaluate\nScore 1-10]
    D3 --> E3[Evaluate\nScore 1-10]
    
    E1 --> F{Prune Weak\nBranches}
    E2 --> F
    E3 --> F
    
    F --> G[Expand Best\nBranches]
    G --> H{Depth Reached?}
    
    H -->|No| C
    H -->|Yes| I[Compare All\nComplete Paths]
    
    I --> J[Select Best Path]
    J --> K[Final Answer]
    
    style A fill:#e3f2fd
    style K fill:#e8f5e9
    style C fill:#fff3e0
    style F fill:#fff3e0
    style H fill:#fff3e0
```

### 3. Graph of Thoughts (GoT)
```mermaid
flowchart TD
    A[Start: User Query] --> B[Generate Initial Thoughts]
    
    B --> C1[Thought Node 1]
    B --> C2[Thought Node 2]
    B --> C3[Thought Node 3]
    
    C1 --> D1[Refine / Merge]
    C2 --> D2[Refine / Merge]
    C3 --> D3[Refine / Merge]
    
    D1 --> E[Aggregation Node]
    D2 --> E
    D3 --> E
    
    E --> F[Refinement Loop]
    F --> G[Distillation]
    
    G --> H[Final Synthesized Solution]
    
    style A fill:#e3f2fd
    style H fill:#e8f5e9
    style E fill:#fff3e0
    style F fill:#f3e5f5
```

## Bird's Eye View Comparison

| Framework | Structure | Key Operations | Best Use Cases | Complexity |
|-----------|-----------|----------------|----------------|------------|
| **CoT** | Linear Chain | Sequential steps | Standard reasoning, math, logic | Low |
| **ToT** | Tree (Branching) | Branch, Evaluate, Prune | Planning, puzzles, search | Medium |
| **GoT** | Arbitrary Graph | Merge, Refine, Aggregate, Loops | Complex synthesis, creativity, strategy | High |

**Visualization Summary**: CoT is a straight line → ToT is a tree with branches → GoT is a full interconnected graph with merging and feedback loops.

Clone this repo and open README.md in any Markdown viewer that supports Mermaid (GitHub, VS Code, Obsidian, etc.).