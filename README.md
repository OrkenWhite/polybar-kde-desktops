# polybar-kde-desktops
This is a Python script for Polybar, which displays the available KDE virtual desktops, highlighting the current one.

The script uses D-Bus for monitoring desktop change events and only updates when needed.

## Arguments
| Argument       | Description                                         |
|----------------|-----------------------------------------------------|
| -n             | Print desktop names instead of numbers              |
| -ac *COLOR*    | Use another highlight color for active desktop      |
| -s *SEPARATOR* | Use another separator character                     |
| prev           | Switch to the previous desktop and terminate script |
| next           | Switch to the next desktop and terminate script     |

## Example Polybar configuration
```ini
[module/kde-desktops]
type = custom/script
exec = ~/.config/polybar/scripts/polybar-kde-desktops
scroll-up = ~/.config/polybar/scripts/polybar-kde-desktops prev &
scroll-down = ~/.config/polybar/scripts/polybar-kde-desktops next &
tail = true
label = %output%
```
## Credits
This script was inspired by [kaythomas0's](https://github.com/kaythomas0) [kde-virtual-desktops-polybar](https://github.com/kaythomas0/kde-virtual-desktops-polybar).
