# MangaAtlas — GitHub Pages setup

This repository is the clean new MangaAtlas deployment.

## 1. GitHub Pages

In GitHub: Settings → Pages → Deploy from a branch → `main` / root.

The repository already contains `.nojekyll` and uses relative URLs, so the same code works for a user site or a project site.

## 2. Admin access

Open `/admin/` on the deployed site. Enter a GitHub Personal Access Token with repository Contents read/write permission.

The admin detects `owner/repository` from the current GitHub Pages hostname. You can also edit those fields manually before connecting.

Do not put the token in source code, JSON, or Git history. The browser stores it only in `sessionStorage` and the Forget token button clears it.

## 3. Content model

`data/content.json` starts empty:

```json
{
  "version": 1,
  "mangas": [],
  "chapters": []
}
```

Admin creates manga records, uploads covers to `manga-covers/<slug>/cover.webp`, creates chapters, and uploads chapter pages to `chapter-images/<manga-id>/chapter-<number>/`.

## 4. URLs

Manga: `manga.html?slug=<manga-slug>`

Chapter: `chapter.html?slug=<chapter-slug>`

The GitHub Pages 404 fallback also supports `/manga/<slug>` and `/chapter/<slug>` on a user-site deployment.

## 5. SEO

The homepage and content pages include canonical metadata, Open Graph basics, robots rules, sitemap support and the supplied Google Search Console verification meta tag.

The admin regenerates `sitemap.xml` whenever manga/chapter content changes.
