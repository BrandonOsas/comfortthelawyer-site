# ComfortTheLawyer — Ebook Launch Landing Page

## What this is
A landing page for Comfort Iyiewuare's Employment Tribunal ebook launch. Built for
her business "ComfortTheLawyer" — a resource for litigants-in-person (primarily
Black women) navigating UK Employment Tribunals without legal representation.

## Stack
- Single static HTML file (`comfortthelawyer-clone.html` / deployed as `index.html`)
- Plain HTML/CSS/JS — no build step, no framework
- Hosted on Netlify (free tier)
- Domain: comfortthelawyer.com, registered on Namecheap, DNS pointed at Netlify
  nameservers (dns1-4.p01.nsone.net)

## What's done
- Full page layout cloned from the original MailerLite landing page: hero,
  feature checklist, about section, waitlist/pricing section, testimonials,
  FAQ accordion, contact section, footer
- Countdown timer (currently a placeholder set to 14 days from page load —
  needs the real launch date hardcoded in the `<script>` block)
- Contact form wired to **Netlify Forms** (`data-netlify="true"`, honeypot
  field included) — submits via fetch, shows success/error message
- **Calendly booking widget** wired in for 1-on-1 sessions
  (https://calendly.com/comfortthelawyer/30min) — popup widget with a
  fallback to opening in a new tab if the Calendly script fails to load
  (e.g. blocked by an ad blocker)
- Placeholder visuals built in pure CSS (no real image files yet):
  - Book cover mockup (burgundy box, title + author name) in the hero
  - Author avatar ("CI" initials) in the About section
  - Testimonial avatars ("ER" / "SA" initials)
- Domain DNS is set up and resolving (confirmed working on mobile data;
  was a local DNS cache issue on the owner's Mac/Arc browser, not a real bug)

## What's NOT done yet / next steps
1. **Stripe Payment Link** — "Pre-Order Now" button still needs a real Stripe
   Payment Link wired in for the ebook pre-order
2. **Real testimonials** — still placeholder names/quotes (Emily Rodriguez,
   Sophia Adichie) — need real reader testimonials before launch, or remove
   the section until there are some
3. **Real images** — no real book cover, author photo, or testimonial photos
   yet. CSS placeholders are in place and can be swapped for real `<img>`
   tags whenever assets are ready
4. **Countdown timer real date** — needs the actual ebook launch date/time
   hardcoded (currently just "14 days from whenever the page loads")
5. **Email list / launch announcements** — MailerLite was dropped in favor
   of a fully custom build. Still need a lightweight way to email people at
   launch (options discussed: Buttondown, or a Google Form → Google Sheet)

## Decisions already made (don't re-litigate unless asked)
- No Python/Flask backend — going with static HTML + no-code tools
  (Netlify, Netlify Forms, Calendly, Stripe Payment Links) to keep hosting
  free and avoid maintaining a server
- No MailerLite — fully custom build instead
- No Formspree — using Netlify Forms since hosting is already on Netlify
- Booking must stay on-page as a popup, not send visitors to an external site
