# gamehouse-halloween-pumpkins

Halloween promotion for GameHouse.com: a pick-a-pumpkin popup game.

## What it does

`pumpkins.html` is a self-contained widget (inline HTML, CSS, JS; no logos, no backend, no tracking). The only external request is the Source Sans Pro font from Google Fonts.

- Nine pumpkins in a 3x3 grid. The visitor must find 3 treat pumpkins with at most 2 mistakes.
- The visitor always wins. The script decides each outcome, not the pumpkin clicked: picks 1-4 hold exactly 2 treats and 2 misses in a random order (shuffled per play), and pick 5 is always a treat.
- Winners and mistakes counters update as the visitor plays; each pumpkin flips to a candy treat or a spooky ghost, and revealed pumpkins are disabled.
- On the third treat it reveals the code `SCARY2026` with a **Copy** button.
- Styled with gamehouse.com's palette (sky blue `#2eb2ea`, orange `#ff6b42`) and Source Sans Pro. Responsive from phone to desktop, and honors `prefers-reduced-motion`.

## Add it to getsitecontrol

1. In getsitecontrol, create a new widget and pick **Custom HTML** (or add a Custom HTML block to a popup).
2. Paste the entire contents of `pumpkins.html` into the HTML editor.
3. Under targeting, choose the pages and triggers you want (e.g. on page load or exit intent).
4. Set the widget background to transparent and remove any default title or button so only the game shows.
5. Preview on desktop and mobile, then publish.

To change the code, edit `COUPON` in the script and the `#ghp-code` text. To preview locally, open `pumpkins.html` in a browser.
