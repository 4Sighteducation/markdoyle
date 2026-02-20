# Mark Doyle CV Website

- Public CV page: `/`
- Editor (Decap CMS): `/admin/`

## Local dev

```bash
npx -y pnpm@latest install
npx -y pnpm@latest run dev
```

## Editing content

The CV content lives in `src/content/cv.json`.

In production, edits happen via `/admin/` and are committed back to GitHub, then Vercel redeploys.

## Printing

Use the **Print / Save as PDF** button on the page. The layout is designed as an A4-like page on desktop, and print CSS is applied so the PDF matches what you see.

