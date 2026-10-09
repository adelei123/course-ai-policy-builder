# Course AI Policy Builder

A guided tool that helps University of Oregon instructors draft a course Generative AI policy. It is aligned with UO Teaching Engagement Program / CTL syllabus samples. Answers are saved only in the user's browser; nothing is sent anywhere.

## Live tool
`index.html` is the complete tool in one self-contained file. To publish it with GitHub Pages:
1. Upload this folder to a repository.
2. Go to **Settings → Pages**, set Source to *Deploy from a branch*, choose `main` and `/ (root)`, then save.
3. The tool will be live at `https://<username>.github.io/<repo-name>/`.

`index.html` also works opened straight from disk.

## Contents
| Path | What it is |
| --- | --- |
| `index.html` | Published tool (single file, works offline) |
| `source/policy-builder.dc.html` | Editable source of the tool: questions, branching logic, policy language |
| `source/question-progression-reference.dc.html` | Visual reference of every step and branch |
| `source/wcag-audit-report.dc.html` | WCAG 2.2 Level A/AA audit report (Round 3), which reads `audit-r3.json` |
| `source/support.js`, `source/doc-page.js`, `source/_ds/` | Runtime and stylesheet the source pages need |
| `docs/question-progression.doc` | Question progression as a Word document |
| `docs/wcag-2.2-audit-checklist.csv` | Audit checklist, one row per criterion |

The `source/` pages must be served over http(s), for example via GitHub Pages at `/source/policy-builder.dc.html`. Opened from disk, the browser blocks the files they load.

## Updating
Edit `source/policy-builder.dc.html`, then rebuild `index.html` as a single self-contained file and replace it here.

## Accessibility status
All WCAG 2.2 Level A and AA web criteria are supported except 4.1.3 Status Messages, which still needs a screen-reader test (NVDA/VoiceOver). Accessibility of the Word and PDF output has not been verified.

## Generative AI disclosure
This tool was built with help from Claude, an AI assistant. All policy language was reviewed by the project author.
