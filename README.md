# AI Usage

Widget id: `io.github.dexterhere.ai-usage`. A no-code spec widget that shows three numbers about your AI tool use: sessions, requests and active minutes. Six variants.

## Privacy: read this first

This is private-content class data. Even three counters describe how you use AI tools: when you work, how much, and how often. Treat a screenshot of this widget as personal information.

- Only three numbers are exposed: `sessions`, `requests` and `activeMinutes`.
- Prompts, replies, file names, project names and any other content are never exposed and have no field in the catalog.
- The widget has no network, files or programs (`network [] files [] spawn []`), so it cannot send these numbers anywhere itself. That is a declaration checked by the registry, not a promise that the whole system is safe or sandboxed.
- Sample data in `widget.json` is made up.

## Status

- Tier: spec widget. There is no code, only `manifest.json`, `widget.json` and `layout.json`.
- Registry status: `planned`. Version `0.1.0`, pre-release.
- The `ai-usage` provider does not exist yet. The topic is in the provider catalog but not served by the daemon, and the desktop renderer for spec widgets is not built. The widget cannot run on a real desktop today. It validates and previews on the website emulator from `sampleData`.

## Variants

| Variant         | Shows                                                    | Fits           |
| --------------- | -------------------------------------------------------- | -------------- |
| `counts`        | Sessions, requests and active minutes in a 2-column grid | desktop        |
| `sessions-only` | One large session count                                  | desktop or bar |
| `activity`      | Ring and large active minutes, sessions beneath          | desktop        |
| `chip`          | Icon and session count in one row                        | bar            |
| `minimal`       | Request count only                                       | desktop or bar |
| `detailed`      | Title, three columns of numbers and an active-time bar  | desktop        |

The default tree (no variant chosen) is the same as `counts`.

## Data

Only the `ai-usage.sessions` topic with fields `sessions`, `requests` and `activeMinutes`. No auth, no network, no files, no programs.

## Settings

None. `widget.json` declares an empty `settings` list because the layout format cannot honour options such as a time range yet. Choose a look by choosing a variant.

## Check

Validated with the website repository's registry code (schemas, layout, bindings, sample data) and its gates. See `docs/content/next/create/check-and-preview.md` there.

## License

MIT, see `LICENSE`.
