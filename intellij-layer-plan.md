# IntelliJ Shortcuts — Layer 3 Design Plan

## Context

The design intent:
- **Layer 1 (Nav&Num)** = base layer for IntelliJ usage (navigation, browsing)
- **Layer 3 (Customs)** = IntelliJ shortcut layer, triggered by holding both `mo 1` (left thumb) + `mo 2` (right thumb) simultaneously (tri-layer)
- Layer 3 keys should be **positionally related** to their Layer 1 counterparts where possible
- Layer 3 keys are explicit — `trans` is not relied on for passthrough

---

## Step 1 — Layer 1 Current Layout

Notation: `tap | hold` for hold-tap keys · `___` = no physical key · `---` = transparent · <u>underline</u> = tap · *italic* = hold (hold-tap)

**Base Layer (letter reference)**

Left side:

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | Esc | 1 | 2 | 3 | 4 | 5 | ___ |
| R1 | Tab | Q | W | E | R | T | ___ |
| R2 | Caps | A | S | D | F | G | ___ |
| R3 | LCtrl | Z | X | C | V | B | ___ |
| R4 | ___ | Mute | GUI | Alt | Shift | L1 | Space |

Right side:

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | ___ | 6 | 7 | 8 | 9 | 0 | [ |
| R1 | ___ | Y | U | I | O | P | ] |
| R2 | ___ | H | J | K | L | ; | ' |
| R3 | ___ | N | M | , | . | / | Enter |
| R4 | Bksp | L2 | RShift | Del | L4 | ___ | ___ |

**Left side (7×5)** — C7 is the encoder button column

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | ` | F1 | F2 | F3 | F4 | F5 | ___ |
| R1 | --- | Home\|Bksp | ↑ | End\|Del | PgU\|^Home | (\|) | ___ |
| R2 | Ins | ← | ↓ | → | PgD\|^End | [\|] | ___ |
| R3 | LCtrl | ^Z | ^X | ^C | ^V | '\|" | ___ |
| R4 | ___ | --- | --- | --- | --- | L1 | --- |

**Right side (7×5)** — C1 is the encoder button column

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | ___ | F6 | F7 | F8 | F9 | F10 | F11 |
| R1 | ___ | - | 7 | 8 | 9 | PgUp | F12 |
| R2 | ___ | + | 4 | 5 | 6 | PgDn | --- |
| R3 | ___ | * | 1 | 2 | 3 | \ | Del |
| R4 | RShft | --- | 0 | . | = | ___ | ___ |

Key: `M↑/↓/←/→` = mouse move · `M1` = left click · `M3` = middle click · `^` = Ctrl+

---

## Step 2 — IntelliJ Shortcuts to Include

### Navigation
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Alt+Left` | Navigate Back (history) | High | ✓ |
| `Alt+Right` | Navigate Forward (history) | High | ✓ |
| `Ctrl+B` | Go to Declaration | High | ✓ |
| `Ctrl+Alt+B` | Go to Implementation | High | ✓ |
| `Ctrl+Alt+F7` | Show Usages | High | ✓ |
| `Ctrl+E` | Recent Files | Medium | ✓ |
| `Ctrl+Shift+Backspace` | Last Edit Location | High | ✓ |
| `F2` | Next Error/Warning | High | ✓ |
| `Shift+F2` | Previous Error/Warning | Medium | ✓ |
| `Ctrl+F12` | File Structure Popup | Medium | ✓ |
| `F7` | Next Difference (diff view) | Medium | ✓ |
| `Shift+F7` | Previous Difference (diff view) | Medium | ✓ |
| `Ctrl+[` | Move to Code Block Start | Medium | ✓ |
| `Ctrl+]` | Move to Code Block End | Medium | ✓ |

### Code Actions
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Alt+Enter` | Show Intention Actions / Quick Fix | High | ✓ |
| `Ctrl+Alt+L` | Reformat Code | High | ✓ |
| `Ctrl+Alt+H` | Call Hierarchy | Medium | ✓ |
| `Ctrl+Shift+U` | Toggle Case | Medium | ✓ |
| `Ctrl+Alt+Shift+T` | Refactor This | High | ✓ |
| `Ctrl+Alt+T` | Surround With | Medium | ✓ |
| `Ctrl+O` | Override Methods | High | ✓ |
| `Alt+Insert` | Generate | High | ✓ |
| `Ctrl+U` | Go to Super | Medium | ✓ |
| `Ctrl+H` | Class Hierarchy | Medium | ✓ |
| `Ctrl+Shift+T` | Go to Test / Create Test | Medium | ✓ |
| `Ctrl+Shift+F10` | Run Current File/Test | Medium | ✓ |
| `Ctrl+Alt+O` | Optimize Imports | Medium | ✓ |
| `Ctrl+D` | Duplicate Line | High | ✓ |
| `Ctrl+X` | Delete Line | High | ✓ |
| `Ctrl+/` | Comment / Uncomment Line | High | ✓ |
| `Ctrl+Shift+/` | Block Comment | Medium | ✓ |
| `Ctrl+W` | Expand Selection | Low | ✓ |
| `Ctrl+Shift+W` | Shrink Selection | Low | ✓ |
| `Alt+J` | Add Next Occurrence | Medium | ✓ |
| `Alt+Shift+J` | Remove Last Occurrence | Medium | ✓ |
| `Shift+Esc` | Hide Active Panel | Medium | ✓ |
| `Ctrl+Shift+J` | Join Lines | Medium | ✓ |
| `Ctrl+Shift+V` | Paste from History | Medium | ✓ |
| `Shift+Alt+Up` | Move Line Up | High | ✓ |
| `Shift+Alt+Down` | Move Line Down | High | ✓ |

### VCS
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Alt+`` ` | VCS Operations Popup | High | ✓ |

