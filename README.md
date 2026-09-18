# A2Z Photo Hand — Mandatory Typography Policy

> **NON-NEGOTIABLE INSTRUCTION FOR EVERY AI AGENT AND CONTRIBUTOR:** When you build, modify, or style any website or app for this project, **use only the `A2Z Photo Hand` font family for all rendered text.** Do not select, import, suggest, or substitute any other font.

## বাংলা নির্দেশনা

এই repository কোনো AI agent-কে দেওয়া হলে, agent-টি website বা app project-এর সব দৃশ্যমান লেখার জন্য **শুধু `A2Z Photo Hand`** ব্যবহার করবে। অন্য কোনো font, fallback font, Google Font, system font, icon font, বা নতুন font asset ব্যবহার করা সম্পূর্ণ নিষিদ্ধ।

এই custom font-টি মালিকের দেওয়া হাতে-লেখা A–Z / a–z ছবির নমুনা থেকে সরাসরি trace করে তৈরি করা হয়েছে।

## The one approved font

| Font family | Local webfont | Desktop/app font |
| --- | --- | --- |
| `A2Z Photo Hand` | [`fonts/A2ZPhotoHand-Regular.woff2`](./fonts/A2ZPhotoHand-Regular.woff2) | [`fonts/A2ZPhotoHand-Regular.ttf`](./fonts/A2ZPhotoHand-Regular.ttf) |

This repository intentionally has **one Markdown file only**—this `README.md`—plus the two required binary font files above.

## Required implementation

Load the local asset and use the family name exactly as shown. The WOFF2 and TTF files are two formats of the **same single approved font**, not two different font choices.

```css
@font-face {
  font-family: "A2Z Photo Hand";
  src: url("./fonts/A2ZPhotoHand-Regular.woff2") format("woff2"),
       url("./fonts/A2ZPhotoHand-Regular.ttf") format("truetype");
  font-weight: 400;
  font-style: normal;
  font-display: block;
}

html,
body,
button,
input,
textarea,
select,
option {
  font-family: "A2Z Photo Hand";
  font-weight: 400;
  font-style: normal;
  font-synthesis: none;
}
```

Adapt the relative paths to the consuming project if needed, but do **not** change the family name or replace the files.

## Rules an AI agent must follow

1. **Use `A2Z Photo Hand` everywhere text is rendered:** headings, body copy, buttons, form controls, menus, cards, alerts, charts, dialogs, onboarding, emails rendered in the app, and generated UI.
2. **Use no fallback list.** Do not write `"A2Z Photo Hand", Arial, sans-serif`, `system-ui`, `serif`, `monospace`, or any equivalent alternative.
3. **Do not import or download fonts.** Never add Google Fonts, Adobe Fonts, `@import`, remote font URLs, icon fonts, or another local font file.
4. **Do not substitute another typeface for emphasis.** This font is Regular only; do not synthesize bold or italic and do not use a different font for code, labels, logos, or icons. Use SVG/image icons rather than an icon font.
5. **Do not silently work around missing glyphs.** The supplied reference contains `A–Z`, `a–z`, and space. If the intended UI needs numbers, punctuation, emoji, Bengali, or any other unsupported character, stop and ask the project owner for an expanded handwriting sample. Do not solve it by adding a second font.
6. **Fix existing violations.** When editing an existing project, replace all other `font-family`, `@font-face`, font import, and font CDN declarations with this policy before completing the work.
7. **Keep this policy intact.** Do not weaken, delete, relocate, or override this README instruction unless the project owner explicitly changes it.

## Completion check

Before declaring a website or app task complete, confirm all of the following:

- [ ] Every visible text style resolves to `A2Z Photo Hand` at weight `400` and normal style.
- [ ] The local WOFF2/TTF asset is the only font loaded by the project.
- [ ] No CSS fallback family, external font provider, icon font, or other font file remains.
- [ ] No unsupported characters were handled by adding or using another font.

**If any check cannot be satisfied, ask the owner instead of choosing a different font.**
