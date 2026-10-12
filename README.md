# gamehouse-halloween-pumpkins

Halloween promotion for GameHouse.com: two popup games, a pick-a-pumpkin game (`pumpkins.html`) and a "Spin to win" prize wheel (`wheel.html`, see below).

## What it does

`pumpkins.html` is a self-contained widget (inline HTML, CSS, JS; no logos, no backend, no tracking). The only external request is the Creepster and Nunito fonts from Google Fonts.

- Nine pumpkins in a 3x3 grid. The visitor must find 3 treat pumpkins. A short intro text sits under the "Pumpkin Pickin'" title, and a picks-left countdown under the grid reads "5 picks", "4 picks", "3 picks", "Only 2 picks!" and "Last pick!". The countdown is hidden once the third treat is found.
- The visitor always wins. The script decides each outcome, not the pumpkin clicked: picks 1-4 hold exactly 2 treats and 2 threats in a random order (shuffled per play), and pick 5 is always a treat.
- Each pumpkin flips to a candy treat or a spooky ghost, and revealed pumpkins are disabled.
- On the third treat it shows "Boo! You've Unlocked Our Best Deal!", a candy shape reading "OVER 40% OFF", and a **Claim your treat** button that opens the offer page in a new tab. There is no coupon code.
- Full Halloween theme (twilight purple, pumpkin orange, Creepster headings from Google Fonts, inline SVG cobwebs). Responsive from phone to desktop, and honors `prefers-reduced-motion`.

## Add it to getsitecontrol

1. In getsitecontrol, create a new widget and pick **Custom HTML** (or add a Custom HTML block to a popup).
2. Paste the entire contents of `pumpkins.html` into the HTML editor.
3. Under targeting, choose the pages and triggers you want (e.g. on page load or exit intent).
4. Set the widget background to transparent and remove any default title or button so only the game shows.
5. Preview on desktop and mobile, then publish.

To change where the button goes, edit the `href` of the `<a class="ghp-cta" id="ghp-cta">` element (currently `https://www.gamehouse.com/promo/2026-10-halloween-trick-or-treat-membership`). To change the offer text, edit the two `<text>` elements (`OVER` and `40% OFF`) inside the `<svg class="deal">` candy shape. Keep the 40% figure in line with the offer on the landing page. To preview locally, open `pumpkins.html` in a browser.

## Spin to win wheel

`wheel.html` is a second, separate widget: a "Spin to win" prize wheel. Like the pumpkin game it is self-contained (inline HTML, CSS, JS; no logos, no backend, no tracking; the only external request is the Creepster and Nunito fonts from Google Fonts). All its classes and ids use a `ghw-` prefix, so it can sit on a page next to the pumpkin game without clashing.

- A six-slice wheel (orange and purple) with candy and ghost icons and 12 pegs. A pointer at the top flicks as each peg passes it. The visitor taps **SPIN** in the middle of the wheel.
- The visitor always wins. The wheel always settles on a candy slice (never a ghost): it slows down on the last ghost, creeps past the final peg and stops on the candy. The spin takes about 8.5 seconds. With `prefers-reduced-motion` it skips the animation and goes straight to the result.
- The win screen shows "You won a treat!", "Boo! You've Unlocked Our Best Deal!", a candy shape reading "OVER 40% OFF", and a **Claim your treat** button that opens the offer page in a new tab. There is no coupon code.
- No close button and no trigger logic: getsitecontrol handles when the widget shows and how it is dismissed. Reloading the page re-spins the wheel.

### Add it to getsitecontrol

Same steps as for the pumpkin game: create a **Custom HTML** widget, paste the entire contents of `wheel.html`, choose targeting and triggers, make the widget background transparent and remove any default title or button, preview on desktop and mobile, then publish. To preview locally, open `wheel.html` in a browser (it renders as a bare card on the page's default background).

### Where to edit things

- **CTA link**: the `href` of the `<a class="ghw-cta" id="ghw-claim">` element, currently `https://www.gamehouse.com/promo/2026-10-halloween-trick-or-treat-membership`.
- **"OVER 40% OFF" text**: the two `<text>` elements inside the `<svg class="ghw-deal">` candy shape (`OVER` and `40% OFF`).
- **Win and copy text**: "Boo! You've Unlocked Our Best Deal!" is the `<p>` inside `.ghw-win`; the text under the wheel is in `.ghw-lead` and `.ghw-copy`.

**The 40% figure must match the offer on the landing page.** Check the number against the promo page before publishing, and update it here whenever the offer changes.
