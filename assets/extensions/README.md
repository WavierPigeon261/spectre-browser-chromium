# Bundled extensions

The Windows build downloads and SHA-256-verifies these pinned upstream CRX
releases before compilation:

- uBlock Origin 1.75.0, signed release ID `fkgkibajhfbepljeaefdnfnegdcjomkh`
- Chromium Web Store 1.5.5.4, ID `ocaahdebbfolfmndjeplogmgcagdmblk`

The bundled Web Store helper is the verified GitHub release with ID
`ocaahdebbfolfmndjeplogmgcagdmblk`; it is not the `oboonakemofpalcgghocldedbnnbapid`
ID previously suggested. Its signed identity is preserved.

uBlock Origin is installed as a regular external extension, so users can remove
it from `chrome://extensions`. The Web Store helper is loaded as an external
component extension, so users cannot disable or remove it through the browser
UI. This uses Chromium's component-extension location, not an enterprise
force-install policy. Both signed CRX files are included in the release ZIP and
installer. Extension updates are pinned to browser releases; update the
versions, URLs, and hashes in `downloads.ini` together when rolling either
extension.

The GitHub uBlock release is signed with a different key from the Chrome Web
Store listing, so its ID differs from `cjpalhdlnbpafiamejdnhcphjbkeiagm`.
The browser uses the CRX's authentic signed ID rather than changing or
misrepresenting its signature.

The Chromium Web Store helper uses the existing ungoogled-chromium
`extension-mime-request-handling` patch. Spectre Browser allows its HTTPS CRX
downloads only when initiated by that helper or a Chrome Web Store page; users
still confirm each installation in Chromium's normal extension install prompt.
No general Google services or enterprise extension policies are enabled.
