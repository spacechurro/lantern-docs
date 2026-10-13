# Getting started

Lantern checks whether a URL is up. You need Python 3.9 or newer. There is nothing to install.

From a checkout of [lantern](https://github.com/spacechurro/lantern):

```bash
python3 lantern.py check https://example.com

You can also watch a URL:

```bash
python3 lantern.py watch https://example.com
```

```

Lantern requests the URL and follows redirects. A final status from 200 through 399 prints `up` and that status, and the command exits 0.

```text
up 200
```

A status from 400 through 599 prints `down` and the status, and the command exits 1. A timeout or a connection failure prints `down no response`.

```text
down no response
```

When standard output is a terminal and color is on, `up` is green and `down` is red. Piping the command, or passing `--no-color`, prints plain text.

Lantern reads `lantern.toml` in the current directory when that file exists. Flags override the file. See [Commands](cli.md) and [Configuration](configuration.md).
