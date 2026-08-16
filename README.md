# Tenvar

**Transcription and evidence, entirely on your own machine.**

Tenvar turns recordings and documents into text, helps you find what matters in them, and builds
reports that cite the exact moment — with no account, no cloud processing and no telemetry. Your
recordings, transcripts, notes and reports stay on your disk, encrypted at rest.

This repository contains **no source code**. It exists to distribute the installers and to answer
the app's update check.

---

## Download

**Latest: v0.1.0 — early access**

| Platform | Download | Size |
| --- | --- | --- |
| **Windows** 10 (2004+) / 11, 64-bit | [Tenvar_0.1.0_x64-setup.exe](https://github.com/jBlanca/tenvar.app/releases/download/v0.1.0/Tenvar_0.1.0_x64-setup.exe) | 686 MB |
| Windows — managed deployment | [Tenvar_0.1.0_x64_en-US.msi](https://github.com/jBlanca/tenvar.app/releases/download/v0.1.0/Tenvar_0.1.0_x64_en-US.msi) | 777 MB |
| **macOS** 14.4+, Apple Silicon | [Tenvar_0.1.0_aarch64.dmg](https://github.com/jBlanca/tenvar.app/releases/download/v0.1.0/Tenvar_0.1.0_aarch64.dmg) | 100 MB |
| **Linux** — any distribution | [Tenvar_0.1.0_amd64.AppImage](https://github.com/jBlanca/tenvar.app/releases/download/v0.1.0/Tenvar_0.1.0_amd64.AppImage) | 1.29 GB |
| Linux — Debian & Ubuntu | [Tenvar_0.1.0_amd64.deb](https://github.com/jBlanca/tenvar.app/releases/download/v0.1.0/Tenvar_0.1.0_amd64.deb) | 1.14 GB |

Every version, including older ones, is on the [Releases page](https://github.com/jBlanca/tenvar.app/releases).

> **Why are the Linux files so much larger?**
> They carry both NVIDIA (CUDA) and cross-vendor (Vulkan) acceleration, so the app runs fast on
> whatever graphics card it finds without you choosing a build. Windows and macOS ship a single
> acceleration path each.

Speech, language and OCR models are **not** included in the installer. The app offers them on first
run and downloads only the ones you pick — so the installed size grows according to what you use.

---

## Installing

### Windows

These early-access builds are **not yet code-signed**, so Windows will warn you the first time:

1. Run the installer. SmartScreen says *"Windows protected your PC."*
2. Click **More info**, then **Run anyway**.

If you would rather verify the file first, see [Verifying your download](#verifying-your-download).

### macOS

Apple Silicon only (M1 and later). The build is **signed and notarized by Apple**, so it opens
normally — drag it to Applications and launch it.

### Linux

**AppImage** — runs on any distribution, no installation:

```sh
chmod +x Tenvar_0.1.0_amd64.AppImage
./Tenvar_0.1.0_amd64.AppImage
```

If it will not start, you may need FUSE (`sudo apt install libfuse2` on Ubuntu 22.04 and later).

**Debian / Ubuntu package**:

```sh
sudo apt install ./Tenvar_0.1.0_amd64.deb
```

System audio recording needs PipeWire or PulseAudio, which nearly every desktop already runs.

---

## Verifying your download

Each release lists the SHA-256 of every file in its notes. Compare it with the file you received —
if they differ, do not run it.

```sh
# macOS
shasum -a 256 Tenvar_0.1.0_aarch64.dmg

# Linux
sha256sum Tenvar_0.1.0_amd64.AppImage
```

```powershell
# Windows
Get-FileHash .\Tenvar_0.1.0_x64-setup.exe -Algorithm SHA256
```

---

## How updates work

Tenvar **never checks for updates on its own.** There is no background check, no automatic
download and no silent install.

When you open **Settings → About** and press **Check GitHub**, the app reads this repository's
public releases list, compares it with your installed version, and tells you what it found. If an
update exists, downloading it is a second, separate press. Every one of those requests is written
to the audit log in **Settings → Privacy → Network activity**, alongside every other byte the app
has ever sent.

If the check cannot reach GitHub, nothing happens and your installation is untouched.

---

## What it costs

**Three folders. Everything else unlimited.**

Inside them: as many recordings, videos, documents and notes as you like, transcribed for as long
as you like, with every feature switched on. No account, no card, no time limit, no watermark, no
export restriction. Nothing is held back for a paid tier — there is no paid tier, only a limit on
how many projects you keep at once.

A folder is a *project*, not a file drawer, so for many people three is simply enough and Tenvar
stays free permanently. A linked notes folder does not count toward it, and neither does the shared
library.

If you do need a fourth, lifting the limit is a **one-time purchase, never a subscription**, and
includes v1 and every update to it. The app shows it when you reach the limit.

This is version 0.1.0 — a real working tool, not a demo, but early. Expect rough edges, and expect
things to move between releases. Right now the most useful thing anyone can do is use it and say
what is wrong.

Activating a license needs an internet connection once. After that Tenvar re-checks it at most
weekly, and being offline is never treated as a failure — if a check cannot complete, your license
stays active. Only an explicit statement that the key was revoked will deactivate it.

---

## Privacy

The short version: recordings, transcripts, documents, notes and reports never leave your machine.

The app's interface is blocked from reaching the network at all. The only things that ever go out
are model downloads you start, an optional web/email import that is **off by default**, and the
licence check described above — and all three are recorded in an audit log you can read inside the
app.

The full account is in [PRIVACY.md](PRIVACY.md).

---

## Requirements

| | Minimum |
| --- | --- |
| **Windows** | Windows 10 version 2004, or Windows 11. 64-bit. |
| **macOS** | macOS 14.4, Apple Silicon. Capturing a specific window needs macOS 15. |
| **Linux** | 64-bit. PipeWire or PulseAudio for system audio. |
| **Memory** | 8 GB works. 16 GB is comfortable once you use the larger speech and language models. |
| **Graphics** | Optional. NVIDIA, AMD, Intel and Apple graphics all accelerate transcription; without one, everything still runs on the processor, more slowly. |

---

## Support

- Questions and problems: [open an issue](https://github.com/jBlanca/tenvar.app/issues)
- Changes in each version: [CHANGELOG.md](CHANGELOG.md)

Tenvar is commercial software. Its source code is not public.
