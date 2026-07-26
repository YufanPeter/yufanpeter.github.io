---
permalink: /
title: "Yufan Shi"
show_title: false
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div class="home-intro">
  <p class="home-kicker"><span aria-hidden="true"></span>AI systems · agents · retrieval</p>
  <h1 id="home-title">Hi, I’m Yufan.</h1>
  <p class="home-lead">
    I’m an M.S. student in <strong>Electrical and Computer Engineering at UC San Diego</strong>.
    My work focuses on reliable AI agents, retrieval-augmented generation, and multimodal
    systems. I’m currently developing multi-agent tools for cloud incident analysis at
    <strong>Microsoft</strong>.
  </p>
  <div class="home-actions">
    <a class="home-button home-button--primary" href="/projects/">View projects <span aria-hidden="true">↗</span></a>
    <a class="home-button" href="mailto:{{ site.author.email }}">Email me</a>
  </div>
</div>

<section class="home-section" id="research" aria-labelledby="focus-title">
  <div class="section-heading">
    <p>Research</p>
    <h2 id="focus-title">What I’m exploring</h2>
  </div>
  <div class="focus-grid focus-grid--three">
    <article class="focus-card">
      <span>01</span>
      <h3>Agentic AI systems</h3>
      <p>Multi-agent orchestration, tool use, workflow design, and reliable reasoning for complex tasks.</p>
    </article>
    <article class="focus-card">
      <span>02</span>
      <h3>Retrieval and knowledge</h3>
      <p>Hybrid RAG, GraphRAG, reranking, memory, and evaluation for grounded language-model applications.</p>
    </article>
    <article class="focus-card">
      <span>03</span>
      <h3>Multimodal and efficient LLMs</h3>
      <p>Vision-language systems, parameter-efficient fine-tuning, and practical on-device inference.</p>
    </article>
  </div>
</section>

<section class="home-section" id="experience" aria-labelledby="experience-title">
  <div class="section-heading">
    <p>Experience</p>
    <h2 id="experience-title">Microsoft</h2>
  </div>
  <article class="experience-item experience-item--detailed">
    <div class="experience-mark" aria-hidden="true">M</div>
    <div class="experience-body">
      <div class="experience-heading">
        <div>
          <p class="experience-meta">AI Application Development Intern</p>
          <h3>Multi-agent root cause analysis for cloud incidents</h3>
        </div>
        <time>Mar 2026 - Present</time>
      </div>
      <ul>
        <li>Developed a hierarchical multi-agent RCA system that reasons over change signals, incident context, and historical cases.</li>
        <li>Built a retrieval-augmented knowledge layer with vector search, confidence filtering, and caching to improve inference efficiency.</li>
        <li>Introduced fallback and reviewer mechanisms, reducing problematic RCA samples by about 10% and improving pass rate by about 30%.</li>
      </ul>
    </div>
  </article>
</section>

<section class="home-section" id="education" aria-labelledby="education-title">
  <div class="section-heading">
    <p>Education</p>
    <h2 id="education-title">Academic background</h2>
  </div>
  <div class="education-list">
    <article class="education-item">
      <div>
        <h3>University of California San Diego</h3>
        <p>M.S. in Electrical and Computer Engineering · GPA 3.7/4.0</p>
        <p class="education-detail">Coursework: Deep Generative Models, Natural Language Processing, and Recommender Systems.</p>
      </div>
      <time>2025 - 2027</time>
    </article>
    <article class="education-item">
      <div>
        <h3>Xi’an Jiaotong-Liverpool University</h3>
        <p>B.S. in Computer Science · GPA 3.76/4.0</p>
        <p class="education-detail">Academic Achievement Scholarship, School of Advanced Technology (Top 10%).</p>
      </div>
      <time>2021 - 2025</time>
    </article>
  </div>
</section>

<section class="home-section" id="publication" aria-labelledby="publication-title">
  <div class="section-heading">
    <p>Publication</p>
    <h2 id="publication-title">Selected writing</h2>
  </div>
  <a class="publication-item" href="https://doi.org/10.1007/s10462-026-11538-1">
    <div>
      <p>Artificial Intelligence Review · 2026</p>
      <h3>On-Device Large Language Models: A Survey of Model Compression and System Optimization</h3>
    </div>
    <span aria-hidden="true">↗</span>
  </a>
</section>

<section class="home-section home-section--skills" aria-labelledby="skills-title">
  <div class="section-heading">
    <p>Toolkit</p>
    <h2 id="skills-title">Technologies I work with</h2>
  </div>
  <div class="skill-groups">
    <p><strong>Languages</strong><span>Python, Java, C++, C, SQL, Git</span></p>
    <p><strong>Agents &amp; retrieval</strong><span>LangGraph, LangChain, MCP, GraphRAG, Vector RAG, BM25, ChromaDB, FAISS</span></p>
    <p><strong>Machine learning</strong><span>PyTorch, PEFT / LoRA, Transformers, NLP, multimodal LLMs</span></p>
  </div>
</section>
