# My Engineering Portfolio

This is my portfolio site for our intro-to-engineering/robotics course. It's
a plain HTML/CSS website — no build tools, nothing to install — that
documents each in-class activity and project as I complete it, and doubles
as a public page I can point people to.

## Getting started (do this first)

If you just got this template, work through this list before anything else:

- [ ] Replace every `FIRSTNAME LASTNAME` with your name (search the whole
      project for it — it appears in `index.html`'s header, hero text, and
      `<title>` tags).
- [ ] Swap `images/header.jpg` for your own photo or banner image.
- [ ] Update the LinkedIn and GitHub links in `index.html`'s social box
      (search for `your-username`).
- [ ] Confirm you have the rights to publish any images you use — swap out
      any placeholder/stock images that aren't yours.
- [ ] Turn on GitHub Pages (below) and check the live link actually works.

Then, as you complete each activity/project, replace its lorem-ipsum text
and placeholder image, and give its `<title>` tag a real, specific value
(see [AGENTS.md](./AGENTS.md)).

## Viewing it

- **Locally:** just open `index.html` in a browser (double-click it, or in
  VS Code right-click it and choose "Open with Live Server" if you have
  that extension, which auto-refreshes as you edit).
- **Live, on the internet:** `https://<your-github-username>.github.io/<this-repo-name>/`
  once GitHub Pages is turned on (see below).

## Publishing with GitHub Pages (one-time setup)

1. Push this repo to GitHub.
2. On GitHub, go to the repo's **Settings → Pages**.
3. Under "Build and deployment," set **Source** to "Deploy from a branch,"
   branch `main`, folder `/ (root)`. Save.
4. Wait a minute, then visit the URL GitHub shows you. That's your public
   portfolio link.

No build step is needed — the site is plain HTML/CSS, and the `.nojekyll`
file tells GitHub Pages to serve it as-is.

## How the site is organized

```
index.html          Home page — intro + a grid of cards, one per activity/project
index.css           Styles just for the home page
project.css         Shared styles for every activity/project detail page
theme.css           Colors/fonts used by both stylesheets, in one place
template.html       Starting point for a new activity or project page
activityNN.html     One in-class activity's page (e.g. activity01.html)
projectNN.html      One project's page (e.g. project01.html)
images/             All images, named to match their page (e.g. project04.png)
```

Each activity/project gets **one card** on the home page (image, title,
one-line description) that links to **one detail page** with the fuller
write-up: a hero image, a description, and optionally a photo gallery,
an embedded video, or a code sample.

## Adding a new activity or project

The easiest way is to ask your AI assistant. Something like:

> Add a new project page for "Project 4: <name>". Here's my description:
> <a paragraph about what I built and learned>. My hero image is
> `images/project04.png`. Follow the pattern in AGENTS.md.

Under the hood, that means: copy `template.html` to `project04.html`, fill
in the image/title/description, delete whichever optional blocks (gallery,
video, code) don't apply, and add a matching card to `index.html`. See
[AGENTS.md](./AGENTS.md) for the exact recipe your assistant should follow —
worth skimming yourself too, so you can do it by hand if you ever need to.

Other things you can ask for once the basics are in place:
- *"Add a photo gallery to project04.html with these three images."*
- *"Embed my YouTube video <link> on project04.html."*
- *"Change the site's accent color to blue"* — this only requires editing
  `theme.css`, since both stylesheets pull their colors from there.

## Working with an AI assistant — good habits

This is also a chance to practice a real skill: directing an AI coding tool
instead of hand-writing everything, and instead of blindly accepting
whatever it produces.

- Be specific about *what* you want and *where* (which page, which section).
- After it makes a change, open the page in a browser and actually look —
  don't just trust that it worked.
- Read the diff before accepting it. If something looks unfamiliar, ask the
  assistant to explain it.
- Commit often, with a message that says what changed (`git commit -m "Add
  project 4"`), so you have a history to fall back on.
- Never let it invent your results, reflections, or data — that content has
  to be yours.

## For AI assistants

See [AGENTS.md](./AGENTS.md) — it has the structural rules, the recipe for
adding pages, and the content guardrails to follow.
