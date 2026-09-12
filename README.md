# MangaAtlas

Clean GitHub Pages manga discovery site with a GitHub-only content/admin system.

## Repository

- Owner: `mangaatlasraw`
- Repository: `mangaatlasraw.github.io`
- Branch: `main`
- Content database: `data/content.json`
- Manga covers: `manga-covers/`
- Chapter images: `chapter-images/`
- Admin: `admin/`

## Admin

Open `/admin/` and connect a GitHub Personal Access Token that has Contents read/write access to this repository. The admin auto-detects the current GitHub Pages owner/repository, but both fields remain editable for project-site use.

The token is kept in `sessionStorage` only and is not written to the repository.

Admin supports:
- manga create/edit/delete
- cover upload with WebP compression
- chapter create/edit/delete
- chapter image upload in Part 1 (1–10) and Part 2 (11–20)
- image compression/conversion and progress messages
- deletion of chapter images
- automatic `content.json` updates
- automatic sitemap regeneration after content changes

## Clean state

The initial database is intentionally empty. No old manga, chapters, covers or chapter images are included.

## GitHub Pages

The site uses relative paths and the current repository origin. No old MangaAtlas repository, Supabase project, Vercel deployment, or hardcoded legacy content API is required.

Google Search Console verification is included with the supplied verification meta tag.
