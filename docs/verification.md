# Verification — 2026-08-31

- Static preview at `http://127.0.0.1:4173` returns HTTP 200.
- Checked desktop (1710px), tablet (768px), and phone (390px and 320px) layouts. No horizontal document overflow at those widths.
- Inspected the hero, publication list, education/industry section, and contact/footer visually in the browser.
- All four publication filters return the intended counts: all 4; Video-LLMs 2; recognition 1; efficiency 1. Active state and screen-reader announcement update.
- Honors expand by click and collapse with Enter. Top navigation and back-to-top links work; contact highlights correctly at the document bottom.
- Four individual BibTeX links point to four distinct existing files. All local links, fonts, CSS resources, and fragment targets resolve; IDs are unique; the page has one h1.
- The paper image loaded successfully. No browser console warnings or errors were recorded from the site.
- `node --check assets/site.js` and `git diff --check` passed.
- Main content and citation downloads are static HTML. Filters are only shown once JavaScript runs; reduced-motion and print styles are included. No separate no-JavaScript browser emulation was performed.
- All three arXiv abstract links, the linked PDF, GitHub profile/repository, Google Scholar, and SPIE DOI destination responded successfully in HTTP checks. The IEEE DOI resolves to the intended IEEE document with HTTP 202; full publisher content was not verified.
- Tianjin University's old English path was replaced with its currently indexed official English site, `https://en.tju.edu.cn/`. Search independently confirms that destination; direct command-line HTTPS access encounters a TLS connection error in this environment, so it is not claimed to pass the local HTTP probe.
- GitHub API confirmed the existing Pages source: `main`, `/`, legacy build, custom domain `junzhec.top`. The initial preview did not change remote content, deployment settings, or DNS records. The owner subsequently authorized publishing to this existing source.
- Screenshots are saved locally under `.preview/` (gitignored).

The previous homepage remains in Git history. On 2026-08-31 the owner confirmed JHU dates (January 2024–May 2025), their Ph.D. status at Tianjin University, and authorization to publish this redesign to the existing `main` branch. Deployment completion must be checked against the Pages build status and the live homepage.

## 2026-10-15 academic style revision

- Replaced the decorative design with a white academic layout: left profile sidebar, right content column, standard section headings, blue resource links, and numbered text publications. All four titles and complete author lists are retained. Preprints and peer-reviewed publications are explicitly grouped.
- Rechecked the supplied Google Scholar profile on 2026-10-15; its table still lists these four publications. Retrieved the public profile successfully after the web retrieval service returned HTTP 429. The current source does not claim unlisted conference acceptances.
- Inspected the new desktop layout visually at the normal 1280px viewport, and checked 768px, 390px, and 320px widths. None has horizontal document overflow. On mobile the sidebar becomes a profile block above the main content.
- Checked publication and education anchor navigation against the sticky header. The destinations appear below the header. Awards are now visible without expanding a disclosure.
- Confirmed all four paper titles, the owner-confirmed Ph.D. role, January 2024–May 2025 JHU dates, and the original CNAME are retained. Checked local citation/resources and fragment destinations; the document has one h1 and unique IDs.
- The HTML has no scripts and loads no external font, decoration image, or tracking resource. All page content and resource links work without JavaScript.
- README and content-source notes describe the current structure. Previous design assets remain in the repository for provenance but are not used by the page.
- `git diff --check` passed. Local preview returns HTTP 200. Detailed external-link responses and before/after screenshots are under `.preview/2026-10-15/` (gitignored).

## 2026-10-15 icons, advisor, and illustrated publications

- Added the owner-confirmed advisor Xiaojie Guo (郭晓杰) to the biography and both page sidebars, linking to his verified personal homepage.
- Added restrained teal accents and local decorative Lucide icons, retaining text labels and the academic two-column structure.
- Added an independent `publications.html` with four complete paper entries, grounded descriptions, original figures for SlotNarrative/TOC-Bench/LCPAQ, per-paper jump links, full-size image links, PDFs, code where public, and BibTeX. Semi-RSTOD retains a text introduction because the publisher's public request returned an anti-bot message; no figure is invented.
- Homepage research highlights preview the two recent video papers and link directly to their publication sections. Small image derivatives reduce homepage image transfer to about 640 KiB while keeping original files accessible.
- Compared all four complete author lists against the preceding version. All match. Confirmed the existing JHU dates, Ph.D. status, and CNAME are preserved.
- Checked all local page/fragment links, image alt attributes and files, unique IDs and one h1 per page, local CSS icon references, and page-specific title/canonical/Open Graph metadata.
- HTTP checks passed for 29 distinct local pages and linked resources, including figures, icon SVGs, and citations.
- Visually inspected homepage and illustrated publications on desktop; inspected the TOC-Bench and LCPAQ figures and their descriptions. All three publication figures loaded. Checked the publication page at 320px, 390px, 768px, and 1280px without horizontal overflow, and the homepage at 390px.
- Confirmed homepage-to-paper and back-to-home navigation, publication jump links, and target positions below the fixed header. The page does not require JavaScript.
- `git diff --check` passed. Local screenshots and preparation notes are stored under `.preview/2026-10-15-publications/` (gitignored).

## Semi-RSTOD fourth illustration

- Added a source-grounded explanatory SVG with the same figure/caption/full-size-link layout as the other three papers. The page now has four figures across four articles.
- The original figure was not publicly available behind the SPIE subscription boundary. The new graphic and caption explicitly identify it as a schematic redrawn from the publisher's abstract.
- Parsed the SVG as XML; checked its linked local path and meaningful alt text. Inspected its desktop rendering and verified the image loaded. At 390px the document has no horizontal overflow and the full-size link resolves to the SVG.
- No browser console errors or warnings were recorded. `git diff --check` passed.
