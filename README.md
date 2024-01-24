﻿# OoT Speedrunning

Source of the documentation for Zelda: Ocarina of Time Speedrunning.

This whole documentation repository is licensed under CC0-1.0, see the LICENSE.rst file. Make sure what you contribute can be licensed this way!

## Contributing

Fork this repo, edit what you want, and open pull requests!

See instructions below for setting up locally.

The documentation source is written in reStructuredText, a simple and well-defined markup language. To learn about it, check out or copy-paste from:
- https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html
- https://docutils.sourceforge.io/rst.html

If you're adding a new glitch, please try to write the discovery date at the top of the main page of it.
You can find the discovery list [here](https://docs.google.com/document/d/1KymmXOp-b_PA4ErWX70VRV5TcpbC5Nh6espdCOlwtd0/edit).

## Building locally

(This assumes you are using something like Ubuntu or Debian, natively or in WSL)

Clone and enter your local repository:

```
git clone ...
cd oot_docs
```

Setup a virtual environment and install Sphinx:

```
sudo apt install python3 python3-pip python3-venv
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install --upgrade pip
python3 -m pip install -r requirements.txt
```

You can then use `make` to build the documentation (e.g. `make html`).

Make sure to activate the virtual environment with `source .venv/bin/activate` when needed.

## Preview with VS Code

Set the Python interpreter to the virtual environment's.

Install the following extensions:
- `reStructuredText` https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext
- `reStructuredText Syntax highlighting` https://marketplace.visualstudio.com/items?itemName=trond-snekvik.simple-rst

The `reStructuredText` extension will eventually ask to install the Esbonio language server, say yes.

Set `esbonio.sphinx.confDir` to `${workspaceFolder}`.

The HTML preview should now be seen in VS Code and update live.
