# MAME Cheatsheet

    brew install mame

Should be installed in `/usr/local/Cellar/mame/{{ version number }}/bin/`

I'm not sure I recommend using homebrew to install mame. Doesn't seem to read the mame.ini (which is created in ~). It also doesn't integrate well with ia-mame. When using from the commandline it will read roms from ~/roms. When using ia-mame it uses the bin folder...

## IA-MAME

First we need java greater than version 6(?).

    brew install java

Install IA-MAME

    sudo curl -fsSLo /usr/local/bin/ia-mame https://github.com/TiBeN/ia-mame/releases/download/0.9/ia-mame
    sudo chmod +x /usr/local/bin/ia-mame

Add to your .bash_profile

    export MAME_EXEC=/usr/local/Cellar/mame/{{ version number }}/bin/mame

Make a `rom` folder: `/usr/local/Cellar/mame/{{ version number }}/roms`

Make that writeable:

    chmod +w /usr/local/Cellar/mame/{{ version number }}/roms

## My preferred mame.ini settings

    filter 0
