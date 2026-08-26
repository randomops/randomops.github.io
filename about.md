---
layout: default
title: "Tentang randomOps"
---

<div class="container container-narrow">
  <!-- About Hero Card -->
  <section class="about-hero-card">
    <div class="about-grid">
      <div>
        <div class="hero-badge">
          <span>🎙️ THE STORY & CULTURE</span>
        </div>
        <h1 style="font-size: 2.25rem; font-weight: 800; margin-bottom: 1rem; line-height: 1.2;">
          Tentang <span class="gradient-text">randomOps</span>
        </h1>
        <p style="font-size: 1.1rem; line-height: 1.6; color: var(--text-secondary); margin-bottom: 1.25rem;">
          Sebuah podcast santai dalam bahasa Indonesia oleh <a href="https://www.robee.id" target="_blank" rel="noopener noreferrer"><strong>Robee</strong></a> bersama kawan-kawan sekantor. Membahas suka duka software engineering, cloud infrastructure, hal-hal teknis yang kadang bikin pusing, dan obrolan rehat ngopi yang sayang kalau menguap begitu saja.
        </p>
        <p style="font-size: 1rem; color: var(--text-secondary); line-height: 1.6; margin-bottom: 0;">
          Diisi oleh sekumpulan orang yang kebetulan berkantor bareng. Daripada obrolan seru di dekat dispenser terbuang sia-sia, mending kami rekam saja jadi podcast. Kualitas audio mungkin apa adanya, tapi insyaAllah ada faedahnya (sedikit).
        </p>
      </div>

      <div class="about-profile-wrapper">
        <img class="about-cover-img" src="{{ site.baseurl }}/{{ site.profile-picture }}" alt="randomOps Studio / Office Team">
        <span class="about-cover-caption">Teman-teman sekantor di balik mic</span>
      </div>
    </div>
  </section>

  <!-- Manifesto Quote -->
  <blockquote style="font-size: 1.15rem; line-height: 1.6; margin: 2.5rem 0; padding: 1.25rem 1.75rem;">
    "Buanglah waktu Anda yang berharga itu untuk mendengarkan podcast kami dengan kualitas sederhana tapi isinya (kadang) bermutu."
  </blockquote>


  <!-- Topics Bento Section -->
  <section style="margin: 3rem 0;">
    <h2 style="font-size: 1.5rem; font-weight: 800; margin-bottom: 1.25rem;">Apa Saja yang Dibahas?</h2>
    
    <div class="topics-bento-grid">
      <div class="topic-card">
        <div class="topic-icon">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M17.5 19H9a7 7 0 1 1 6.71-9h1.79a4.5 4.5 0 1 1 0 9Z"/>
          </svg>
        </div>
        <div class="topic-name">Cloud & Multi-Cloud</div>
        <p class="topic-desc">Pengalaman nyata menggunakan AWS, GCP, on-premise, arsitektur hybrid, dan strategi migrasi.</p>
      </div>

      <div class="topic-card">
        <div class="topic-icon">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 12h-4l-3 9L9 3l-3 9H2"/>
          </svg>
        </div>
        <div class="topic-name">SRE & Incident Response</div>
        <p class="topic-desc">Suka duka on-call, post-mortem blameless, monitoring vs observability, dan mengelola burnout.</p>
      </div>

      <div class="topic-card">
        <div class="topic-icon">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/>
            <circle cx="9" cy="7" r="4"/>
            <path d="M22 21v-2a4 4 0 0 0-3-3.87"/>
            <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
          </svg>
        </div>
        <div class="topic-name">Culture & Hiring</div>
        <p class="topic-desc">Pair interview, remote work, kolaborasi engineering, hingga dinamika tim teknologi.</p>
      </div>

      <div class="topic-card">
        <div class="topic-icon">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m9 12 2 2 4-4"/>
            <path d="M5 7c0-1.1.9-2 2-2h10a2 2 0 0 1 2 2v12H5V7Z"/>
          </svg>
        </div>
        <div class="topic-name">Test Engineering & QA</div>
        <p class="topic-desc">Best practice pengujian otomatis, shift-left testing, dan menjaga reliabilitas rilis kode.</p>
      </div>
    </div>
  </section>

  <!-- Contact & Collaboration Callout -->
  <section class="contact-callout-card">
    <h2 class="contact-title">Tertarik Berdiskusi atau Kolaborasi?</h2>
    <p class="contact-desc">
      Ingin menjadi guest speaker, berdiskusi topik teknis tertentu, mengajak meetup komunitas, atau sekadar menyapa tim randomOps? Pintu kami selalu terbuka.
    </p>
    <div class="contact-links-row">
      <a href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener noreferrer" class="btn-platform btn-primary-platform">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/>
        </svg>
        <span>GitHub Repository</span>
      </a>

      <a href="https://www.robee.id" target="_blank" rel="noopener noreferrer" class="btn-platform">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="10"></circle>
          <line x1="2" y1="12" x2="22" y2="12"></line>
          <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path>
        </svg>
        <span>Website Robee (robee.id)</span>
      </a>
    </div>
  </section>
</div>



