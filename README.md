# Shishir Khan — Portfolio

A modern, premium, fully responsive personal portfolio built with **Next.js 15 (App Router)**, **TypeScript**, **Tailwind CSS**, and **Framer Motion**. Glassmorphism UI, blue/purple gradient theme, dark & light mode, smooth animations throughout.

## Tech Stack

- Next.js 15 (App Router) + React 19 + TypeScript
- Tailwind CSS
- Framer Motion (animations)
- Lucide Icons
- next-themes (dark / light mode)
- SEO metadata, custom 404, scroll progress bar, custom cursor, loading screen

## Getting Started

```bash
# 1. Install dependencies
npm install

# 2. Run the dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view it.

## Project Structure

```
app/
  layout.tsx        # Root layout, fonts, metadata, theme provider
  page.tsx           # Assembles all homepage sections
  globals.css        # Design tokens, glassmorphism utilities, animations
  not-found.tsx       # Custom 404 page
components/
  navbar.tsx, hero.tsx, about.tsx, skills.tsx, featured-project.tsx,
  projects.tsx, research.tsx, experience.tsx, education.tsx,
  certificates.tsx, testimonials.tsx, contact.tsx, footer.tsx
  theme-provider.tsx, theme-toggle.tsx, scroll-progress.tsx,
  cursor.tsx, loading-screen.tsx, animated-background.tsx,
  section-heading.tsx
data/
  site.ts            # ALL editable content lives here (single source of truth)
hooks/
  use-active-section.ts
  use-scroll-progress.ts
lib/
  utils.ts           # cn() class-merging helper
public/
  projects/          # add project screenshots here
  testimonials/       # add avatar images here
  resume.pdf          # add your resume here (referenced by the Hero download button)
```

## Customizing Content

Everything you'd want to edit — your name, roles, bio, skills, projects, experience, education, certificates, testimonials, and social links — lives in **`data/site.ts`**. Update that file and the whole site updates.

To add real images:
1. Drop project screenshots into `public/projects/`.
2. Drop testimonial avatars into `public/testimonials/`.
3. Add your resume as `public/resume.pdf`.
4. Replace the placeholder GitHub/LinkedIn/email URLs in `data/site.ts`.

## Wiring Up the Contact Form

The contact form in `components/contact.tsx` currently simulates a submission. To make it functional, connect it to a service like [Formspree](https://formspree.io), [Resend](https://resend.com), or [EmailJS](https://emailjs.com) inside the `handleSubmit` function.

## Deployment

The easiest way to deploy is [Vercel](https://vercel.com/new):

```bash
npm run build
```

Push this repo to GitHub, then import it in Vercel — it will detect Next.js automatically.

## License

Free to use and modify for your own portfolio.
