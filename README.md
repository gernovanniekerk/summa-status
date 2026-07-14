# summa-status — public status feed for the Summa Console app

`snapshot.json` is the App Factory portfolio state (app names + pipeline stage only — no secrets, no revenue) that the Summa Console iPhone app fetches on launch so it shows live-ish status without a paid backend.

Regenerate + publish from a machine with the app clones:

    node "<app-factory>/tools/gen-snapshot.mjs" > snapshot.json && git commit -am update && git push

This repo is PUBLIC so the app can fetch the raw URL with no token. Keep it to low-sensitivity status only; move to a gated feed before adding revenue.
