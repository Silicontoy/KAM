# KAM: An AI Development Methodology for Decoupling Knowledge and Implementation

This framework defines "Knowledge" in the AI era as a core concept within the Large Language Model (LLM) domain, placing it alongside terms like flow, skill, and agent.

---

## I. Core Concept Definitions

### 1. What is KAM (Knowledge Application Methodology)?

* **Definition:** KAM is a four-layer decoupled methodology for transforming domain expertise into AI-ready capabilities.
* **Core Logic:** The development of AI application tools is divided into general practices (e.g., algorithmic code) and domain-specific components, which is especially critical in complex, long-chain automated tasks. KAM uses a standardized architecture to strip an expert's "intuition," clean it, and reconstruct it into machine-consumable "logical assets."
* **Methodology Vision:** To conquer the final barrier of the most difficult automation tasks.

### 2. What is Knowledge (The New AI-Era Definition)?

* **Conceptual Decoupling:** "Knowledge" decouples the domain information required by LLM tools from the actual AI tool development actions. It represents the sum of all information needed to build automated LLM tools.
* **New Definition Formula:** In the KAM context, Knowledge = Sum of {Specific Information + Data Flow + Control Flow}. One part acts as static material, and the other part acts as the processing method for that material.
* **Internalized Form:** Inserted into the model via training or fine-tuning.
* **Externalized Form:** Dynamically injected via context prompts or RAG/agent skills (which ultimately function as context input).
* **The Next Step for Knowledge:** It can be processed into datasets (for training/fine-tuning), flows (processes and logic), agents (loops), or skills/MCPs (connecting professional and general tools).
* **Requirement:** Project knowledge must be exact—neither too much nor too little. For example, knowing "C" is a prerequisite for "C++", but RV32I and RV64I are parallel concepts; the foundational requirement is knowing what an ISA is.
* **Essence:** By decoupling domain information from general AI project workflows, KAM introduces "Knowledge Engineering" to solve highly complex, long-chain problems.

### 3. What is Knowledge Engineering?

* **Definition:** The entire process of processing raw, fragmented, and implicit domain data into standardized, AI-consumable "knowledge blocks." It acts as pseudocode written by non-software domain experts.
* **Knowledge Classification:** Capturing top-tier industry information down to the minute-level logs and intentions of an expert.
* **Global Perspective:** The knowledge engineer must be a highly capable engineer (staff level or above) who understands the overarching goals of the expert's work, even if they cannot execute it themselves.
* **Knowledge Completion:** Identifying and filling in the "implicit basic knowledge" that is universally assumed in the industry but missing from the model.
* **Deterministic Construction:** Building Checkers with clear Pass/Fail criteria.
* **Modality Planning:** Deciding which knowledge goes into RAG, fine-tuning, or hardcoded scripts.
* **Extensibility:** Planning how knowledge storage should evolve as model capabilities increase and training costs decrease.

---

## II. KAM Overall Architecture: The Four-Layer Pipeline

**Purpose:** To decouple professional knowledge from engineering implementation, turning AI development into a reusable, replaceable, and independently evolving universal pathway.

**Overall Architecture Flow:** Domain Information Layer (Expert) → Knowledge Processing Layer (Knowledge Engineer) → AI Tool Planning Layer (AI Architect) → Tool Development Layer (Development Engineer). *Note: External dependencies continuously influence all layers.*

### Layer 1: Professional Knowledge Layer

* **Responsible Role:** Domain Expert
* **Input:** The expert's own domain knowledge, experience, and judgment criteria.
* **Processing:** Experts reorganize their knowledge specifically for machine consumption based on real, cutting-edge workflows. They must log their work by the minute/hour, detailing actions and intentions.
* **Output - Initial Data:** Real domain cases, samples, documents, and operational logs (Time + Action + Purpose).
* **Output - Label Definitions:** Clear explanations of key concepts, categories, and judgment criteria.
* **Constraints:** Experts do not need to understand AI principles, but they must provide initial data and label definitions as a minimum viable delivery.
* **Pass Criteria:** Data must authentically cover core domain scenarios, and labels must be unambiguous and actionable.

### Layer 2: Knowledge Processing Layer

* **Responsible Role:** Knowledge Engineer
* **Input:** Initial data and label definitions from Layer 1.
* **Core Principle:** Raw knowledge cannot automatically become usable knowledge.
* **Process 1 - Knowledge System Establishment:** The engineer builds a comprehensive domain knowledge map, dissecting prerequisite knowledge. They must uncover hidden premises (e.g., the four years of semiconductor physics a chip designer intuitively uses, which the model lacks).
* **Process 2 - Control Flow Planning:** Determining how knowledge is dispatched at runtime.

