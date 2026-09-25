# Kostiantyn Bank

**Backend, infrastructure, and applied AI engineering · Ukraine 🇺🇦**

I build and operate Linux-first systems where correctness, observability, and
recovery matter. My work spans backend services, PostgreSQL, search systems,
infrastructure automation, security tooling, and evidence-driven AI agents.

## Engineering focus

- **Backend and data:** Python, PostgreSQL, SQL, REST APIs, search and retrieval
- **Infrastructure:** Linux, systemd, Podman, Nginx, GitHub Actions, backup and DR
- **Security:** dependency analysis, secret protection, least-privilege automation
- **Applied AI:** reproducible agent evaluation, deterministic gates, grounded reviews

## Selected public work

### [SUPERBENCH](https://github.com/BenkiNew/superbench)

[![Validate](https://github.com/BenkiNew/superbench/actions/workflows/ci.yml/badge.svg)](https://github.com/BenkiNew/superbench/actions/workflows/ci.yml)
[![Live leaderboard](https://img.shields.io/badge/leaderboard-live-2ea44f)](https://benkinew.github.io/superbench/)

A reproducible benchmark for AI coding agents built from real, anonymized
engineering incidents. It combines pinned fixtures, atomic evaluation criteria,
independent reviewer roles, deterministic reduction, and replayable evidence.

### [OSV-Scanner contribution](https://github.com/google/osv-scanner/pull/3038)

An upstream documentation improvement clarifying how open version ranges in
manifest files are extracted and why resolved lockfiles provide stronger
installed-version evidence.

### [8821au-20210708 driver fixes](https://github.com/morrownr/8821au-20210708/pull/210)

Fixed four kernel-API incompatibilities blocking the RTL8821AU Wi-Fi driver
build on Linux kernel 7.1/7.2 (hidden flexible-array members, a removed
`strncpy()`, the `cfg80211_ops` net_device→wireless_dev migration, and a
retired wiphy flag) — found bringing up real hardware on a current kernel.
Followed up with [#211](https://github.com/morrownr/8821au-20210708/pull/211)
to version-gate the `cfg80211_ops` migration across kernel.org tags, preserving
backward build compatibility on kernels 5.4 through 7.0.

### [systemd SELinux/stdio ordering fix](https://github.com/systemd/systemd/pull/43646)

Traced a production SELinux denial to service-manager code opening
`StandardOutput=`/`StandardError=`/`StandardInput=` targets before the unit's
own domain exists, and got the ordering documented in `systemd.exec(5)`.
Verified live across two hosts with independent kernel and policy builds
before submitting.

## How I work

- Production claims need live, reproducible evidence.
- A backup is only trustworthy after a successful restore test.
- Automation should fail visibly and have a rollback path.
- Secrets and real personal data do not belong in Git history.
- AI output is a proposal until deterministic checks validate it.

## Contact

- Email: [benkinew@gmail.com](mailto:benkinew@gmail.com)
- X: [@benkinew](https://x.com/benkinew)
- GitHub: [@BenkiNew](https://github.com/BenkiNew)

I welcome technically grounded collaboration around developer tooling,
reliability, security, search, and practical AI evaluation.
