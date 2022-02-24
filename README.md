# vs-code-guides

> How to be hyper productive in VS Code

## Minimize visual clutter

## Good keybindings

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

