# Forkast

A swipe-to-decide recipe app: swipe right to save a recipe, left to pass.

Planned live site: https://alexhuyton.github.io/forkast/

## Where this came from

Forkast started as a hackday experiment in the
[hello-hackday](https://github.com/alexhuyton/hello-hackday) repository, which
grew from a "hello world" page into a recipe app. This repository starts from
that prototype (commit `bfbe94b` there), renamed.

What the prototype already does (`index.html`, one self-contained page):

- A deck of 14 Italian recipe cards. Swipe or drag right (or ♥, or the right
  arrow key) to save, left (✕, or the left arrow key) to pass, ↶ to go back.
- "See the full recipe" opens ingredients and method.
- A Saved page: open a recipe, remove it, or put back recipes you passed.
- A home page that sells the idea (your flavours, never the same dinner
  twice) with food photos from Unsplash, and a bottom navigation bar (Home,
  Discover, Saved, Together). Each page has its own link (`#discover`,
  `#saved`, `#together`), so the back button works.
- Saved is split into To cook and Cooked: tap "I cooked it" to move a dish
  across and rate it.
- Together: the dishes you and your partner both saved. "Share my likes" sends
  a link (`#match=…`) that loads your saves on their phone; until then the
  partner's likes are sample data.
- Forkast Wrapped: a year-end recap preview, built with sample data.
- Saved recipes and ratings are kept in the browser only (`localStorage`), so
  they don't follow you between devices.
- Visual style: sand, maroon, blue and white palette; Archivo Black headings,
  DM Sans body text.

## Next

The prototype was built straight away, without first working out who it's for.
The next step is a research-led design brief and product requirements, before
more building.
