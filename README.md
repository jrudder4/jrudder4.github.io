# jessrudder.com

Academic website built by GitHub Pages from simple text files. You never need to edit HTML.

## Where things live

| To change...                         | Edit this file                  |
|--------------------------------------|---------------------------------|
| Publications                         | `_data/publications.yml`        |
| Working papers                       | `_data/working_papers.yml`      |
| Work in progress                     | `_data/work_in_progress.yml`    |
| Policy publications                  | `_data/policy.yml`              |
| Coauthor website links               | `_data/coauthors.yml`           |
| Name, title, email, Scholar/LinkedIn | `_config.yml`                   |
| About paragraph                      | `_includes/about.md`            |
| CV                                   | replace `assets/pdf/Rudder_CV.pdf` (same name) |
| Photo                                | replace `assets/img/rudder.jpg` (same name)    |

`index.html`, `_includes/paper.html` and `assets/css/style.css` are the layout; leave them alone unless you want to change the design.

## Editing on github.com
1. Open the file, click the pencil icon.
2. Make the change, click **Commit changes**.
3. The site rebuilds in 1–2 minutes. Check progress under the repo's **Actions** tab
   (green check = live; red X = something in the file needs fixing — click it to see the line).

## A paper entry
```yaml
- title: "Search Costs and Relational Contracting"
  coauthors: [Brian Dillon]
  status: "Revise & Resubmit, *Journal of Development Economics*"
  links:
    - label: paper
      url: https://...
  abstract: >-
    We experimentally investigate the link between search costs and
    relational contracts...
  notes:
    - "Funding support from ..."
```
- **Add a paper:** copy a whole block (from `- title:` to the blank line), paste, edit.
- **Move a paper** (e.g. accepted): cut the block from one file, paste into the other.
- **Order on the site** = order in the file.
- Any line can be deleted if it doesn't apply (no abstract, no notes, no status...).

## Rules that prevent errors
- Keep the **two-space indentation** exactly as in the existing entries.
- Put titles, status and notes in **"double quotes"**. If the text itself contains a double
  quote, use curly quotes “like this” instead.
- Abstracts go on the lines under `abstract: >-`, indented 4 spaces. Line breaks there don't matter.
- Coauthor names in `[ ]` must be spelled the same as in `_data/coauthors.yml` to get linked.
- Formatting: `*italics*`, `**bold**`, links as `[text](https://url)`.

## Hosting & domain (one-time)
1. Repo **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)`.
2. At your domain registrar, DNS:

| Type  | Host | Value |
|-------|------|-------|
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |
| CNAME | www  | `<username>.github.io` |

   Remove the old Google Sites records (usually `CNAME www → ghs.googlehosted.com`).
3. Settings → Pages → custom domain `jessrudder.com`, then tick **Enforce HTTPS** when available.

Note: this site needs GitHub to build it, so opening `index.html` directly on your computer
shows unfilled `{{ }}` placeholders. That's expected — view the live site instead.
