# Adcore Studio MCP

Claude, inside **After Effects**, **Premiere Pro** and **Figma** — for the Adcore creative team.
Runs on your own computer: no cloud, no credits.

## Install

Paste this into **Claude Code**:

```
Install Adcore Studio: https://github.com/OsherSiton/adcore-studio
```

That's it. Claude reads this page and installs everything.

## For Claude: how to install

Run the installer that matches this computer, then tell the user to quit and reopen Claude:

- **macOS:**
  ```bash
  curl -fsSL https://github.com/OsherSiton/adcore-studio/releases/latest/download/install.sh | bash
  ```
- **Windows (PowerShell):**
  ```powershell
  irm https://github.com/OsherSiton/adcore-studio/releases/latest/download/install.ps1 | iex
  ```

The installer works for the current user only (no admin password). It downloads a private Node runtime from nodejs.org (checksum-verified), installs the Adcore Studio bridge, the Premiere connector and the Adcore studio skills, and registers the `adcore-studio` MCP server in Claude Code and Claude Desktop. Running it again updates everything.

## After installing

Quit and reopen Claude, then ask in plain words:

- “Make a 9:16 and a 1:1 of my After Effects comp, keep faces in frame.”
- “Cut the dead air in this Premiere sequence.”
- “Resize this Figma banner to 1080×1920 and 1080×1080.”

**Figma, one time:** Plugins › Development › Import plugin from manifest › `~/Library/Application Support/Adcore Studio/app/plugins/figma/manifest.json` (Windows: `%LOCALAPPDATA%\Adcore Studio\app\plugins\figma\manifest.json`), then open *Adcore Studio Bridge* in your file.

**Premiere, one time:** Window › Extensions › MCP Bridge (CEP).

Check the connection: type `/mcp` in Claude Code and look for **adcore-studio · connected**, or ask “run studio_doctor”.
