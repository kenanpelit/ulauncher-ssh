# A [Ulauncher](https://ulauncher.io) extension to start SSH connections with local tmux and remote byobu support.

![extension screenshot](https://imgur.com/glgIVgM.png)

This extension lets you quickly connect to SSH hosts with automatic local tmux session management and remote byobu integration.

## Features

- Automatically builds connection list from ~/.ssh/config and known_hosts
- Creates a dedicated local tmux session for each SSH connection
- Automatically connects to a specified byobu session on the remote server
- Integrates seamlessly with foot terminal (other terminals supported as well)

## Setup

### Basic Configuration

1. Install the extension
2. Configure the terminal settings in Ulauncher preferences:
   - Terminal: `/usr/bin/foot` (or your preferred terminal)
   - Terminal arg: `-e`
   - Leave Terminal cmd empty for automatic tmux+byobu integration
   - Optionally set a custom byobu session name (defaults to 'kenan')

### SSH Configuration

Add your SSH hosts to ~/.ssh/config. Example:
```
## Server Example ##
Host feynman
     HostName 192.168.1.100
     User myuser
```

For passwordless login, setup your SSH keys as described [here](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/).

## How it Works

When you select a host (e.g., 'feynman'):
1. Creates/attaches to a local tmux session named 'feynman'
2. Establishes SSH connection to the remote host
3. Automatically connects to the specified byobu session on the remote server

## Terminal Support

### Foot Terminal
Works out of the box with foot terminal. Just set the terminal path to `/usr/bin/foot` in the extension preferences.

### Other Terminals
For other terminals, adjust the terminal path and arguments in the extension preferences accordingly.

## Contributing

Feel free to submit issues and pull requests on [GitHub](https://github.com/kenanpelit/ulauncher-ssh).

## Credits
Original extension by [Jonas Bendlin](https://github.com/jonasbendlin)
Modified with tmux+byobu support by [Kenan Pelit](https://github.com/kenanpelit)
Icon from [shareicon.net](https://www.shareicon.net/terminal-94589)
