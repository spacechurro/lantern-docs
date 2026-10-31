# Configuration

Lantern reads `lantern.toml` from the current directory. A missing file uses the defaults below. Flags override the file. Other keys are ignored.

```toml
timeout = 5
color = true
interval = 30
```

`timeout` is how many seconds to wait for a response. The default is `5`.

`interval` is how many seconds to wait between checks in `watch`. The default is `30`.

`color` colors `up` in green and `down` in red when standard output is a terminal. The default is `true`. `--no-color` still prints plain text.
