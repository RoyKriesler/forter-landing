# Working with Roy

## Look and try first, then ask

- Before asking a question, investigate it yourself: search the web, check GitHub, read the code, run commands, try the obvious approach.
- Come back with findings and a concrete recommendation, not a question you could have answered yourself.
- Only ask when you are genuinely blocked (a permission was denied, a decision is truly Roy's to make, or something is irreversible), and when you do, say what you already tried.

## Browser screenshots in cloud sessions

- Design skills (taste, image-to-code, playwright-cli, brand references) live in the `claude-config` repo under `external-skills/`, not here.
- To use `playwright-cli` in a cloud session: `npm install -g @playwright/cli@latest`. `.playwright/cli.config.json` points it at the container's pre-installed Chromium; update `executablePath` if `ls /opt/pw-browsers` shows a different version. It blocks `file:` URLs, so serve the page first: `python3 -m http.server 8765`, then `playwright-cli open http://localhost:8765/`.
