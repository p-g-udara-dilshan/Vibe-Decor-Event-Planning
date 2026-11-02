<div align="center">

# ✨ Vibe Decor — Event Planning Website

**A modern, responsive website for an event decoration and planning business in Badulla, Sri Lanka.**

Built as a **real freelance client project** with a focus on visual storytelling, clear service information, and easy customer enquiries.

[**🌐 View Live Website**](https://vibe-decor-event-planning.vercel.app/) · [**💻 Source Repository**](https://github.com/p-g-udara-dilshan/Vibe-Decor-Event-Planning)

![React](https://img.shields.io/badge/React-Frontend-149ECA?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-Type%20Safe-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-Build%20Tool-646CFF?logo=vite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-CMS%20Integration-3FCF8E?logo=supabase&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-Deployment-000000?logo=vercel&logoColor=white)

</div>

---

## 📸 Project Preview

![Vibe Decor homepage — dark-and-gold event planning website](docs/images/hero-preview.png)

<details>
<summary><strong>View full-page website screenshot</strong></summary>

![Vibe Decor complete website preview](docs/images/full-page-preview.png)

</details>

> Screenshot captured from the deployed website in November 2026. Business details, event images and package information are managed by the client and may change.

## 📖 About the Project

**Vibe Decor Event Planning** is a client-focused web experience designed to help visitors discover event decoration services, browse previous work, compare packages, and contact the business without a complicated booking process.

The project emphasizes:

- A premium **black-and-gold visual identity** suitable for weddings and celebrations.
- Responsive layouts across desktop and mobile viewports.
- A visual portfolio for event photography and decoration work.
- Clear, conversion-oriented calls to action, including **WhatsApp enquiries**.
- An optional **Supabase-backed administration and content management** workflow.

**Project type:** Freelance client website · **Development period:** October–November 2026 · **Deployment:** Vercel

## ✨ Features

| Area | What it offers |
| --- | --- |
| **Responsive landing page** | Branded hero, introduction, services and calls to action. |
| **Services** | Event decoration and planning services presented in organized sections. |
| **Event portfolio** | Event cards, category filters, and individual event/photo viewing. |
| **Engagement packages** | Package comparisons, inclusions, and enquiry-oriented actions. |
| **Contact & WhatsApp** | Quick access to business contact information and WhatsApp enquiries. |
| **Admin/CMS interface** | Admin-oriented tools for managing event content, galleries, services, packages and site details; requires Supabase configuration. |
| **Default site content** | The public-facing site can display its configured default content without connecting a Supabase project. |

**Scope clarification:** This is an event planning **marketing and enquiry website**, not an online payment or confirmed booking-processing system. Admin functions depend on the actual Supabase project and security configuration.

## 🛠️ Tech Stack

| Purpose | Technology |
| --- | --- |
| Frontend | **React**, **TypeScript** |
| Development/build | **Vite**, **npm** |
| Styling | **CSS** |
| Database / content services | **Supabase** (PostgreSQL, Authentication and Storage when configured) |
| Hosting and deployment | **Vercel** |
| Version control | **Git & GitHub** |

## 🗂️ Project Structure

Selected paths documented in the repository:

```text
Vibe-Decor-Event-Planning/
├── public/                     # Images and public assets
├── src/
│   ├── App.tsx                 # Page composition / routing
│   ├── components/
│   │   ├── Navbar.tsx          # Navigation and mobile menu
│   │   ├── About.tsx           # About section
│   │   ├── Services.tsx        # Service presentation
│   │   ├── Packages.tsx        # Package comparison and enquiries
│   │   ├── Portfolio.tsx       # Event portfolio
│   │   ├── EventGallery.tsx    # Gallery and event image views
│   │   ├── Contact.tsx         # Contact section
│   │   └── FloatingWhatsApp.tsx
│   ├── pages/
│   │   └── AdminPage.tsx       # Admin content management UI
│   ├── data/
│   │   └── siteData.ts         # Default content
│   ├── lib/
│   │   └── cms.ts              # CMS / Supabase helpers
│   └── index.css
├── supabase/
│   └── setup.sql               # Database setup and access policies
├── .env.example                # Example environment variables
├── package.json
├── vite.config.ts
└── vercel.json
```

> This is a selected-file overview, not an exhaustive tree. Refer to the repository for the current directory structure.

## 🚀 Getting Started

### Prerequisites

- **Node.js 20 or later** and npm
- Git
- A Supabase project **only if you want to configure dynamic CMS / admin features**

### 1. Clone the repository

```bash
git clone https://github.com/p-g-udara-dilshan/Vibe-Decor-Event-Planning.git
cd Vibe-Decor-Event-Planning
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the development server

```bash
npm run dev
```

Open the local address printed by Vite in your terminal (usually `http://localhost:5173`).

### 4. Build for production

```bash
npm run build
```

The public-facing website can render with its default content; database-managed updates, administrator sign-in, and cloud uploads need a configured Supabase project.

## 🗄️ Supabase Setup (Optional CMS / Admin Features)

> Follow the repository's `.env.example`, `SETUP-SL.txt` (if applicable), and `supabase/setup.sql`. Set up a separate test project first; do not run SQL against an existing client database without reviewing it.

1. Create a project in the [Supabase dashboard](https://supabase.com/dashboard).
2. Copy `.env.example` to `.env.local` (the file must remain untracked).
3. Configure the project URL and the intended **public/anon** key using the names required by the code:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_or_publishable_key
```

4. Review and run `supabase/setup.sql` in the Supabase SQL Editor. Confirm schema creation and **Row Level Security (RLS)** policies.
5. Configure **Supabase Authentication** and an authorized administrator account according to the setup instructions included in the repository.
6. Configure the required **Supabase Storage** bucket and its permissions for event images.
7. Restart the local dev server and test sign-in, content editing, and image uploads as the authorized administrator.

**Important security guidance**

- Never commit `.env.local`, private API keys, database passwords, Supabase `service_role` keys, or client credentials.
- `VITE_` variables are shipped to the browser. Use only an appropriately scoped **public/anon** key there; keep all privileged secrets server-side.
- Enforce authorization with Supabase Auth and database RLS, not merely by hiding an administrator URL.
- Disable public sign-ups if the business requires an owner-only content management workflow.
- Before publishing changes, verify the client's contact details, images, permissions, and package information.

## 📱 Responsive Design

The interface is designed for smaller screens as well as desktop browsing, with a responsive navigation menu, adaptable content grids, and accessible contact actions.

## ☁️ Deployment

The frontend is deployed using **Vercel**:

**https://vibe-decor-event-planning.vercel.app/**

For a separate deployment, import the GitHub repository into Vercel. Use the project's build script (`npm run build`), provide any needed **public** Supabase environment variables in Vercel project settings, and make sure SPA routing uses the repository's `vercel.json` configuration.

## 💡 Development Experience

This project provided practical experience in:

- Understanding requirements from a **real business client**.
- Translating a client's branding and event packages into a web interface.
- Structuring reusable React components with TypeScript.
- Building responsive, media-rich layouts and event portfolios.
- Creating enquiry paths with WhatsApp and contact information.
- Working with content management, Supabase integration, and deployment workflows.

## 🤝 Credits & Client Work

Developed as a freelance client project. The repository reflects collaborative work; please refer to its **Contributors** panel for the current contributor list.

Client branding, photography, brochure-derived content and business contact information belong to their respective owners and should only be republished with permission. Before changing public prices, events, or contact details, obtain client confirmation.

## 📫 Developer

**Udara Dilshan**

- **GitHub:** [p-g-udara-dilshan](https://github.com/p-g-udara-dilshan)
- **LinkedIn:** [p-g-udara-dilshan](https://www.linkedin.com/in/p-g-udara-dilshan)
- **Email:** [udara.profile@gmail.com](mailto:udara.profile@gmail.com)

---

<div align="center">

**Built to turn memorable events into a polished digital experience.** ✨

</div>
