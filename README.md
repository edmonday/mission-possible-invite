# Mission Possible 2027 - Invite

A single, self-contained `index.html` spy-themed registration invite for the
**Mission Possible 2027** conference (16-22 January 2027). No build step, no
dependencies beyond Google Fonts.

## The experience

1. A sealed envelope with a wax seal - tap to open.
2. The envelope opens and a "Your mission, should you choose to accept it…"
   briefing types itself out.
3. **Accept Mission** (and a **Decline** button that refuses to be clicked).
4. A "this message will self-destruct in 5…" countdown.
5. An explosion (flash, shake, particles).
6. Redirect to the registration Google Form.

## Configuring it

Open `index.html` and edit the two values at the top of the `<script>`:

```js
const CONFIG = {
  GOOGLE_FORM_URL: "PASTE_GOOGLE_FORM_URL_HERE",
  COUNTDOWN_START: 5
};
```

- **GOOGLE_FORM_URL** - paste your Google Form link. While it's still the
  placeholder, the page shows a visible link instead of redirecting, so it's
  fully testable without a real form. Once a real `https://` URL is set, it
  redirects automatically after the countdown.
- **COUNTDOWN_START** - the number the self-destruct countdown begins from.

## Accessibility & behaviour

- Mobile-first and responsive (built for QR-code scans).
- Visible keyboard focus rings.
- Respects `prefers-reduced-motion` (no shaking/strobing).
- No autoplay audio - sound is created only after the first tap and has a
  mute toggle.

## Hosting

Served by GitHub Pages from the `main` branch root (Settings → Pages →
"Deploy from a branch" → `main` / `/`).

Live: https://edmonday.github.io/mission-possible-invite/
