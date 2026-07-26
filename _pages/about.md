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
  <h1 id="home-title">Hi, I’m Yufan.</h1>
  <p class="home-lead">
    I’m an M.S. student in <strong>Electrical and Computer Engineering at UC San Diego</strong>.
    My recent work focuses on <strong>AI Agent Development, Harness Engineering, Self-Evolving Agent</strong>.
    I’m currently developing multi-agent system for root cause analysis @ <strong>Microsoft</strong>.
  </p>
  <div class="home-interests">
    <span>Interests</span>
    <ul>
      <li>Reinforcement Learning</li>
      <li>Agent Systems</li>
      <li>RAG</li>
      <li>Multimodal LLMs</li>
    </ul>
  </div>
  <div class="home-actions">
    <a class="home-button home-button--primary" href="/projects/">View projects <span aria-hidden="true">↗</span></a>
    <a class="home-button" href="mailto:{{ site.author.email }}">Email me</a>
  </div>
</div>

<section class="home-section" id="experience" aria-labelledby="experience-title">
  <div class="section-heading">
    <h2 id="experience-title">Experience</h2>
  </div>
  <article class="experience-item experience-item--detailed">
    <div class="experience-mark"><img src="/assets/images/microsoft-symbol.svg" alt="Microsoft"></div>
    <div class="experience-body">
      <div class="experience-heading">
        <div>
          <p class="experience-meta">Microsoft · App Development Intern</p>
          <h3>Multi-Agent Root Cause Analysis for Cloud Incidents</h3>
        </div>
        <time>Mar 2026 - Present</time>
      </div>
      <ul>
        <li>Developed a hierarchical multi-agent RCA system to automate diagnosis of cloud incidents by correlating change signals, incident context, and historical cases.</li>
        <li>Orchestrated specialized agents to analyze different signals, aggregate root-cause hypotheses, and retrieve relevant incident history using confidence filtering and caching.</li>
        <li>Improved reliability with fallback handling and reviewer validation, reducing problematic RCA samples by about 10% and increasing pass rate by about 30%.</li>
      </ul>
    </div>
  </article>
</section>

<section class="home-section" id="education" aria-labelledby="education-title">
  <div class="section-heading">
    <h2 id="education-title">Education</h2>
  </div>
  <div class="education-list">
    <article class="education-item">
      <div class="education-logo">
        <img src="/assets/images/uc-san-diego-logo.svg" alt="UC San Diego logo">
      </div>
      <div class="education-body">
        <h3>University of California San Diego</h3>
        <p>M.S. in Electrical and Computer Engineering · GPA 3.7/4.0</p>
        <p class="education-detail">Coursework: Deep Generative Models, Natural Language Processing, and Recommender Systems.</p>
      </div>
      <time>2025 - 2027</time>
    </article>
    <article class="education-item">
      <div class="education-logo">
        <img src="/assets/images/xjtlu-logo.svg" alt="Xi’an Jiaotong-Liverpool University logo">
      </div>
      <div class="education-body">
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
    <h2 id="publication-title">Publication</h2>
  </div>
  <a class="publication-item" href="https://doi.org/10.1007/s10462-026-11538-1">
    <div>
      <p>Artificial Intelligence Review · 2026</p>
      <h3>On-Device Large Language Models: A Survey of Model Compression and System Optimization</h3>
    </div>
    <span aria-hidden="true">↗</span>
  </a>
</section>
