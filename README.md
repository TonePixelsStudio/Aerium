# Aerium by TonePixels Studio

Aerium is a free acoustic-guitar tone-shaping plugin with microphone IR processing, Acoustic Tone Match, EQ and studio effects.

## Aerium 1.1.1 — macOS beta

**Beta software for testing.** Bugs, compatibility problems or crashes may occur. Save your DAW projects regularly.

- Universal Apple Silicon and Intel VST3 and Audio Unit plugins.
- VST3, AU or both in the installer; both are selected by default.
- The original 83 factory IR WAVs and four presets: Default, Dry Default, Ambient Dream and Martin.
- Approved audio processing and plugin identities retained.
- Factory presets and IRs load from Application Support independently of optional Documents setup.

[Download macOS installer](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/Aerium-1.1.1-macOS.pkg) · [Read the illustrated beta installation guide](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/README-FIRST-BEFORE-INSTALLATION.pdf) · [User manual](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/Aerium-User-Manual.pdf) · [Checksums](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/SHA256SUMS.txt)

## Requirements and installation

macOS 12 or later, an Apple Silicon or Intel Mac, and a compatible VST3/AU host. Your DAW may require a newer macOS version. No Windows installer is included.

1. Read the illustrated guide, save your work and close your audio hosts.
2. Download `Aerium-1.1.1-macOS.pkg` and compare its SHA-256 with `SHA256SUMS.txt`.
3. Open the installer and choose VST3, Audio Unit, or both under Customise. Complete the normal administrator authentication.
4. Reopen your DAW and load **Aerium**. Use VST3 in Ableton Live or AU in Logic Pro/GarageBand. Rescan plugins if necessary.

The installer is **unsigned and unnotarised**. Its plugins are ad-hoc signed, not Developer ID signed. If macOS blocks this installer, follow the screenshots in the guide and Apple's [per-installer opening instructions](https://support.apple.com/en-us/102445) only if you trust the source and have verified the download. Do not disable Gatekeeper or override an explicit malware detection.

## Your files

The installer places selected formats at:

```text
/Library/Audio/Plug-Ins/VST3/Aerium.vst3
/Library/Audio/Plug-Ins/Components/Aerium.component
```

Shared read-only factory content is installed at:

```text
/Library/Application Support/TonePixels Studio/Aerium/Factory Resources/
```

Your editable content remains at:

```text
~/Documents/Aerium/
├── Microphone IRs/
├── Factory Presets/
├── Presets/
├── EQ Profiles/
├── Tone Match Profiles/
└── Aerium User Manual.pdf
```

Aerium copies missing factory content and the manual to Documents when access permits. Existing same-name custom or modified files are preserved. If Documents setup is incomplete, readable factory content remains available from Application Support. The setup notice offers **RETRY SETUP**, **COPY DETAILS** and **DISMISS**. User saves still require access to the intended Documents location; they are not silently redirected.

If Documents is in iCloud Drive, use Finder's **Keep Downloaded** option where available for user IRs and profiles needed offline. Allow your host Documents access if macOS asks and you trust the host. Do not delete your Aerium folder, move plugin bundles manually or change user-folder ownership as a troubleshooting shortcut.

- `.tps` stores a complete Aerium preset.
- `.tpseq` stores an EQ profile; loading it changes EQ without changing unrelated effects.
- Fresh instances start with Default; saved DAW projects recall their saved state.
- Separately named beta plugins and their data are not automatically removed or migrated.

## Beta feedback

Open Aerium Settings and click **REPORT A BUG** (the "Report for Error" function described in the guide). This opens an unsent email draft for you to review. Include your Mac model, macOS and DAW versions, audio interface, steps to reproduce and a screenshot where helpful.

Installation help: [tonepixelsstudio@gmail.com](mailto:tonepixelsstudio@gmail.com).

## Validation and content notices

See [VALIDATION.md](VALIDATION.md) for the exact tested scope and remaining limits. Successful local installation, Ableton AU/VST3 loading/project recall, Logic AU loading, and native/Rosetta AU validation are recorded. Genuine TCC-denied and redirected-iCloud host scenarios, GarageBand and physical Intel hardware remain unverified.

Bundled third-party resources retain their licence terms. Redistribution evidence remains unresolved for twelve IR files in the existing records; this release does not claim those permissions are cleared. The rejected synthetic IR replacements are not included.

This is a distribution/documentation repository. It does not currently contain the plugin source, dependencies or a self-contained build system. This cleanup does not publish private development material or rewrite Git history.
