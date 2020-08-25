---
title: Visual Studio Code Notes
icon: ✍️
tags:
  - vscode
---

## Definition of a Workspace

Workspaces are a saved snapshot of the state of a Visual Studio Code window. This includes any workspace settings, unsaved buffers, extensions, terminal state, etc.

## Where to Store Workspaces

Do not save workspaces into project folders as other people working in the same project will be forced to use your exact settings and may modify your personal settings for that workspace.

Instead, put workspaces into a local or remote folder only you have access to and is outside any particular project's path.

Use [extension recommendations](#recommending-extensions), [tasks](#declaring-tasks), and [.editorconfig](editorconfig.html) to declare project-level recommendations and settings.

## Recommending Extensions

Declare [recommended extensions](https://code.visualstudio.com/docs/editor/extension-gallery#_workspace-recommended-extensions) in project folders @ `.vscode/extensions.json`:

```json
{
  "EditorConfig.editorconfig"
}
```

## Declaring Tasks

Declare project-specific [tasks](https://code.visualstudio.com/docs/editor/tasks) in project folders @ `.vscode/tasks.json`:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "build",
      "type": "shell",
      "command": "npm build"
    }
  ]
}
```
