
# Karabiner-Elements Custom Rules – Linux-style shortcuts for macOS

This configuration brings Linux/X11-style keyboard and mouse behavior to macOS using [Karabiner-Elements](https://karabiner-elements.pqrs.org/). It includes intuitive text editing, window and tab control, and middle-click paste.

---

## Keyboard Mappings

### Ctrl-based Shortcuts
Replicates common Linux/X11 keyboard shortcuts:
- `Ctrl+X/C/V/A/Z` → `⌘+X/C/V/A/Z` (Cut, Copy, Paste, Select All, Undo)
- `Ctrl+T/W/Q/R/L/Space` → `⌘+T/W/Q/R/L/Space` (New tab, Close tab, Quit, Reload, Focus address bar, Spotlight)
- `Ctrl+←/→` → `⌥+←/→` (move cursor by word)
- `Ctrl+Backspace` → `⌥+Backspace` (delete word)

### Home/End Behavior
- `Home` → `⌘+←` (beginning of line)
- `End` → `⌘+→` (end of line)
- `Shift+Home/End` → select to start/end of line

### Delete Key Behavior
- `Delete` (Supr) key → `⌘+Delete` in **Finder only** to move selected files to Trash

### Window Management

- `Option` (mapped Start key) → `Ctrl+↑` to trigger **Mission Control**
- `Cmd+Click` → `Cmd+Ctrl+Click` → enables window dragging from anywhere on the window

> ⚠️ To activate drag-anywhere behavior, macOS needs a hidden gesture setting enabled.
> Run the following command in Terminal and **log out/in**:
>
> ```bash
> defaults write -g NSWindowShouldDragOnGesture -bool true
> ```

---

## Mouse

- **Mouse Button 3 (middle-click)** → `⌘+V` to paste  
  (mimics Linux/X11 middle-click paste)

---

## Files in this repo

- `karabiner.json` — Drop-in config with all rules applied
- `README.md` — Explanation of what each rule does and setup instructions

---

## How to Use

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
2. Replace your config file:
   ```bash
   cp karabiner.json ~/.config/karabiner/karabiner.json
   ```
3. Log out and log back in, or restart Karabiner
4. (Optional) Enable window drag gesture:
   ```bash
   defaults write -g NSWindowShouldDragOnGesture -bool true
   ```

---

Enjoy Linux-style shortcuts on macOS
