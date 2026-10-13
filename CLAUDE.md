# Working with Roy

## Look and try first, then ask

- Before asking a question, investigate it yourself: search the web, check GitHub, read the code, run commands, try the obvious approach.
- Come back with findings and a concrete recommendation, not a question you could have answered yourself.
- Only ask when you are genuinely blocked (a permission was denied, a decision is truly Roy's to make, or something is irreversible), and when you do, say what you already tried.

## Design tools in this repo

- Skills in `.claude/skills/`: `design-taste-frontend` (anti-generic landing page design), `image-to-code` (build from screenshots/mockups), `playwright-cli` (browser automation and screenshots).
- `playwright-cli` needs the CLI installed each new cloud session: `npm install -g @playwright/cli@latest`.
  `.playwright/cli.config.json` points it at the cloud container's pre-installed Chromium; update `executablePath` if `ls /opt/pw-browsers` shows a different version. It blocks `file:` URLs, so serve the page first: `python3 -m http.server 8765`, then `playwright-cli open http://localhost:8765/`.
- Brand design-system references in `.claude/design-references/` (Stripe, Linear, Vercel), from VoltAgent/awesome-design-md. Use them as style inspiration, not to copy a brand.
