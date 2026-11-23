# Knights of Columbus Council #11984 — Website

A simple website for **Father Edward L. Richardson, SMA Council #11984** (Chesapeake, VA).
It is plain HTML and CSS: no special software, no build step. You can edit it with any text editor
(Notepad on Windows, TextEdit on Mac in "plain text" mode, or the free VS Code).

## What's in the folder

| File / folder | What it is |
|---|---|
| `index.html` | Home page |
| `about.html` | Council history, parishes, namesake (Fr. Richardson), officers |
| `events.html` | Events Calendar (upcoming events table) |
| `recurring.html` | Monthly meetings and annual traditions |
| `join.html` | How to Join |
| `gallery.html` | Photo Gallery |
| `benefits.html` | Fraternal Benefits (insurance, annuities, Asset Advisors, field agent) |
| `css/style.css` | Colors and layout (rarely needs editing) |
| `js/main.js` | Mobile menu and photo pop-up (no need to edit) |
| `images/gallery/` | Put gallery photos here |

## Previewing
Double-click `index.html` to open it in your web browser. After you save a change, refresh the browser.

## Editing text
1. Open the page file (for example `events.html`) in your text editor.
2. Find the words you want to change and type over them. Only change text **between** tags,
   e.g. in `<p>Hello</p>` change `Hello`, but leave `<p>` and `</p>` alone.
3. Save and refresh the browser.

**Highlighted yellow boxes** on the site are placeholders: information we still need. In the files they look like
`<span class="ph">[Name]</span>`. Replace the whole thing (including `<span class="ph">` and `</span>`) with the real info.
Placeholders still to fill: officer names, upcoming event dates, annual-tradition dates/details, field agent contact,
current dues amount, and the current join promo code.

**Header/footer:** the menu and footer are repeated at the top and bottom of every page. If you change, say,
the contact email, change it in each `.html` file (most editors have "Find in Files / Replace All").

## Adding an event
In `events.html`, find the table. Copy one whole row, from `<tr>` to `</tr>`, paste it below, and edit the text:
```html
<tr><td>Fri, Mar 6</td><td>5:00 pm</td><td><strong>Lenten Fish Fry</strong><br>Dine in or carry out.</td><td>Parish Hall</td></tr>
```

## Adding photos
1. Shrink photos first if they are huge (about 1600 pixels wide is plenty). Use simple names with no spaces, like `golf2026.jpg`.
2. Copy the photo into `images/gallery/`.
3. In `gallery.html`, replace one placeholder block (`<figure>…Photo coming soon…</figure>`) with:
```html
<figure><img src="images/gallery/golf2026.jpg" alt="Knights at the golf outing"><figcaption>Golf Outing, 2026</figcaption></figure>
```
Get permission before posting photos of children, and don't post photos of restricted base areas.

## Optional: show a Google Calendar
In Google Calendar: Settings → pick the council calendar → "Integrate calendar" → copy the **Embed code**.
In `events.html`, paste it in place of the card that says "Optional: embed the council's Google Calendar here".

## The emblem
The site uses a simple cross mark, not the official Knights of Columbus emblem (a registered trademark).
If the council is authorized to use the emblem, save it as `images/emblem.png` and follow the comment near the top of each page.

## Putting it online for free
- **Netlify:** go to https://app.netlify.com/drop and drag this whole folder onto the page. You get a free web address
  right away; you can connect a custom domain later.
- **GitHub Pages:** create a free GitHub account, make a new repository, upload these files, then
  Settings → Pages → "Deploy from branch" → `main`.
