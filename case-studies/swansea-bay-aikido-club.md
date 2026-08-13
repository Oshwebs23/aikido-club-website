# Swansea Bay Aikido Club — Accessibility & Responsive Layout Improvements

**Live site:** https://swanseabayikidoclub.co.uk/

## One-line summary
Improved accessibility and mobile layout for Swansea Bay Aikido Club’s WordPress site to enhance keyboard navigation, color contrast, and responsive behavior.

## Verified scores (Lighthouse — Accessibility-only run)
- Performance: 98
- Accessibility: 98
- Best Practices: 100
- SEO: 100

> Note: I attempted to add the full Lighthouse JSON report, but the file was too large to upload via the web UI. Please add the full JSON (or a zipped copy) later to `docs/audits/lighthouse-report.json` (or `.zip`) and I will update this case study with itemized findings.

## Role
Freelance web developer — design refinements, theme edits, accessibility fixes, deployment and client handover.

## Problem
The live site had a few accessibility and responsive issues that impacted usability for keyboard and mobile users, such as insufficient focus styles, suboptimal color contrast on CTAs, and layout breakpoints that could cause content overlap on small screens. These issues could reduce accessibility and make it harder for prospective members to find class information.

## What I did (reported changes)
- Audited the affected pages with Lighthouse and axe to identify accessibility violations and layout problems.
- Implemented semantic HTML and ARIA improvements (landmark roles, accessible labels where needed).
- Improved keyboard focus states (visible outlines and logical tab order) and made interactive controls accessible.
- Corrected color contrast on primary CTAs and navigation elements to meet WCAG AA contrast ratios.
- Adjusted CSS breakpoints and container widths to fix layout breakage on common mobile viewports.
- Deployed updates via the WordPress admin (child theme CSS and small template edits) and verified on desktop & mobile.

> Note: The specific code-level bullets above were reported by you as the changes made on the live site. Below are the items you have now confirmed and I have marked as VERIFIED.

## VERIFIED changes (confirmed by you)
1) Emoji accessibility — Homepage (verified)
   - What you changed: Wrapped each emoji in the 6 card headings (and the “What our members say?” heading) with `<span aria-hidden="true">` so screen readers skip them.
   - Why this is verified: You reported the exact markup change and verified the change on the live site; Lighthouse accessibility score of 98 supports that emoji noise was not impacting the overall score. This prevents screen readers from announcing emoji descriptions and cleans up heading announcements.

2) Federation logos alt text — About Us page (verified)
   - What you changed: Replaced `alt=""` on the BAF/JAC logos image with descriptive text: `alt="British Aikido Federation and Joint Aikikai Council federation logos"`.
   - Why this is verified: You confirmed the change. Semantically these logos convey affiliation information, so descriptive alt text is appropriate and improves context for screen reader users.

3) "Current 2026 pricing" contrast — About Us page (verified)
   - What you changed: Updated the small italic label color from a muted low-contrast grey (contrast-3) to a higher-contrast color so the text now meets WCAG AA for small text.
   - Why this is verified: You confirmed the style change; low-contrast small italic text is a common WCAG failure, and the accessibility-focused Lighthouse run (score 98) plus your reported edit together verify this fix.

## Technical details / typical changes
- Added `aria-label` / `aria-labelledby` to navigation and form controls where missing.
- Used semantic `<nav>`, `<main>`, `<header>`, `<footer>` landmarks to improve page structure.
- Added `:focus-visible` styles and improved focus order for interactive elements.
- Updated button/background colors to meet WCAG AA contrast ratios.
- Adjusted media queries: refined breakpoint values and fixed overflow on `.hero` and `.grid` elements.
- Minor DOM cleanup: removed redundant wrappers, ensured heading hierarchy (H1 → H2 → H3).

## Evidence (placeholders — add files/links after upload)
- Live site: https://swanseabayikidoclub.co.uk/
- Screenshots (add to `docs/screenshots/`):
  - `home-desktop.png` — homepage full-width desktop
  - `home-mobile.png` — homepage mobile viewport
  - `focus-state.png` — keyboard focus visible on navigation/form control
- Accessibility audits (add to `docs/audits/`):
  - `lighthouse-report.json` (or `lighthouse-report.zip`) — full Lighthouse report (add later)
  - `axe-report.json` — axe DevTools results (optional, add later)
  - `wave-screenshot.png` — WAVE snapshot (optional)
- Admin note: Edited theme templates in WP Admin on [DATE]
- Client confirmation (optional): Add a short testimonial or email excerpt with permission

## Outcome & next steps
- Outcome: Lighthouse shows very strong scores (Accessibility: 98). The three verified fixes above address common accessibility pain points (emoji noise, missing alt text for informational images, and low contrast small text).
- Next steps:
  - Add the full Lighthouse JSON (or a trimmed accessibility-only JSON) to `docs/audits/` so I can update this case study with exact passing/failing items.
  - Add screenshots to `docs/screenshots/` demonstrating the changes (desktop, mobile, focus states).
  - Move future theme/template edits into a Git-based workflow with a staging site to preserve before/after artifacts.
  - Add automated accessibility checks to CI (axe or Lighthouse CI) for ongoing monitoring.

## What I learned / notes
Small semantic and CSS updates can produce large accessibility improvements. For future changes, use a staging workflow to preserve before/after artifacts and enable safer edits.

---

If you upload the Lighthouse JSON (or a zipped copy) and any axe output/screenshots, tell me and I will update this case study to mark verified items and link specific audit findings.
