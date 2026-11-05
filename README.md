# uShutter Invert

uShutter Invert is a desktop application for photographers who scan film with a digital camera. It reads camera RAW files, converts color negatives into positive images, keeps the work organized by roll, and exports color-managed JPEG or 16-bit TIFF files.

The application is macOS-first and is currently under active development.

## Why uShutter Invert

Camera scanning can capture a great deal of detail, but converting a full roll often means repeating the same steps in a general-purpose photo editor. Film base sampling, inversion, frame alignment, cropping, color correction, and export all have to stay consistent without forcing every frame to look identical.

uShutter Invert puts those steps into one roll-based workflow. Each photo keeps its own settings. When a correction should apply to the whole roll, the user can copy it deliberately with **Sync to Roll**.

## A film-first workflow

1. Import the camera RAW files for a roll.
2. Sample a clear film-base area.
3. Detect the frame and review the suggested crop before applying it.
4. Correct alignment, tone, and color while viewing the positive image.
5. Adjust individual frames or sync selected settings across the roll.
6. Export finished JPEG files or 16-bit TIFF files for further editing.

The source RAW files are never modified. uShutter Invert stores the work in a versioned `.ushutter-invert` project beside the roll and restores the most recent project when the application opens again.

## Frame detection that respects the film

uShutter Invert can detect a centered film frame and correct its rotation. The crop remains a constrained rectangle, so adjusting a corner cannot introduce free-form keystone distortion.

Two film-aware crop modes are available:

- **135 · Preserve sprocket holes** keeps the perforated film area when it is part of the intended image.
- **120 · Preserve film border** keeps a measured border around the frame.

The detected crop is only a suggestion. Nothing changes until the user confirms it. Lens distortion can be corrected before detection, and a line drawn along a film edge can be used to straighten the frame. Separate 90-degree controls change the output orientation without adding another interpolation step.

[Image: detected 135 or 120 frame with the editable crop overlay]

## RAW processing and film inversion

Camera RAW files are decoded through LibRaw and processed as 16-bit linear image data. uShutter Invert estimates the film base from a selected area and performs the first conversion in optical-density space.

The positive preview can then be adjusted with controls for:

- exposure
- black and white points
- midtones and highlight protection
- temperature and tint
- saturation

Preview rendering runs in the background so the interface remains responsive while moving through a roll.

[Image: before and after film-base sampling and inversion]

## Output for sharing or further editing

uShutter Invert supports two output paths:

- **JPEG** in sRGB, with resolution and quality controls for viewing and sharing
- **16-bit TIFF** in ProPhoto RGB for an editable handoff to applications such as Adobe Lightroom or Photoshop

Both formats include an embedded ICC profile. Export runs in the background and processes full-resolution frames one at a time.

## Film metadata, without scan-camera clutter

The metadata editor describes the photograph on film: film camera, lens, film stock, roll, frame number, original capture date, author, and notes.

Exported files do not copy the digital scan camera's MakerNotes, serial numbers, GPS data, or scan exposure settings. The output keeps the film metadata, color profile, and image information needed for the finished photograph.

## Current compatibility

The current RAW workflow has been verified with Sony α7R II and α7R III ARW files, including full-resolution decoding and export. The processing path is camera-independent, but testing with more camera models and more film stocks is still in progress.

The interface is available in English and Simplified Chinese.

## Development status

uShutter Invert is under active development and is not yet a public release. Download information, system requirements, and licensing details will be added here when they are ready.

---

## Review notes (not part of the published page)

Please confirm these points before upload:

1. Keep the status as **under active development**, or announce a preview/beta?
2. Mention the planned uShutterUp authorization model now, or wait until licensing is final?
3. Add a download or mailing-list button, or leave the page informational for now?
4. Which screenshots should be published? Suggested set:
   - main three-pane roll workflow
   - frame-detection crop overlay
   - converted positive with tone/color controls
   - TIFF/JPEG export dialog
5. Should the page stay English-only to match the current website, or include a Chinese section?
