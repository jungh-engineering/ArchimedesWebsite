# Header Redesign — Descriptions Only (Matches Reference)

> Solid, opaque header. Links on the left. Logo centered. “Apply” button on the right. Spacing via box model: container width, paddings, gaps, borders, fixed height.

## 1) Structure
- One sticky header bar at the top. No transparency or blur.
- Single row with three zones:
  1. **Primary nav (left):** About, Teams, FAQ, Sponsor, Contact.
  2. **Logo (center):** lightbulb/gear mark, visually centered.
  3. **Primary CTA (right):** “Apply” outlined button.
- Mobile adds a hamburger at far left; logo stays centered; CTA stays right until very narrow.

## 2) Box Model and Spacing
- **Header container:**
  - Full‑width.
  - Fixed height desktop ~64px; tablet/mobile ~56px.
  - Solid dark background; 1px bottom divider.
- **Inner row:**
  - Max width ~1280px.
  - Horizontal paddings ~24px desktop, ~20px tablet/mobile.
  - Three‑zone layout: left start, center center, right end.
- **Nav items:**
  - Horizontal gap ~24px desktop, ~20px tablet.
  - Clickable height equals header height.
  - No underlines; base opacity slightly muted; hover/focus full.
- **Logo:**
  - Locked to exact horizontal center of viewport.
  - Icon height ~32px; no extra margins.
- **CTA button:**
  - Outlined yellow stroke with matching text.
  - Corner radius ~12px.
  - Inner padding ~10px vertical, ~18px horizontal.
  - Hover/focus: fill turns yellow, text turns dark.
- **Hamburger (mobile):**
  - Three thin bars; hidden on desktop; shown ≤768px.

## 3) Alignment and Rhythm
- Vertical centering for all items.
- Left group aligns to inner left padding edge.
- Right CTA aligns to inner right padding edge.
- Logo remains centered regardless of left/right widths.

## 4) States and Interactions
- Hover: nav opacity increases to full.
- Focus visible: 2px high‑contrast ring on links, button, hamburger.
- Active: no layout shift.
- Sticky on scroll; no opacity change.

## 5) Content and Copy
- Left links order: **About · Teams · FAQ · Sponsor · Contact**.
- Right button text: **Apply**.
- Logo alt: “Site logo”.

## 6) Responsive
- ≤1024px: header height ~56px; gaps and paddings reduce to ~20px.
- ≤768px: hide left nav; show hamburger; layout = **hamburger | logo | CTA**.
- ≤420px: hide CTA; layout = **hamburger | logo**.

## 7) Accessibility
- Keyboard order: nav → logo → CTA → hamburger.
- Visible focus indicators on dark background.
- Maintain WCAG‑appropriate contrast.
- Primary nav labeled for assistive tech; hamburger manages expanded state.

## 8) Reference Mapping
- Solid dark header, not transparent, matches screenshot.
- Five left links with even spacing.
- Centered logo not affected by side content.
- Right “Apply” is rounded, outlined, thin border, yellow.
- Subtle bottom divider line.

## 9) Do/Don’t
- **Do:** keep logo centered independent of nav/CTA width.
- **Do:** keep nav hit‑targets full header height.
- **Don’t:** use transparency, blur, or animated underlines.
- **Don’t:** let CTA wrap or push logo off center.
