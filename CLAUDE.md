# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a collection of operational scripts for **DaVinci Resolve** — scripts that have been tested and approved for production use. The primary language for Resolve scripting is Python (or Lua), executed within Resolve's embedded scripting environment.

## DaVinci Resolve Scripting Context

DaVinci Resolve exposes a scripting API via a built-in module called `DaVinciResolveScript`. Scripts are not run as standalone programs — they are loaded by Resolve itself from predefined directories:

- **macOS**: `~/Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion/Scripts/`
- **Linux**: `~/.local/share/DaVinciResolve/Fusion/Scripts/`
- **Windows**: `%APPDATA%\Blackmagic Design\DaVinci Resolve\Support\Fusion\Scripts\`

Subdirectories within `Scripts/` determine when a script appears in Resolve's UI:
- `Utility/` — appears under **Workspace > Scripts**
- `Comp/` — appears in the Fusion page
- `Edit/` — appears in the Edit page

### Bootstrapping the API

Scripts that need to run outside Resolve (e.g. via command line) must resolve the module path manually:

```python
import sys
sys.path.insert(0, "/Library/Application Support/Blackmagic Design/DaVinci Resolve/Developer/Scripting/Modules/")
import DaVinciResolveScript as dvr_script

resolve = dvr_script.scriptapp("Resolve")
```

When running inside Resolve (via the Scripts menu), `resolve` is injected automatically as a global — no import needed.

### API Entry Points

```
resolve
└── GetProjectManager()          → ProjectManager
    └── GetCurrentProject()      → Project
        ├── GetCurrentTimeline() → Timeline
        ├── GetMediaPool()       → MediaPool
        └── GetSetting(key)      → str
```

All API calls return `None` on failure rather than raising exceptions — always check return values.

## Conventions

- Scripts are self-contained single files; shared utilities live alongside them (no package structure yet).
- File names use snake_case and describe the operation (e.g. `export_stills.py`, `rename_clips.py`).
- The README (in Portuguese) tracks which scripts are approved and in active use.
