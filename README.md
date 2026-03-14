# 🚀 Tejas C S - DevOps Engineer Portfolio

A stunning, modern, and responsive web portfolio built with React, Vite, and Tailwind CSS. Features an AI-powered chatbot, contact form, SEO optimization, and Google Analytics tracking.

![Portfolio Preview](https://img.shields.io/badge/Status-Live-brightgreen)
![React](https://img.shields.io/badge/React-19.2.0-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-7.2.5-646CFF?logo=vite)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.1-38B2AC?logo=tailwind-css)

🌐 **Live:** [sanjaysundarmurthy-portfolio.vercel.app](https://sanjaysundarmurthy-portfolio.vercel.app)

---

## ✨ Features

- **Modern UI/UX** - Sleek dark theme with cyan/purple gradient accents
- **Smooth Animations** - Powered by Framer Motion for stunning transitions
- **Interactive Elements** - Custom cursor effects, particle background, and hover animations
- **Fully Responsive** - Optimized for all screen sizes (mobile, tablet, desktop)
- **Fast Performance** - Built with Rolldown-Vite for lightning-fast builds
- **🤖 AI Chatbot** - Google Gemini-powered assistant that knows everything about Tejas
- **📧 Contact Form** - Integrated with EmailJS for direct messaging
- **📊 Google Analytics** - Track visitors and engagement
- **🔍 SEO Optimized** - Meta tags, Open Graph, sitemap, robots.txt, JSON-LD structured data
- **🖼️ OG Image** - Beautiful preview cards when shared on LinkedIn/Facebook
- **📱 PWA Ready** - Can be installed as a mobile/desktop app

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Frontend** | React 19, JSX |
| **Styling** | Tailwind CSS 4, Custom CSS |
| **Animations** | Framer Motion |
| **Build Tool** | Vite (Rolldown) |
| **AI Chatbot** | Google Gemini AI (gemini-2.5-flash) |
| **Contact Form** | EmailJS |
| **Analytics** | Google Analytics 4 |
| **Icons** | React Icons (Font Awesome, Simple Icons, Heroicons) |
| **Type Animation** | react-type-animation |
| **Hosting** | Vercel (auto-deploy from GitHub) |

---

## 📁 Project Structure

```
Web-portfolio/
├── public/
│   ├── favicon.svg            # Custom "S" branded favicon
│   ├── og-image.svg           # OG image source (SVG)
│   ├── og-image.png           # OG image for social sharing (1200x630)
│   ├── robots.txt             # Search engine crawl rules
│   ├── sitemap.xml            # Sitemap for Google indexing
│   ├── site.webmanifest       # PWA manifest
├── scripts/
│   └── convert-og-image.js    # SVG to PNG converter for OG image
├── src/
│   ├── components/
│   │   ├── About.jsx          # About section with bio & stats
│   │   ├── Chatbot.jsx        # 🤖 AI chatbot (Google Gemini)
│   │   ├── Contact.jsx        # Contact form (EmailJS)
│   │   ├── CustomCursor.jsx   # Interactive cursor effect
│   │   ├── Experience.jsx     # Timeline of work & education
│   │   ├── Footer.jsx         # Footer with social links
│   │   ├── Hero.jsx           # Landing section with CTA
│   │   ├── Loader.jsx         # Initial loading animation
│   │   ├── Navbar.jsx         # Responsive navigation
│   │   ├── ParticleBackground.jsx  # Animated background
│   │   ├── Projects.jsx       # Project showcase with GitHub links
│   │   └── Skills.jsx         # Technical skills & certifications
│   ├── App.jsx                # Main application component
│   ├── index.css              # Global styles & Tailwind config
│   └── main.jsx               # React entry point
├── .env.local                 # 🔒 API keys (NOT in Git)
├── .gitignore                 # Git ignore rules
├── eslint.config.js           # ESLint config
├── index.html                 # HTML with SEO meta tags & Analytics
├── og-image-generator.html    # Visual OG image template
├── package.json               # Dependencies & scripts
├── vite.config.js             # Vite configuration
└── README.md                  # This file
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **npm** (v9 or higher)
- **Git**

### Step 1: Clone the Repository

```bash
git clone https://github.com/tejascs57/
cd tejas-portfolio
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Set Up Environment Variables

Create a `.env.local` file in the project root:

```env
# EmailJS Configuration (for contact form)
VITE_EMAILJS_SERVICE_ID=your_service_id
VITE_EMAILJS_TEMPLATE_ID=your_template_id
VITE_EMAILJS_PUBLIC_KEY=your_public_key

# Google Gemini AI Configuration (for chatbot)
VITE_GEMINI_API_KEY=your_gemini_api_key
```

> ⚠️ **IMPORTANT:** Never commit `.env.local` to Git. It's already in `.gitignore`.

### Step 4: Start Development Server

```bash
npm run dev
```

### Step 5: Open in Browser

```
http://localhost:5173
```

---

## 📦 Build for Production

```bash
# Create optimized production build
npm run build

# Preview production build locally
npm run preview
```

The build output goes to the `dist/` folder.

---

## 📜 Available Scripts

| Script | Command | Description |
|--------|---------|-------------|
| **Development** | `npm run dev` | Start dev server with hot reload |
| **Build** | `npm run build` | Create optimized production build |
| **Preview** | `npm run preview` | Preview production build locally |
| **Lint** | `npm run lint` | Run ESLint for code quality |

---

## 🔧 Configuration Guide

### 1. EmailJS (Contact Form)

The contact form sends emails directly without a backend server.

**Setup Steps:**
1. Create account at [emailjs.com](https://www.emailjs.com/) (free tier: 200 emails/month)
2. Create an email service (Gmail, Outlook, etc.)
3. Create an email template with these variables:
   - `{{from_name}}` - Sender's name
   - `{{from_email}}` - Sender's email
   - `{{subject}}` - Email subject
   - `{{message}}` - Email message
4. Copy your Service ID, Template ID, and Public Key
5. Add to `.env.local`:
   ```
   VITE_EMAILJS_SERVICE_ID=service_xxxxx
   VITE_EMAILJS_TEMPLATE_ID=template_xxxxx
   VITE_EMAILJS_PUBLIC_KEY=your_public_key
   ```
6. Add the same variables to **Vercel → Settings → Environment Variables**

---

### 2. AI Chatbot (Google Gemini)

The chatbot uses Google Gemini AI to answer questions about Tejas's profile.

**Setup Steps:**
1. Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
2. Click **"Create API key in new project"**
3. Copy the API key (starts with `AIzaSy...`)
4. Add to `.env.local`:
   ```
   VITE_GEMINI_API_KEY=AIzaSy_xxxxx
   ```
5. Add the same variable to **Vercel → Settings → Environment Variables**

**Customizing Chatbot Context:**
- Edit `src/components/Chatbot.jsx`
- Update the `TEJAS_CONTEXT` constant with your information
- This tells the AI what it knows about you (experience, skills, projects, etc.)

**Model:** `gemini-2.5-flash` (free tier: 15 requests/min, 1500 requests/day)

**Important Notes:**
- Vite env variables are embedded at **build time**
- After changing keys in Vercel → you MUST **Redeploy without cache**
- If you get 429 errors → rate limit hit, wait 30 seconds
- If quota fully exhausted → create a new API key in a new GCP project

---

### 3. Google Analytics

Track visitors, traffic sources, and engagement.

**Setup Steps:**
1. Go to [analytics.google.com](https://analytics.google.com/)
2. Create a property for your portfolio
3. Get the Measurement ID (e.g., `G-XXXXXXXXXX`)
4. Edit `index.html` — replace `G-XXXXXXXXXX` with your Measurement ID (appears in 2 places)
5. Push to GitHub — Vercel auto-deploys

**View Dashboard:** [analytics.google.com](https://analytics.google.com/) (data starts appearing in 24-48 hours)

**What you can track:**
- 👥 Total visitors
- 🌍 Geographic location
- 📱 Device types (mobile/desktop)
- 🔗 Traffic sources (LinkedIn, Google, Direct)
- ⏱️ Time spent on site
- 📈 Trends over time

**Cost:** 100% FREE, no limits, no credit card required.

---

### 4. SEO & Social Sharing

**Already configured in `index.html`:**
- ✅ SEO meta tags (title, description, keywords, author)
- ✅ Open Graph tags (LinkedIn/Facebook preview cards)
- ✅ JSON-LD structured data (rich Google search results)
- ✅ Canonical URL
- ✅ Sitemap (`public/sitemap.xml`)
- ✅ Robots.txt (`public/robots.txt`)

**To update the OG image:**
1. Edit `public/og-image.svg` (source design)
2. Convert to PNG: `node scripts/convert-og-image.js`
3. Push to GitHub

**Test your social preview:**
- [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/) — enter your URL
- [OpenGraph Preview](https://www.opengraph.xyz/) — preview all platforms

---

### 5. Theme Colors

Edit `src/index.css` — modify the `@theme` section:

```css
@theme {
  --color-primary-*: /* Cyan shades (main accent) */
  --color-accent-*:  /* Purple shades (secondary accent) */
  --color-dark-*:    /* Dark theme background shades */
}
```

---

### 6. Personal Information Update Guide

| What to Update | File | What to Change |
|----------------|------|----------------|
| Name, title, intro | `src/components/Hero.jsx` | Main heading & description text |
| Bio, stats, info | `src/components/About.jsx` | Bio paragraphs, stat numbers, quick info |
| Work history | `src/components/Experience.jsx` | Timeline entries (company, role, date, tech) |
| Skills & certs | `src/components/Skills.jsx` | Skill categories, proficiency, certifications |
| Projects | `src/components/Projects.jsx` | Project cards (name, description, GitHub URL, tags) |
| Contact info | `src/components/Contact.jsx` | Email, phone, location |
| Social links | `src/components/Hero.jsx` & `Footer.jsx` | GitHub & LinkedIn URLs |
| AI chatbot context | `src/components/Chatbot.jsx` | Update `TEJAS_CONTEXT` constant |
| Page title & SEO | `index.html` | Meta tags, JSON-LD structured data |

---

## 🌐 Deployment

### Vercel (Current Setup)

The portfolio **auto-deploys** when you push to `main` branch.

**Daily Workflow:**
```bash
# Make changes locally
npm run dev          # Test at http://localhost:5173

# Deploy
git add .
git commit -m "your message"
git push origin main  # Vercel auto-deploys in ~1 min
```

**First-time Vercel Setup:**
1. Go to [vercel.com](https://vercel.com) → Import Project
2. Select your GitHub repo
3. Build settings (auto-detected):
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Add **Environment Variables** (Settings → Environment Variables):
   ```
   VITE_EMAILJS_SERVICE_ID     → your_service_id
   VITE_EMAILJS_TEMPLATE_ID    → your_template_id
   VITE_EMAILJS_PUBLIC_KEY     → your_public_key
   VITE_GEMINI_API_KEY         → your_gemini_key
   ```
5. Deploy!

**After changing environment variables in Vercel:**
1. Go to **Deployments** → Click 3 dots → **Redeploy**
2. ❌ **UNCHECK** "Use existing Build Cache"
3. Click Redeploy

> 💡 Vite bakes env variables at build time, so you MUST rebuild after changing them.

---

## 📱 Responsive Design

The portfolio is fully responsive across all devices:

| Device | Breakpoint | Status |
|--------|-----------|--------|
| Mobile (small) | < 640px | ✅ Optimized |
| Mobile (large) | 640px+ (sm) | ✅ Optimized |
| Tablet | 768px+ (md) | ✅ Optimized |
| Laptop | 1024px+ (lg) | ✅ Optimized |
| Desktop | 1280px+ (xl) | ✅ Optimized |

**Key responsive features:**
- Hamburger menu on mobile
- Stacking layouts on small screens
- Font scaling across breakpoints
- Full-width chatbot on mobile
- Touch-friendly (custom cursor hidden on touch devices)
- Canvas particles scale with screen size

---

## 🔑 Environment Variables Reference

| Variable | Service | Where to Get | Required For | Cost |
|----------|---------|-------------|--------------|------|
| `VITE_EMAILJS_SERVICE_ID` | EmailJS | emailjs.com dashboard | Contact form | Free (200/mo) |
| `VITE_EMAILJS_TEMPLATE_ID` | EmailJS | emailjs.com dashboard | Contact form | Free |
| `VITE_EMAILJS_PUBLIC_KEY` | EmailJS | emailjs.com dashboard | Contact form | Free |
| `VITE_GEMINI_API_KEY` | Google AI | aistudio.google.com/apikey | AI Chatbot | Free (1500/day) |

> ⚠️ Set in **both** `.env.local` (local) and **Vercel Environment Variables** (production).

---

## 🔧 Troubleshooting

### Chatbot Issues

| Problem | Solution |
|---------|----------|
| "I'm having trouble connecting" | Check `VITE_GEMINI_API_KEY` in `.env.local` |
| 404 error | Model name outdated — update in `Chatbot.jsx` |
| 429 error (rate limit) | Wait 30 seconds and retry |
| "limit: 0" (quota exhausted) | Create new API key in **new project** at aistudio.google.com |
| Works locally, not on Vercel | Add env var to Vercel → Redeploy **without cache** |

### Contact Form Issues

| Problem | Solution |
|---------|----------|
| Form not sending | Verify 3 EmailJS env vars in `.env.local` |
| Emails not received | Check EmailJS template has correct variable names |
| Quota exceeded | Free tier = 200 emails/month |

### Development Issues

| Problem | Solution |
|---------|----------|
| Port 5173 in use | `npx kill-port 5173` or `npm run dev -- --port 3000` |
| Vite cache error | `Remove-Item node_modules/.vite -Recurse -Force` then `npm run dev` |
| Node modules broken | Delete `node_modules` & `package-lock.json`, run `npm install` |
| Build fails | `npm run build -- --force` |

### SEO Issues

| Problem | Solution |
|---------|----------|
| OG image not showing on LinkedIn | Use [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/) to clear cache |
| Not appearing on Google | Submit sitemap at [Google Search Console](https://search.google.com/search-console) |

---

## 🏆 Featured Skills & Certifications

### Technical Expertise

| Category | Skills |
|----------|--------|
| **Cloud** | Azure (AKS, ADF, App Services, Functions, Key Vault, Monitor), AWS, GCP |
| **Containers** | Kubernetes, Docker, Helm, ArgoCD, Istio, Service Mesh |
| **CI/CD** | Azure DevOps, GitHub Actions, Jenkins, GitOps, FluxCD |
| **IaC** | Terraform, Ansible, ARM Templates, Bicep, Pulumi |
| **Monitoring** | Prometheus, Grafana, ELK Stack, Azure Monitor, Datadog |
| **Security** | SonarQube, Trivy, Snyk, Vault, OWASP, OPA/Gatekeeper |
| **Languages** | Python, Bash, PowerShell, Go, YAML |

### Microsoft Certifications

- 🏆 **AZ-900** - Microsoft Azure Fundamentals
- 🛡️ **SC-900** - Microsoft Security, Compliance & Identity
- ⚡ **PL-900** - Microsoft Power Platform Fundamentals

### Awards

- 🥇 Microsoft Cybersecurity Award - Accenture Azure Tech Competition
- ⭐ Multiple Awards for High-Impact DevOps Contributions

---

## 🔒 Safety & Backup

A safety backup branch exists: `backup-before-chatbot`

To revert to pre-chatbot state if needed:
```bash
git checkout backup-before-chatbot
```

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Tejas C S**

| | |
|---|---|
| 📍 Location | Bangalore, Karnataka, India |
| 💼 Role | Senior DevOps Engineer @ AspenTech (Emerson) |
| 🎓 Education | B.E. Aeronautical Engineering - DSCE (VTU) |
| 📧 Email | tejascs99@gmail.com |
| 📱 Phone | +91 9880475198 |
| 🔗 LinkedIn | [linkedin.com/in/tejas-c-s-439a021b1/](https://www.linkedin.com/in/tejas-c-s-439a021b1/) |
| 💻 GitHub | [github.com/tejascs57](https://github.com/tejascs57) |
| 🌐 Portfolio | [tejascs.vercel.app/](https://tejascs.vercel.app/) |

---

## 🙏 Acknowledgments

- [React](https://react.dev/) - UI Library
- [Vite](https://vitejs.dev/) - Build Tool
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Framer Motion](https://www.framer.com/motion/) - Animations
- [Google Gemini AI](https://ai.google.dev/) - AI Chatbot
- [EmailJS](https://www.emailjs.com/) - Email Service
- [React Icons](https://react-icons.github.io/react-icons/) - Icons
- [Vercel](https://vercel.com/) - Hosting
- [Google Analytics](https://analytics.google.com/) - Analytics

---

⭐ **If you found this portfolio helpful, please give it a star!**

Made with ❤️ by Tejas C S