### Run / Debug
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Alt+Shift+F10` | Choose & Run Configuration (Shift in popup to debug) | High | ✓ |
| `Ctrl+F2` | Stop | Low | ✓ |
| `Alt+F8` | Evaluate Expression | Low | ✓ |
| `F8` | Step Over | Low | ✓ |
| `F7` | Step Into | Low | ✓ |
| `Shift+F8` | Step Out | Low | ✓ |

### Quick Info
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Ctrl+Q` | Quick Documentation | High | ✓ |
| `Ctrl+P` | Parameter Info | High | ✓ |
| `Ctrl+Shift+I` | Quick Definition | High | ✓ |

### Popup & Panel
| Shortcut | Action | Priority | Confirmed |
|---|---|---|---|
| `Ctrl+Tab` | Switcher | High | ~~dropped — Ctrl-hold navigation not viable on tri-layer~~ |
| `Alt+1` | Project Panel | High | ✓ |
| `Alt+5` | Debug Panel | Low | ✓ |
| `Alt+6` | Problems Panel | Low | ✓ |
| `Alt+8` | Services Panel | Medium | ✓ |
| `Alt+9` | Git Panel | Low | ✓ |
| `Alt+0` | Commit Panel (hold-tap with Project) | High | ✓ |
| `Alt+F12` | Terminal | High | ✓ |
| `Alt+4` | Run Panel (hold-tap with Terminal) | Medium | ✓ |
| `Alt+3` | Find Panel | Medium | ✓ |
| `Ctrl+Alt+K` | Send to Claude Code | High | ✓ |

---

## Step 3 — Position Mapping

**Layer 3 Left side (7×5)**

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | Hide Panel | <u>Terminal</u><br>*Run Panel* | <u>Project</u><br>*Commit* | <u>Call Hierarchy</u><br>*Class Hierarchy* | Find Panel | DB (Alt+D) | ___ |
| R1 | <u>Next Diff</u><br>*Prev Diff* | <u>Block Start</u><br>*Remove Occ* | <u>Decl</u><br>*Impl* | <u>Block End</u><br>*Add Next Occ* | <u>Last Edit</u><br>*Recent Files* | | ___ |
| R2 | Toggle Case | <u>Nav Back</u><br>*Shrink Sel* | <u>Show Usages</u><br>*File Structure* | <u>Nav Forward</u><br>*Expand Sel* | <u>Intention Actions</u><br>*Param Info* | <u>Quick Definition</u><br>*Quick Doc* | ___ |
| R3 | | Stop | <u>Run Config</u><br>*Run Current* | <u>Comment</u><br>*Javadoc* | Paste History | <u>Next Error</u><br>*Prev Error* | ___ |
| R4 | ___ | | | | | | |

**Layer 3 Right side (7×5)**

| | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|---|---|---|---|---|---|---|---|
| R0 | ___ | | Git | Services | Problems | <u>Debug Panel</u><br>*Eval Expr* | |
| R1 | ___ | <u>Move Line Up</u><br>*Join Lines (select+join)* | <u>Go to Test</u><br>*Go to Super* | Override | Send to Claude | Step Out | |
| R2 | ___ | <u>Move Line Down</u><br>*Dupe Line* | Refactor This | Generate | Surround With | <u>Step Over</u><br>*Step Into* | |
| R3 | ___ | Delete Line | VCS Popup | Reformat | Optimize Imports | Resume | |
| R4 | | | | | | ___ | ___ |

Guiding principles:
1. **Positional inheritance** — Layer 3 key should be semantically related to the Layer 1 key at the same position
2. **Frequency = ergonomics** — High priority shortcuts go to the most comfortable positions (home row, strong fingers), Low priority go to the periphery
3. **Shift variants share a key** — shortcuts that are Shift variants of each other use mod-morph on the same key where possible
4. **Action clusters** — group by type: navigation cluster on left nav area, code actions on edit row, run/debug on right side
5. **Avoid overriding useful pass-through** — keys still useful from Layer 1 should not be replaced unless the Layer 3 action is strictly better in that context
6. **Left hand = navigation, right hand = actions** — mirrors IntelliJ usage: left hand browses, right hand acts
7. **Modifier column as fallback** — C6 (left) or C2 (right), both inner index finger columns, can serve as a Shift modifier when key positions are exhausted

---

## Naming Convention

- Macros: `ij_<short>` — e.g. `ij_decl`, `ij_reformat`, `ij_refactor`
- Each macro includes a comment with the full shortcut and action:
  ```c
  label = "IJ_DECL"; // Ctrl+B — Go to Declaration
  ```

---

## Files to Modify

- `config/eyelash_sofle.keymap` — Layer 3 bindings + any needed macros
- `keymap-drawer/eyelash_sofle.yaml` — update visualization

---
## remaining
- VCS operation
- Java doc macro: /** + Enter (no navigation — cursor must be pre-positioned)