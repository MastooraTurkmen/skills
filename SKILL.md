---
name: accessibilty-checklist
description: Run the full checlist across code quality, and accessibility. Report each item as PASS, FAIL, or MANUAL (requires browser/external tool).
user_invocable: true
---


# Accessibility (A11Y)
- [ ] **Lang attribute** — Verify `<html lang="en">` (or appropriate language) is set in the document
- [ ] **Image alt text** — Every `<img>` must have an `alt` attribute; decorative images should have `alt=""`; meaningful images need descriptive alt text
- [ ] **Heading hierarchy** — Verify headings follow a logical structure (one `<h1>`, `<h2>` under sections, no skipped levels like `<h1>` → `<h3>`)
- [ ] **Skip links** — Check for a "Skip to main content" link as the first focusable element in the DOM
- [ ] **Form labels** — Every form input must have an associated `<label>` (via `for`/`id` or wrapping); check for `autocomplete` attributes on name/email/phone fields
- [ ] **Accessible error handling** — Form error messages must use `role="alert"` or `aria-live` so screen readers announce them
- [ ] **Tab accessibility** — Verify all interactive elements are reachable via Tab key (no missing `tabindex`, no focusable elements hidden from tab order)
- [ ] **ARIA landmarks** — Verify landmark roles are used (`role="banner"`, `role="navigation"`, `role="main"`, `role="contentinfo"`) or equivalent semantic HTML5 elements
- [ ] **Role/Name/Value** — Buttons must have accessible names, form inputs have labels, custom controls have appropriate `role`, `aria-label`, or `aria-labelledby`
- [ ] **Color contrast** — Check CSS color values against WCAG AA contrast ratios (4.5:1 for normal text, 3:1 for large text). Brand colors: Black `#201F1F` on Ivory `#EFEFEF` and White `#FFFFFF`
- [ ] **Prefers-reduced-motion** — Verify CSS includes `@media (prefers-reduced-motion: reduce)` to disable or simplify animations
- [ ] **Keyboard navigation** — Trace tab order through the DOM; verify focus styles are visible (`:focus` or `:focus-visible`); confirm no keyboard traps exist
- [ ] **Screen reader readability** — Check that content reads logically in DOM order; verify `aria-hidden` is used appropriately; check for meaningful link text (no "click here")
### Manual A11Y (flag for human tester)
- [ ] **MANUAL: AXE DevTools / WAVE** — Run website through AXE DevTools or WAVE to catch remaining issues
- [ ] **MANUAL: Screen reader testing** — Manually test with a screen reader (VoiceOver, NVDA)
- [ ] **MANUAL: Accessibility statement** — Verify an accessibility statement exists with contact info for reporting issues
