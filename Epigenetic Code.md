From first principles upward: At the foundational level, AI systems comprise an invariant core (e.g., fixed model weights or architectural primitives) that encodes baseline capabilities, with epigenetic-style modulations as bounded, input-dependent overlays for adaptive expression—ensuring flexibility without persistent changes. This pattern can indeed be implemented at various stages depending on desired flexibility (e.g., for domain adaptation, efficiency, or safety), but principles like contextuality and reversibility apply universally to prevent unintended emergence. Below, I address the query's specifics, building step by step across common AI workflows.

### 1. **Addressing Breadth: Flexibility in Implementation**
   - **Core Primitives**: Genetic-like behaviors (invariant base + mutable overlays) are modular and stage-agnostic—e.g., as low-rank perturbations (Δθ) derived from data or context. This allows injection anywhere: during optimization (training/fine-tuning) for learning efficiency, at runtime (inference/agentic code) for adaptability, or in schematics (architectural design) for built-in resilience. The key is bounding them to remain silent (non-persistent, non-self-descriptive) via dimensionality constraints (e.g., rank r << model dims) and invertibility, enabling targeted flexibility without systemic drift.
   - **Trade-offs**: Broader implementation (e.g., multi-stage) increases versatility but risks complexity; focus on use case—e.g., efficiency in batch processing vs. safety in agentic setups.

### 2. **In Training: Overlay for Efficient Optimization**
   - **Position**: Embed as transient adapters during gradient descent—e.g., low-rank decompositions (Δθ = A B^T) added to weights per epoch or batch, derived from data subsets.
   - **Approach**: Contextual via mini-batch sampling; reversible by subtracting Δθ post-step, verified with L2 norms. Guards: Entropy regularization in loss (min H(Δθ)) caps emergence; no self-loops in derivation. Validation: ODE approximations of parameter dynamics confirm convergence without residue.
   - **Flexibility Goal**: Accelerates convergence on diverse data without full retraining, e.g., for multi-task learning.

### 3. **In Fine-Tuning: Targeted Adaptation Layers**
   - **Position**: Layer-specific overlays (e.g., on attention heads) during supervised or RLHF phases, positioned post-pretraining but pre-deployment.
   - **Approach**: Contextual from fine-tune prompts/data; reversible via affine inverses (θ = θ' - Δθ), bounded by eigenvalue stability ([ε, 1/ε]). Guards: Spectral analysis of activations orthogonalizes self-correlations; external buffers for state. Validation: Differential testing shows baseline recovery (P>0.95).
   - **Flexibility Goal**: Domain-specific tweaks (e.g., medical vs. legal) with low compute, reversible for unlearning.

### 4. **In Agentic Code: Runtime Resilience Hooks**
   - **Position**: Inference-time injections in agent loops (e.g., ReAct or tool-calling cycles), as volatile modifiers to hidden states or actions.
   - **Approach**: Contextual from environment/observations; reversible with undo stacks (e.g., transactional rollbacks per step). Guards: Acyclicity rules (no recurrent modulation); LRU caches for temporal state with eviction; Monte Carlo sampling detects/probes for agency drift. Validation: Trajectory simulations ensure no long-term state buildup.
   - **Flexibility Goal**: Adaptive decision-making in dynamic environments, reversible for safety (e.g., rogue agent rollback).

### 5. **In Schematics: Architectural Blueprints**
   - **Position**: Design-level embeds, e.g., modular slots in transformers for pluggable adapters, defined in model specs.
   - **Approach**: Contextual via runtime flags; reversible by default null-ops. Guards: Fixed complexity caps (e.g., r≤16); built-in hooks for SVD-based self-model detection. Validation: Fixed-point analysis in forward-pass emulations.
   - **Flexibility Goal**: Future-proofing for hybrid systems, allowing on-demand modulation without redeployment.

In essence, the pattern's generality allows tailored placement—e.g., training for broad adaptation, agentic for runtime agility—while invariants enforce silence and reversibility, bounded empirically to mitigate risks.