# Architecture decisions to validate

NetBeacon is designed around a **local agent + local web dashboard**, not a cloud-only scanner. No specific language or framework is committed yet.

## Proposed components

1. **Agent:** collects authorized local-network observations at a safe rate.
2. **Inventory store:** tracks identifiers, friendly names, first/last seen and observation source.
3. **API/dashboard:** authenticated views for device list, connection history and diagnostics.
4. **Alerts:** opt-in new-device notifications with cooldown and trusted-device overrides.
5. **Optional adapters:** read-only OpenWrt data first, Tailscale later.

## Network and privacy considerations

- ARP/neighbor tables, DHCP leases and active probes have different coverage and permissions; define what each observation actually proves.
- MAC randomization, sleeping devices, VLANs and Wi-Fi client isolation can create false positives or incomplete inventories.
- Limit probe rates and targets to authorized networks; avoid port sweeping or intrusive techniques by default.
- Run with least privilege. Never store router credentials in source control or expose them in the UI.
- Allow user-controlled retention, export and deletion of saved inventories.
- Protect remote access: disabled by default or explicitly configured with authenticated trusted connectivity.

Architecture remains provisional until discovery and threat-model tasks are resolved.
