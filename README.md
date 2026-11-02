# whoisthat-core

Go daemon that powers [WhoisThat](https://github.com/kvunoff/whoisthat): Xray-core
runtime, TUN mode, kill-switch, subscriptions, encrypted profile storage and the
JSON IPC protocol used by the Rust TUI/CLI.

> **Generated repository.** Every file except `README.md`, `.gitignore` and
> `.github/` is mirrored automatically from
> [`kvunoff/whoisthat`](https://github.com/kvunoff/whoisthat) (`core/core`).
> Open issues and pull requests there. Commits here are made by
> `github-actions[bot]` and carry a `Source-SHA:` trailer pointing at the
> original commit.

## Build

```bash
go build -o whoisthat-core
sudo setcap cap_net_admin,cap_net_raw,cap_setpcap=+ep whoisthat-core
```

Requires Go 1.26+ (see `go.mod`). The daemon is normally started by the TUI, not
by hand; see the [main repository](https://github.com/kvunoff/whoisthat) for
installation and usage.

## Test

```bash
go test ./...
```

TUN/firewall integration tests are gated behind the `integration` build tag and
need root plus `/dev/net/tun`.

## License

MIT — see [LICENSE](LICENSE).
