# list_user_displays

This script lists all the displays associated to a specific user. This can be useful when trying to generate plots through code or when you want to open an image in a certain display.

## Getting started

To run this command, simply:

```bash
list_user_displays user_name
```

```bash
mrt@atenea /home/mrt $ list_user_displays mrt
[sudo] password for mrt:
DISPLAY=localhost:12.0 -> PIDs: 51060,51061,968770,
DISPLAY=localhost:11.0 -> PIDs: 968519,968562,
DISPLAY=localhost:10.0 -> PIDs: 968473,
DISPLAY=localhost:14.0 -> PIDs: 1510075,1510141,
```

> [!Note]
This script requires `sudo` permission to work.
