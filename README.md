# KeySlip MCPB binary releases

This public repository distributes KeySlip's compiled MCP Bundle (`.mcpb`) installers and SHA-256 checksums. The KeySlip application source repository remains private. Releases contain six binaries for Linux, macOS, and Windows on x86-64 and ARM64, plus the matching `server.json` metadata.

## License and use

Copyright © 2026 SURCOD S.R.L. KeySlip is proprietary software, all rights reserved. The KeySlip source repository has no separate software license file; these binaries are not open-source releases. Downloads are provided for installing and running KeySlip's local MCP server with the KeySlip service, subject to the [KeySlip Terms of Use](https://keyslip.app/terms). No redistribution or other license is granted here; all other rights are reserved, subject to applicable law and any separate written permission.

## Verify a release

Download the bundle for your OS and architecture together with `SHA256SUMS`, then verify the bundle before installation:

```sh
sha256sum -c SHA256SUMS
```
