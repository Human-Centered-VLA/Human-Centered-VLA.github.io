# Human-Centered VLA — single-page website

Open **`index.html` directly in your browser**. No build, server, package
installation, or network connection is needed to view the page and use its
search, filters, figure viewer, or citation selection.

Keep the `assets/` folder beside `index.html` so figures and original PDFs load.
External paper and GitHub links naturally require internet access.

The site is prepared for publication through GitHub Pages.

## Included on the page

- Survey title, all 19 authors, and affiliations.
- Prominent “Read preprint” button and navigation link to https://www.preprints.org/manuscript/202610.2762.
- Use-case perspectives and lifecycle framework.
- All five original manuscript figures, with zoom and PDF links.
- The five comparison tables included by `overleaf/main_arxiv.tex`:

  | Manuscript table | Entries |
  | --- | ---: |
  | Design-time learning-based alignment | 24 |
  | Deployment-time runtime safeguards | 26 |
  | OOD runtime triggers and responses | 7 |
  | Safety benchmarks and evaluation | 21 |
  | Adversarial and backdoor attacks | 19 |

- A searchable reference collection with 182 unique references.
- Research outlook, repository citation, and contribution links.

All tables and references are included in the HTML. JavaScript opens the
manuscript tables and enables interactive figure viewing and reference filters.
Wide comparison tables scroll horizontally and keep the method column visible.
The page uses the figures' deep purple
(`#45008b`), navy (`#062870`), teal, and green accents.

## Page organization

The page follows a numbered outline: overview, lifecycle taxonomy, research
landscape, manuscript comparisons, architectures, outlook, references, and
citation. A persistent contents column provides section links on desktop and
becomes a compact dropdown on smaller screens.

The five manuscript tables are grouped under design, deployment, and validation
and are shown in full. Supplementary paper groupings remain collapsible.
Lifecycle cards link directly to the corresponding table. The landscape and
timeline figures are paired, and the reference collection scrolls within its
own panel. All 182 references remain in the page.

## Files and maintenance

- `index.html`: the finished page, including its CSS, JavaScript, manuscript
  tables, and embedded reference data. Edit this file directly.
- `assets/`: figure images, original PDFs, favicon, and the five original table
  `.tex` files under `source-tables/`.
- `reference_audit.csv`: reference provenance from the survey repository.
- `citation.bib`: repository citation; this does not assert manuscript publication.
- `table-provenance.json`: table source paths, row counts, and citation links.
- `.github/workflows/pages.yml`: optional manual publishing workflow.

The comparison tables use the **active Overleaf manuscript tables**, including
multi-level columns, method groups, annotations, incident coverage, and captions.
Commented-out rows and unused alternative tables are excluded. Checkmark and
cross meanings follow each original caption; a cross is not reinterpreted as a
claim of unsafe behavior. The reference list remains the accompanying audited
README collection rather than a substitute for those manuscript tables.

Table citations resolve through the manuscript bibliography, with canonical URLs
and title corrections from the existing reference audit where available. Source
annotations are reproduced rather than independently reclassified. Figure
statistics remain manuscript snapshots.

## Publishing

This directory is configured for the repository
`Human-Centered-VLA/Human-Centered-VLA.github.io`:

1. Push the static files and `.github/` workflow to that repository.
2. Select **GitHub Actions** in the repository's **Settings → Pages**.
3. Push to `main` or run **Publish organization website** manually from **Actions**.

The workflow copies the finished HTML and assets into the Pages artifact;
there is no website build. The website address is
<https://human-centered-vla.github.io/>.
