---
permalink: /
layout: portfolio
title: "Yufan Shi - AI Systems Engineer"
description: "Yufan Shi builds reliable AI agents, retrieval systems, and multimodal intelligence."
redirect_from:
  - /about/
  - /about.html
---

<header class="site-header" data-header>
  <a class="wordmark" href="#top" aria-label="Yufan Shi, home">
    <span class="wordmark__monogram">YS</span>
    <span class="wordmark__meta">AI Systems<br>Engineer</span>
  </a>
  <nav class="site-nav" aria-label="Primary navigation">
    <a href="#work">Work</a>
    <a href="#experience">Experience</a>
    <a href="#about">About</a>
  </nav>
  <a class="header-contact" href="mailto:peteryufan28@gmail.com">
    Let's talk <span aria-hidden="true">↗</span>
  </a>
</header>

<main id="main">
  <section class="hero" id="top" aria-labelledby="hero-title">
    <div class="hero__eyebrow" data-reveal>
      <span class="status-dot" aria-hidden="true"></span>
      <span>San Diego / Shanghai</span>
      <span class="hero__eyebrow-rule"></span>
      <span>M.S. ECE @ UC San Diego</span>
    </div>

    <div class="hero__grid">
      <div class="hero__copy">
        <p class="section-index" data-reveal>01 / Profile</p>
        <h1 id="hero-title" data-reveal>
          Building AI systems<br>
          that <em>reason, retrieve,</em><br>
          and recover.
        </h1>
        <div class="hero__bottom" data-reveal>
          <p>
            I'm Yufan Shi, an AI engineer focused on reliable agents,
            retrieval-augmented generation, and multimodal systems.
            Currently developing multi-agent root cause analysis at Microsoft.
          </p>
          <div class="hero__actions">
            <a class="button button--dark" href="#work">Explore selected work</a>
            <a class="button button--line" href="https://www.linkedin.com/in/yufan-shi/" target="_blank" rel="noopener">LinkedIn <span aria-hidden="true">↗</span></a>
          </div>
        </div>
      </div>

      <div class="agent-canvas" aria-label="Diagram of a multi-agent reasoning system" data-reveal>
        <div class="agent-canvas__grid" aria-hidden="true"></div>
        <p class="agent-canvas__label">LIVE SYSTEM / 04 AGENTS</p>
        <div class="agent-node agent-node--main">
          <span>01</span>
          <strong>ORCHESTRATOR</strong>
          <small>route · coordinate · verify</small>
        </div>
        <div class="agent-node agent-node--a">
          <span>02</span><strong>RETRIEVAL</strong>
        </div>
        <div class="agent-node agent-node--b">
          <span>03</span><strong>REASONING</strong>
        </div>
        <div class="agent-node agent-node--c">
          <span>04</span><strong>REVIEWER</strong>
        </div>
        <span class="agent-line agent-line--a" aria-hidden="true"></span>
        <span class="agent-line agent-line--b" aria-hidden="true"></span>
        <span class="agent-line agent-line--c" aria-hidden="true"></span>
        <div class="agent-canvas__signal" aria-hidden="true"><span></span><span></span><span></span><span></span></div>
        <p class="agent-canvas__result"><span></span> hypothesis verified</p>
      </div>
    </div>

    <div class="metric-strip" data-reveal>
      <div><strong>+30%</strong><span>RCA pass rate</span></div>
      <div><strong>96.5%</strong><span>Medical RAG Hit@5</span></div>
      <div><strong>100%</strong><span>Agent routing accuracy</span></div>
      <div><strong>3.7</strong><span>UCSD GPA / 4.0</span></div>
    </div>
  </section>

  <section class="work section" id="work" aria-labelledby="work-title">
    <div class="section-head" data-reveal>
      <p class="section-index">02 / Selected work</p>
      <h2 id="work-title">Systems with measurable<br><em>intelligence.</em></h2>
      <p>From retrieval quality to production reliability, I design the full path between a user question and a trustworthy answer.</p>
    </div>

    <article class="project project--medical" data-reveal>
      <div class="project__info">
        <div class="project__number">PROJECT / 01</div>
        <p class="project__type">Multi-agent medical question answering</p>
        <h3>MedMARS</h3>
        <p class="project__lede">A LangGraph-based medical assistant that routes questions across diagnosis, medication consultation, general QA, and visual question answering.</p>
        <div class="project__metrics">
          <div><strong>96.5%</strong><span>Hit@5</span></div>
          <div><strong>0.81</strong><span>MRR</span></div>
          <div><strong>0.845</strong><span>NDCG@5</span></div>
        </div>
        <ul class="project__details">
          <li>Orchestrator with safety routing, query rewriting, conditional workflows, and multi-turn memory.</li>
          <li>GraphRAG + VectorRAG over 47K medical records using FAISS, BM25, and reciprocal rank fusion.</li>
          <li>LoRA-tuned Mistral-7B and Qwen2-VL-7B with CPU-GPU memory scheduling.</li>
        </ul>
        <a class="text-link" href="https://github.com/Cruise-pp/MedMARS" target="_blank" rel="noopener">View repository <span aria-hidden="true">↗</span></a>
      </div>
      <figure class="project__visual project__visual--medical architecture" aria-label="Code-verified MedMARS LangGraph workflow">
        <figcaption class="architecture__head">
          <span>MEDMARS / LANGGRAPH RUNTIME</span>
          <span class="verified-badge">CODE VERIFIED</span>
        </figcaption>

        <div class="med-ingress">
          <div class="arch-source"><span>INPUT A</span><strong>TEXT QUERY</strong></div>
          <div class="arch-source arch-source--optional"><span>INPUT B</span><strong>MEDICAL IMAGE</strong><small>optional</small></div>
        </div>

        <div class="med-router-card arch-card">
          <span class="arch-step">01 / CONTROL</span>
          <strong>ORCHESTRATOR</strong>
          <div class="arch-pills"><span>Safety check</span><span>Context arbitration</span><span>Query rewrite</span><span>Intent routing</span></div>
          <div class="med-router-card__exit"><span>emergency / self-harm</span><strong>SAFETY EXIT →</strong></div>
        </div>

        <div class="arch-flow-label"><span></span><strong>SAFE REQUEST</strong><span></span></div>

        <div class="med-vision-row">
          <div class="med-vision-card arch-card">
            <span class="arch-step">02 / OPTIONAL VISION</span>
            <strong>QWEN2-VL-7B + LORA</strong>
            <small>Image analysis → clinical evidence</small>
          </div>
          <div class="med-vram-card">
            <span>VRAM SCHEDULER</span>
            <strong>Mistral ⇄ Qwen2-VL</strong>
            <small>dynamic CPU / GPU swap</small>
          </div>
        </div>

        <div class="med-knowledge-head"><span>03 / KNOWLEDGE ROUTING</span><span>ONE ACTIVE BRANCH</span></div>
        <div class="med-branch-grid">
          <div class="med-branch med-branch--diagnosis">
            <span class="med-branch__code">A / SYMPTOMS</span>
            <strong>DIAGNOSIS</strong>
            <ol>
              <li>Completeness gate</li>
              <li>Follow-up loop</li>
              <li>Mistral-7B + LoRA</li>
            </ol>
            <small>DDXPlus / differential diagnosis</small>
          </div>
          <div class="med-branch med-branch--medication">
            <span class="med-branch__code">B / MEDICATION</span>
            <strong>DRUG SAFETY</strong>
            <ol>
              <li>Drug extraction</li>
              <li>Exact → fuzzy resolve</li>
              <li>Pairwise DDI lookup</li>
            </ol>
            <small>DrugBank / SQLite GraphRAG</small>
          </div>
          <div class="med-branch med-branch--general">
            <span class="med-branch__code">C / GENERAL QA</span>
            <strong>HYBRID RAG</strong>
            <ol>
              <li>FAISS vector recall</li>
              <li>BM25 + RRF fusion</li>
              <li>Confidence gate</li>
            </ol>
            <small>MedQuAD / 47K QA pairs</small>
          </div>
        </div>

        <div class="med-merge" aria-hidden="true"><span></span><strong>MERGE EVIDENCE</strong><span></span></div>
        <div class="med-synth-card arch-card">
          <span class="arch-step">04 / RESPONSE</span>
          <strong>SYNTHESIZER</strong>
          <div class="arch-pills"><span>Grounded response</span><span>Faithfulness check</span><span>Rolling summary</span></div>
          <p><span class="status-dot"></span> PATIENT-FRIENDLY ANSWER</p>
        </div>
      </figure>
    </article>

    <article class="project project--commerce" data-reveal>
      <div class="project__info">
        <div class="project__number">PROJECT / 02</div>
        <p class="project__type">ByteDance AI Full-Stack Challenge</p>
        <h3>Multimodal<br>E-commerce Agent</h3>
        <p class="project__lede">A controllable shopping agent combining image-text retrieval, deterministic tool orchestration, and structured streaming responses.</p>
        <div class="project__metrics">
          <div><strong>+14%</strong><span>Recall@5</span></div>
          <div><strong>+6%</strong><span>NDCG@5</span></div>
          <div><strong>100%</strong><span>Recall@10*</span></div>
        </div>
        <ul class="project__details">
          <li>Hybrid retrieval with query understanding, hard filters, multimodal embeddings, and reranking.</li>
          <li>Function-calling intent router across seven deterministic tools with 100% routing accuracy.</li>
          <li>SSE pipeline for staged delivery of decisions, product cards, and generated text.</li>
        </ul>
        <a class="text-link" href="https://github.com/YufanPeter/E-commerce-AI-Agent" target="_blank" rel="noopener">View repository <span aria-hidden="true">↗</span></a>
        <p class="project__footnote">* Structured-query Recall@10.</p>
      </div>
      <figure class="project__visual project__visual--commerce architecture" aria-label="Code-verified CartPilot controlled agent and retrieval workflow">
        <figcaption class="architecture__head">
          <span>CARTPILOT / CONTROLLED AGENT</span>
          <span class="verified-badge verified-badge--dark">CODE VERIFIED</span>
        </figcaption>

        <div class="cartpilot-ingress">
          <div class="cartpilot-inputs"><span>TEXT</span><span>VOICE</span><span>IMAGE</span></div>
          <div class="cartpilot-api arch-card">
            <span class="arch-step">01 / INTERFACE</span>
            <strong>FASTAPI / CHAT STREAM</strong>
            <small>session state · REST · Server-Sent Events</small>
          </div>
        </div>

        <div class="cartpilot-routing">
          <div class="cartpilot-router arch-card">
            <span class="arch-step">02 / DECIDE</span>
            <strong>FUNCTION-CALLING ROUTER</strong>
            <small>intent → rewritten query → confidence</small>
          </div>
          <div class="cartpilot-image arch-card">
            <span class="arch-step">IMAGE PATH</span>
            <strong>VLM QUERY EXTRACTION</strong>
            <small>image → searchable product phrase</small>
          </div>
        </div>

        <div class="cartpilot-tools">
          <div class="cartpilot-tools__head"><span>03 / DETERMINISTIC TOOLS</span><span>7 ROUTES</span></div>
          <div class="cartpilot-tools__grid">
            <span class="is-primary">Recommend</span><span>Refine</span><span>Compare</span><span>Detail</span><span>Cart</span><span>Clarify</span><span>Fallback</span>
          </div>
        </div>

        <div class="cartpilot-search">
          <div class="cartpilot-search__head"><span>04 / RECOMMENDATION SEARCH</span><strong>HYBRID RAG</strong></div>
          <div class="cartpilot-search__steps">
            <div><span>01</span><strong>UNDERSTAND</strong><small>constraints + user memory</small></div>
            <div><span>02</span><strong>HARD FILTER</strong><small>category · brand · SKU price</small></div>
            <div><span>03A</span><strong>CHROMA</strong><small>vector evidence</small></div>
            <div><span>03B</span><strong>BM25 + RRF</strong><small>lexical fusion</small></div>
            <div><span>04</span><strong>RERANK</strong><small>optional relevance API</small></div>
            <div><span>05</span><strong>AGGREGATE</strong><small>negative filters + product level</small></div>
          </div>
          <div class="cartpilot-visual-fusion"><span>IMAGE ONLY</span><strong>TEXT RELEVANCE 60%</strong><i>+</i><strong>VISUAL SIMILARITY 40%</strong></div>
        </div>

        <div class="cartpilot-facts-row">
          <div><span>FACT SOURCE</span><strong>SQLITE</strong><small>products · SKUs · stock · cart</small></div>
          <div><span>WORKING MEMORY</span><strong>SESSION</strong><small>last hits · constraints · references</small></div>
        </div>

        <div class="cartpilot-output">
          <div class="cartpilot-result"><span>05</span><strong>STRUCTURED TOOL RESULT</strong></div>
          <span class="cartpilot-output__arrow" aria-hidden="true">→</span>
          <div class="cartpilot-composer"><span>06</span><strong>ANSWER COMPOSER</strong></div>
          <span class="cartpilot-output__arrow" aria-hidden="true">→</span>
          <div class="cartpilot-sse"><span>07</span><strong>SSE → SWIFTUI</strong></div>
        </div>
        <div class="cartpilot-events">session · status · meta · tool_result · token* · memory_update · done</div>
      </figure>
    </article>
  </section>

  <section class="experience section" id="experience" aria-labelledby="experience-title">
    <div class="section-head section-head--compact" data-reveal>
      <p class="section-index">03 / Experience</p>
      <h2 id="experience-title">Engineering for<br><em>reliability.</em></h2>
    </div>
    <article class="experience-card" data-reveal>
      <div class="experience-card__company">
        <div class="microsoft-mark" aria-hidden="true"><i></i><i></i><i></i><i></i></div>
        <div><strong>Microsoft</strong><span>AI Application Development Intern</span></div>
      </div>
      <time>MAR 2026 - PRESENT</time>
      <div class="experience-card__story">
        <p>Building a hierarchical multi-agent root cause analysis system for cloud incidents, where specialist agents attribute different change signals and an aggregation layer forms the final hypothesis.</p>
        <p>Designed retrieval over historical incidents, confidence filtering, caching, fallback mechanisms, and a reviewer layer - reducing problematic RCA samples by approximately 10% and improving pass rate by approximately 30%.</p>
      </div>
      <div class="experience-card__tags"><span>AIOps</span><span>Multi-Agent</span><span>RAG</span><span>Evaluation</span><span>Reliability</span></div>
    </article>
  </section>

  <section class="about section" id="about" aria-labelledby="about-title">
    <div class="section-head" data-reveal>
      <p class="section-index">04 / About</p>
      <h2 id="about-title">Curious by nature.<br><em>Rigorous by design.</em></h2>
      <p>I work at the intersection of model behavior and production systems: designing orchestration, retrieval, evaluation, and safeguards that make AI useful beyond the demo.</p>
    </div>

    <div class="about-grid">
      <div class="education-panel" data-reveal>
        <p class="panel-label">EDUCATION</p>
        <article>
          <div><span>2025 - 2027</span><h3>University of California San Diego</h3><p>M.S. in Electrical and Computer Engineering · GPA 3.7/4.0</p></div>
          <strong>UCSD</strong>
        </article>
        <article>
          <div><span>2021 - 2025</span><h3>Xi'an Jiaotong-Liverpool University</h3><p>B.S. in Computer Science · GPA 3.76/4.0 · Top 10% scholarship</p></div>
          <strong>XJTLU</strong>
        </article>
      </div>

      <a class="publication-panel" href="https://doi.org/10.1007/s10462-026-11538-1" target="_blank" rel="noopener" data-reveal>
        <div class="publication-panel__top"><span>PUBLICATION / 2026</span><span aria-hidden="true">↗</span></div>
        <p>Artificial Intelligence Review</p>
        <h3>On-Device Large Language Models: A Survey of Model Compression and System Optimization</h3>
        <div class="publication-panel__doi">DOI / 10.1007/s10462-026-11538-1</div>
      </a>
    </div>
  </section>

  <section class="capabilities" aria-label="Technical capabilities">
    <div class="capabilities__track" aria-hidden="true">
      <span>LANGGRAPH</span><i>✳</i><span>PYTORCH</span><i>✳</i><span>RAG</span><i>✳</i><span>MULTI-AGENT</span><i>✳</i><span>LLM</span><i>✳</i><span>LANGGRAPH</span><i>✳</i><span>PYTORCH</span><i>✳</i><span>RAG</span><i>✳</i><span>MULTI-AGENT</span><i>✳</i><span>LLM</span><i>✳</i>
    </div>
  </section>

  <section class="contact section" id="contact" aria-labelledby="contact-title">
    <p class="section-index" data-reveal>05 / Contact</p>
    <h2 id="contact-title" data-reveal>Let's build something<br><em>intelligent.</em></h2>
    <a class="contact__email" href="mailto:peteryufan28@gmail.com" data-reveal>
      <span>peteryufan28@gmail.com</span><span aria-hidden="true">↗</span>
    </a>
    <div class="contact__links" data-reveal>
      <a href="https://github.com/YufanPeter" target="_blank" rel="noopener">GitHub ↗</a>
      <a href="https://www.linkedin.com/in/yufan-shi/" target="_blank" rel="noopener">LinkedIn ↗</a>
      <a href="https://github.com/YufanPeter" target="_blank" rel="noopener">More work ↗</a>
    </div>
  </section>
</main>

<footer class="site-footer">
  <span>© <span data-year>2026</span> YUFAN SHI</span>
  <span>DESIGNED FOR CLARITY / BUILT FOR THE WEB</span>
  <a href="#top">BACK TO TOP ↑</a>
</footer>
