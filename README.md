# Rishith Manchala — Personal Site

Hey, this is my little corner of the internet.

It's a single-page portfolio I built from scratch — no frameworks, no build step, no `npm install` ritual. Just one `index.html` doing all the work. Open it in a browser and it runs.

## What's inside

The site opens with a short intro animation: my logo spins in, then my name assembles itself letter by letter. After that it fades into the actual page, which has four parts:

- **Hero** — big name, a link to [Yuvora](https://yuvora.org), and the line *Design & Develop*.
- **About** — a short intro and a photo.
- **Projects** — Scholarstock, CS School Sync, Yuvora, IRIS, and Solar Saathi, each with links to the code and a live demo where one exists.
- **Contact** — email, GitHub, and Slack.

There are a few extra touches if you poke around: a custom cursor ring, glassy cards, and a canvas behind everything where particles slowly drift into the shape of my portrait, react to your mouse, and scatter when you get close.

## Running it locally

You don't really need anything special. Either:

1. Double-click `index.html`, or
2. Serve the folder if you want everything to behave exactly like production:

```bash
# Python is already on most machines
python -m http.server 8000
```

Then head to `http://localhost:8000`.

A tiny local server is the safer bet if you want the portrait-particle effect to work without browser file-security complaints.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole site — markup, styles, and the canvas logic |
| `Logo.png` | The logo used in the intro animation |
| `portrait.jpg` | My photo — also sampled to build the particle portrait |
| `Rishtih Manchala.JPG` | Extra photo, kept around |

## Notes for future me

- Everything lives in `index.html` right now, including a fairly long `<style>` block and the particle animation script. If this grows much more, it's probably time to split CSS and JS out.
- The portrait effect reads pixels from `portrait.jpg`, so swapping the photo automatically changes the particle shape. If the image fails to load, it falls back to a soft circular cloud of dots instead of breaking.
- Animations are timed to roughly line up with the intro sequence (the nav and hero fade in around the 6.3s mark). If you shorten the welcome animation, bump those delays down too.

## Credit

Designed and built by me, Rishith Manchala. Fonts are DM Serif Display and Merriweather from Google Fonts.

If you want to build something together, my email is in the contact section.
