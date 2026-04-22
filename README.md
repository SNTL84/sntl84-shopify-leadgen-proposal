<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>desidevloper | Premium Shopify Development & AI Automation</title>
  <meta name="description" content="End-to-end Shopify solutions: custom stores, AI automations, conversion systems, and growth retainers. Launch, scale, dominate.">
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #050505;
      --surface: #0c0c0c;
      --card: #111111;
      --card-hover: #181818;
      --text: #f2efe9;
      --muted: #a3a09b;
      --accent: #9bdc4a;
      --accent-dark: #7cb434;
      --accent-glow: rgba(155, 220, 74, 0.12);
      --border: rgba(255,255,255,0.06);
      --border-accent: rgba(155, 220, 74, 0.35);
      --radius-xl: 24px;
      --radius-lg: 18px;
      --radius-md: 14px;
      --transition: all 0.3s cubic-bezier(0.2, 0.8, 0.4, 1);
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.5;
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    /* grain & glow */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background: radial-gradient(circle at 20% 40%, rgba(155,220,74,0.02) 0%, transparent 60%);
      pointer-events: none;
      z-index: 0;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
      position: relative;
      z-index: 2;
    }

    /* typography */
    h1, h2, h3, .font-display {
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      letter-spacing: -0.02em;
    }

    h1 {
      font-size: clamp(2.8rem, 7vw, 4.8rem);
      line-height: 1.1;
      margin-bottom: 1.25rem;
    }

    h2 {
      font-size: clamp(1.8rem, 4vw, 2.4rem);
      margin: 3rem 0 1.5rem;
      border-left: 4px solid var(--accent);
      padding-left: 1rem;
    }

    .gradient-text {
      background: linear-gradient(135deg, #FFFFFF 30%, var(--accent) 80%);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    /* buttons & badges */
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: var(--accent);
      color: #0a0a0a;
      padding: 0.9rem 1.9rem;
      border-radius: 60px;
      font-weight: 700;
      font-family: 'Syne', sans-serif;
      text-decoration: none;
      transition: var(--transition);
      border: none;
      cursor: pointer;
      font-size: 0.9rem;
    }

    .btn-outline {
      background: transparent;
      border: 1.5px solid var(--accent);
      color: var(--accent);
    }

    .btn-outline:hover {
      background: var(--accent);
      color: #0a0a0a;
      transform: translateY(-2px);
    }

    .btn:hover {
      background: #b0f05c;
      transform: translateY(-3px);
      box-shadow: 0 10px 25px -8px rgba(155,220,74,0.4);
    }

    .badge {
      background: var(--accent-glow);
      border: 1px solid var(--border-accent);
      color: var(--accent);
      border-radius: 40px;
      padding: 0.25rem 0.9rem;
      font-size: 0.7rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      display: inline-block;
      margin-bottom: 1rem;
    }

    /* cards */
    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.8rem;
      transition: var(--transition);
      height: 100%;
      backdrop-filter: blur(2px);
    }

    .card:hover {
      transform: translateY(-6px);
      border-color: var(--border-accent);
      background: var(--card-hover);
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.5);
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 1.8rem;
      margin: 1.5rem 0;
    }

    .stats-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 1.5rem;
      background: rgba(12,12,12,0.7);
      border-radius: var(--radius-xl);
      padding: 2rem 1.5rem;
      margin: 2rem 0;
      border: 1px solid var(--border);
    }

    .stat {
      text-align: center;
      flex: 1;
    }
    .stat-number {
      font-size: 2.2rem;
      font-weight: 800;
      font-family: 'Syne', sans-serif;
      color: var(--accent);
    }

    /* lead form */
    .lead-form {
      background: linear-gradient(145deg, #0e0e0e 0%, #080808 100%);
      border-radius: var(--radius-xl);
      border: 1px solid var(--border-accent);
      padding: 2rem;
      margin: 2rem 0;
    }
    .form-group {
      margin-bottom: 1.2rem;
    }
    input, select, textarea {
      width: 100%;
      background: #121212;
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 0.9rem 1rem;
      color: white;
      font-family: inherit;
      transition: 0.2s;
    }
    input:focus, select:focus, textarea:focus {
      outline: none;
      border-color: var(--accent);
      box-shadow: 0 0 0 3px var(--accent-glow);
    }
    label {
      font-size: 0.8rem;
      font-weight: 500;
      color: var(--muted);
      margin-bottom: 0.3rem;
      display: block;
    }

    /* comparison table */
    .comp-table {
      width: 100%;
      border-collapse: collapse;
      background: var(--surface);
      border-radius: var(--radius-lg);
      overflow: hidden;
    }
    .comp-table th, .comp-table td {
      padding: 1rem 0.8rem;
      text-align: left;
      border-bottom: 1px solid var(--border);
    }
    .comp-table th {
      font-family: 'Syne', sans-serif;
      color: var(--accent);
      font-weight: 600;
    }
    .check { color: var(--accent); font-weight: bold; font-size: 1.2rem; }
    .dash { color: #4a4a4a; }

    /* testimonial */
    .testimonial-card {
      background: rgba(17,17,17,0.8);
      border-radius: 24px;
      padding: 1.5rem;
      border: 1px solid var(--border);
      font-style: normal;
    }

    /* floating whatsapp */
    .float-wa {
      position: fixed;
      bottom: 28px;
      right: 28px;
      background: #25D366;
      width: 58px;
      height: 58px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 5px 20px rgba(0,0,0,0.4);
      transition: transform 0.2s;
      z-index: 99;
    }
    .float-wa:hover {
      transform: scale(1.05);
    }
    .float-wa img {
      width: 32px;
      filter: brightness(0) invert(1);
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(25px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate {
      animation: fadeUp 0.6s ease forwards;
    }
    .reveal {
      opacity: 0;
      animation: fadeUp 0.5s ease forwards;
    }
    footer {
      border-top: 1px solid var(--border);
      margin-top: 4rem;
      padding: 2rem 0;
      text-align: center;
      color: var(--muted);
    }
    @media (max-width: 800px) {
      .container { padding: 0 20px; }
      .stats-grid { flex-direction: column; align-items: center; }
      .grid-3 { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<div class="container">
  <!-- Header -->
  <div class="reveal" style="margin-top: 2rem;">
    <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem; margin-bottom: 2rem;">
      <div class="badge" style="margin-bottom: 0;">⚡ desidevloper × AI commerce</div>
      <div style="display: flex; gap: 1rem;">
        <a href="https://wa.me/919727413309" style="color: var(--muted); text-decoration: none; font-size: 0.85rem;">📞 +91 97274 13309</a>
        <span style="color: var(--muted);">|</span>
        <a href="#lead-form" style="color: var(--accent); text-decoration: none; font-size: 0.85rem; font-weight: 500;">📩 Request quote</a>
      </div>
    </div>
    <h1>Build. Automate.<br><span class="gradient-text">Dominate Shopify.</span></h1>
    <p style="font-size: 1.1rem; max-width: 700px; color: var(--muted); margin-bottom: 2rem;">End-to-end Shopify development, AI automation & growth systems — built for D2C brands ready to scale revenue.</p>
    <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
      <a href="#packages" class="btn">🚀 Explore packages</a>
      <a href="#lead-form" class="btn btn-outline">🎯 Free consultation →</a>
    </div>
  </div>

  <!-- stats -->
  <div class="stats-grid reveal">
    <div class="stat"><div class="stat-number">50+</div><div>Stores launched</div></div>
    <div class="stat"><div class="stat-number">98%</div><div>Client retention</div></div>
    <div class="stat"><div class="stat-number">4.9/5</div><div>Google rating</div></div>
    <div class="stat"><div class="stat-number">40%</div><div>Avg. revenue lift</div></div>
  </div>

  <!-- Packages Section -->
  <h2 id="packages">⚡ Service packages <span style="font-size: 1rem; font-weight: normal; color: var(--muted);"> — tailored to your growth stage</span></h2>
  <div class="grid-3">
    <!-- Starter -->
    <div class="card reveal">
      <span class="badge">LAUNCH READY</span>
      <div class="price" style="font-family: 'Syne'; font-size: 2rem; font-weight: 800;">₹29,999<span style="font-size: 0.9rem;"> / project</span></div>
      <p style="margin: 0.5rem 0 1rem;">MVP stores, local brands going online — clean, fast & conversion-focused.</p>
      <ul style="margin-bottom: 1.2rem; list-style: none; padding-left: 0;">
        <li style="margin-bottom: 0.4rem;">✓ Theme setup + 30 products</li>
        <li style="margin-bottom: 0.4rem;">✓ Payment & basic shipping</li>
        <li style="margin-bottom: 0.4rem;">✓ Meta Pixel + GA4 setup</li>
        <li style="margin-bottom: 0.4rem;">✓ Mobile-optimized, 7-10 days</li>
      </ul>
      <a href="https://wa.me/919727413309?text=Hi%2C%20I'm%20interested%20in%20your%20STARTER%20Shopify%20package%20(%C2%B929%2C999).%20Please%20share%20details." class="btn" style="background: #2c2c2c; color: white; width: 100%; justify-content: center;">Get quote →</a>
    </div>
    <!-- Growth (Most popular) -->
    <div class="card reveal" style="border: 1px solid var(--accent); box-shadow: 0 0 18px rgba(155,220,74,0.15);">
      <span class="badge" style="background: var(--accent); color: #0a0a0a;">⭐ MOST POPULAR</span>
      <div class="price" style="font-family: 'Syne'; font-size: 2rem; font-weight: 800;">₹49,999<span style="font-size: 0.9rem;"> / project</span></div>
      <p style="margin: 0.5rem 0 1rem;">D2C brands, conversion-first custom store + email & marketing automation.</p>
      <ul style="margin-bottom: 1.2rem; list-style: none; padding-left: 0;">
        <li>✓ Custom theme + 100 products</li>
        <li>✓ Klaviyo full flows (abandoned, welcome, post)</li>
        <li>✓ Reviews (Judge.me) + loyalty (Smile.io)</li>
        <li>✓ Shiprocket / OMS, CAPI + GMC</li>
      </ul>
      <a href="https://wa.me/919727413309?text=Hi%2C%20I'm%20interested%20in%20the%20GROWTH%20Shopify%20package%20(%C2%B779%2C999).%20Let's%20discuss%20my%20store." class="btn" style="width: 100%; justify-content: center;">Start scaling →</a>
    </div>
    <!-- Scale -->
    <div class="card reveal">
      <span class="badge">ENTERPRISE / SCALE</span>
      <div class="price" style="font-family: 'Syne'; font-size: 2rem; font-weight: 800;">₹99,999+<span style="font-size: 0.9rem;"> / custom</span></div>
      <p style="margin: 0.5rem 0 1rem;">High-volume, Shopify Plus, headless, custom apps, AI automations & ERP sync.</p>
      <ul style="margin-bottom: 1.2rem; list-style: none; padding-left: 0;">
        <li>✓ Custom Shopify App (Node.js / Remix)</li>
        <li>✓ n8n automations + AI product descriptions</li>
        <li>✓ Headless / Hydrogen storefront</li>
        <li>✓ Advanced analytics + server-side tracking</li>
      </ul>
      <a href="https://wa.me/919727413309?text=Hi%2C%20I%20need%20a%20SCALE%20solution%20for%20Shopify%20(enterprise).%20Let's%20talk%20about%20custom%20features." class="btn btn-outline" style="width: 100%; justify-content: center;">Talk to expert →</a>
    </div>
  </div>

  <!-- monthly retainers -->
  <h2>🔄 Monthly retainers & support</h2>
  <div class="grid-3">
    <div class="card"><h3 style="color: var(--accent); margin-bottom: 0.5rem;">🔧 Store Management</h3><div style="font-size: 1.8rem; font-weight: 700;">₹19,999<span style="font-size: 0.9rem;">/mo</span></div><ul style="margin-top: 1rem;"><li>15 update requests/month</li><li>Product uploads, collections, banners</li><li>Performance & app health</li></ul></div>
    <div class="card"><h3 style="color: var(--accent); margin-bottom: 0.5rem;">📈 Growth Retainer</h3><div style="font-size: 1.8rem; font-weight: 700;">₹34,999<span style="font-size: 0.9rem;">/mo</span></div><ul style="margin-top: 1rem;"><li>CRO + A/B testing, heatmaps</li><li>Klaviyo flow optimization</li><li>Server-side tracking + monthly audit</li></ul></div>
    <div class="card"><h3 style="color: var(--accent); margin-bottom: 0.5rem;">🤖 AI Automation Add‑on</h3><div style="font-size: 1.8rem; font-weight: 700;">₹24,999<span style="font-size: 0.9rem;">/mo</span></div><ul style="margin-top: 1rem;"><li>n8n workflows & automation maintenance</li><li>WhatsApp order notifications</li><li>AI product desc & chatbot training</li></ul></div>
  </div>

  <!-- why choose + testimonials -->
  <h2>✨ Why brands choose desidevloper</h2>
  <div class="grid-3">
    <div class="card"><h3>🎯 Shopify-first strategy</h3><p>We don't just build stores — we engineer revenue engines with deep Shopify ecosystem knowledge.</p></div>
    <div class="card"><h3>⚡ AI & automation core</h3><p>n8n, Make, Claude API: we automate operations, reduce manual work, and boost margins.</p></div>
    <div class="card"><h3>📊 Transparent process</h3><p>Slack updates, Notion roadmap, and post-launch training — you're never left guessing.</p></div>
  </div>

  <!-- Testimonials -->
  <div class="grid-3" style="margin-top: 1rem;">
    <div class="testimonial-card"><p style="color: var(--accent);">“Store speed increased by 50% and sales up 35% in 3 months. Klaviyo flows are pure gold.”</p><p style="margin-top: 0.8rem;">— Rhea Mehta, Organic D2C brand</p></div>
    <div class="testimonial-card"><p style="color: var(--accent);">“The team built a custom Shopify app for our subscription box — saved us thousands in manual work. Highly recommend!”</p><p style="margin-top: 0.8rem;">— Aarav Singh, Wellness Co.</p></div>
    <div class="testimonial-card"><p style="color: var(--accent);">“n8n automation + WhatsApp notifications changed our customer support game. Absolute legends.”</p><p style="margin-top: 0.8rem;">— Nikita Shah, Fashion label</p></div>
  </div>

  <!-- Comparison table -->
  <h2>📋 Package comparison</h2>
  <div style="overflow-x: auto;">
    <table class="comp-table">
      <thead><tr><th>Feature</th><th>Starter</th><th>Growth</th><th>Scale</th></tr></thead>
      <tbody>
        <tr><td>Custom theme sections</td><td class="dash">—</td><td class="check">✓</td><td class="check">✓</td></tr>
        <tr><td>Klaviyo email flows</td><td class="dash">—</td><td class="check">Full setup</td><td class="check">Advanced + A/B</td></tr>
        <tr><td>Meta CAPI + GA4</td><td>Basic</td><td class="check">✓</td><td class="check">Server-side + GTM</td></tr>
        <tr><td>Loyalty / Reviews</td><td class="dash">—</td><td class="check">Smile + Judge.me</td><td class="check">Custom</td></tr>
        <tr><td>Custom Shopify App</td><td class="dash">—</td><td class="dash">—</td><td class="check">Node/Remix</td></tr>
        <tr><td>AI automation (n8n/API)</td><td class="dash">—</td><td class="dash">—</td><td class="check">Full integration</td></tr>
        <tr><td>Post-launch support</td><td>14 days</td><td>30 days</td><td>60 days + Slack</td></tr>
      </tbody>
    </table>
  </div>

  <!-- LEAD GENERATION FORM (HIGH CONVERSION) -->
  <div id="lead-form" class="lead-form reveal">
    <div style="text-align: center; margin-bottom: 1rem;">
      <span class="badge" style="background: var(--accent); color: #000;">🎯 free project estimate</span>
      <h3 style="font-size: 1.8rem; margin: 0.5rem 0;">Get a custom quote + audit</h3>
      <p style="color: var(--muted);">Share your vision — we’ll reply within 4 hours with a tailored roadmap & pricing.</p>
    </div>
    <form id="leadForm">
      <div class="form-group">
        <label>Full name *</label>
        <input type="text" id="name" required placeholder="e.g., Priya Sharma">
      </div>
      <div class="form-group">
        <label>Email address *</label>
        <input type="email" id="email" required placeholder="hello@brand.com">
      </div>
      <div class="form-group">
        <label>Store URL (if any)</label>
        <input type="text" id="storeUrl" placeholder="yourstore.myshopify.com or custom domain">
      </div>
      <div class="form-group">
        <label>Project type *</label>
        <select id="projectType">
          <option value="Starter (₹29,999)">Starter (Launch ready)</option>
          <option value="Growth (₹79,999)">Growth (Conversion & Klaviyo)</option>
          <option value="Scale (Custom 1.5L+)">Scale (Enterprise / App / AI)</option>
          <option value="Monthly Retainer">Monthly Retainer / Support</option>
          <option value="Other / Consultation">Other / Consultation</option>
        </select>
      </div>
      <div class="form-group">
        <label>Tell us about your brand / requirements</label>
        <textarea rows="3" id="message" placeholder="e.g., need a fashion store with subscription, WhatsApp automation, etc."></textarea>
      </div>
      <div style="display: flex; gap: 1rem; flex-wrap: wrap; justify-content: space-between; align-items: center;">
        <button type="submit" class="btn" style="background: var(--accent); color: black;">📲 Send & discuss on WhatsApp →</button>
        <p style="font-size: 0.7rem; color: #5a5a5a;">We respect privacy. No spam, ever.</p>
      </div>
    </form>
  </div>

  <!-- CTA Banner + final -->
  <div style="background: radial-gradient(ellipse at 70% 30%, #1a2a0a 0%, #030303 100%); border-radius: 32px; padding: 2.5rem; text-align: center; margin: 2rem 0; border: 1px solid var(--border-accent);">
    <h3 style="font-size: 1.7rem;">🚀 Ready to dominate your niche?</h3>
    <p style="max-width: 550px; margin: 1rem auto;">Let’s build a Shopify store that converts, automates, and scales beyond expectations.</p>
    <a href="https://wa.me/919727413309?text=Hey!%20I%20saw%20your%20Shopify%20proposal%20and%20want%20to%20discuss%20my%20project." class="btn" style="background: white; color: black;">📱 Chat with founder directly →</a>
  </div>

  <footer>
    <p>© 2026 <strong style="color: var(--accent);">desidevloper</strong> · SNTL 84 · <strong>desidevloper.com</strong></p>
    <p style="margin-top: 0.4rem;">Shopify Development · AI Workflows · CRO · Growth Systems</p>
    <p>📞 WhatsApp: <strong>+91 97274 13309</strong> | GitHub: SNTL84 | LinkedIn: sntl2784</p>
    <p style="font-size: 0.7rem;">⭐ 100% project delivery guarantee | 30+ Shopify Partners network</p>
  </footer>
</div>

<!-- Floating WhatsApp -->
<a href="https://wa.me/919727413309?text=Hi%20desidevloper%2C%20I%20need%20Shopify%20help!" class="float-wa" target="_blank" rel="noopener">
  <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="white"><path d="M.057 24l1.687-6.163C.802 16.063.492 14.121.492 12.164.492 5.431 5.79.132 12.523.132c6.732 0 12.03 5.299 12.03 12.03 0 6.732-5.298 12.031-12.03 12.031-1.956 0-3.899-.31-5.723-.885L.057 24zM12.523 1.88c-5.68 0-10.294 4.615-10.294 10.294 0 1.839.496 3.629 1.429 5.187l-.979 3.576 3.66-.96c1.512.853 3.218 1.3 5.003 1.3 5.68 0 10.295-4.615 10.295-10.295 0-5.679-4.615-10.294-10.295-10.294zM17.88 14.47c-.215.604-1.267 1.106-1.735 1.156-.463.05-.891.076-1.432-.288-.727-.491-2.865-1.13-3.936-2.405-.915-1.09-1.224-2.405-1.347-3.103-.064-.363.054-.707.282-.961.194-.215.433-.358.542-.558.11-.2.146-.335.219-.56.073-.226.036-.424-.018-.583-.055-.159-.494-1.192-.677-1.632-.178-.43-.36-.372-.497-.38-.128-.006-.273-.008-.418-.008-.195 0-.511.073-.778.365-.267.292-1.02.997-1.02 2.432 0 1.435 1.045 2.822 1.191 3.017.146.195 2.057 3.14 4.984 4.403.697.3 1.24.48 1.665.615.699.222 1.335.19 1.837.115.562-.084 1.267-.518 1.446-1.018.18-.5.18-.928.126-1.018-.054-.09-.198-.145-.414-.253-.216-.108-1.276-.63-1.473-.703-.198-.073-.342-.108-.486.108-.144.216-.558.703-.684.847-.126.144-.252.163-.468.054s-.918-.338-1.748-1.078c-.646-.576-1.083-1.287-1.209-1.504-.126-.217-.013-.335.095-.443.097-.098.216-.254.324-.382.108-.128.144-.216.216-.36.072-.144.036-.27-.018-.378-.054-.108-.486-1.172-.666-1.604-.176-.42-.355-.363-.485-.372-.126-.008-.27-.008-.414-.008-.144 0-.378.054-.576.27-.198.216-.756.74-.756 1.802 0 1.062.773 2.088.881 2.233.108.144 1.523 2.324 3.689 3.258.515.223.917.357 1.231.457.517.164.988.14 1.361.085.415-.062 1.277-.523 1.458-1.027.18-.504.18-.936.126-1.026-.054-.09-.198-.145-.414-.253z"/></svg>
</a>

<script>
  // Lead form submission -> redirect to WhatsApp with structured lead data
  const form = document.getElementById('leadForm');
  if(form) {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const storeUrl = document.getElementById('storeUrl').value.trim();
      const projectType = document.getElementById('projectType').value;
      const message = document.getElementById('message').value.trim();

      if(!name || !email) {
        alert("Please provide your name and email to get a free quote.");
        return;
      }
      if(!email.includes('@')) {
        alert("Enter a valid email address.");
        return;
      }

      // Build WhatsApp text
      let waText = `🚀 *New Lead from desidevloper.com*%0A%0A`;
      waText += `*Name:* ${encodeURIComponent(name)}%0A`;
      waText += `*Email:* ${encodeURIComponent(email)}%0A`;
      if(storeUrl) waText += `*Store URL:* ${encodeURIComponent(storeUrl)}%0A`;
      waText += `*Project:* ${encodeURIComponent(projectType)}%0A`;
      if(message) waText += `*Requirements:* ${encodeURIComponent(message)}%0A`;
      waText += `%0A👉 Please reply with next steps.`;

      const whatsappURL = `https://wa.me/919727413309?text=${waText}`;
      window.open(whatsappURL, '_blank');
      alert("✔️ Thank you! We'll redirect you to WhatsApp to complete your request. One of our experts will reply within 4 hours.");
      form.reset();
    });
  }

  // optional: smooth scroll for anchor links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const targetId = this.getAttribute('href');
      if(targetId === "#" || targetId === "") return;
      const target = document.querySelector(targetId);
      if(target) {
        e.preventDefault();
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
</script>
</body>
</html>
