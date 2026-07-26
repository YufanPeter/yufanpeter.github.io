---
permalink: /projects/cartpilot/
layout: portfolio
title: "CartPilot - Yufan Shi"
description: "Case study of CartPilot, a controlled multimodal shopping agent with hybrid retrieval and deterministic tools."
---

<header class="site-header" data-header>
  <a class="wordmark" href="{{ site.baseurl }}/" aria-label="Yufan Shi, home">
    <span class="wordmark__monogram">YS</span>
    <span class="wordmark__meta">AI Systems<br>Engineer</span>
  </a>
  <nav class="site-nav" aria-label="Project navigation">
    <a href="{{ site.baseurl }}/#work">Selected work</a>
    <a href="https://github.com/YufanPeter/E-commerce-AI-Agent" target="_blank" rel="noopener">GitHub ↗</a>
  </nav>
  <a class="header-contact" href="{{ site.baseurl }}/#contact">Let's talk <span aria-hidden="true">↗</span></a>
</header>

<main id="main" class="case-study">
  <section class="case-hero" id="top">
    <a class="case-back" href="{{ site.baseurl }}/#work">← Back to selected work</a>
    <div class="case-award case-award--hero">
      <img src="{{ site.baseurl }}/images/bytedance.svg" alt="ByteDance">
      <div><strong>BYTEDANCE PROJECT ACHIEVEMENT AWARD</strong><span>TOP 12% · 9 OUT OF 80</span></div>
    </div>
    <div class="case-hero__grid">
      <div>
        <p class="case-kicker">PROJECT CASE STUDY / 02</p>
        <h1>Multimodal<br>E-commerce Agent</h1>
        <p class="case-hero__lede">A controlled shopping agent that accepts text, voice, and product images, then combines deterministic tools with hybrid retrieval and structured streaming output.</p>
      </div>
      <div class="case-hero__aside">
        <span>ROLE</span><strong>AI full-stack engineering</strong>
        <span>CLIENT</span><strong>SwiftUI · iOS 17+</strong>
        <span>BACKEND</span><strong>FastAPI · Chroma · SQLite · SSE</strong>
      </div>
    </div>
    <div class="case-actions">
      <a class="button button--dark" href="https://github.com/YufanPeter/E-commerce-AI-Agent" target="_blank" rel="noopener">View repository ↗</a>
      <a class="button button--line" href="#architecture">Explore architecture ↓</a>
    </div>
  </section>

  <figure class="case-figure" id="architecture">
    <a href="{{ site.baseurl }}/images/cartpilot-handdrawn-pipeline-v4.png" target="_blank" rel="noopener">
      <img src="{{ site.baseurl }}/images/cartpilot-handdrawn-pipeline-v4.png" alt="CartPilot controlled shopping-agent pipeline">
    </a>
    <figcaption><span>CODE-VERIFIED PIPELINE</span><span>CLICK TO VIEW FULL SIZE ↗</span></figcaption>
  </figure>

  <section class="case-metrics" aria-label="CartPilot retrieval results">
    <div><strong>+14%</strong><span>Recall@5</span></div>
    <div><strong>+6%</strong><span>NDCG@5</span></div>
    <div><strong>100%</strong><span>Structured Recall@10</span></div>
    <div><strong>7</strong><span>Deterministic tools</span></div>
  </section>

  <section class="case-section">
    <div class="case-section__label">01 / Challenge</div>
    <div class="case-section__body">
      <h2>Conversational shopping still needs deterministic control.</h2>
      <p>Users describe products through incomplete text, voice, follow-up constraints, or images. The system must understand that intent without allowing generated prose to invent prices, stock, product attributes, or cart state.</p>
    </div>
  </section>

  <section class="case-section">
    <div class="case-section__label">02 / Agent</div>
    <div class="case-section__body">
      <h2>Router → tool → structured result → composer.</h2>
      <div class="case-tool-list">
        <span>recommend</span><span>refine</span><span>compare</span><span>product_detail</span><span>cart</span><span>clarify</span><span>fallback</span>
      </div>
      <p>The function-calling router selects one registered tool and rewrites the request using recent context. Tools execute deterministically and return a structured <code>ToolResult</code>; the composer controls wording but never mutates the cart or creates product facts.</p>
      <p>Image requests follow a separate path: VLM query extraction bypasses the router and enters recommendation directly, with optional user text merged into the retrieval query.</p>
    </div>
  </section>

  <section class="case-section">
    <div class="case-section__label">03 / Retrieval</div>
    <div class="case-section__body">
      <h2>Constraints first, relevance second.</h2>
      <ol class="case-steps">
        <li><span>01</span><div><strong>Understand</strong><p>Extract category, price, brands, exclusions, soft preferences, and a standalone retrieval query.</p></div></li>
        <li><span>02</span><div><strong>Filter</strong><p>Apply structured Chroma filters, negative constraints, and true SKU price ranges before ranking.</p></div></li>
        <li><span>03</span><div><strong>Retrieve</strong><p>Combine Chroma vector order with BM25 lexical ranking through reciprocal-rank fusion.</p></div></li>
        <li><span>04</span><div><strong>Rerank</strong><p>Optionally rerank evidence, then aggregate chunks into product-level results.</p></div></li>
        <li><span>05</span><div><strong>Visual fusion</strong><p>For image search, fuse 60% text relevance with 40% image similarity.</p></div></li>
      </ol>
    </div>
  </section>

  <section class="case-section">
    <div class="case-section__label">04 / Delivery</div>
    <div class="case-section__body">
      <h2>Facts remain inspectable from retrieval to UI.</h2>
      <ul class="case-list">
        <li><strong>SQLite source of truth.</strong> Product identity, SKUs, price, stock, cart state, and preferences come from deterministic storage.</li>
        <li><strong>Session working memory.</strong> Last hits, constraints, focused products, and pending clarification state support multi-turn references.</li>
        <li><strong>Structured streaming.</strong> FastAPI emits session, status, metadata, tool results, generated tokens, memory updates, and completion over SSE.</li>
        <li><strong>SwiftUI client.</strong> Structured product cards render immediately while the narrative continues streaming.</li>
      </ul>
    </div>
  </section>

  <nav class="case-next" aria-label="Project navigation">
    <span>PREVIOUS CASE STUDY</span>
    <a href="{{ site.baseurl }}/projects/medmars/">MedMARS <span aria-hidden="true">←</span></a>
  </nav>
</main>

<footer class="site-footer">
  <span>© <span data-year>2026</span> YUFAN SHI</span>
  <a href="{{ site.baseurl }}/#work">ALL PROJECTS ↑</a>
</footer>
