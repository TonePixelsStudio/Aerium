# Aerium by TonePixels Studio

Aerium is a free acoustic-guitar tone-shaping plugin with microphone IR processing, Acoustic Tone Match, EQ and studio effects.

## Aerium 1.1.1 for macOS

- Universal Apple Silicon (`arm64`) and Intel (`x86_64`) plugin binaries.
- VST3 and Audio Unit formats; choose either or both in the installer.
- Original approved DSP, microphone IR library and four factory presets: **Default**, **Dry Default**, **Ambient Dream** and **Martin**.
- The revised user manual and factory content use **Documents/Aerium**.
- No experimental synthetic replacement IRs are included.

[Download Aerium 1.1.1 for macOS](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/Aerium-1.1.1-macOS.pkg) · [Release notes](https://github.com/TonePixelsStudio/Aerium/releases/tag/v1.1.1) · [User manual](https://github.com/TonePixelsStudio/Aerium/releases/download/v1.1.1/Aerium-User-Manual.pdf)

## Requirements

macOS 12 or later, an Apple Silicon or Intel Mac, and an audio host supporting VST3 or Audio Units. Administrator approval is required to install into the system plugin folders. Actual support also depends on your host and macOS version.

## Install

Read [README FIRST BEFORE INSTALLATION](<README FIRST BEFORE INSTALLATION.txt>) before running the installer.

1. Save your work and quit your audio hosts.
2. Download `Aerium-1.1.1-macOS.pkg` from the release linked above. Compare its SHA-256 with the release's `SHA256SUMS.txt`.
3. Open the installer. Use **Customise** to select VST3, Audio Unit, or both. At least one format is required.
4. Complete installation, then reopen your host and scan for the selected plugin format. The plugin is named **Aerium**.
5. Open a fresh Aerium instance. If macOS asks your audio host for Documents access, allow it so Aerium can prepare its user folders.
6. Factory content and the manual are copied into your own `Documents/Aerium` folder on the first successful plugin launch. Existing same-name user files are preserved.

### Unsigned and unnotarised installer

This installer is **not Developer ID signed or notarised**. macOS may block it or warn that the developer cannot be verified. The plugin executables have ad-hoc signatures; these are not Developer ID signing or Apple notarisation.

Only proceed if you trust the source and have verified the package checksum. If macOS blocks this specific installer, follow Apple's [supported Privacy & Security / Open Anyway instructions](https://support.apple.com/en-us/102445), where available. Do not disable Gatekeeper or use security-bypass scripts. Do not override a warning that explicitly identifies malware.

## Installed locations

```text
/Library/Audio/Plug-Ins/VST3/Aerium.vst3
/Library/Audio/Plug-Ins/Components/Aerium.component
/Library/Application Support/TonePixels Studio/Aerium/Factory Resources/
```

The selected plugin formats determine which plugin bundle is installed. Factory resources are shared; each user's editable data lives separately in Documents:

```text
~/Documents/Aerium/
├── Microphone IRs/
├── Factory Presets/
├── Presets/
├── EQ Profiles/
├── Tone Match Profiles/
└── Aerium User Manual.pdf
```

- `.tps` stores a complete Aerium preset.
- `.tpseq` stores an EQ correction/profile. Loading it into Acoustic Response changes the EQ, not unrelated effects.
- Existing beta installations and their separate user data are not migrated or removed automatically.
- The installer was updated on 21 November 2026 to correct unreadable shared factory-resource metadata that could cause “Aerium could not prepare Documents/Aerium.” If affected, close audio hosts and reinstall the current package; preserve your existing Documents/Aerium folder. The audio binaries and factory-content bytes are unchanged.
- If folder preparation still fails after the updated installer, check free space and the host's Documents access in macOS Privacy & Security. Aerium does not silently switch to another data folder.
- Release attachments labelled `superseded` are rollback archives of the earlier installer and checksum. Use `Aerium-1.1.1-macOS.pkg` and `SHA256SUMS.txt` for the correction.

## Factory presets

**Default**, **Dry Default**, **Ambient Dream** and **Martin** retain their approved settings and original IR assignments. Fresh instances start with Default; saved DAW projects recall their saved plugin state.

## Third-party content

Bundled resources retain their own licence terms. See the included IR licence notices and attribution. Permission to use an IR in audio processing is distinct from permission to redistribute its data file; this README does not represent unresolved permissions as cleared.

## Validation scope

The build was checked using offline VST3/AU hosts on Apple Silicon natively and under Rosetta, including factory-state/audio comparisons. These checks do not replace testing in your DAW, physical Intel hardware, or every supported macOS version. For the Documents repair, fresh/repeated provisioning passed on arm64 and x86_64/Rosetta, and existing installed AU/VST3 loading was checked in Ableton. Privileged reinstallation and fresh-setup confirmation in Ableton/GarageBand on the affected Mac remain pending. No Windows installer is included in this macOS release.
