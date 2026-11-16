# The Birthday Tribune — GitHub Pages Project

A lightweight, mobile-first collection of ten independent landing pages for the NFC tags in Aman's birthday memory book.

Each page contains a personal memory, an illustrated photograph, and an optional audio or video recording.

## Project Structure

```text
aman-chronicle/
├── 01.html ... 10.html
├── assets/
│   └── style.css
├── images/
│   ├── 01.png ... 10.png
├── media/
│   └── (add your MP3/MP4 files here)
└── README.md
```

There is intentionally **no homepage**. Each NFC tag opens its corresponding memory page directly.

## Edit Each Page

Open the relevant numbered HTML file (`01.html`, `02.html`, etc.) to edit its content.

You can customise:

1. **Kicker** — the small introductory text above the headline.
2. **Headline** — the main title of the memory.
3. **Deck** — the short description below the headline.
4. **Photo caption** — the text underneath the illustration.
5. **Personal message** — the text inside `<p class="message">`.
6. **Recording section** — add an audio or video file if desired.

The matching black-and-white illustration is already connected:

- `01.html` uses `images/01.png`
- `02.html` uses `images/02.png`
- `03.html` uses `images/03.png`
- And so on through `10.html`.

Keep the numbered image filenames unchanged unless you also update the corresponding HTML image source.

## Add an Audio Recording

1. Put your audio file in the `media` folder, for example `media/01.mp3`.
2. Open the corresponding HTML file.
3. Find the section labelled `AUDIO OPTION`.
4. Remove the placeholder `<div class="placeholder">...</div>`.
5. Uncomment the `<audio>` block by removing the opening `<!--` and closing `-->`.
6. Make sure the source filename matches your uploaded file.

Example:

```html
<audio controls preload="metadata">
  <source src="media/01.mp3" type="audio/mpeg">
  Your browser does not support audio playback.
</audio>
```

## Add a Video Instead

Put your video in the `media/` folder, for example `media/01.mp4`.

In the corresponding HTML file:

1. Remove the recording placeholder.
2. Uncomment the `VIDEO OPTION` block instead of the audio block.
3. Ensure the source filename matches your uploaded video.

Example:

```html
<video controls playsinline preload="metadata">
  <source src="media/01.mp4" type="video/mp4">
  Your browser does not support video playback.
</video>
```

Use either audio or video on a page. The controls are user-operated; media does not autoplay.

## Published Website

The project is hosted using GitHub Pages.

**Repository:** `kgspam00-pixel/a25`

**Website base URL:**

https://kgspam00-pixel.github.io/a25/

Each memory has its own independent URL.

## The Ten NFC URLs

These are the final URLs to be encoded into the ten NFC tags.

| Memory | NFC URL |
|---|---|
| Memory 01 | https://kgspam00-pixel.github.io/a25/01.html |
| Memory 02 | https://kgspam00-pixel.github.io/a25/02.html |
| Memory 03 | https://kgspam00-pixel.github.io/a25/03.html |
| Memory 04 | https://kgspam00-pixel.github.io/a25/04.html |
| Memory 05 | https://kgspam00-pixel.github.io/a25/05.html |
| Memory 06 | https://kgspam00-pixel.github.io/a25/06.html |
| Memory 07 | https://kgspam00-pixel.github.io/a25/07.html |
| Memory 08 | https://kgspam00-pixel.github.io/a25/08.html |
| Memory 09 | https://kgspam00-pixel.github.io/a25/09.html |
| Memory 10 | https://kgspam00-pixel.github.io/a25/10.html |

### Encoding the NFC Tags

Using the NFC Tools app:

1. Open NFC Tools.
2. Select **Write**.
3. Choose **Add a record**.
4. Select **URL/URI**.
5. Paste the corresponding memory URL.
6. Select **Write** and tap the NFC tag against your phone.

Repeat for all ten tags, making sure each tag contains the correct numbered URL.

**Important:** Test every NFC tag with your phone before attaching or hiding it underneath its corresponding physical `Tap Me` tab.

## Publish or Update on GitHub Pages

Whenever you make changes to the website:

1. Open the GitHub repository.
2. Upload or commit the updated files.
3. Preserve the existing folder structure.
4. Wait for GitHub Pages to finish deploying.
5. Open the corresponding page URL to verify the changes.

GitHub Pages is configured to deploy from the `main` branch and the repository root (`/(root)`).

You do not need to create a new deployment configuration for routine content updates.

## Important Notes

- The layout is designed mobile-first and adapts to larger screens.
- This project uses plain HTML and CSS: no framework, build step, database, or JavaScript.
- GitHub Pages provides static hosting. Anyone with a page URL can view its contents, so do not upload anything intended to remain private.
- Compress videos before uploading. Large media files may take longer to load on mobile data.
- The root URL does not contain a homepage by design. Use the ten numbered URLs for testing and NFC encoding.
- Keep the numbered HTML and image filenames consistent to avoid broken links.

---

**The Birthday Tribune**

*Ten moments. One beautiful story. Made with all my love.* ♥
