---
permalink: /projects/
title: "Projects"
show_title: false
author_profile: true
---

<div class="projects-intro">
  <p class="home-kicker"><span aria-hidden="true"></span>Selected work</p>
  <h2>Agents, retrieval, and multimodal systems.</h2>
  <p>Projects where I designed the full path from model and retrieval choices to orchestration, evaluation, and deployment.</p>
</div>

<div class="project-list">
  <article class="project-card">
    <div class="project-card__topline">
      <p>Multi-agent medical question answering</p>
      <time>Jan - Mar 2026</time>
    </div>
    <h2>MedMARS</h2>
    <p class="project-summary">
      A LangGraph-based medical assistant that routes requests across diagnosis,
      medication consultation, general medical QA, and visual question answering.
    </p>
    <div class="project-metrics" aria-label="Selected project results">
      <p><strong>96.5%</strong><span>Hit@5</span></p>
      <p><strong>0.81</strong><span>MRR</span></p>
      <p><strong>0.845</strong><span>NDCG@5</span></p>
    </div>
    <ul>
      <li>Designed the orchestrator, safety routing, query rewriting, conditional workflows, and multi-turn memory.</li>
      <li>Combined GraphRAG, FAISS vector retrieval, BM25 sparse retrieval, and reciprocal rank fusion over 47K medical records.</li>
      <li>Fine-tuned Mistral-7B and Qwen2-VL-7B with LoRA and built CPU-GPU memory scheduling for stable multi-model inference.</li>
    </ul>
    <div class="project-tags"><span>LangGraph</span><span>GraphRAG</span><span>FAISS</span><span>LoRA</span><span>Qwen2-VL</span></div>
    <a class="project-link" href="https://github.com/Cruise-pp/MedMARS">View on GitHub <span aria-hidden="true">↗</span></a>
  </article>

  <article class="project-card">
    <div class="project-card__topline">
      <p>ByteDance AI Full-Stack Challenge</p>
      <time>May - Jun 2026</time>
    </div>
    <h2>Multimodal E-commerce AI Agent</h2>
    <p class="project-summary">
      A controllable shopping agent with multimodal retrieval, deterministic tool
      orchestration, product comparison, and structured streaming responses.
    </p>
    <div class="project-metrics" aria-label="Selected project results">
      <p><strong>+14%</strong><span>Recall@5</span></p>
      <p><strong>+6%</strong><span>NDCG@5</span></p>
      <p><strong>100%</strong><span>Routing accuracy</span></p>
    </div>
    <ul>
      <li>Built a multimodal RAG pipeline with query understanding, hard filters, hybrid retrieval, post-filtering, and reranking.</li>
      <li>Combined vision-language query generation with multimodal embeddings for image-text retrieval and graceful fallback.</li>
      <li>Designed function-calling orchestration across seven tools and an SSE pipeline for staged, low-latency responses.</li>
    </ul>
    <div class="project-tags"><span>Multimodal RAG</span><span>Function Calling</span><span>Reranking</span><span>SSE</span></div>
    <a class="project-link" href="https://github.com/YufanPeter/E-commerce-AI-Agent">View on GitHub <span aria-hidden="true">↗</span></a>
  </article>
</div>
