# KeySlip MCPB binary releases

This public repository distributes KeySlip's compiled MCP Bundle (`.mcpb`) installers and SHA-256 checksums. The KeySlip application source repository remains private. Releases contain six binaries for Linux, macOS, and Windows on x86-64 and ARM64, plus matching `server.json` metadata.

## License and use

KeySlip is proprietary, closed-source software. The source repository has no standalone software license file; these releases are binary downloads only, not open-source releases. Use is subject to the [KeySlip Terms of Use](https://keyslip.app/terms). No broader license is stated here.

## Publish a later release

After the matching version is deployed on keyslip.app, run the **Release KeySlip MCPB binaries** workflow with that exact version. It reads the live `server.json` and `MCP-SHA256SUMS`, downloads the six public website bundles, verifies each SHA-256 value and version, then creates a new immutable release using this repository's own `GITHUB_TOKEN`. Existing tags are never replaced.

## Verify a release

Download the bundle for your OS and architecture together with `SHA256SUMS`, then verify the bundle before installation:

```sh
sha256sum -c SHA256SUMS
```
