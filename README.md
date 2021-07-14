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

You have to edit your alacritty config for this script to work. Otherwise you have to make changes in the script.

- alacritty config should be `~/.config/alacritty/alacritty.yml`, or you have to change the `CONFIG` variable in `alacritty-conf`
- the opacity option `background_opacity: 1` should not have any space in front
- for the color scheme to work, enclose your color settings between `## BEGIN-COLOR` and `## END-COLOR`, and put the themes in `~/.config/alacritty/themes` - get alacritty themes [here](https://github.com/eendroroy/alacritty-theme)
```yaml
## BEGIN-COLOR
# Colors (Gruvbox dark)
colors:
  # Default colors
  primary:
    # hard contrast: background = '0x1d2021'
    background: '0x282828'
    # soft contrast: background = '0x32302f'
    foreground: '0xebdbb2'
            :
            :
            :
    yellow:  '0xfabd2f'
    blue:    '0x83a598'
    magenta: '0xd3869b'
    cyan:    '0x8ec07c'
    white:   '0xebdbb2'
## END-COLOR
```
- indent the `padding:` section in your config as follows:

```yaml
  padding:
    x: 10
    y: 10
```
i.e. two spaces before `padding` and four spaces before `x` and `y`


## Installation

- copy `alacritty-conf` to any directory in your `$PATH`
- copy `rofi-alacritty` to `~/.config/rofi`
- set a keybind to run `~/.config/rofi/rofi-alacritty/rofi-alacritty`