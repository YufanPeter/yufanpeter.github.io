---
permalink: /projects/medmars/
layout: portfolio
title: "MedMARS - Yufan Shi"
description: "Case study of MedMARS, a safety-aware multi-agent medical reasoning and retrieval system."
---

<header class="site-header" data-header>
  <a class="wordmark" href="{{ site.baseurl }}/" aria-label="Yufan Shi, home">
    <span class="wordmark__monogram">YS</span>
    <span class="wordmark__meta">AI Systems<br>Engineer</span>
  </a>
  <nav class="site-nav" aria-label="Project navigation">
    <a href="{{ site.baseurl }}/#work">Selected work</a>
    <a href="https://github.com/Cruise-pp/MedMARS" target="_blank" rel="noopener">GitHub ↗</a>
  </nav>
  <a class="header-contact" href="{{ site.baseurl }}/#contact">Let's talk <span aria-hidden="true">↗</span></a>
</header>

<main id="main" class="case-study">
  <section class="case-hero" id="top">
    <a class="case-back" href="{{ site.baseurl }}/#work">← Back to selected work</a>
    <div class="case-hero__grid">
      <div>
        <p class="case-kicker">PROJECT CASE STUDY / 01</p>
        <h1>MedMARS</h1>
        <p class="case-hero__lede">A safety-aware LangGraph system that coordinates specialized medical agents across diagnosis, medication safety, general medical QA, and image understanding.</p>
      </div>
      <div class="case-hero__aside">
        <span>ROLE</span><strong>Agent workflow · Fine-tuning · RAG</strong>
        <span>SYSTEM</span><strong>Multi-agent medical reasoning</strong>
        <span>STACK</span><strong>LangGraph · PyTorch · FAISS · BM25</strong>
      </div>
    </div>
    <div class="case-actions">
      <a class="button button--dark" href="https://github.com/Cruise-pp/MedMARS" target="_blank" rel="noopener">View repository ↗</a>
      <a class="button button--line" href="#architecture">Explore architecture ↓</a>
    </div>
  </section>

  <figure class="case-figure" id="architecture">
    <a href="{{ site.baseurl }}/images/medmars-handdrawn-pipeline-v4.png" target="_blank" rel="noopener">
      <img src="{{ site.baseurl }}/images/medmars-handdrawn-pipeline-v4.png" alt="MedMARS multi-agent medical pipeline">
    </a>
    <figcaption><span>CODE-VERIFIED PIPELINE</span><span>CLICK TO VIEW FULL SIZE ↗</span></figcaption>
  </figure>

  <section class="case-metrics" aria-label="MedMARS retrieval results">
    <div><strong>96.5%</strong><span>Hit@5</span></div>
    <div><strong>0.81</strong><span>MRR</span></div>
    <div><strong>0.845</strong><span>NDCG@5</span></div>
    <div><strong>47K</strong><span>Medical QA records</span></div>
  </section>

  <section class="case-section">
    <div class="case-section__label">01 / Challenge</div>
    <div class="case-section__body">
      <h2>Medical questions need different forms of reasoning.</h2>
      <p>A symptom description, a drug-interaction question, and an uploaded medical image should not follow the same path. MedMARS separates routing, specialist reasoning, evidence retrieval, and response synthesis while carrying safety and conversation context across the workflow.</p>
    </div>
  </section>

  <section class="case-section">
    <div class="case-section__label">02 / Runtime</div>
    <div class="case-section__body">
      <h2>One orchestrator, four specialist agents.</h2>
      <div class="case-card-grid case-card-grid--agents">
        <article><span>CONTROL</span><h3>Orchestrator</h3><p>Runs safety classification, gathering arbitration, intent routing, and query rewriting before any specialist work begins.</p></article>
        <article><span>OPTIONAL IMAGE</span><h3>Vision Agent</h3><p>Uses Qwen2-VL-7B with LoRA to turn a medical image into clinical evidence for a downstream knowledge agent.</p></article>
        <article><span>SYMPTOMS</span><h3>Diagnosis Agent</h3><p>Checks information completeness, asks follow-up questions when needed, then runs LoRA-tuned Mistral-7B on DDXPlus.</p></article>
        <article><span>MEDICATION</span><h3>Medication Agent</h3><p>Resolves drug names against DrugBank and performs pairwise drug-drug interaction retrieval through SQLite GraphRAG.</p></article>
        <article><span>GENERAL QA</span><h3>General QA Agent</h3><p>Retrieves MedQuAD evidence with FAISS, BM25, reciprocal-rank fusion, and a confidence gate.</p></article>
        <article><span>RESPONSE</span><h3>Synthesizer</h3><p>Combines visual findings, retrieved evidence, and clinical reasoning into a patient-friendly response.</p></article>
      </div>
    </div>
  </section>

  <section class="case-section">
    <div class="case-section__label">03 / Reliability</div>
    <div class="case-section__body">
      <h2>Safety and grounding are part of the graph.</h2>
      <ul class="case-list">
        <li><strong>Safety exit.</strong> Emergency and self-harm requests bypass all generative knowledge agents and return fixed response templates.</li>
        <li><strong>Follow-up loop.</strong> The diagnosis branch gathers missing information before attempting a preliminary assessment.</li>
        <li><strong>Faithfulness check.</strong> Synthesized claims are checked against retrieved context, with warnings for unsupported or low-confidence output.</li>
        <li><strong>Memory and scheduling.</strong> A rolling clinical summary preserves multi-turn context while diagnosis and vision models dynamically swap CPU/GPU memory.</li>
      </ul>
    </div>
  </section>

  <nav class="case-next" aria-label="Project navigation">
    <span>NEXT CASE STUDY</span>
    <a href="{{ site.baseurl }}/projects/cartpilot/">Multimodal E-commerce Agent <span aria-hidden="true">→</span></a>
  </nav>
</main>

<footer class="site-footer">
  <span>© <span data-year>2026</span> YUFAN SHI</span>
  <a href="{{ site.baseurl }}/#work">ALL PROJECTS ↑</a>
</footer>
