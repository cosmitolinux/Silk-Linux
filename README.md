# Silk Linux

> **v0.172 Testing** — Arch-based · Driver-First · Pre-built Binaries

![Status](https://img.shields.io/badge/status-testing-blue) ![Version](https://img.shields.io/badge/version-0.172-lightblue) ![Base](https://img.shields.io/badge/base-Arch-informational)

Silk Linux is an Arch-based GNU/Linux distribution with an obsessive focus on **driver reliability** and **long-term system stability**. Built on pacman and the Arch ecosystem with pre-built binary packages — no compiling required.

---

## What Makes Silk Different

- **Driver-first philosophy** — every driver is individually tested before it reaches your machine
- **Arch-based** — pacman, AUR, rolling release, all the Arch goodness
- **Pre-built binaries** — no compiling, just install and go
- **Silk Packages** — universal CLI tools that work on any Linux distro
- **Three kernel flavors** — Latest-Silk, Asahi-Based Silk (Apple Silicon), and Optimized Silk
- **Full driver coverage** — AMD, Intel, NVIDIA (open + blob), Realtek, MediaTek, Broadcom WiFi

---

## Downloads

| Edition | Target | Size | Type |
|---|---|---|---|
| Intel / AMD | x86_64 Desktop & Server | 1.2 GB | CLI only · install tool included |
| Asahi-Based Project | Apple Silicon | 2.7 GB | Live KDE environment |

---

## Installation

### Guided (recommended)

As soon as you boot up, run:

```bash
silk install system
```

Go through the installer and finish it — it handles partitioning, driver detection, and base setup automatically.

### Manual (with drivers)

Do it like Arch, but use `silkdvrfetch` to extract drivers to your mount point:

```bash
silkdvrfetch -ETR /path/to/drivers >> /mnt
```

---

## Silk Packages

Silk ships a suite of universal CLI tools that run on **any Linux distro**, not just Silk.

| Command | What it does |
|---|---|
| `sk g <package>` | Install a package — resolves the right package manager automatically |
| `sk r <package>` | Remove a package and clean up orphans |
| `sku` | Full system update |
| `skgit <url>` | Reliable git clone with retries, integrity checks, and GPG verification |

Every command produces structured output with `[OK]`, `[ERR]`, `[WARN]`, and `[INFO]` prefixes.

---

## Kernels

| Kernel | Description | Status |
|---|---|---|
| Latest-Silk | Stable build for Intel / AMD | Current |
| Asahi-Based Silk | Apple Silicon · boots into live KDE | Beta |
| Optimized Silk | Performance-tuned build | Beta |

---

## Driver Compatibility

| Vendor | Coverage |
|---|---|
| AMD GPU | Full |
| Intel GPU | Full |
| NVIDIA (open) | Full |
| NVIDIA (blob) | Full |
| Realtek WiFi | Full |
| MediaTek WiFi | Full |
| Broadcom WiFi | Full |

---

## Contributing

Silk is in early testing — contributions are very welcome.

- Found a driver bug? Open an issue
- Want to contribute a driver package? See the Driver DB
- General discussion: IRC `#silk-linux` on Libera.Chat or the Discord server

---

## License

Silk Linux is free, open-source software released under the GPL-2.0 license.  
Silk Packages are MIT-licensed and distro-agnostic.
