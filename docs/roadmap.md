# NetBeacon roadmap

This is a planning document, **not a list of completed features**. The agent, UI and storage designs will be validated before coding.

| Stage | Goal | Exit criteria |
| --- | --- | --- |
| **Discovery** | Research user problems, available interfaces and privacy implications | MVP and threat model documented |
| **v0.1** | Local agent, authorized network inventory, responsive dashboard | Real devices and last-seen signals, with limitations surfaced |
| **v0.2** | OpenWrt read-only integration | Least-privilege access and reliable polling of supported data |
| **v0.3** | Latency, availability trends and Wi-Fi diagnostics where measurable | History with measurement caveats and sensible sampling |
| **v0.4** | New-device alerts, trusted device labels, events | Low-noise notification rules and user overrides |
| **v0.5** | Optional Tailscale read-only integration and multiple networks | Documented privacy, permissions and identity handling |
| **v1.0** | Tested Windows/Linux install and secure remote UI access | Reproducible builds, upgrade path, documentation and backups |

## Non-goals

- Exploitation, password attacks or high-volume scans.
- Promising complete device detection on every network.
- Collecting traffic contents or exposing network inventory to a public service by default.
- Treating guessed device identity as a fact.

## Quality gates

Define permission boundaries, optional read-only router access, data retention, encrypted authentication, and network-safe scan budgets. Test with opt-in lab devices on a network the operator controls.

See GitHub Issues for specific work packages.
