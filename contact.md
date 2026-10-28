---
title: "Contact"
layout: single
permalink: /contact/
classes: wide
author_profile: false
---

<style>
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.75rem;
    margin: 2rem 0;
  }
  @media (max-width: 900px) {
    .contact-grid { grid-template-columns: 1fr; }
  }

  .contact-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-top: 4px solid #009639;
    border-radius: 10px;
    padding: 2rem 1.75rem;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-width: 0;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .contact-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 20px rgba(0, 150, 57, 0.12);
  }

  .contact-icon {
    width: 3.2rem;
    height: 3.2rem;
    border-radius: 50%;
    background: #e6f5ec;
    color: #009639;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.3rem;
    margin-bottom: 1rem;
  }

  .contact-card h3 {
    margin: 0 0 0.75rem 0;
    font-size: 1.3rem;
    color: #1f2937;
    overflow-wrap: anywhere;
  }

  .contact-card p {
    font-size: 0.95rem;
    line-height: 1.6;
    color: #4b5563;
    margin-bottom: 1rem;
  }

  .contact-card ul {
    font-size: 0.9rem;
    color: #4b5563;
    padding-left: 1.2rem;
    margin-bottom: 1.5rem;
  }

  .contact-card .note {
    font-size: 0.85rem;
    color: #6b7280;
  }

  .contact-btn {
    display: block;
    text-align: center;
    padding: 0.8rem 1.2rem;
    border-radius: 6px;
    background: #009639;
    color: #ffffff !important;
    font-weight: 600;
    font-size: 0.95rem;
    text-decoration: none !important;
    margin-top: 1rem;
    border: 2px solid #009639;
    transition: all 0.2s ease;
  }
  .contact-btn:hover {
    background: #007a2f;
    border-color: #007a2f;
  }
  .contact-btn--outline {
    background: transparent;
    color: #009639 !important;
  }
  .contact-btn--outline:hover {
    background: #009639;
    color: #ffffff !important;
  }

  .social-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0;
  }
  .social-card {
    display: flex;
    align-items: center;
    gap: 0.85rem;
    padding: 1rem 1.25rem;
    border-radius: 6px;
    background: #f9fafb;
    border: 1px solid #e5e7eb;
    text-decoration: none !important;
    color: #374151 !important;
    transition: all 0.2s ease-in-out;
  }
  .social-card:hover {
    border-color: #009639;
    background: #ffffff;
    box-shadow: 0 2px 6px rgba(0, 150, 57, 0.1);
  }
  .social-card i { font-size: 1.3rem; color: #009639; }
  .social-card .name { font-weight: 600; font-size: 0.95rem; }
  .social-card .desc { font-size: 0.8rem; color: #6b7280; }
</style>

Whether you would like to present your research, receive seminar announcements, or get in touch with the team, there are several ways to engage with <em>Fusion EP Talks</em>.

<div class="contact-grid">

  <!-- Call for Speakers -->
  <div class="contact-card">
    <div>
      <div class="contact-icon"><i class="fas fa-microphone-alt"></i></div>
      <h3>Call for Speakers</h3>
      <p>
        Are you conducting research in magnetic confinement fusion, plasma diagnostics, theoretical physics, or engineering? We welcome proposals from master's students, PhD researchers, postdocs, and senior scientists worldwide.
      </p>
      <ul>
        <li>Format: 40–45 min talk + 15–20 min live Q&amp;A</li>
        <li>Open to all plasma and fusion subfields</li>
      </ul>
    </div>
    <a href="https://forms.gle/cwShFC7zUmn12q2R6" target="_blank" rel="noopener noreferrer" class="contact-btn">Propose a Talk</a>
  </div>

  <!-- Seminar Announcements -->
  <div class="contact-card">
    <div>
      <div class="contact-icon"><i class="fas fa-paper-plane"></i></div>
      <h3>Seminar Announcements</h3>
      <p>
        Subscribe to our mailing list to receive email notifications, abstracts, and direct Zoom links a few days before each scheduled talk.
      </p>
      <p class="note"><em>No spam. Only seminar dates and session announcements.</em></p>
    </div>
    <a href="#" target="_blank" rel="noopener noreferrer" class="contact-btn">Subscribe to Alerts</a>
  </div>

  <!-- General Inquiries -->
  <div class="contact-card">
    <div>
      <div class="contact-icon"><i class="fas fa-envelope"></i></div>
      <h3>General Inquiries</h3>
      <p>
        For administrative questions, institutional partnerships, or certificate validation, get in touch directly with our coordinating team.
      </p>
      <p class="note"><em>Inquiries are typically answered within 2–3 business days.</em></p>
    </div>
    <a href="mailto:contact@example.com" class="contact-btn contact-btn--outline">Send an Email</a>
  </div>

</div>

---

## Community & Social Channels

Follow our channels for slide releases, full-length recording uploads, and speaker spotlights:

<div class="social-grid">

  <a href="https://www.linkedin.com/company/fusion-ep-talks/" target="_blank" rel="noopener noreferrer" class="social-card">
    <i class="fab fa-linkedin"></i>
    <div>
      <div class="name">LinkedIn</div>
      <div class="desc">Announcements & network</div>
    </div>
  </a>

  <a href="https://www.youtube.com/@fusioneptalks" target="_blank" rel="noopener noreferrer" class="social-card">
    <i class="fab fa-youtube"></i>
    <div>
      <div class="name">YouTube</div>
      <div class="desc">Full seminar recordings</div>
    </div>
  </a>

  <a href="https://www.facebook.com/fusioneptalks" target="_blank" rel="noopener noreferrer" class="social-card">
    <i class="fab fa-facebook"></i>
    <div>
      <div class="name">Facebook</div>
      <div class="desc">Community updates</div>
    </div>
  </a>

  <a href="#" class="social-card">
    <i class="fab fa-x-twitter"></i>
    <div>
      <div class="name">X (Twitter)</div>
      <div class="desc">Coming soon</div>
    </div>
  </a>

  <a href="#" class="social-card">
    <i class="fab fa-instagram"></i>
    <div>
      <div class="name">Instagram</div>
      <div class="desc">Coming soon</div>
    </div>
  </a>

</div>
