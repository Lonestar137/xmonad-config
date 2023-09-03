# Requirements

## Using GHCUP(recommended)

Run:
`curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh`

I have had the best experience with the ghcup install method. 
If the above command doesn't work: (ghcup official docs)[https://www.haskell.org/ghcup/]

## Cabal-install package

If you're on linux you can use your system package manager by using one of the below commands:
```
sudo apt install cabal-install

sudo dnf install cabal-install

sudo pacman -S cabal-install (not recommended)

```



# Build and install

Clone all the submoduels down:
`git submodule update --init --recursive`

Build and install the project:
`./build.sh`


# Optional

## Desktop files

### $HOME/.xsession

Create the file: `/usr/share/xsessions/default.desktop`
```
[Desktop Entry]
Name=Default X Session
Type=Application
Exec=default
```

and, add to `~/.xsession`:
`exec $HOME/.cache/xmonad/xmonad`

This will execute the freshly compiled version of xmonad everytime you load the xsession.


