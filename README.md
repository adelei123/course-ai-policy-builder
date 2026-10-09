# Course AI Policy Builder

A guided tool that helps University of Oregon instructors draft a course Generative AI policy. It is aligned with UO Teaching Engagement Program / CTL syllabus samples. Answers are saved only in the user's browser; nothing is sent anywhere.

## Live tool
`index.html` is the tool itself, in readable and editable form. To publish it with GitHub Pages:
1. Upload this folder to a repository.
2. Go to **Settings → Pages**, set Source to *Deploy from a branch*, choose `main` and `/ (root)`, then save.
3. The tool will be live at `https://<username>.github.io/<repo-name>/`.

Any edit you commit to `index.html` goes live within about a minute.

## Contents
| Path | What it is |
| --- | --- |
| `index.html` | The tool: questions, branching logic, policy language |
| `support.js`, `organic-styles.css` | Runtime and stylesheet `index.html` needs. Keep them next to it. |
| `policy-builder-offline.html` | Single-file copy that works offline or opened from disk. It does not update when `index.html` changes. |
| `source/question-progression-reference.dc.html` | Visual reference of every step and branch |
| `source/wcag-audit-report.dc.html` | WCAG 2.2 Level A/AA audit report (Round 3), which reads `audit-r3.json` |
| `source/support.js`, `source/doc-page.js` | Runtime the reference pages need |
| `docs/question-progression.doc` | Question progression as a Word document |
| `docs/wcag-2.2-audit-checklist.csv` | Audit checklist, one row per criterion |

`index.html` and the `source/` pages must be served over http(s), for example GitHub Pages or VS Code's Live Server. Opened by double-clicking, the browser blocks the files they load. Use `policy-builder-offline.html` for offline use.

## Editing
Open `index.html` in any text editor, or click the pencil icon on github.com.
- **Questions, options and on-screen wording:** the HTML in the top half of the file.
- **Generated policy language:** the JavaScript in the lower half. Shortened syllabus sentences are in constants starting with `SYL_`.
- **Branching:** logic near `STEPS` and `visible(`.

Change only the text inside quotes. Keep quote marks, commas and the double-curly-brace placeholders intact.

## Accessibility status
All WCAG 2.2 Level A and AA web criteria are supported except 4.1.3 Status Messages, which still needs a screen-reader test (NVDA/VoiceOver). Accessibility of the Word and PDF output has not been verified.

## Generative AI disclosure
This tool was built with help from Claude, an AI assistant. All policy language was reviewed by the project author.
