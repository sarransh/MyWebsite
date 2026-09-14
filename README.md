# sarranshagrawal.com

Personal site for Sarransh Agrawal — Product Owner and UX, Pune.

One file, no build step, no dependencies to install. `index.html` contains the
markup, the styles and the WebGL scene. Three.js is the only external script and
it loads from cdnjs at a pinned version.

## What is in it

- A WebGL globe with animated great-circle routes between supplier hubs, three
  orbiting satellites, and a fresnel atmosphere. Camera choreography is driven
  by scroll position.
- **Sprint triage** — a six-ticket game where the visitor sorts real backlog
  items into Now / Next / Later and sees the reasoning either way.
- A click-to-enter gate, scroll reveals, and a contact sheet with five working
  routes (Gmail compose, mailto, copy, WhatsApp, LinkedIn).

## Editing

Open `index.html` and edit. There is nothing to compile.

To preview locally:

    python -m http.server 8000

then open http://localhost:8000

## Deploying

Netlify is connected to this repository — a push to `main` publishes.

## Accessibility and motion

Everything degrades: without JavaScript the gate never appears and the whole
page is readable; `prefers-reduced-motion` disables the globe animation, the
gate and every transition.
