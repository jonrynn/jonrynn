# Jon Rynn bibliography

Jon Rynn's bibliography of books, articles, talks and research, moved here from the old Drupal site (`jonrynn.html` on economicreconstruction.org). One hand-written HTML page plus the files it links to. No framework, no build step, no package manager.

- **Repo:** https://github.com/jonrynn/jonrynn (public)
- **Live site:** https://jonrynn.github.io/jonrynn/ via GitHub Pages, publishing from `main` at the repo root. Pushing to `main` updates the live site.
- **Sister site:** the Green New Deal Plan, https://github.com/jonrynn/greennewdealplan. Its `jonrynn.html` redirects here, and the page header here links back to it.

## Layout

```
index.html     the whole bibliography
css/style.css  all styles: color tokens (light + dark), Public Sans font, layout
pdf/           PDFs: papers, dissertation chapters, essays
files/         other documents: slides, audio, spreadsheet, SVG, guest pages
sra/           saved copies of the 17 Sanders Research Associates articles
.nojekyll      tells GitHub Pages to serve files as-is
```

## Page anatomy

- Sections, in order: `#books`, `#articles`, `#talks`, `#sra`, `#dissertation`, `#unpublished`, `#data`, `#guests`. The `.toc` nav at the top links to each. Keep the ids and the nav in step.
- Each work is an `<li>` with `a.title` (or `span.title` when there's no link), an optional `span.tag` for the file type (`PDF`, `PPTX`, `MP3`, …), `span.meta` for publisher and date, and `span.extra` for secondary links.
- Lists of dated works (`ul.works.dated`) wrap the entry in a `<div>` after a `span.year`. Newest first.
- The Sanders Research `<summary>` says "Show all 17 articles". Update the count if articles are added or removed.

## Conventions

- Files hosted here go in `pdf/` or `files/` and are linked relatively (`pdf/APSAPaper.pdf`). Use file names without spaces.
- Copy the `sra/` pages exactly as saved. Their old sandersresearch.com menu images are broken and are left that way.
- For a dead external link, use a web.archive.org copy rather than deleting the entry.
- Colors go in the tokens at the top of `css/style.css`. The page must work in light and dark mode and at phone widths (check 360px and 390px).
- GitHub rejects files over 100 MB and warns over 50 MB. Ask before adding anything that big.

## Still linked to economicreconstruction.org

Jon will decide later what to do with these. Don't move them without asking.

- **"A Green Energy Manufacturing Stimulus Strategy" PDF:** a published book chapter marked "Not for distribution". Don't commit it to this public repo.
- **"Planet Earth needs a global Green New Deal" PowerPoint** (`PlanetEarthNeedsGreenNewDeal.pptx`): 270 MB, almost all uncompressed TIFF images, so over GitHub's file limit. Jon said not to copy it for now. Options when he comes back to it: attach it to a GitHub release, or shrink its images.
- **"Democracy or Disaster" presentation version** (`DemocracyOrDisaster_files/frame.htm`): an old PowerPoint web export made of many files. Jon said it's not important.
- **The *Manufacturing Green Prosperity* book page and the Grist "List of posts"** (globalmakeover.com): web pages, not files.

## Other people's work

`pdf/BeyondCapitalism.pdf` (Olivier Mathey) and `files/JimHaughtonPoems.htm` (Jim Haughton) are by guest writers. They were already public on the old site.

## Checking changes

There's no test suite. Before committing:

- Make sure every local `href`/`src` resolves to a file, and every `#anchor` exists.
- Open the page in a browser at desktop width and phone width, in both light and dark mode.

## Workflow

- Commit and push only when Jon asks.
- Work goes directly on `main`.
