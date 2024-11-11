# Getting Started with Neovim

## Introduction

Neovim is a modern, extensible text editor designed as a fork of Vim, aiming to improve the user experience, codebase, and plugin system. Neovim offers powerful features, including the ability to implement plugins in the Lua programming language, support for asynchronous workflows via remote procedure calls (RPCs), and compatibility with most Vim plugins with minimal modifications. Due to its performance improvements and modern features, Neovim has gained popularity among developers, while Vim remains a widely-used editor. 

## Installing Neovim

To install neovim, update your system and install `nvim`

```
sudo apt update
sudo apt install nvim
```

## Entering Insert Mode

In **Neovim** (and Vim), you can enter `--INSERT--` mode in several ways:

- `i` - Insert at the current character
- `a` - Append after the current character
- `I` - Insert at the start of the line
- `A` - Append at the end of the line

## Basic Motions

Navigate text with basic motion commands:

- `h`, `j`, `k`, `l` - Move **left**, **down**, **up**, **right**
- `w` - Move to the start of the **next word**
- `b` - Move **back** to the start of the previous word
- `e` - Move to the **end** of the current word
- `^` - Move to the **start** of the line
- `$` - Move to the **end** of the line
- `%` - Jump between matching **brackets** or **parentheses**

### Advanced Motions

- `G` - Jump to the **end** of the file
- `gg` - Jump to the **top** of the file
- `H` - Move to the **top** of the window
- `L` - Move to the **bottom** of the window

## Editing Commands

Here are some essential editing commands in Neovim:

- `x` - **Delete** character under cursor
- `r` - **Replace** character under cursor
- `d` + motion - **Delete** according to motion (e.g., `dw` deletes a word)
- `c` + motion - **Change** according to motion (similar to delete, but enters Insert mode)
- `y` + motion - **Yank (copy)** text according to motion
- `p` - **Paste** after the cursor
- `u` - **Undo** the last change
- `Ctrl + r` - **Redo** the undone change
- `v` - Enter **visual mode** (select text by character)
- `V` - Enter **line visual mode** (select by line)
- `Ctrl + v` - Enter **block visual mode** (select vertically over lines)

### Advanced Editing Techniques

- Use `.` to **repeat the last command**, which is helpful for repeating complex edits.
- In visual mode, `>` and `<` indent and outdent selected lines.

### Visual Block Editing

The `Ctrl + v` command enters **visual block** mode, allowing you to select vertically across multiple lines.

1. Select a column of text using `Ctrl + v`.
2. Use `I` or `A` to **insert** or **append** text across the selected lines.
3. Press `<Esc>` to apply the change to all lines.

## Combining Commands and Motions

In Neovim, commands can be combined with counts and motions to create powerful edits:

- `d2w` - **Delete** the next 2 words
- `dG` - **Delete** to the end of the file
- `c$` - **Change** to the end of the line
- `Vgg` - **Select** to the top of the file
- `3yy` - **Yank** (copy) 3 lines

## Ex Commands (Command-line Mode)

Neovim supports **Ex commands** for saving, quitting, and advanced file manipulation:

- `:w` - **Write (save)** file
- `:q` - **Quit** file
- `:wq` - **Write and quit** file

### Search and Replace

- **Basic Replace**: `:s/old/new` - Replaces `old` with `new` on the current line.
- **Global Replace**: `:%s/old/new/g` - Replaces `old` with `new` throughout the entire file.
- **Confirm Replace**: Add `c` to prompt for each replacement (e.g., `:%s/old/new/gc`).

### Searching Text

- **Search**: `/pattern` - Search forward for `pattern`.
- **Cycle Search Results**: `n` (next) and `N` (previous) to navigate results.

## Useful Neovim Features

Neovim provides additional capabilities and settings:

- **Split Windows**:
  - `:vsp filename` - Open `filename` in a **vertical split**
  - `:sp filename` - Open `filename` in a **horizontal split**

- **Window Navigation**:
  - `Ctrl + w h/j/k/l` - Move to the left/down/up/right window
  - `Ctrl + w w` - Cycle through open windows

- **Tabs**:
  - `:tabnew filename` - Open a file in a **new tab**
  - `gt` - Go to the **next tab**
  - `gT` - Go to the **previous tab**
