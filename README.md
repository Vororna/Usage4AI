# Usage4AI

A macOS menu bar app for monitoring Claude API usage.

![Screenshot](screenshot.png)

## Features

- Real-time 5-hour and 7-day usage monitoring
- Menu bar progress bars with percentage display
- Customizable refresh intervals (30s - 10m)
- Usage alerts when exceeding 90%
- Auto-retry on network failure
- Supports both Claude Pro and Claude Max subscriptions

## Requirements

- macOS 15.0+
- [Claude Code CLI](https://github.com/anthropics/claude-code) installed and logged in (for OAuth token)

## Installation

### Option 1: Download Release

Download the latest version from [Releases](https://github.com/lion9453/Usage4AI/releases).

### Option 2: Build from Source

```bash
git clone https://github.com/lion9453/Usage4AI.git
cd Usage4AI
xcodebuild -scheme Usage4AI -configuration Release -derivedDataPath build build
cp -R build/Build/Products/Release/Usage4AI.app /Applications/
```

### First Launch Setup

1. Make sure you have [Claude Code CLI](https://github.com/anthropics/claude-code) installed and logged in
2. Open Usage4AI from Applications or Spotlight (`Cmd + Space`, type "Usage4AI")
3. **Important**: When prompted for Keychain access, enter your Mac password and click **"Always Allow"**

This grants Usage4AI permission to read the OAuth token from Claude Code's Keychain.

## Troubleshooting

### "Failed to Load" Error

If you see "Failed to Load" after reopening the app, it's usually a Keychain permission issue. Run this command to reset:

```bash
security delete-generic-password -s "Usage4AI-token" && open /Applications/Usage4AI.app
```

Then click **"Always Allow"** when the Keychain dialog appears.

### Common Causes

| Issue | Solution |
|-------|----------|
| Keychain permission denied | Reset token cache (see above) and click "Always Allow" |
| Claude Code not logged in | Run `claude` in terminal and complete login |
| Token expired | Re-login to Claude Code CLI |

### How Keychain Works

Usage4AI reads your OAuth token from Claude Code's Keychain and caches it locally:

1. First launch: Reads from `Claude Code-credentials` (requires password)
2. Subsequent launches: Reads from `Usage4AI-token` cache (no password needed)
3. If cache becomes invalid: Delete it with the command above

## Tips

### Launch at Login

To start Usage4AI automatically when you log in:

1. Click the Usage4AI icon in the menu bar
2. Click **Settings** (gear icon)
3. Enable **"Launch at Login"**

### Quick Reopen

- **Spotlight**: `Cmd + Space` → type "Usage4AI" → Enter
- **Terminal**: `open /Applications/Usage4AI.app`

## Disclaimer

This is an unofficial tool, not affiliated with Anthropic. Usage data may differ from official dashboard.

## License

[AGPL-3.0](LICENSE)

Copyright 2026 [lion9453](https://github.com/lion9453)
