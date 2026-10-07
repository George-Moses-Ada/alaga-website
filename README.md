# Àṣà — Alaga website source

This is an editable, standalone export of the website concept. Plain HTML, CSS and JavaScript: no framework, package install or build step required.

## Start

Unzip the download, open this folder in your editor and open `index.html` in a browser. For a local web server, run the following from this folder, then visit http://localhost:8000:

```bash
python3 -m http.server 8000
```

VS Code Live Server is another option. Use a consistent local server address when testing saved enquiries, since local storage is specific to the browser and origin.

## Where to customize

| File | What to change |
| --- | --- |
| `index.html` | Brand name, title, metadata, navigation, section copy, services, product names, forms, image captions and links |
| `style.css` | Colours in `:root`, typography, spacing, image layouts, breakpoints and animation styling |
| `app.js` | Scroll effects, menu, gallery filters, dialogs, academy curriculum, enquiry bag and contact form behaviour |
| `assets/` | Three downloaded reference photographs |
| `assets/fonts.css` and `assets/fonts/` | Local font declarations and files, including Google Material Symbols |
| `ASSET-NOTES.md` | Image provenance and font licensing sources |

The sections use these IDs: `home`, `about`, `services`, `experience`, `gallery`, `academy`, `shop`, `contact`. Keep navigation href values in sync if you rename them.

### Branding and colours

Search `index.html` and `app.js` for `Àṣà`, `àṣà` and `THE ALAGA HOUSE`. The logo is styled text, not a separate graphic. The primary colour tokens in `style.css` are `--cream`, `--olive`, `--ink`, `--muted`, `--line` and `--orange`.

### Images

Replace `assets/couple.jpg`, `assets/green.jpg` and `assets/pink.jpg` with your own licensed imagery. Update alt text and credits in `index.html`. You can retain these filenames or update every matching `src` reference. Shop product illustrations are made with HTML/CSS and can be edited directly.

### Icons and fonts

Icons use Google Material Symbols Outlined. Change the text inside a span with `class="material-symbols-outlined"` to the desired symbol name. The included font files support the icons offline. The typefaces are DM Sans and Italiana; Georgia is used for italic accents. Font declarations are included locally in this export.

### Academy

The overview is in `index.html`. The expanded curriculum is in the `curriculum-btn` click handler in `app.js`. Replace proposed modules and add confirmed dates, fees and instructors.

### Shop

This is an enquiry shop, not a payment system. Product names appear in `index.html` in headings and `data-product` attributes. Keep those values aligned. Selected items are saved in local storage as `asa-enquiry-bag` and can be added to a contact enquiry.

### Contact form

The form currently saves data on the visitor's browser under `asa-last-enquiry` and offers a text download. It does NOT email the company or submit to a server. To receive real enquiries, replace the `contact-form` submit handler in `app.js` with an integration to your chosen form endpoint or backend. Update the button text, privacy notes and status message accordingly. Never put private API keys in frontend JavaScript.

### Animation

Scroll reveals use `.reveal` and an IntersectionObserver. The hero parallax and reading progress bar are in `scrollEffect()` in `app.js`. The moving text uses `@keyframes marquee` in `style.css`. Reduced-motion settings disable nonessential motion. Responsive rules are at the end of `style.css`.

## Publish anywhere

Upload `index.html`, `style.css`, `app.js` and the whole `assets/` folder to a static host, keeping their relative paths intact. This export is independent of the original hosting service. Hosting credentials, Git history and account-specific configuration are intentionally excluded.

## Before the client's public launch

Replace provisional branding, reference photos and illustrative product/course content with approved company information. Connect contact delivery and add the company's real contact details. If a payment shop is wanted, integrate a commerce provider. No testimonials, past clients or event statistics are claimed by this concept.

## Checks

JavaScript syntax and internal section links were checked. Image files were validated. This export includes local fonts so it does not require Google Fonts requests to render. Full visual testing across browsers remains to be done.
