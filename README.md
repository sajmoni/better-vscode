# vs-code-guides

> How to boost productivity in VS Code

## 🚄 Productivity boosters

> Settings to increase productivity

### Always update imports when a file is moved

```json
"javascript.updateImportsOnFileMove.enabled": "always",
```

### Increase line height

```json
"editor.lineHeight": 24,
```

### Add a vertical line at max line width

```json
"editor.rulers": [80],
```

### Improve bracket pair visualization

```json
  "editor.bracketPairColorization.enabled": true,
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
  "explorer.experimental.fileNesting.enabled": true,
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

## ⌨️ Keybindings

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

### Navigate back / forward

> Go to the previous / next cursor position

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

### Cycle tabs

> Go to the next / previous tab

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

