<h1><img src="assets/appicon.png" width="36" height="36" align="absmiddle" /> FastFileExplorer</h1>

A lightning-fast Windows file explorer with real-time folder sizes, Quick Look preview, and a sleek dark UI — built with Go and Wails.

![Demo](assets/demo.gif)

---

## Features

- **Instant directory listing** — reads directory entries immediately with no blocking
- **Concurrent folder sizes** — all folder sizes calculated in parallel using Windows native `FindFirstFile` API, streamed live as they arrive
- **Sort by size** — list re-sorts in real time as folder sizes load in; sort preference persists across sessions and folder navigation
- **Quick Look** (`Space`) — preview images (JPG, PNG, GIF, SVG, WebP…), source code and text files, or folder stats — without opening a separate app
- **Arrow navigation in preview** (`←` / `→`) — flip through files while Quick Look stays open
- **Real-time search** — filters the current directory as you type
- **Drive panel** — shows all drives with usage bars and free space
- **Recycle Bin delete** (`Delete`) — sends files to Recycle Bin, never permanently deletes
- **Rename** (`F2`), **New Folder**, **Copy**, **Open in Explorer**
- **Virtual scroll** — renders only visible rows; handles 100 000+ files without lag
- **Keyboard-first navigation** — arrow keys, Enter, Backspace, Alt+←/→

---

## Download

Grab the latest `FastFileExplorer.exe` from the [**Releases**](https://github.com/djekanovic/FastFileExplorer/releases) page.

No installation required — just run the `.exe`. Windows 10/11 has WebView2 built in.

---


## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Space` | Open / close Quick Look |
| `← →` | Navigate files in Quick Look |
| `Esc` | Close Quick Look |
| `Enter` | Open file or folder |
| `F2` | Rename |
| `Delete` | Move to Recycle Bin |
| `Backspace` | Go up one level |
| `Alt + ←` | Back |
| `Alt + →` | Forward |
| Arrow keys | Move focus up / down |

---

## Tech stack

| Layer | Technology |
|-------|-----------|
| Backend | Go — file I/O, concurrent folder sizing, Windows API calls |
| Frontend | Vanilla JS + Vite — zero framework overhead |
| Bridge | Wails v2 — wraps WebView2 (built into Windows 10/11) |

---

## Requirements

- Windows 10 or Windows 11
- No additional runtime — WebView2 is built into the OS

