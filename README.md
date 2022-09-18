# better-vscode <!-- omit in toc -->

> Tips and tricks for working with VS Code

## Index <!-- omit in toc -->

- [🔧 Settings](#-settings)
  - [🚄 Improve productivity](#-improve-productivity)
    - [Always update imports when a file is moved](#always-update-imports-when-a-file-is-moved)
    - [Add a vertical line at max line width](#add-a-vertical-line-at-max-line-width)
    - [Improve bracket pair visualization](#improve-bracket-pair-visualization)
    - [Display function references](#display-function-references)
    - [Opened files remain open](#opened-files-remain-open)
    - [Don't require confirmation when files are moved](#dont-require-confirmation-when-files-are-moved)
    - [Auto-close JSX tags](#auto-close-jsx-tags)
    - [Auto rename HTML closing tag](#auto-rename-html-closing-tag)
    - [Use native tabs (MacOS only)](#use-native-tabs-macos-only)
  - [✨ Minimize visual clutter](#-minimize-visual-clutter)
    - [Turn off breadcrumbs](#turn-off-breadcrumbs)
    - [Hide tab close button](#hide-tab-close-button)
    - [Turn off minimap](#turn-off-minimap)
    - [Enable file nesting](#enable-file-nesting)
    - [Fold imports](#fold-imports)
    - [Hide unnecessary Gitlens features](#hide-unnecessary-gitlens-features)
    - [Increase line height](#increase-line-height)
    - [Add a delay before hover information is shown](#add-a-delay-before-hover-information-is-shown)
    - [Less information in tabs](#less-information-in-tabs)
    - [No git decorations](#no-git-decorations)
    - [Better window title](#better-window-title)
  - [🎊 Flair](#-flair)
    - [Smooth scrolling](#smooth-scrolling)
    - [Smooth cursor animation](#smooth-cursor-animation)
- [⌨️ Keybindings](#️-keybindings)
    - [Find references](#find-references)
    - [Rename symbol](#rename-symbol)
    - [Go to the previous / next cursor position](#go-to-the-previous--next-cursor-position)
    - [Go to the next / previous tab](#go-to-the-next--previous-tab)
    - [Increase / decrease view size](#increase--decrease-view-size)
    - [Add a cursor to each highlighted line](#add-a-cursor-to-each-highlighted-line)
    - [Split editor](#split-editor)
- [🧩 Extensions](#-extensions)
    - [Error lens](#error-lens)
    - [Auto close tag](#auto-close-tag)
    - [Turbo Console Log](#turbo-console-log)
    - [Template String Converter](#template-string-converter)
    - [Markdown All in One](#markdown-all-in-one)
    - [file-icons](#file-icons)
    - [Code Spell checker](#code-spell-checker)
    - [Color highlight](#color-highlight)
    - [indent-rainbow](#indent-rainbow)
    - [Peacock](#peacock)
    - [Gitlens](#gitlens)
    - [Bracketeer](#bracketeer)
    - [Highlight](#highlight)
  - [Snippets](#snippets)
    - [Ava](#ava)
    - [eslint-disable-snippets](#eslint-disable-snippets)
- [💅 Themes](#-themes)
    - [Tokyo Night](#tokyo-night)
    - [Github](#github)

# 🔧 Settings

## 🚄 Improve productivity

### Always update imports when a file is moved

```json
  "typescript.updateImportsOnFileMove.enabled": "always",
```

### Add a vertical line at max line width

```json
"editor.rulers": [80],
```

### Improve bracket pair visualization

```json
  "editor.guides.bracketPairs": true,
```

### Display function references

> Easily spot if a function is unused

```json
  "typescript.referencesCodeLens.enabled": true,
  "typescript.referencesCodeLens.showOnAllFunctions": true,
```

### Opened files remain open

```json
  "workbench.editor.enablePreview": false,
```

### Don't require confirmation when files are moved

```json
  "explorer.confirmDragAndDrop": false,
```

### Auto-close JSX tags

```json
  "typescript.autoClosingTags": true,
```

### Auto rename HTML closing tag

```json
  "editor.linkedEditing": true,
```

### Use native tabs (MacOS only)

```json
  "window.nativeTabs": true,
```

You need to open projects separately and then merge windows with: `Merge all windows`

---

## ✨ Minimize visual clutter

### Turn off breadcrumbs

```json
  "breadcrumbs.enabled": false,
```

### Hide tab close button

> You can close tabs with the keyboard shortcut anyway

```json
  "workbench.editor.tabCloseButton": "off",
```

### Turn off minimap

> You have scrollbar annotations anyway

```json
"editor.minimap.enabled": false,
```

### Enable file nesting

```json
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.expand": false,
```

### Fold imports

```json
  "editor.foldingImportsByDefault": true
```

### Hide unnecessary Gitlens features

```json
  "gitlens.codeLens.authors.command": false,
  "gitlens.codeLens.authors.enabled": false,
  "gitlens.codeLens.recentChange.enabled": false,
  "gitlens.statusBar.enabled": false,
  "gitlens.statusBar.pullRequests.enabled": false,
```

### Increase line height

```json
"editor.lineHeight": 24,
```

### Add a delay before hover information is shown

```json
  "editor.hover.delay": 500,
```

### Less information in tabs

```json
  "workbench.editor.labelFormat": "short",
```

### No git decorations

```json
  "git.decorations.enabled": false,
```

### Better window title

```json
  "window.title": "${rootName}${separator}${activeEditorMedium}",
```

---

## 🎊 Flair

### Smooth scrolling

```json
  "editor.smoothScrolling": true,
  "workbench.list.smoothScrolling": true,
```

### Smooth cursor animation

```json
  "editor.cursorSmoothCaretAnimation": true,
  "editor.cursorBlinking": "phase",
```

---

# ⌨️ Keybindings

### Find references

> View the places where a function or variable is used

```json
{
  "key": "shift+cmd+r",
  "command": "references-view.findReferences",
  "when": "editorHasReferenceProvider"
}
```

### Rename symbol

> Rename a variable, property or function globally

```json
{
  "key": "cmd+r",
  "command": "editor.action.rename",
  "when": "editorHasRenameProvider && editorTextFocus && !editorReadonly"
},
```

### Go to the previous / next cursor position

```json
{
  "key": "ctrl+left",
  "command": "workbench.action.navigateBack"
},
{
  "key": "ctrl+right",
  "command": "workbench.action.navigateForward"
}
```

### Go to the next / previous tab

```json
{
  "key": "alt+cmd+right",
  "command": "workbench.action.nextEditor"
},
{
  "key": "alt+cmd+left",
  "command": "workbench.action.previousEditor"
},
```

### Increase / decrease view size

```json
{
  "key": "shift+cmd+[Minus]",
  "command": "workbench.action.increaseViewSize"
},
{
  "key": "shift+cmd+-",
  "command": "workbench.action.decreaseViewSize"
},
```

### Add a cursor to each highlighted line

> Default keybinding

```json
{
  "key": "shift+alt+i",
  "command": "editor.action.insertCursorAtEndOfEachLineSelected",
  "when": "editorTextFocus"
}
```

### Split editor

```json
{
  "key": "ctrl+alt+cmd+[Period]",
  "command": "workbench.action.moveEditorToNextGroup"
},
```

# 🧩 Extensions

### [Error lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)

> Improve highlighting of errors, warnings and other language diagnostics

Recommended settings:

```json
  "errorLens.delay": 1000,
  "errorLens.excludeBySource": ["cSpell"]
```

### [Auto close tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

> Automatically add HTML/XML close tag, same as Visual Studio IDE or Sublime Text does

### [Turbo Console Log](https://marketplace.visualstudio.com/items?itemName=ChakrounAnas.turbo-console-log)

> Automating the process of writing meaningful log messages

### [Template String Converter](https://marketplace.visualstudio.com/items?itemName=meganrogge.template-string-converter)

> Converts a string to a template string when ${ is typed

### [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)

> All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)

### [file-icons](https://marketplace.visualstudio.com/items?itemName=file-icons.file-icons)

> File-specific icons in VSCode for improved visual grepping

### [Code Spell checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

> Spelling checker for source code

### [Color highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)

> Highlight web colors in your editor

### [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)

> Makes indentation easier to read

### [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)

> Subtly change the workspace color of your workspace. Ideal when you have multiple VS Code instances and you want to quickly identify which is which

### [Gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

> Supercharge the Git capabilities built into Visual Studio Code

### [Bracketeer](https://marketplace.visualstudio.com/items?itemName=pustelto.bracketeer)

> Easy manipulation with brackets and quotes

Keybindings to automatically remove corresponing bracket:

```json
{
  "key": "shift+cmd+backspace",
  "command": "bracketeer.removeBrackets"
},
```

### [Highlight](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-highlight)

> Advanced text highlighter based on regexes. Useful for todos, annotations, colors etc.

Highlight `only` tests example:

```json
"highlight.regexes": {
  "(it|describe|test)(\\.only.*)": {
    "filterFileRegex": "(.*)spec|test(.*)",
    "decorations": [
      {
        "overviewRulerColor": "#ffcc00",
        "backgroundColor": "#ffcc00",
        "color": "#1f1f1f",
        "fontWeight": "bold"
      },
      {
        "backgroundColor": "#ffcc00",
        "color": "#1f1f1f"
      }
    ]
  }
}
```

## Snippets

### [Ava](https://marketplace.visualstudio.com/items?itemName=samverschueren.ava)

> Snippets for AVA

### [eslint-disable-snippets](https://marketplace.visualstudio.com/items?itemName=drKnoxy.eslint-disable-snippets)

> Simple snippets for disable eslint rules

# 💅 Themes

### [Tokyo Night](https://marketplace.visualstudio.com/items?itemName=enkia.tokyo-night)

> A clean Visual Studio Code theme that celebrates the lights of Downtown Tokyo at night

### [Github](https://marketplace.visualstudio.com/items?itemName=GitHub.github-vscode-theme)

> GitHub theme for VS Code
