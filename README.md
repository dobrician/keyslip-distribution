# KeySlip MCPB binary releases

This public repository distributes KeySlip's compiled MCP Bundle (`.mcpb`) installers and SHA-256 checksums. The KeySlip application source repository remains private. Releases contain six binaries for Linux, macOS, and Windows on x86-64 and ARM64, plus matching `server.json` metadata.

## License and use

KeySlip is proprietary, closed-source software. The source repository has no standalone software license file; these releases are binary downloads only, not open-source releases. Use is subject to the [KeySlip Terms of Use](https://keyslip.app/terms). No broader license is stated here.

## Handing a credential to a contractor

**EN:** Handing a credential to a contractor? Send a KeySlip link instead of pasting it into chat. Read the [contractor guide](https://keyslip.app/share-access-with-contractors) and try the [free flow](https://keyslip.app/). The link does not prevent copying or capture. Expiring or consuming the message does not revoke the underlying credential; revoke or rotate it separately at its source.

**RO:** Predai un credential unui contractor? Trimite un link KeySlip în loc să-l lipești în chat. Citește [ghidul pentru contractori](https://keyslip.app/share-access-with-contractors) și încearcă [fluxul gratuit](https://keyslip.app/). Linkul nu împiedică copierea sau capturarea. Expirarea sau consumarea mesajului nu revocă credentialul; revocă-l sau rotește-l separat în sistemul sursă.

## Publish a later release

After the matching version is deployed on keyslip.app, run the **Release KeySlip MCPB binaries** workflow with that exact version. It reads the live `server.json` and `MCP-SHA256SUMS`, downloads the six public website bundles, verifies each SHA-256 value and version, then creates a new immutable release using this repository's own `GITHUB_TOKEN`. Existing tags are never replaced.

## Verify a release

Download the bundle for your OS and architecture together with `SHA256SUMS`, then verify the bundle before installation:

```sh
sha256sum -c SHA256SUMS
```
