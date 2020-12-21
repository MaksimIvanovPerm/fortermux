# fortermux
some developments for use youtube-dl in termus;
See [Intents and Hooks](https://wiki.termux.com/wiki/Intents_and_Hooks) at [termux-wiki](https://wiki.termux.com/wiki)
I merely added some shell-wrapper to youtube-dl which adds some more functionality, that is usefull&suitable in termux, as it seems to me;
That is, in essential, the following code is placed to `~/bin/termux-url-opener`:
```"/data/data/com.termux/files/home/bin/download_from_youtube.sh" -u "$1" -m ask```

So, you just install termux and do:
```apt update
apt upgrade
apt install -y git wget curl python ffmpeg iconv && pip install youtube-dl
mkdir ~/bin; cd ~/bin
GITHUBREP="https://github.com/MaksimIvanovPerm/fortermux.git"
git clone "$GITHUBREP" ./
whereis youtube-dl
youtube-dl --version
```

Also, a bit of userfullness for termus:
```mkdir ~/.termux
echo "extra-keys = [ \\
 ['ESC','|','/','HOME','UP','END','PGUP','DEL'], \\
 ['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN','BKSP'] \\
]"> ~/.termux/termux.properties
cd ~
termux-reload-settings
```
