# qMarkdown

qMarkdown is a simple Qt-based markdown viewer, it's light-weight and easy to use.

![C/C++ CI](https://github.com/Peterkmoss/qmarkdown/workflows/C/C++%20CI/badge.svg)

## Screenshots

![Light](./public/light_small.png)

## License

This software is provided under the
[GNU GLPv3](https://www.gnu.org/licenses/gpl-3.0.en.html) license.

## Dependencies

`qt` version `5.9.0` or above

### Pacman packages

* `qt5-base`
* `qt5-webengine`
* `qt5-webchannel`

#### Optional

* `ttf-roboto` - default font, but fallbacks to *sans-serif*

## Installation

### Compile dependencies

* `git` (to clone repository)
* `c++` or similar compiler with support for c++17
* `cmake` >= `3.1.0`
* `make`
* `sudo` or other way to grant root privileges (like `doas`)

#### Clone and compile

```shell
git clone https://github.com/Peterkmoss/qmarkdown.git
cd qmarkdown
mkdir build
cd build
cmake ..
make
```

#### Install

```shell
sudo make install
```

### Arch based distros

There is an
[AUR package available](https://aur.archlinux.org/packages/qmarkdown/) for all
arch-based users

## Usage

`qmarkdown [colorscheme] <file>`

### Colorschemes

* Light `-l` or `--light`
* Dark `-d` or `--dark`

### Keybindings

* `q` - Exits the program
* `g` - Go to TOP of file
* `G` - Go to BOTTOM of file
* `j` - Scroll DOWN
* `k` - Scroll UP
* `h` - Scroll LEFT
* `l` - Scroll RIGHT

#### WIP

* `o` - Opens a text field to enter filename of new file (WIP)

## More screenshots

![Dark](./public/dark_small.png)

## Disclaimer

This software is provided as-is with all faults, security issues and alike that
might come with it.

By using this software product the user understands, and agrees to, that there is
no warranty on this product.
