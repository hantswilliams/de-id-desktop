# De-ID Desktop

De-ID Desktop takes names, IDs, contact details and faces out of text and
files on your own computer, so AI tools such as ChatGPT, Claude, Gemini and
Copilot only get the version without them. It runs on macOS, Windows and
Linux, with no account, no cloud and no network connections of its own.

**Get it at [deid-tool.com](https://deid-tool.com/install.html):** $29.99
once, for one person, with updates included and a full refund within 30
days. It's in alpha (0.8.4), so what it does and how it looks may change
from one version to the next.

This repository has no code. It's where De-ID Desktop's release notes and
checksums are published, and where you can report a problem or ask for
something.

## Report a problem or ask for something

[Open an issue](https://github.com/hantswilliams/de-id-desktop/issues/new/choose).
Something it missed is the most useful thing you can send.

**Issues are public, so please don't post real names, patient or student
information, or documents.** De-identify first, or describe the shape of the
problem: "a name split over two lines in a scanned PDF wasn't caught".

To report a security problem privately, see [SECURITY.md](SECURITY.md).

## Releases and checksums

Each version's notes are under [Releases](https://github.com/hantswilliams/de-id-desktop/releases),
and in [`releases/`](releases/) in this repository. The installers come from
Polar after you buy; `SHA256SUMS.txt` lists each file's SHA-256 checksum so
you can check that what you downloaded is what was built.

| System | Command, run in the folder you saved the file to |
|---|---|
| Mac | `shasum -a 256 De-ID_0.8.4_aarch64.dmg` |
| Windows | `certutil -hashfile De-ID_0.8.4_x64-setup.exe SHA256` |
| Linux | `sha256sum De-ID_0.8.4_amd64.deb` |

The result should match the line for that file in `SHA256SUMS.txt`.

## More

- [Security review](https://deid-tool.com/security.html): what it stores
  and where, what it connects to (nothing), how releases are tested, and
  what it can't promise.
- [Website privacy](https://deid-tool.com/privacy.html): what deid-tool.com
  collects. The app itself sends nothing.
- Email: [hantsawilliams@gmail.com](mailto:hantsawilliams@gmail.com)

De-ID Desktop is made by Hants Williams.
