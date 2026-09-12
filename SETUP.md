# MangaAtlas Clean Template

This is a clean, content-free copy of the MangaAtlas GitHub Pages site.

Included:
- Full static site pages and styling
- Admin panel and GitHub token-based upload system
- Empty `data/content.json`
- Empty `data/chapter-dates.json`
- Empty `chapter-images/` and `manga-covers/` folders
- Ads, analytics, SEO files, and scripts

Removed:
- All manga records
- All chapter records
- All chapter images
- All manga cover images
- RAR/archive files
- Supabase files
- Existing sitemap URLs

## Deploy

Upload the contents of this ZIP to the new GitHub Pages repository. For a user site, use `<username>.github.io`; for a project site, the admin detects the first project path segment automatically.

Open `/admin/`, enter a GitHub Personal Access Token with permission to write to the new repository, and connect. The admin will use the current GitHub Pages repository instead of the original MangaAtlas repository.
