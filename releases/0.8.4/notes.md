# De-ID Desktop 0.8.4 Alpha

**Alpha.** An early version, for testing: what it does and how it looks may
change from one version to the next.

**Get it at [deid-tool.com](https://deid-tool.com/install.html):** $29.99 once,
with updates included. The installers come from Polar after you buy;
invited testers use the link in their invite. `SHA256SUMS.txt`, attached below, lists
each file's SHA-256 checksum, so you can check that what you downloaded is
what we built.

## Which file

| Your computer | File |
|---|---|
| Mac with Apple silicon (M1 or newer) | `De-ID_0.8.4_aarch64.dmg` |
| Mac with Intel | `De-ID_0.8.4_x64.dmg` |
| Windows 10 or 11 (Intel or AMD), Windows 11 (ARM) | `De-ID_0.8.4_x64-setup.exe` |
| Ubuntu 22.04+ or Debian 12+, Intel or AMD | `De-ID_0.8.4_amd64.deb` |
| Ubuntu 22.04+ or Debian 12+, ARM | `De-ID_0.8.4_arm64.deb` |
| Fedora 36+ or RHEL, Rocky, Alma 10, Intel or AMD | `De-ID-0.8.4-1.x86_64.rpm` |
| Fedora 36+ or RHEL, Rocky, Alma 10, ARM | `De-ID-0.8.4-1.aarch64.rpm` |

Not sure? On a Mac, Apple menu → **About This Mac** shows "Chip: Apple M…"
or "Processor: … Intel …". On Linux, `uname -m` prints `x86_64` (Intel or
AMD) or `aarch64` (ARM).

## Install

- **Mac** (macOS 14 or later): open the DMG and drag **De-ID** to
  Applications.
- **Windows:** run the installer. It installs for your account only and
  needs no admin rights. It isn't signed yet, so the first time Windows
  asks, choose **More info → Run anyway**.
- **Ubuntu and Debian:** in a terminal, in the folder you saved it to,
  `sudo apt install ./De-ID_0.8.4_amd64.deb` (or the `arm64` file).
- **Fedora, RHEL, Rocky and Alma:** `sudo dnf install ./De-ID-0.8.4-1.x86_64.rpm`
  (or the `aarch64` file). On RHEL, Rocky and Alma 10, turn on EPEL first
  (`sudo dnf install epel-release` on Rocky and Alma).

The first launch takes up to a minute. To update, install the new version
over the old one; your data is kept.

## What it does

De-identifies documents on your computer, with no network at all: PDFs
(scans too, read with OCR), Word, Excel, CSV, Parquet, text and photos. Drop
in files or a folder, choose how, and get clean copies next to your
originals. Each file is checked after cleaning, and anything that still
looks like an identifier is held back for you to review.

## New in 0.8.4

- **De-ID says it's in alpha.** The sidebar shows ALPHA beside the version,
  and Settings → About says what that means.

## Since 0.5.1, the last release

- **Review, then apply once.** Make all your corrections in Review, then
  apply them together. Nothing reaches an AI before you apply.
- **Audit a run:** a few random pages for someone to check, with a fix for
  anything they find.
- **Names and IDs to remove,** typed or taken from a spreadsheet, with one
  token per person.
- **Bigger, faster tables:** Excel about 8 times faster, files up to 100 MB,
  every sheet of a workbook, and Review shows a table as a table. Choose
  which columns hold personal data before a run.
- **Healthcare:** clinical notes, HL7 messages, the HIPAA Limited Data Set,
  provider and health plan numbers, and vehicle and device IDs.
- **Better with PDFs:** letter-spaced names, names broken over two lines,
  turned text, and letters on letterhead pictures. A name found once is
  removed everywhere in the file.
- **Labels or tokens:** replace names with labels (`<PERSON>`) or with the
  same token for the same person each time.
- **AI workspace** (was AI terminal): it can install an AI tool for you
  (Claude Code, Codex, Antigravity or OpenCode), says what each session's
  AI may do, and lets it read what you attach. **Logs** keeps a
  de-identified timeline and replay of each session.
- **Shared computers:** each account has its own private data folder, and
  the computer's own login is De-ID's login.

## What it doesn't do

- Read handwriting, or guarantee that badly degraded scans are clean.
  **Review redacted scans before sharing them.**
- Catch every face, or judge what else in a photo identifies someone.
  **Review every photo.**
- Read HEIC pictures (export them as JPEG first).
- Check for updates, or send anything anywhere.

## Where your data is

| | Folder |
|---|---|
| Mac | `~/Library/Application Support/app.deid.desktop/` |
| Windows | `%LOCALAPPDATA%\app.deid.desktop\` |
| Linux | `~/.local/share/app.deid.desktop/` |

It holds the crosswalk, which maps clean copies back to the real names, so
it's as sensitive as your originals. Keep the disk encrypted.

## Questions and problems

[Open an issue](https://github.com/hantswilliams/de-id-desktop/issues/new/choose),
without real identifiers, or email hello@deid-tool.com. The
[security review](https://deid-tool.com/security.html) says what De-ID
stores, what it connects to, and what it can't promise.
