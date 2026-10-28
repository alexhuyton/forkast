# Forkast

A swipe-to-decide recipe app that learns the flavours you love, finds new
dishes that hit the same notes, and adapts every recipe to suit you.

Live site: https://alexhuyton.github.io/forkast/

The design brief and PRD are linked from [docs/brief.md](docs/brief.md).

## Where this came from

Forkast started as a hackday experiment in the
[hello-hackday](https://github.com/alexhuyton/hello-hackday) repository, which
grew from a "hello world" page into a recipe app. This repository starts from
that prototype (commit `bfbe94b` there), renamed.

## What it does

Everything lives in `index.html`, one self-contained page.

- **First run.** A new user sees a "Tell us what you love" home page and three
  quick questions: flavours you love, things to avoid, how many you cook for.
  You can skip and just swipe. "Start over as a new user" (at the bottom of
  Home) clears everything on that device, which is handy for demos.
- **Discover.** A deck of 14 Italian recipes, each with a photo (Wikimedia
  Commons and Unsplash, credited in the recipe view). Three labelled choices:
  **Save** (swipe right), **Not now** (swipe left; it comes back later) and
  **Never** (button only, so it can't happen by accident). A first-time tip
  explains them, a small slip springs back, and every choice shows an Undo.
  Double-tap a card to super like it.
- **Recipes adapted to you.** Things you avoid are swapped out where a good
  swap exists (white miso for anchovies, chilli paste for 'nduja, and so on);
  dishes where that ingredient is the whole point are skipped. Flavours you
  love get a nudge ("we've added 2 extra anchovies"). Changed ingredients are
  marked, with an "Adapted for you" note explaining why.
- **Taste learning.** Each choice counts towards the recipe's tags. Tags you
  keep saving come forward ("You like chilli"). Skip a tag 3+ times without
  saving it and Forkast infers a dislike, ignoring tags that only appear
  alongside a stronger suspect; it swaps that ingredient out where it can. A
  "Learning" strip shows what it has picked up, with one tap to undo.
- **Saved.** To cook and Cooked. "I cooked it" asks for a 1–5 rating and
  anything you'd change; those notes show at the top of the recipe next time
  as "your version". Servings scale in the recipe view. Dishes marked Never
  can be put back.
- **Household.** The dishes you and your partner both saved. "Share my likes"
  sends a link (`#match=…`) that loads your saves on their phone; until then
  the partner's likes are sample data.
- **Forkast Wrapped.** A year-end recap preview, built with sample data.
- Each page has its own link (`#start`, `#discover`, `#saved`, `#together`),
  so the back button works. Everything is stored in the browser only
  (`localStorage`), so it doesn't follow you between devices.
- Visual style: sand, maroon, blue and white palette; Archivo Black headings,
  DM Sans body text.