| Control Method | Description | Applicable Scenario |
| --- | --- | --- |
| **Script** | Hardcoded fixed processes | Highly deterministic, rarely changes |
| **Model** | Autonomous judgment by the model | Flexible flows requiring comprehension |
| **Skill** | Pre-defined capability modules | Clear capabilities requiring reliability |
| **Agent** | Autonomous planning and execution | Open-ended tasks requiring autonomy |

* **Process 3 - Data Flow Planning:** Determining how knowledge interacts with the model.

| Interaction Method | Cost | Depth of Effect | Flexibility |
| --- | --- | --- | --- |
| **Full Training** | Highest | Deepest | Lowest |
| **Fine-tuning** | High | Deep | Low |
| **RAG (Retrieval)** | Medium | Medium | High |
| **Context Learning** | Lowest | Shallowest | Highest |

* **Process 4 - Knowledge Processing:** Annotation, redundancy cleaning, making implicit knowledge explicit, granularity splitting, and formatting.
* **Output:** **Knowledge Blocks.** Standardized knowledge units covering the full spectrum from basic to advanced, complete with preliminary control and data flow plans.
* **Pass Criteria:** Must cover the complete knowledge hierarchy, include implicit foundational knowledge, maintain uniform formatting, and be directly usable by the next layer.

### Layer 3: AI Tool Planning Layer

* **Responsible Role:** AI Architect
* **Input:** Knowledge blocks and flow plans from Layer 2.
* **Feasibility & Cost Assessment:** Determining which technical routes are viable and calculating financial, time, and maintenance costs.
* **Effect & Evaluation Design:** Forecasting the ceiling of each route and defining clear metrics, test sets, and rollback plans.
* **Key Decisions:** Choosing between training custom models vs. commercial APIs, RAG architecture, prompt engineering ratios, and module integration.
* **Output:** **Specific Solution Document.** Includes technical routes, architecture, evaluation methods, budgets, and risk plans.
* **Pass Criteria:** The plan must be immediately executable by developers and contain clear evaluation and fallback mechanisms.

### Layer 4: Tool Development Layer

* **Responsible Role:** Developer (General & Dedicated)
* **Input:** Specific solution document from Layer 3.
* **General Development (100% AI):** Interaction design (web/CLI/desktop), system architecture (API wrappers, concurrency), and deployment (monitoring, logging).
* **Dedicated Development (100% Domain):** Integrating professional software APIs (CAD, ERP, etc.), parsing proprietary data formats, and orchestrating domain-specific workflows.
* **Output:** **Executable AI Tool** delivered to the real-world environment.
* **Pass Criteria:** The tool must meet the functional and performance metrics defined in Layer 3.

---

## III. External Dependencies and Feedback Mechanisms

* **External Dependencies:** The foundation models, new paradigms (e.g., Computer Use, Skill mechanisms), open-source ecosystems, and frameworks (LangChain, Dify) continuously impact decisions across all four layers.
* **Execution Rule:** Work progresses sequentially through the layers. A layer cannot pass its deliverables down until its specific criteria are met.

**Layer-to-Layer Feedback Mechanism:**

| Issue Manifestation | Trace Back To | Resolution Action |
| --- | --- | --- |
| Tool performance fails metrics | **Layer 3** | Re-evaluate the architectural plan and technical routes. |
| Plan cannot be designed | **Layer 2** | Reprocess knowledge, adjust granularity, or improve annotations. |
| Missing foundational concepts | **Layer 1** | Request experts to supplement data or source textbook knowledge. |
| All routes too costly/ineffective | **External** | Wait for tool/model evolution or adjust the project's target scope. |

---

## IV. Appendix: Data vs. Knowledge (A Poetry Example)

To illustrate the difference between raw data and KAM-defined knowledge:

* **Data:** A collection of poems, classic literature, dictionaries.
* **Explicit Knowledge:** * Specific excerpts from classic literature.
* Annotations of those excerpts (the result of looking up words in a dictionary).


* **Implicit Knowledge (The Hidden Premises):**
* What actually defines a poem (e.g., the concept of rhyming, which isn't explicitly defined inside a poetry book).
* How to judge if a poem is good (e.g., assessing emotion and imagery).
* The exact step-by-step process of writing a poem.
* Boundary constraints: It cannot be an essay, a limerick, a brain-teaser, or an academic paper.
* Tool awareness: Knowing the difference between using pen and paper vs. a computer.
* Operational flow: If using a computer, knowing you must first boot it up, open a text editor, type words, decide where to break lines, press "Enter", and finally translate the text into English.


