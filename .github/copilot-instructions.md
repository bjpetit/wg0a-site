# WG0A Site Authoring Instructions

Use these rules for all future edits to this repository so pages maintain a consistent WG0A look-and-feel.

## Design Goal

Match the operator-focused style used on https://wg0a.net:8443:
- clean, readable, practical, and documentation-first
- light theme with warm neutral surfaces
- clear section cards, simple hierarchy, and low visual noise

## Required Layout Rules

1. Use a centered content column.
- `main` max width: `920px`
- horizontal centering via `margin: 0 auto`
- page padding: `2rem 1rem 3rem`

2. Use card-style sections for content blocks.
- `section` background: `var(--surface)`
- `section` border: `1px solid var(--line)`
- `section` border radius: `12px`
- `section` padding: `1rem`
- `section` top margin: `1rem`

3. Keep a hero section at the top for major pages.
- gradient background using warm-to-cool subtle tones
- rounded corners (`14px`)
- concise intro paragraph

## Required Color and Typography Rules

Use this baseline token set unless a user explicitly requests a redesign:

```css
:root {
  --bg: #f4efe6;
  --surface: #fffaf0;
  --ink: #1e2a2f;
  --muted: #4c5a61;
  --accent: #2f6f74;
  --line: #d9ccba;
}
```

Typography rules:
- body font: `"Trebuchet MS", "Segoe UI", sans-serif`
- body line-height: `1.6`
- heading line-height: `1.2`
- `h1` color: `#7b341f`
- links use accent color and medium/semibold emphasis

## Component Rules

1. Code blocks
- use rounded bordered blocks
- monospaced font (`DejaVu Sans Mono` fallback stack)
- horizontal scroll enabled

2. Tables
- full width tables for comparisons and technical details
- collapsed borders
- bordered cells with consistent padding
- no decorative table effects

3. Callouts
- light tinted background
- left border accent
- short, action-oriented text

4. Labels/Badges
- optional small pill badge above key `h1` titles
- neutral warm background and subtle border

## Content Structure Rules

- Prefer short sections with clear `h2` titles.
- Keep paragraphs concise and operational.
- Prefer concrete command examples over abstract prose.
- For troubleshooting content, include copy/paste command snippets.
- Preserve explicit comparisons when discussing alternatives (for example, systemd vs screen/cron).

## Consistency Rules Across Files

- When updating styles in one HTML page, apply equivalent changes to other pages unless intentionally page-specific.
- Do not introduce a new visual language for a single page.
- Keep spacing rhythm and heading hierarchy consistent across `index.html` and topic pages.

## Change Checklist (Run Before Finalizing)

- Are `:root` tokens consistent with existing pages?
- Does the page use the same layout width and section card pattern?
- Are headings and paragraph spacing visually consistent?
- Do tables/code blocks/callouts follow the same styling approach?
- If one page style changed, were other related pages reviewed for consistency?

If a request conflicts with these rules, follow the user request and then update this file to document the new standard.
