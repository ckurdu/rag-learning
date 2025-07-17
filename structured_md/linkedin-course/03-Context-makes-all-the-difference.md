# Context Makes All the Difference

## Core Idea

Providing context to an LLM dramatically improves the relevance and accuracy of its output. Just as we narrow our conversations with friends by adding details, LLMs leverage contextual cues to guide their probabilistic text completions.

```mermaid
flowchart LR
  subgraph ChatHistory
    SM[System Message]
    U1[User Prompt]
    R1[LLM Response]
  end
  U2[New Context] --> ChatHistory
  ChatHistory --> AC[Auto-Completion with Context]
```

## Everyday Analogy

When you want to bake a cake, you don’t ask, “What are the ingredients for cake?” You specify which cake by saying, “What are the ingredients for a carrot cake?” The word “carrot” provides crucial context that changes the recipe.

```mermaid
flowchart LR
  P1[Prompt: cake ingredients] --> R1[Response: Flour, Sugar, Eggs]
  P2[Prompt: carrot cake ingredients] --> R2[Response: Flour, Sugar, Eggs, Carrots]
```

## Prompt Engineering

Prompt engineering is simply the art of providing the right context (system messages + user instructions + documents) so that the LLM’s auto-completion stays on target.

```mermaid
flowchart TD
  Docs[(Documents / Webpage / Transcript)] --> CTX[Context Block]
  CTX & U[User Query] --> LLM[LLM Inference]
  LLM --> R[Response]
```

## Takeaway

Any time you find an LLM answer going off-track, consider what additional context you can supply. That simple act is often enough to steer the model back in line.
