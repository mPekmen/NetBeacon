# NetBeacon

**Know what's on your network.**

NetBeacon is a planned, local-first, self-hostable network visibility tool for home users and small networks. The concept combines **device inventory, connection changes, latency trends, and understandable security notifications**, with optional OpenWrt integration.

> **Status: planning / pre-development.** This repository currently contains a roadmap and design tasks, not a working scanner or security product.

## Who it's for

People who want to understand what is connected to their own network, notice unexpected changes, and troubleshoot everyday connectivity problems without learning a full enterprise monitoring suite.

## Proposed first release (MVP)

- A lightweight **local agent** running on an explicitly authorized network.
- A device inventory with seen/last-seen records and user-friendly names.
- Conservative local discovery and reachability checks.
- A responsive web dashboard with real observations and clear uncertainty.
- Opt-in notifications when a previously unseen device appears.
- A documented install, permissions model, and storage policy.

**Not in the MVP:** vulnerability exploitation, invasive packet inspection, remote scanning of third-party networks, or cloud-managed accounts.

## Principles

- **Authorized networks only.** No intrusive scanning, brute force, or attack traffic.
- Local-first. Device identifiers and network topology should remain on the user's system by default.
- Explain uncertainty: a missing ping response is **not proof a device is offline**, and MAC addresses may be randomized.
- Explicit, least-privilege integration with OpenWrt, and optional Tailscale visibility later.
- Useful diagnostics without alarmist or unsupported security claims.

## Project planning

See [the roadmap](docs/roadmap.md), [initial architecture notes](docs/architecture.md), and [GitHub Issues](../../issues).

## License

A license has **not been selected yet**. Public source visibility does not by itself grant a right to reuse the code when implementation begins.

---

Maintained by Mert Pekmen. Not affiliated with existing products with similar names.
