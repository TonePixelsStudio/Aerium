# Aerium 1.1.1 beta — validation scope

Candidate: 22 November 2026 reliable-setup build, both plugin formats at version 1.1.1.

Installer SHA-256:

```text
726df8c78b16c36a33f6262fb78bc300ff4cde85018dcc6bb320cd20db067cf6
```

| Check | Evidence and scope |
|---|---|
| Normal graphical macOS installation | Same-version upgrade completed successfully after administrator authentication; AU and VST3 were selected by default |
| Installed AU/VST3 | Executable hashes and ad-hoc signatures matched the validated package |
| Ableton Live 12.4.16 / Rosetta | Both formats loaded from their installed system paths; setup returned success; disposable project restart and saved bypass-state recall passed |
| Logic Pro 11.2 | Installed AU opened with its Main editor and IR picker visible; native arm64 AUHostingService reported successful setup |
| Apple's AU validator | Passed on arm64 and x86_64/Rosetta, including rendering and parameter scheduling |
| Approved audio | Four presets at 44.1/48 kHz on both architectures: all 16 comparisons matched the approved VST3 audio exactly; state recall matched |
| Latency | Unchanged in the comparison configuration: 29 samples at 44.1 kHz and 0 at 48 kHz |
| Fresh Documents synchronisation | Isolated normal-user fixture produced byte-identical copies of 83 IRs, four presets and the manual |
| Read-only Documents | POSIX-denied fixture retained factory access, rejected saves without redirecting and recovered after explicit Retry |
| Missing/unreadable optional metadata | Did not block factory-content synchronisation |
| Existing user content | Modified IR/custom preset fixtures were preserved; tracked production/user/beta files had no unexpected content changes |
| UI harness | All four preset callbacks, 83 IR validations and editor reopening passed; error notice/Retry recovery passed |

## Limits

- The recurring error reported on a different beta tester's Mac was not directly traced there. Its exact initial filesystem error remains unknown.
- A POSIX read-only fixture is not a genuine macOS TCC-denial test.
- Redirected iCloud Documents, a newly created macOS user account, GarageBand and physical Intel hardware were not tested.
- Actual-DAW guitar listening, real input latency and continuous playback performance were not established by the GUI checks. Ableton's audio engine was disabled during those loading/recall checks.
- Logic file-picker automation stalled while navigating a path; the user dismissed it. Do not interpret that attempted navigation as a completed direct-factory selection in Logic.
- The installer remains unsigned/unnotarised; ad-hoc signatures are not Developer ID signing or Apple notarisation.
- Existing records still lack verified redistribution evidence for twelve bundled IR files. No rights clearance is asserted.

No DSP algorithm, factory IR WAV, factory preset or user-manual bytes were changed by this packaging proposal. The illustrated installation guide is a separately reviewed documentation asset.
