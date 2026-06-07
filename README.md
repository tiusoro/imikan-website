# Imikan Technologies AI — RAG & Shopify AI Integrations Landing Page

A modern, production-ready landing page for an AI integrations company specializing in **Retrieval-Augmented Generation (RAG)** pipelines and **Shopify AI automation**.

![Tech Stack](https://img.shields.io/badge/Tailwind%20CSS-3.4-38B2AC?logo=tailwindcss)
![HTML5](https://img.shields.io/badge/HTML5-Semantic-E34F26?logo=html5)
![JavaScript](https://img.shields.io/badge/Vanilla%20JS-ES6+-F7DF1E?logo=javascript)
![License](https://img.shields.io/badge/License-MIT-8B5CF6)

---

## 🎨 Design System

| Token | Value | Usage |
|-------|-------|-------|
| **Primary Purple** | `#8B5CF6` → `#7C3AED` | CTAs, highlights, RAG accents |
| **Accent Blue** | `#3B82F6` → `#2563EB` | Shopify section, links, trust indicators |
| **Background** | `#0F0F1A` | Deep navy-black base |
| **Glass Surface** | `rgba(255,255,255,0.03)` + `blur(20px)` | Cards, nav, overlays |
| **Text Primary** | `#FFFFFF` | Headlines |
| **Text Secondary** | `#9CA3AF` | Body copy, descriptions |

### Typography
- **Display**: `Space Grotesk` — Bold, geometric, tech-forward
- **Body**: `Inter` — Clean, highly legible at all sizes

---

## 🚀 Quick Start

```bash
# Clone or download the repository
git clone https://github.com/tiusoro/imikan-website.git

# Navigate to the project
cd imikan-landing

# Open in browser (no build step required)
open index.html
# Or serve locally
npx serve .
# Or with Python
python -m http.server 8000
```

> **No build tools required.** This is a single-file HTML landing page with inline CSS and JavaScript. All dependencies are loaded via CDN.

---

## 📁 Project Structure

```
Imikan-landing/
├── index.html          # Complete landing page (single file)
├── README.md           # This file
└── assets/             # Optional: images, favicon, OG tags
    ├── og-image.png
    └── favicon.ico
```

---

## ✨ Features

### Visual Effects
- **Glassmorphism** — Frosted glass cards with `backdrop-filter: blur(20px)`
- **Gradient Mesh Background** — Multi-layer radial gradients (purple/blue)
- **Noise Texture Overlay** — Subtle SVG noise at 3% opacity for premium feel
- **Gradient Borders** — Animated border gradients on feature cards
- **Mouse Parallax** — Hero glow follows cursor movement

### Animations
- **Scroll Reveal** — IntersectionObserver triggers fade-up animations
- **Typing Effect** — Hero headline cycles through 4 value propositions
- **Floating Elements** — Decorative orbs with staggered float animations
- **Hover States** — Cards lift with shadow expansion on hover
- **Pulse Indicators** — Live status dots and breathing glows

### Sections
| Section | Purpose |
|---------|---------|
| **Navigation** | Sticky glass nav with blur backdrop |
| **Hero** | Value prop, stats, dual CTAs |
| **Trust Bar** | Logo strip for social proof |
| **RAG Engine** | Feature list + code snippet display |
| **Shopify AI** | Interactive chatbot mockup |
| **Features Grid** | 6 capability cards with icons |
| **How It Works** | 3-step process with connector line |
| **Pricing** | 3-tier cards (Free / Pro / Enterprise) |
| **CTA** | Final conversion push |
| **Footer** | Links, social, status indicator |

---

## 🛠️ Customization Guide

### Change Brand Colors
Edit the Tailwind config in the `<script>` tag:

```javascript
tailwind.config = {
  theme: {
    extend: {
      colors: {
        primary: { 500: '#8B5CF6', 600: '#7C3AED' },  // Purple
        accent: { 500: '#3B82F6', 600: '#2563EB' },    // Blue
      }
    }
  }
}
```

### Update Hero Typing Text
Modify the `texts` array in the JavaScript:

```javascript
const texts = [
  "Understands Your Data",
  "Powers Your Store",
  "Scales Infinitely",
  "Ships in Minutes"
];
```

### Change Pricing Tiers
Locate the **Pricing** section and update:
- Plan names and prices
- Feature lists (`<ul>` items)
- CTA button text and links

### Add/Remove Features
Each feature card follows this pattern:

```html
<div class="group p-8 rounded-2xl glass card-hover gradient-border reveal">
  <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-primary-500/20 to-primary-600/20 ...">
    <i data-lucide="icon-name" class="w-7 h-7 text-primary-400"></i>
  </div>
  <h3 class="text-xl font-display font-bold text-white mb-3">Feature Title</h3>
  <p class="text-gray-400 leading-relaxed">Feature description...</p>
</div>
```

> Replace `icon-name` with any [Lucide icon](https://lucide.dev/icons/).

---

## 🔌 Integration Points

### Connect to Backend
The **RAG code block** and **Shopify chatbot** are visual mockups. To make them functional:

1. **RAG Pipeline** — Replace the static `<pre>` block with a live API call:
   ```javascript
   fetch('/api/rag/status')
     .then(r => r.json())
     .then(data => renderCodeBlock(data));
   ```

2. **Chatbot** — Add WebSocket or fetch-based messaging:
   ```javascript
   async function sendMessage(message) {
     const response = await fetch('/api/chat', {
       method: 'POST',
       headers: { 'Content-Type': 'application/json' },
       body: JSON.stringify({ message, store_id: 'your-store' })
     });
     return response.json();
   }
   ```

3. **Pricing CTAs** — Link to Stripe/Paddle checkout:
   ```html
   <button onclick="window.location.href='https://checkout.stripe.com/...'">
     Start 14-Day Trial
   </button>
   ```

---

## 📱 Responsive Breakpoints

| Breakpoint | Width | Adjustments |
|------------|-------|-------------|
| Mobile | `< 640px` | Single column, stacked nav, reduced padding |
| Tablet | `640px - 1024px` | 2-column grids, medium typography |
| Desktop | `> 1024px` | Full layout, side-by-side sections, max-width containers |

All responsive behavior is handled by Tailwind's utility classes (`md:`, `lg:`, `sm:`).

---

## 🌐 SEO & Meta Tags

Add these inside `<head>` for production:

```html
<meta name="description" content="Imikan AI — Enterprise RAG pipelines and Shopify AI automations. Transform unstructured data into actionable intelligence.">
<meta property="og:title" content="Imikan AI — RAG & Shopify Intelligence">
<meta property="og:description" content="Build intelligent applications with sub-second latency.">
<meta property="og:image" content="https://yoursite.com/assets/og-image.png">
<meta property="og:url" content="https://yoursite.com">
<meta name="twitter:card" content="summary_large_image">
<link rel="canonical" href="https://yoursite.com">
```

---

## 🚢 Deployment Options

### Static Hosting (Recommended)
| Platform | Command / Steps |
|----------|-----------------|
| **Vercel** | `vercel --prod` or drag folder to dashboard |
| **Netlify** | Drag folder to deploy dropzone |
| **GitHub Pages** | Push to `gh-pages` branch |
| **Cloudflare Pages** | Connect Git repo or direct upload |
| **AWS S3** | Upload to bucket + enable static hosting |

### Docker (Optional)
```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/
COPY assets/ /usr/share/nginx/html/assets/
EXPOSE 80
```

---

## 🧪 Performance Checklist

- [ ] **Lighthouse Score** > 90 on all metrics
- [ ] **First Contentful Paint** < 1.5s
- [ ] **Image Optimization** — Convert to WebP/AVIF if adding images
- [ ] **Font Loading** — `font-display: swap` is already set
- [ ] **Minification** — Use `html-minifier` for production builds
- [ ] **CDN Caching** — Set `Cache-Control: max-age=31536000` for assets

---

## 📝 Changelog

### v1.0.0 (2026-06-07)
- Initial release
- Single-file architecture
- 10 complete sections
- Glassmorphism design system
- Scroll-triggered animations
- Responsive across all breakpoints

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

MIT License — feel free to use for personal or commercial projects. Attribution appreciated but not required.

---

## 💬 Support

- **Documentation**: [docs.imikan.ai](https://docs.imikan.ai)
- **Discord**: [discord.gg/imikan](https://discord.gg/imikan)
- **Email**: hello@imikan.ai
- **Status**: [status.imikan.ai](https://status.imikan.ai)

---

<p align="center">
  <strong>Built with 💜 and 💙 by the Imikan Technologies Team</strong><br>
  <sub>Transforming data into intelligence, one query at a time.</sub>
</p>
