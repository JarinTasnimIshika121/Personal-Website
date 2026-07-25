# Personal Academic Website — Jarin Tasnim Ishika

PhD Candidate, Department of Computer Science and Engineering, University of North Texas.

**Live site:** https://jarintasnimishika121.github.io/Personal-Website/
*(after enabling GitHub Pages — see Setup below)*

---

## How to edit the site

Everything you see on the page is generated from a single data block near the top of
`index.html`, marked:

```
/* ============================  SITE DATA  ===============================
   THIS IS THE ONLY PART YOU EDIT.
```

Open `index.html` in any text editor, change the values inside the `SITE` object,
save, and reload the page. You do not need to touch any HTML or CSS.

Nothing below the `END OF SITE DATA` marker needs editing.

### What lives where

| Key in `SITE` | Controls |
|---|---|
| `profile` | Name, role, department, university, tagline, email, CV link, footer |
| `nav` | Navigation buttons and their order |
| `about` | About paragraphs (one string per paragraph) |
| `research` | Research projects — period, name, description, links |
| `publications` | Papers — year, title, authors, venue, link buttons |
| `cv` | Every CV block: education, research, teaching, industry, coursework, skills |
| `cvButtons` | The Download PDF / View full CV buttons |
| `projects` | Projects, grouped (Graduate / Undergraduate) |
| `blog` | Posts — date, title, URL, `external: true` for posts hosted elsewhere |
| `contactLead`, `contactLinks` | Get in Touch text and link cards |
| `navSocial` | Social icons in the navigation bar |

### Adding an entry

Copy an existing entry, paste it below, and change the values. For example, a project:

```js
{ name:"My New Project",
  desc:"What it does and why I built it.",
  tags:["Python","PyTorch"],
  links:[ {label:"GitHub", url:"https://github.com/user/repo", style:"primary", icon:"github"} ] },
```

Available `icon` values: `github`, `linkedin`, `scholar`, `substack`, `mail`,
`download`, `chevron`, `external`.
Available `style` values: `primary` (filled), `outline`, `soft`.

Delete an entry by deleting its lines. Reorder by moving them.

---

## Features

- Light and dark theme, following the visitor's system preference, with a toggle
- Read-aloud voice reader (`Alt` + `R` to start, `Esc` to stop) with speed control
- Fully responsive — desktop, tablet, mobile
- Keyboard navigable, skip-to-content link, WCAG AA colour contrast
- No build step, no dependencies, no tracking

---

## Setup — publishing with GitHub Pages

1. Go to **Settings → Pages** in this repository.
2. Under **Source**, choose **Deploy from a branch**.
3. Set branch to **`main`** and folder to **`/ (root)`**, then Save.
4. Wait about a minute. The site appears at
   `https://jarintasnimishika121.github.io/Personal-Website/`

The `.nojekyll` file in the repository root tells GitHub Pages to serve the files
as-is rather than running them through Jekyll.

---

## Still to add

- Research project names and descriptions
- Graduate project names and repository links
- Blog post titles and links
- Profile photo (replace the upload placeholder with a real `<img>` source)
- CV PDF (`profile.cvFile`)
- Google Scholar and Substack URLs
