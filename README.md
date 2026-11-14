# Lab Onboarding Site

A standalone GitHub Pages onboarding guide for new lab members.
Covers: Discord, Email, GitHub, R & RStudio, HPC cluster, meetings, and lab norms.

## Deploy

1. Push this folder to a GitHub repo (e.g. `[your-org]/onboarding`).
2. Go to **Settings → Pages → Deploy from branch → `main` / root**.
3. Your site will be live at `https://[your-org].github.io/onboarding/`.

## Customise

Search for and replace all placeholders in `index.html`:

| Placeholder             | Replace with                          |
|-------------------------|---------------------------------------|
| `[Your Lab]`            | Your lab name                         |
| `[Department]`          | Your department name                  |
| `[University]`          | Your university                       |
| `[PI Name]`             | PI's name                             |
| `pi@university.edu`     | PI's email                            |
| `[Lab Manager]`         | Lab manager's name                    |
| `manager@university.edu`| Lab manager's email                   |
| `[your-org]`            | Your GitHub organisation slug         |
| `[Month Year]`          | Last-updated date                     |

## Checklist items

Checklist items use `localStorage` to persist across page refreshes (private to each visitor's browser).
To add a task, copy any `.task-item` block inside a `.task-list` div.
To add a new day tab, copy a `<button class="day-tab">` and a matching `<div class="task-list" id="...">`.

## Sections

Sections in the guide are `<section class="guide-section" id="s-NAME">`.
Add a matching `<a href="#s-NAME">` in `.sidenav` to link to it.

## Colours

Change the four root variables at the top of `<style>` to retheme:

```css
--green:   #1B4332;   /* primary / headings */
--sage:    #52796F;   /* accent / links */
--bg:      #F4F6F3;   /* page background */
--surface: #ffffff;   /* cards / panels */
```

Dark mode values are defined separately under `@media (prefers-color-scheme: dark)`.
