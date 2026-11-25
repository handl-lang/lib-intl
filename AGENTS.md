# lib-intl

`intl` — internationalization (Handl stdlib port, pure handl).

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the library entry |
| `pkg.hnl` | manifest — `modules: ["intl"]` |
| `scripts/hnl-gate.sh` | `.hnl` gate |
| `workflows/gate.yaml` | CI — shared `handl-gates` campaign |

## Contract

- Pure `.hnl`, no Rust crate; vendored by consumers via
  `handl-pkg-vendor`.
- The native-speed counterpart is `lib-intl-c` (ICU4C backend).

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
