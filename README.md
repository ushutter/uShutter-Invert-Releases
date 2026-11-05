uShutter Invert 0.1.0 — Apple Silicon test build

SYSTEM REQUIREMENTS
- Apple Silicon Mac (M1 or newer)
- macOS 14 or later

INSTALL
1. Drag “uShutter Invert” to the Applications shortcut.
2. Open /Applications.
3. Because this internal test build is not signed with an Apple Developer ID or notarized, macOS may block the first launch.
4. First try Control-clicking the app, choosing Open, then choosing Open again.
5. If macOS still blocks it, open Terminal and run:

   xattr -dr com.apple.quarantine "/Applications/uShutter Invert.app"

6. Launch the app again.

TEST CHECKLIST
- Create or open a Roll.
- Import a real Sony ARW.
- Confirm preview and Preview Histogram appear.
- Sample Film Base, then sample Neutral Area.
- Test Crop, Straighten, Tone, and Color controls.
- Export one JPEG and one 16-bit TIFF.
- Confirm the Roll saves and reopens.

LIMITATIONS
- Internal arm64 compatibility test only.
- Ad-hoc signed; no Apple Developer ID and no notarization.
- Gatekeeper warnings are expected.
- No custom application icon is included in this build.
- Do not treat this package as a public production release.
