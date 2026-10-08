# MarkBuilder Digital Marketplace 🛍️

> **Official Storefront:** [markbuilder.in](https://markbuilder.in) / [markbuilder.in/store](https://markbuilder.in/store)  
> **Brand:** MarkBuilder Official  
> **Founder & Author:** Priyanshu Mishra ([@markbuilder_in](https://x.com/markbuilder_in))  
> **Support:** support@markbuilder.in  

An Etsy/Amazon-grade, high-conversion responsive digital publication marketplace built with lightweight modern web technologies. Optimized for ultra-fast mobile loading, zero-glitch order delivery, and direct friction-free checkout.

---

## 🔒 MANDATORY POLICY: Future Product Standard Operating Procedure (SOP)
> **Permanent Rule:** *Har naye product me Thank You & Auto-Download Delivery Page (`/download/<token>`) lagana mandatory hai.* Zero exceptions.

Har naye product (Product #5, #6, etc.) ke launch ke waqt ye exact 6-step checklist follow hogi:

1. **Cryptographic PDF Hashing:**
   - PDF filename plain ya guessable nahi hoga (e.g. `playbook.pdf` ❌).
   - Filename hamesha 14-hex cryptographic hash ke sath hoga: `<slug>-mb-<14hex>.pdf` (e.g. `vibe-playbook-mb-ffef44be315c8f.pdf` ✅).
   - Isse direct URL guessing ya scraping impossible ho jati hai.

2. **Universal Delivery Engine Registration (`index.html`):**
   - File `index.html` ke `deliveryTokens` dictionary me naya secret token entry add hogi:
   ```javascript
   '<slug>-mb-<14hex>': {
       title: 'Exact Product Title',
       subtitle: 'Clear Subtitle / Edition',
       pages: 'XX Pages',
       size: 'X.X MB',
       pdf: '<slug>-mb-<14hex>.pdf',
       mockup: '<slug>-mockup.png'
   }
   ```

3. **Thank-You & Auto-Download Delivery Page (`/download/<token>`):**
   - Buyer Razorpay se pay karne ke baad seedha `https://markbuilder.in/download/<token>` par land karega.
   - **Features:**
     - Branded Green Gradient Banner ("🎉 Payment Successful!").
     - Exact Product 3D Mockup, Page Count, File Size aur Subtitle.
     - 2-Second Auto-Download Countdown: Browser automatically buyer ke device ke `Downloads` folder me file download trigger karta hai.
     - Primary Button: `📥 Download PDF to Device` (forced `download` attribute).
     - Secondary Button: `📖 Open & Read in Browser Tab` (preview mode).
     - Founder Support Hotline & Mobile Instructions (iOS Files / Android Downloads).
     - Tampered / Invalid Token Guard: Invalid URL par secure error card render hota hai.

4. **Razorpay Payment Page Setup:**
   - Razorpay Payment Page settings me:
     - **Action after payment:** Redirect to URL
     - **Redirect URL:** `https://markbuilder.in/download/<slug>-mb-<14hex>`
   - Buyer ko payment ke baad zero confusion aur zero wait time ke sath exact purchased PDF deliver hoga.

5. **Gumroad Global Setup:**
   - Square 1:1 Thumbnail (1200x1200px) required for Gumroad discovery.
   - Hashed PDF file upload as attached product content.
   - Redirect URL set to `https://markbuilder.in/download/<token>` or Gumroad instant download page.

6. **Storefront & PDP Integration:**
   - Product Card in Homepage Grid (with ₹99 / 80% OFF badges).
   - Category Sub-nav Tab linking.
   - Dedicated PDP URL (`markbuilder.in/<slug>`).
   - Free Sample Teaser Modal.
   - Multi-token live search indexing.

---

## 📚 Publications Catalog (Live & Active)

| # | Product Title | Pages | Filename / Secret Delivery Token | Live Delivery URL |
|---|---|---|---|---|
| **1** | **50 Micro-SaaS You Can Build Without Coding (2026 Edition)** | 40 Pages | `saas-blueprints-mb-4b8c91a02e5f3d` | [`markbuilder.in/download/saas-blueprints-mb-4b8c91a02e5f3d`](https://markbuilder.in/download/saas-blueprints-mb-4b8c91a02e5f3d) |
| **2** | **The Hidden Tricks Your Brain Plays on You (2026 Master Edition)** | 75 Pages | `brain-tricks-mb-3e91d8b72c4a5f` | [`markbuilder.in/download/brain-tricks-mb-3e91d8b72c4a5f`](https://markbuilder.in/download/brain-tricks-mb-3e91d8b72c4a5f) |
| **3** | **The High-Ticket Client Acquisition Vault (2026 Edition)** | 28 Pages | `vault-dossier-mb-8f92a4c107e3b9` | [`markbuilder.in/download/vault-dossier-mb-8f92a4c107e3b9`](https://markbuilder.in/download/vault-dossier-mb-8f92a4c107e3b9) |
| **4** | **The Non-Coder's Vibe Coding Playbook (2026 Master Edition)** | 22 Pages | `vibe-playbook-mb-ffef44be315c8f` | [`markbuilder.in/download/vibe-playbook-mb-ffef44be315c8f`](https://markbuilder.in/download/vibe-playbook-mb-ffef44be315c8f) |

---

## ✨ Store Features & Architecture

- **📱 Etsy-Style 2-Column Mobile Grid:** Side-by-side square product display matching top e-commerce mobile UX.
- **🔍 Real-Time Multi-Token Search:** Live search engine with multi-keyword indexing and 1-tap `[✕]` Clear button.
- **💳 Frictionless Dual-Checkout Flow:**
  - **Domestic (India):** Direct Razorpay UPI / GPay / Netbanking checkout (₹99).
  - **International (Global):** Direct Gumroad Checkout integration ($9.99 USD) with auto-detection for non-Indian visitors.
- **🎨 Studio White Aesthetic:** Built-in safeguards (`color-scheme: only light` and CSS gradient overrides) preventing aggressive Android/Xiaomi Force Dark Mode inversions.
- **⚡ 60/120 FPS Mobile Performance:** Hardware-accelerated transitions (`transform: translateZ(0)`), zero heavy GPU backdrop filters, and compressed image assets.
- **🌍 Multi-Currency Switcher:** Instant price conversion across INR (₹), USD ($), EUR (€), GBP (£), CAD ($), AUD ($), and AED.
- **🖼️ Fullscreen Lightbox Gallery:** Interactive click-to-zoom slide previews for publication decks.
- **🛡️ Direct URL Protection:** Static rewrite rules in `vercel.json` and client-side router prevent direct scraping of unauthenticated PDF routes.

---

## 🛠️ Architecture & Tech Stack

- **Frontend:** Semantic HTML5, Tailwind CSS, Custom Lightbox, SPA Client-Side Hash & Path Router (Vanilla JavaScript).
- **Backend / Payments:** Serverless Jamstack via Razorpay & Gumroad PCI-DSS secure banking infrastructure.
- **Hosting & CDN:** Vercel Global Edge Network with custom domain `markbuilder.in`.
- **Assets & Media:** High-resolution 3D book mockups, feature slide carousels, and 1200x1200px 1:1 square thumbnails.

---

© 2026 MarkBuilder. All rights reserved.
