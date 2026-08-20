# 🕸️ NEURAL_MESH_ESTABLISHED // SIGNAL: SHAWN

<details>
<summary>🇯🇵 <b>日本語の概要はこちら (Click to expand Japanese summary)</b></summary>

<br />

### 概要 (Overview)

このポートフォリオでは、信頼性・監査可能性・決定論的な設計を重視した、実践的なAIおよび知的システムの構築原則を紹介しています。

### 主要プロジェクトと理論・実装フレームワーク (Featured Architectures & Frameworks)

* **Derivative of Truth Framework**: BM25検索、知識グラフ、語彙的一致、不確実性ペナルティ、Probabilistic Logic Networks（確率論理ネットワーク）を組み合わせ、LLMが生成した主張の証拠支持度を評価する監査可能な真実性スコアリングフレームワーク。低スコアの主張は検出・フラグ付け・抑制できます。
* **LinkedIn SSI Booster**: 真偽検証ゲート、ハイブリッドRAG（Retrieval-Augmented Generation）、継続的学習機能を備えたローカルファーストの自動化エージェント。
* **Regulatory Intelligence Assistant (RIA)**: G7 GovAI Grand Challenge向けに設計した、Elasticsearch、Neo4j、ベクトル検索を組み合わせた多層ハイブリッドRAGアーキテクチャ。
* **Answer42**: 学術研究分析のための9エージェント・パイプライン。クラウドAPIとローカルOllamaモデルのフォールバック処理を備えています。
* **S1gnal-Zero**: Solace Build to Convert Hackathonの受賞作品。Model Context Protocol (MCP) とイベント駆動型メッセージングを活用した、5エージェント分散処理システムです。

### コア技術 (Key Technical Pillars)

1. **真実性評価 (Truth Gate) & Probabilistic Logic Networks**: Derivative of Truth、PLNによる証拠・推論の確率的評価、BM25、NetworkX、spaCyを組み合わせた多段階検証レイヤー。
2. **マルチエージェント・オーケストレーション**: 専門化されたエージェント、フォールバック処理、サーキットブレーカー、MCP/FastMCPベースのツール連携。
3. **ディープインデキシングと検索 (Hybrid RAG)**: Elasticsearch、Neo4j、ベクトル検索を組み合わせた多層検索。
4. **エンタープライズとイベントストリーミング**: Java、JMS、イベントブローカーを活用した高スループット・イベント駆動システム。

</details>

This portfolio showcases engineering principles for building reliable, auditable intelligent systems.

I design systems where AI output is connected to retrieved evidence, explicit workflows, and observable validation rather than being treated as an unexamined answer. The work spans multi-agent orchestration, hybrid search, event-driven processing, local model routing, and creative AI systems.

The goal is practical intelligence with traceable behavior: systems that can explain what they used, why a result was produced, and where uncertainty remains.

---

### 🚀 Active Nodes: Featured Architectures & Frameworks

**[Node 00] The Derivative of Truth Framework**

A structured, auditable evidence-scoring framework for evaluating generated claims against retrieved knowledge.

The framework combines BM25 retrieval, knowledge-graph evidence paths, token-level claim-evidence overlap, source credibility, uncertainty penalties, and Probabilistic Logic Network (PLN) inference.

When PLN-enhanced scoring is enabled, evidence strength and reasoning strength are computed through probabilistic truth-value aggregation rather than relying only on fixed heuristic weights. A legacy weighted-scoring path remains available as a fallback.

The resulting truth-gradient score estimates how strongly a claim is supported by the available evidence. Optional trajectory tracking measures how that score changes across repeated evaluations using $dT/dt$.

Low-scoring claims can be flagged or removed by the post-generation truth gate, with evidence paths, uncertainty sources, reasoning metadata, and scoring explanations retained for auditability.

The framework does not mathematically prove truth or control token generation in real time. It provides an interpretable, evidence-grounded estimate of claim support and exposes the reasoning and uncertainty behind that estimate.

