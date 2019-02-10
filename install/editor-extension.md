---
description: Tools or extensions maintained by third-party developers different editors.
---

# Editor Extension

### [Neovim](https://github.com/fszymanski/fzf-gitignore) — [Filip Szymański](https://github.com/fszymanski)

Install Neovim python client.

```bash
pip3 install --upgrade neovim
```

Use your favorite Neovim plugin manager to install `fzf-gitignore`.

```text
Plug 'junegunn/fzf', {'dir': '~/.fzf', 'do': './install --all'}
Plug 'fszymanski/fzf-gitignore', {'do': ':UpdateRemotePlugins'}
```

### [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=rubbersheep.gi) — [Hasit Mistry](https://github.com/hasit/)

Press `Cmd+P` for MacOS and `Ctrl+P` for Linux/Windows to launch VS Code Quick Open, paste the following command, and press enter.

```text
ext install gi
```

### [GNU Emacs](https://github.com/jupl/helm-gitignore) — [Juan Placencia](https://github.com/jupl)

This package is available on [MELPA](http://melpa.org/) under the name `helm-gitignore`. Please note that gitignore.io’s APIs are available through HTTPS, meaning if you experience issues attempting to connect to the network odds are you may need something like [GnuTLS](http://gnutls.org/).

### 



