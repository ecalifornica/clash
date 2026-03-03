---
name: audit
description: View recent clash permission decisions from the audit log
---
Check if the audit log exists:

```bash
test -f ~/.local/state/clash/audit.jsonl && echo "exists" || echo "missing"
```

If the file is missing, tell the user audit logging is not enabled. They can enable it by adding this to `~/.config/clash/policy.yaml`:

```yaml
audit:
  enabled: true
```

If the file exists, read the last 20 entries:

```bash
tail -20 ~/.local/state/clash/audit.jsonl
```

Parse the JSON Lines output and present a readable summary table. For each entry:

1. **Timestamp** — convert the Unix timestamp (e.g. `1706123456.789`) to a human-readable local time
2. **Decision** — show `ALLOW`, `DENY`, or `ASK`
3. **Tool** — the `tool_name` value
4. **Input** — the `tool_input_summary` (truncated to keep the table readable)
5. **Reason** — show `reason` if present
6. **Rules** — show matched/skipped rule counts if nonzero

If the user asks to filter by tool name, decision type, or time range, use `grep` or `jq` on `~/.local/state/clash/audit.jsonl` to narrow results before presenting them.
