ds-personal-website
====================

Project structure
-----------------

Root
- index.html (main portfolio)
- template.json (page-generation brief)
- assets/
	- images/
		- profile_pic.jpg (or optimized versions)
		- projects/
			- sentiment/ (images for the Sentiment case study)
- projects/
	- sentiment/
		- index.html (case study page)

Conventions
-----------
- New case studies live under `projects/<slug>/index.html`.
- Project-specific images live under `assets/images/projects/<slug>/`.
- Use relative links from project pages back to `../../index.html`.

Adding your 3 images (Sentiment project)
----------------------------------------
Place your images into:
`assets/images/projects/sentiment/`

Suggested filenames:
- `tfidf-similarity.png` (for Content Similarity)
- `emotion-distribution.png` (for Sentiment Analysis)
- `cluster-map.png` (for Clustering)

Then replace the placeholders in `projects/sentiment/index.html`:
- Find the three `<div class="img-slot">` blocks under the Approach section and swap each with an `<img>` tag, e.g.:
	`<img src="../../assets/images/projects/sentiment/tfidf-similarity.png" alt="TF‑IDF similarity visualization" style="width:100%;border:1px solid var(--border);border-radius:12px;" loading="lazy" />`

Adding a new project page
-------------------------
1. Create a folder: `projects/<slug>/` and an `index.html` using `projects/sentiment/index.html` as a starting point.
2. Add images to `assets/images/projects/<slug>/` and reference with `../../assets/images/projects/<slug>/...`.
3. In `index.html` (root), link the project card title to `projects/<slug>/index.html`.

Notes
-----
- Keep CSS/JS inline per page for simplicity; reuse tokens and class names for a consistent look.
- If you prefer a build step later, we can extract shared CSS/JS into `/assets/` and set up a bundler.