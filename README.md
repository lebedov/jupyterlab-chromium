<!--- 
-*- mode:markdown -*-
vi:ft=markdown
-->
Launch JupyterLab as a Chromium App
===================================

This script launches a local JupyterLab server and connects to it with Chromium
running as an app to provide a more IDE-like experience. The server is
terminated after Chromium exits.

Requirements
------------
- [Bash](https://www.gnu.org/software/bash/)
- [Chromium](https://www.chromium.org/)
- [jq](https://stedolan.github.io/jq/)
- [JupyterLab](https://github.com/jupyterlab/jupyterlab)
  
Installation
------------
Drop `jupyterlab-chromium` in your `$PATH`, ensure that it is executable, and
you are all set. If you want to create a shortcut to click on from your desktop 
or from a launcher, you can create a `.desktop` file as follows:

    [Desktop Entry]
    Type=Application
    Version=1.0
    Name=JupyterLab
    GenericName=JupyterLab
    Comment=JupyterLab
    Exec=/path/to/jupyterlab-chromium
    Icon=/path/to/jupyter-logo-transparent.png
    Terminal=false
    StartupWMClass=chromium-browser
    Categories=Development;Science;IDE
    StartupNotify=true

If JupyterLab is installed in a conda environment and your `.bashrc` 
file initializes conda properly, replace the `Exec` line with

    Exec=bash -c "source ~/.bashrc && conda activate env_name && /path/to jupyterlab-chromium"

Author
------
See the included [AUTHORS.md](
https://github.com/lebedov/jupyterlab-chromium/blob/master/AUTHORS.md) file for more
information.

License
-------
This software is licensed under the [MIT License](http://www.opensource.org/licenses/mit-license).  See the included
[LICENSE.md](https://github.com/lebedov/jupyterlab-chromium/blob/master/LICENSE.md) file for more information.

