# gamehouse-halloween-pumpkins

Halloween promotion for GameHouse.com: a pick-a-pumpkin popup game.

## What it does

`pumpkins.html` is a self-contained widget (inline HTML, CSS, JS; no logos, no backend, no tracking). The only external request is the Creepster and Nunito fonts from Google Fonts.

- Nine pumpkins in a 3x3 grid. The visitor must find 3 treat pumpkins; "Treats" and "Threats" counters (each shown out of 3) update as they play. Threats never reaches 3/3: it stops at 2/3 at most.
- The visitor always wins. The script decides each outcome, not the pumpkin clicked: picks 1-4 hold exactly 2 treats and 2 threats in a random order (shuffled per play), and pick 5 is always a treat.
- Each pumpkin flips to a candy treat or a spooky ghost, and revealed pumpkins are disabled.
- On the third treat it reveals the code `SCARY2026` with a **Copy** button.
- Full Halloween theme (twilight purple, pumpkin orange, Creepster headings from Google Fonts, inline SVG moon, bats and cobwebs). Responsive from phone to desktop, and honors `prefers-reduced-motion`.

## Add it to getsitecontrol

1. In getsitecontrol, create a new widget and pick **Custom HTML** (or add a Custom HTML block to a popup).
2. Paste the entire contents of `pumpkins.html` into the HTML editor.
3. Under targeting, choose the pages and triggers you want (e.g. on page load or exit intent).
4. Set the widget background to transparent and remove any default title or button so only the game shows.
5. Preview on desktop and mobile, then publish.

To change the code, edit `COUPON` in the script and the `#ghp-code` text. To preview locally, open `pumpkins.html` in a browser.
