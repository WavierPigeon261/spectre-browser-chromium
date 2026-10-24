# Spectre Browser branding assets

Place the original icon files here using these names:

- `icons/windows/SpectreBrowser.ico` — Windows icon file. This is the file needed to wire in a custom Windows icon.
- `icons/vector/SpectreBrowser.svg` — editable vector original.
- `icons/raster/SpectreBrowser-16.png` through `SpectreBrowser-256.png` — PNG exports, with the pixel size in each filename.

The Windows ICO is copied into Chromium's launcher icon location during source
preparation. The SVG and PNG files are kept as design originals and exports.

The New Tab Page uses a text wordmark, so a separate logo SVG is not needed.
The Poppins Bold font is bundled locally in `fonts/Poppins-Bold.ttf`, with its
SIL Open Font License in `fonts/OFL.txt`; the build does not fetch fonts at
runtime.
