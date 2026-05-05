# Phixzen — Premium Brand Landing Site

A polished, fully responsive single-brand site for **Phixzen**, featuring two hero products (Aqua-Clear Anti Fog Spray and Instant Smooth Anti Wrinkle Spray) with a premium wellness-tech aesthetic.

## Visual Direction

- **Palette:** deep teal primary, muted gold accent, warm cream background, soft white surfaces, charcoal text
- **Style:** glassy product cards, soft layered shadows, botanical/zen line accents, generous whitespace
- **Typography:** elegant serif display headings (Fraunces/Playfair) + clean sans body (Inter)
- **Motion:** smooth scroll, subtle fade/slide reveals on scroll, gentle hover lifts on cards/buttons
- **Imagery:** placeholder product bottle mockups (gradient + bottle silhouette) clearly marked for easy swap with real product photos later

## Page Structure (single landing page, anchored sections)

1. **Sticky header / nav** — Phixzen wordmark, links (Home, Products, How It Works, Benefits, Safety, Contact), gold "Order Now" CTA, mobile drawer
2. **Hero** — headline "Upgrade your life, achieve your zen.", subheading, two product bottles side by side on a soft teal/cream gradient with botanical accents, dual CTAs ("Shop Products", "Explore Benefits"), 4 trust badges (Made in Pakistan, Premium Quality, Easy Daily Use, Compact & Travel Friendly)
3. **Product showcase** — two glass cards (Aqua-Clear, Instant Smooth) with tagline, description, "Best for" chips, key benefits list
4. **Split product detail sections** — alternating image/copy layout for each product with use-case icon grid
5. **How It Works** — tabbed interface switching between Aqua-Clear (Clean → Spray → Buff) and Instant Smooth (Hang → Spray → Smooth) with numbered step cards
6. **Benefits** — 8 premium icon cards in a responsive grid
7. **Brand story "Meet Phixzen"** — centered editorial block with zen accent
8. **Safety / Cautions** — accordion with two groups (Aqua-Clear, Instant Smooth)
9. **Product comparison** — clean responsive table (stacks on mobile)
10. **FAQ** — accordion with all 8 questions
11. **Order / Contact form** — name, email, phone, product dropdown (Aqua-Clear / Instant Smooth / Both), quantity, message, "Submit Order Inquiry" button (with Zod validation, success toast)
12. **Footer** — brand, tagline, contact placeholders (www.phixzen.com, info@phixzen.com, Islamabad), quick links, social icon placeholders

## Components to build

- `Header`, `Hero`, `ProductShowcase`, `ProductDetail` (reusable, alternating), `HowItWorks` (tabs), `Benefits`, `BrandStory`, `Safety` (accordion), `Comparison`, `FAQ` (accordion), `ContactForm`, `Footer`
- `ProductBottle` placeholder mockup component (SVG-based bottle silhouette with gradient label, swap-ready)
- Reusable `Reveal` wrapper for scroll-in animations

## Technical Details

- TanStack Start route: replace `src/routes/index.tsx` placeholder with the full landing page composition
- Tailwind v4 design tokens added in `src/styles.css`: teal/gold/cream semantic colors in oklch, plus reveal/fade keyframes
- shadcn primitives reused: `button`, `card`, `accordion`, `tabs`, `input`, `textarea`, `select`, `label`, `sonner` (toasts), `form`
- Form validation with `zod` + react-hook-form; submission shows success toast (no backend wired — inquiry stub)
- Smooth in-page scroll for nav links via anchor IDs
- IntersectionObserver-based reveal animations (lightweight, no extra deps)
- Fully responsive: mobile-first, tablet, desktop breakpoints; mobile nav drawer via `sheet`
- SEO: route `head()` with Phixzen title, description, og tags
- Deploy-ready on existing TanStack Start + Cloudflare Worker setup

## Out of scope (for this plan)

- Real product photography (placeholders only, swap-ready)
- Real e-commerce checkout / payments
- Backend persistence of order inquiries (form is UI-complete, ready to wire later)
