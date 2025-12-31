---
name: macos-remove-quarantine
description: Remove or check the quarantine extended attribute on macOS files. Use when a downloaded file is blocked by Gatekeeper or shows "unverified developer" warnings.
---

# macOS Remove Quarantine

## When to use this skill

Use when:
- A downloaded file won't open due to Gatekeeper
- User sees "unverified developer" or "can't be opened" warnings
- User wants to check if a file is quarantined

## Remove quarantine

```bash
xattr -d com.apple.quarantine /path/to/file
```

For directories (recursive):

```bash
xattr -dr com.apple.quarantine /path/to/directory
```

## Check quarantine status

```bash
xattr -l /path/to/file | grep quarantine
```

If output is empty, the file is not quarantined.

## Notes

- Only works on macOS
- No `sudo` required for files you own
- The quarantine attribute is `com.apple.quarantine`

