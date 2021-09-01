# alacritty-conf

Script to set basic setting for alacritty terminal, includes a rofi menu version too.

## Usage

```
Usage: alacritty-conf [options] [value] ...
    -h or --help              Show help.
    -c or --color <value>     Set color-scheme.
    -o or --opacity <value>   Set opacity.
    -p or --padding <value>   Set padding.
    -f or --font <value>      Set font.
```
## Dependencies

- `bash`
- `sed`

## Edit your config

Here is a sample config what your config should look like, i only added options which this script modifies, your config will have other options too.

```yaml
# first import the color scheme
# notice the use of absolute path not relative
import:
  - /home/antihero/.config/alacritty/themes/one_dark_pro.yml
# notice that everything is indented by two spaces
window:
  padding:
    x: 40
    y: 40
  opacity: 1.0
# this script replace font in every style to the given font
font:
  normal:
    family: Iosevka Nerd Font
    style: Regular
  bold:
    family: Iosevka Nerd Font
    style: Bold
  italic:
    family: Iosevka Nerd Font
    style: Italic
  bold_italic:
    family: Iosevka Nerd Font
    style: Bold Italic
```

- `CONFIG` var is used to set the location of alacritty config
- `THEME_DIR` var is used to set the location of the folder which contains the themes. You can get many themes from [here](https://github.com/eendroroy/alacritty-theme)

## Installation

- copy `alacritty-conf` to any directory in your `$PATH`, or crete a softlink

For rofi menu:

- copy `rofi-alacritty` directory to `~/.config/rofi`
- set a keybind to run `~/.config/rofi/rofi-alacritty/rofi-alacritty`
- to add more profiles add modify the script, and add more options to it

For dmenu menu:

- just add keybind to `dmalacritty` 

## Preview

![gif-rofi](display.gif)

`rofi-preview`

Open issues if you face any problems.