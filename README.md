# The Birthday Tribune — GitHub Pages project

A lightweight, mobile-first set of ten independent landing pages for the NFC tags in Aman's birthday memory book.

## Project structure

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

There is intentionally **no homepage**. Each NFC tag opens its own page directly.

## Edit each page

Open the relevant numbered HTML file (`01.html`, `02.html`, etc.) and change:

1. `YOUR MEMORY TITLE GOES HERE` — the headline.
2. The sentence under the headline — the short deck/subheading.
3. The text inside `<p class="message">` — your personal message.

The matching black-and-white illustration is already connected:
- `01.html` uses `images/01.png`
- `02.html` uses `images/02.png`
- ...and so on through `10.html`.

Keep the numbered image filenames unchanged unless you also update the matching HTML `src`.

## Add an audio recording

1. Put the file in the `media` folder, for example `media/01.mp3`.
2. In the matching HTML file, find the section labelled `AUDIO OPTION`.
3. Remove the placeholder `<div class="placeholder">...</div>`.
4. Uncomment the `<audio>` block (remove the opening `<!--` and closing `-->`).
5. Make sure the source filename matches your uploaded file.

Example:
```html
<audio controls preload="metadata">
  <source src="media/01.mp3" type="audio/mpeg">
  Your browser does not support audio playback.
</audio>
```

## Add a video instead

Put the video in `media/`, for example `media/01.mp4`. In that page, remove the placeholder and uncomment the `VIDEO OPTION` block instead of the audio block.

```html
<video controls playsinline preload="metadata">
  <source src="media/01.mp4" type="video/mp4">
  Your browser does not support video playback.
</video>
```

Use either audio or video on a page. The controls are intentionally user-operated; media does not autoplay.

## Publish on GitHub Pages

1. Create a new GitHub repository. For free GitHub Pages, make it **public**.
2. Upload the contents of this project folder to the repository root. Upload the ten numbered HTML files, `assets` folder, `images` folder, `media` folder, and this README.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main` and folder `/(root)`, then Save.
6. Wait for GitHub Pages to finish publishing.

Your site base URL will look like:
`https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`

## The ten NFC URLs

Replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your actual GitHub details:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/01.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/02.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/03.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/04.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/05.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/06.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/07.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/08.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/09.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/10.html
```

In NFC Tools: Write → Add a record → URL/URI → paste the matching URL → Write. Test every tag with your phone before hiding it under the physical `Tap Me` tab.

## Important notes

- The layout is designed mobile-first and adapts to larger screens.
- This is plain HTML and CSS: no framework, build step, database, or JavaScript.
- GitHub Pages is static hosting. Anyone with a page URL can view it, so don't upload anything you want to keep private.
- Compress videos before uploading; large media files can take longer to load on mobile data.
- The root URL will not show a homepage because you chose ten independent pages. Use the numbered URLs for testing and NFC encoding.
