# David🥧

[![Netlify Status](https://api.netlify.com/api/v1/badges/057ee517-cc9d-4846-b5a8-5a1d044f4b88/deploy-status)](https://app.netlify.com/sites/davidpie/deploys)

My personal website, built from [eleventy-base-blog v9](https://github.com/11ty/eleventy-base-blog).

Incorporates [CSSBox](https://github.com/TheLastProject/CSSBox) for the Gallery page.

## Todo

- [ ] Make 'notes' and 'links' tag icons for home/archives post listings.
- [x] Change Home to have blog post exerpts + notes
- [ ] Integrate music/spotify api for currently listening
- [x] Redesign Home to be more minimal/typographic
	- [x] add color with paint covering background
	- [x] Add sections for blog, gallery, notes
- [ ] Make notes section browsable by tags

## Getting Started

1. Clone this Repository

```
git clone https://github.com/dapierce/dapierce.github.io.git
```

2. Navigate to the directory and install packages

```
npm install
```

3. Run Eleventy

Generate a production-ready build to the `_site` folder:

```
npx @11ty/eleventy
```

Or build and host on a local development server:

```
npx @11ty/eleventy --serve
```

Or you can run [debug mode](https://www.11ty.dev/docs/debugging/) to see all the internals.

---
The rest is from [eleventy-base-blog v9](https://github.com/11ty/eleventy-base-blog) `README.md`

## Features

- Using [Eleventy v3](https://github.com/11ty/eleventy/releases/tag/v3.0.0) with zero-JavaScript output.
	- Content is exclusively pre-rendered (this is a static site).
	- Can easily [deploy to a subfolder without changing any content](https://www.11ty.dev/docs/plugins/html-base/)
	- All URLs are decoupled from the content’s location on the file system.
	- Configure templates via the [Eleventy Data Cascade](https://www.11ty.dev/docs/data-cascade/)
- **Performance focused**: four-hundos Lighthouse score out of the box!
	- _0 Cumulative Layout Shift_
	- _0ms Total Blocking Time_
- Local development live reload provided by [Eleventy Dev Server](https://www.11ty.dev/docs/dev-server/).
- Content-driven [navigation menu](https://www.11ty.dev/docs/plugins/navigation/)
- Fully automated [Image optimization](https://www.11ty.dev/docs/plugins/image/)
	- Zero-JavaScript output.
	- Support for modern image formats automatically (e.g. AVIF and WebP)
	- Processes images on-request during `--serve` for speedy local builds.
	- Prefers `<img>` markup if possible (single image format) but switches automatically to `<picture>` for multiple image formats.
	- Automated `<picture>` syntax markup with `srcset` and optional `sizes`
	- Includes `width`/`height` attributes to avoid [content layout shift](https://web.dev/cls/).
	- Includes `loading="lazy"` for native lazy loading without JavaScript.
	- Includes [`decoding="async"`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/decoding)
	- Images can be co-located with blog post files.
- Per page CSS bundles [via `eleventy-plugin-bundle`](https://github.com/11ty/eleventy-plugin-bundle).
- Built-in [syntax highlighter](https://www.11ty.dev/docs/plugins/syntaxhighlight/) (zero-JavaScript output).
- Draft content: use `draft: true` to mark any template as a draft. Drafts are **only** included during `--serve`/`--watch` and are excluded from full builds. This is driven by the `addPreprocessor` configuration API in `eleventy.config.js`. Schema validator will show an error if non-boolean value is set in data cascade.
- Blog Posts
	- Automated next/previous links
	- Accessible deep links to headings
- Generated Pages
	- Home, Archive, and About pages.
	- [Atom feed included (with easy one-line swap to use RSS or JSON](https://www.11ty.dev/docs/plugins/rss/)
	- `sitemap.xml`
	- Zero-maintenance tag pages ([View on the Demo](https://eleventy-base-blog.netlify.app/tags/))
	- Content not found (404) page
