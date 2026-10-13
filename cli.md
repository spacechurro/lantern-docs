# Commands

Run Lantern as `python3 lantern.py` from a checkout. You need Python 3.9 or newer.

## check

Check one URL once.

```bash
python3 lantern.py check <url> [--timeout SECONDS] [--color | --no-color]
```

`url` is the address to request, including `https://`. Lantern follows redirects and prints the final status.

`--timeout SECONDS` is how long to wait. It overrides `timeout` in `lantern.toml`. The default is 5 seconds.

`--color` and `--no-color` override `color` in `lantern.toml`. Color is used only when standard output is a terminal. `up` is green. `down` is red.

The command prints one line. A status from 200 through 399 is `up` and exits 0. A status from 400 through 599 is `down` and exits 1. A timeout or a connection failure prints `down no response` and exits 1.

```text
up 200
down 503
down no response
```
