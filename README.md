# Choose Your Character — Paradox Academy

The interactive game for **Session 3 · How to get into tech** (Eng. Hozaifa Moustafa).
One static page, no build step, no backend. Fonts and the QR library are bundled, so it doesn't call any CDN.

| Address | Who uses it |
|---|---|
| `…/#/host` | **You, on the projector.** Levels 0–6, click-to-reveal answers, timers, class scoreboard. |
| `…/#/play` | **Students, on their phones.** Class quiz → class card → 6-month quest card they save as an image. |

## Put it on GitHub Pages (5 minutes)

1. On github.com, create a new **public** repository, e.g. `paradox-quest`.
2. Click **Add file → Upload files**, drag in everything from this folder (`index.html`, `README.md`, the `assets` folder), and commit.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After about a minute the site is live at `https://<your-username>.github.io/paradox-quest/`.
5. Open `…/#/host` on the laptop connected to the projector. The first screen shows a QR code students scan to reach `…/#/play`.

## Host controls

| Key | Action |
|---|---|
| → / Space | Next screen |
| ← | Previous screen |
| 1 2 3 4 | +1 point to Builder / Mind-maker / Engineer / Guardian |
| Alt + 1–4 | −1 point |
| T | Start / pause the timer (screens that have one) |

Scores and your current screen are kept in the browser, so a refresh doesn't lose them. Use **Reset scores** before the session.

## Edit before the day

Open `index.html` and change the `CONFIG` block near the top of the `<script>`:

- `prize`: what the winning class gets
- `story`: your three moments for "My quest so far" (replace the `[ ]` lines)
- `hireLooks`: your "What I look for when I hire" points
- `playerUrl`: leave empty. Set it only if you use a custom domain.

## Notes

- Each phone keeps its own answers. Nothing is sent anywhere, so votes still happen with hands or the colour cards, and you add points on the host screen.
- Quest cards are generated on the phone as a 1080×1350 PNG. **Save image** downloads it; **Share** opens the phone's share sheet where supported.
- Works offline once loaded, except that students need internet to open the site in the first place.