📄 **[Read the Theoretical Paper (PDF)](https://github.com/samjd-zz/linkedin_ssi_booster/blob/main/docs/The%20Derivative%20of%20Truth_%20A%20New%20Mathematical%20Framework%20for%20AI%20Truthfulness.pdf)**

[Node 01] LinkedIn SSI Booster

A truth-gated, continual-learning automation agent driven by a local-first hybrid Retrieval-Augmented Generation (RAG) architecture — and a multi-avatar content-creation system spanning text, image, and music.

It uses BM25 for transparent lexical retrieval, NetworkX for knowledge-graph relationships, and spaCy for semantic and entity-oriented validation. Generated content is evaluated against persona facts, domain knowledge, and article evidence before it reaches the publishing workflow.

🎨 FLUX Capacitor — a local GPU art avatar (FLUX.1-schnell, GGUF-quantized) rendering symbolic visuals for every post, with a shared GPU orchestrator that keeps Ollama-first sequencing on a single RTX 3060.

🎶 Rei Toei — a Suno + Strudel-driven AI music avatar (inspired by William Gibson's Idoru) that converts curated technical knowledge into cyberpop/industrial algorithmic music, complete with its own persona graph and domain-knowledge pack.

🌟 **[Star linkedin_ssi_booster on GitHub](https://github.com/samjd-zz/linkedin_ssi_booster)** 🌟

**[Node 02] Regulatory Intelligence Assistant (RIA)**

Built for the G7 GovAI Grand Challenge, this multi-tiered hybrid RAG architecture combines Elasticsearch, Neo4j graph traversal, and vector search to navigate large federal legal datasets.

The system separates lexical retrieval, graph relationships, and semantic retrieval so that each layer contributes a different form of evidence and context.

🌟 **[Star regulatory-intelligence-assistant on GitHub](https://github.com/samjd-zz/regulatory-intelligence-assistant)** 🌟

**[Node 03] Answer42**

A 9-agent orchestration pipeline designed for academic research analysis.

It uses specialized processing stages, automated fallback logic, and resilience controls to switch between cloud APIs and local Ollama models when the preferred provider is unavailable or unsuitable.

🌟 **[Star answer42 on GitHub](https://github.com/samjd-zz/answer42)** 🌟

**[Node 04] S1gnal-Zero**

An award-winning 5-agent Model Context Protocol (MCP) system created for the Solace Build to Convert Hackathon.

It uses event-driven communication, message-broker routing, and distributed agent coordination to process intelligent signals across multiple specialized nodes.

🌟 **[Star s1gnalzeroapp on GitHub](https://github.com/samjd-zz/s1gnalzeroapp)** 🌟

---

### 🧬 Key Technical Pillars

#### 1. Hybrid RAG, Truth Gates & Evidence Grounding

*Found in: linkedin_ssi_booster | Regulatory Intelligence Assistant (RIA) | Derivative of Truth Framework*

The systems move beyond simple prompt wrapping by combining retrieval, structured evidence, probabilistic reasoning, and post-generation validation.

* **Derivative of Truth:** An evidence-scoring framework that combines evidence quality, reasoning type, source credibility, lexical claim-evidence overlap, and uncertainty penalties.
* **Probabilistic Logic Networks:** PLN-enhanced scoring aggregates evidence and reasoning signals into probabilistic truth values. The system uses this to strengthen claim evaluation, not to prove objective truth.
* **Historical Truth Tracking:** When a claim is evaluated repeatedly, the system can track changes in its truth-gradient score and calculate a historical rate of change, $dT/dt$.
* **Hybrid RAG Pipelines:** Combining deterministic lexical retrieval such as BM25 with knowledge-graph relationships and semantic similarity.
* **Truth Gate:** A multi-stage validation process that evaluates evidence strength, truth-gradient scores, article similarity, organization-name support, and fact-pool similarity.
* **Continual Learning:** The system records selected feedback and published-output signals to improve future ranking, repetition control, and content selection.

The result is an auditable estimate of how well a generated claim is supported by the system's available evidence.

#### 2. Multi-Agent Orchestration & Workflow Design

*Found in: Answer42 | S1gnal-Zero*

The systems use specialized agents and explicit processing stages to divide complex work into observable responsibilities.

* **Agentic Pipelines:** Specialized nodes communicate, transform, validate, and refine intermediate results.
* **Resilience & Local Routing:** Fallback mechanisms, circuit breakers, provider switching, and local model routing help workflows continue when a dependency or model is unavailable.
* **Resource-Aware Processing:** Local systems can coordinate model usage to reduce GPU contention and avoid loading multiple heavy model instances unnecessarily.
* **Protocols & Event Architecture:** MCP and FastMCP-based tool integrations connect agents to capabilities, while Solace and JMS support event-driven messaging patterns.

#### 3. Deep Indexing & Search

*Found in: Regulatory Intelligence Assistant | CIHR Portal | linkedin_ssi_booster*

The search systems combine different retrieval strategies for heterogeneous information sources.

* **The Stack:** Elasticsearch for lexical retrieval and BM25 scoring, Neo4j for graph relationships and traversal, and vector search for semantic similarity.
* **Search Logic:** Multi-stage retrieval and fallback strategies allow the system to use the most suitable available search mechanism for a query.
* **Evidence Composition:** Search results can be combined with structured relationships and domain context before being passed to downstream generation or analysis.
* **Domain Focus:** The work includes large collections of federal, regulatory, technical, and research-oriented documents.

#### 4. Enterprise & Event Streaming

*Found in: TPG/USPS JMS Platform | S1gnal-Zero | Shared Services Canada*

* **High-Throughput Core:** Experience designing, maintaining, and scaling Java enterprise systems and event-driven platforms.
* **Messaging:** JMS and event brokers provide durable communication patterns between services and processing stages.
* **Operational Resilience:** Systems are designed around clear boundaries, failure handling, observability, and controlled recovery paths.
* **Distributed Processing:** Event-driven architecture allows specialized components to process messages independently while remaining connected through explicit contracts.

---

### 🌐 The Network

Whether you're here for the code, the architecture, the algorithmic soundscapes, or simply to connect across the grid:

* 📄 **Research Paper:** [The Derivative of Truth Framework (PDF)](https://github.com/samjd-zz/linkedin_ssi_booster/blob/main/docs/The%20Derivative%20of%20Truth_%20A%20New%20Mathematical%20Framework%20for%20AI%20Truthfulness.pdf) 🚀
* 👤 **LinkedIn:** [Shawn Jackson-Dyck](https://linkedin.com/in/shawn-jackson-dyck-52aa74358/) 🚀
* 🎶 **Suno:** [Rei Toei (@samjd42)](https://suno.com/@samjd42) 🚀
* 🎶 **Audius:** [@samjd42](https://audius.co/samjd42) 🚀
* ▶️ **YouTube:** [@samjd42](https://youtube.com/@samjd42) 🚀

---

### 💫 Support the Architecture

Building evidence-grounded systems and producing algorithmic tracks takes serious compute cycles. If you want to support the late-night builds:

💫 **[Join & Support my work on Buffer](https://join.buffer.com/samjd42)** 🚀
