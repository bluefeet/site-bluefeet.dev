---
title: Remote SSH through WSL in VS Code
icon: 🏝️
tags:
  - ssh
  - vscode
  - wsl
---

Create `C:\wsl-ssh\wsl-ssh.cmd`:

```shell
wsl ssh %*
```

And in your user VS Code settings add:

```json
{
    "remote.SSH.path": "C:\\wsl-ssh\\wsl-ssh.cmd"
}
```

Now when you setup an SSH remote it will use the binary installed in your default WSL distro.
