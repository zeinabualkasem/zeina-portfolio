# Zeina Abualkasem — Portfolio

A plain static site: six HTML files, one `assets/` folder of images, no build step. Works as-is on GitHub Pages.

## Publish it on GitHub Pages

1. Create a new repository (public, so Pages can serve it for free).
2. Upload everything in this folder to the repo root, keeping `assets/` as a folder and `.nojekyll` at the root (it's a hidden file — make sure your upload method doesn't skip it).
3. In the repo: **Settings → Pages → Source → Deploy from a branch → `main` / `(root)`** → Save.
4. GitHub gives you a URL like `https://yourusername.github.io/your-repo-name/`. It can take a minute or two to go live.
5. Open the URL and click through all six pages once, on your phone too, before sharing it.

## Add your résumé

The nav bar and the About page both link to `resume.pdf`, but that file isn't in this package — add your own PDF named exactly `resume.pdf` to the repo root. The links will start working immediately, with no HTML edits. Whenever you want to update your résumé later, just replace that one file in the repo and the links stay pointed at it.

## File map

| File | Page |
|---|---|
| `index.html` | Home |
| `work.html` | Work (all projects) |
| `project1_writeup.html` | Case study: Smart Work (prioritization workshop) |
| `project2_writeup.html` | Case study: Excel Intermediate |
| `about.html` | About |
| `contact.html` | Contact |
| `assets/` | All images used across the site |
| `resume.pdf` | **Not included — add your own** |

## What's still a placeholder

Search any page for text in *italic brackets* (copy to write) or a dashed gray box (an image to add). Right now that's:
- **Home / About:** hero photo, About Me photo, one testimonial
- **Work page:** four project rows not built yet (Soft skills, Logistics, Workforce management, Business communication)
- **Project 2 (Excel):** one image slot — a screenshot of the live session or the dashboard output, if you ever get one

## Adding a new project later

The pattern that's already working for `project1_writeup.html` and `project2_writeup.html`:
1. Copy one of them to `project3_writeup.html`.
2. Replace the hero text, the facts list, and the Problem / Solution / Process / Results sections with the new project's content.
3. Add a new row for it on `work.html` (copy one of the existing `<li class="row">` blocks), linking to `project3_writeup.html`.
4. If it's the new featured project, update the featured block on `index.html` and `work.html` too.

If you hand your next project's materials to Claude the same way you did for these two (storyboard, action map, assessments, any real results), it can build the next case study the same way.

## Editing text or colors

Everything is inline in the HTML — no separate CSS/JS files to hunt for. Each page has a `<style>` block at the top with the color variables (`--navy`, `--accent`, etc.) if you ever want to adjust the palette; changing one page's variables won't change the others, since each file is self-contained, so repeat any color change across all six files.
