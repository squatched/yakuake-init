# yakuake-init
An init script for starting up the fantastic Yakuake console (https://extragear.kde.org/apps/yakuake/) based on a config file that specifies tabs, their names, and what command(s) to initialize them with.

## Usage
```sh
  ./yakuake-init.sh sample.config
```

## Config File Syntax
### Comments
Any line beginning with a `#` is ignored.

### Yakuake Tab
Each non-empty line in the config file is a new tab.

#### Tab Title
The tab title is everything in the line leading up to the first comma or end of the line, whichever comes first.

#### Tab Command
The command run to initialize the tab is everything after the comma.

#### Examples
| Command | Description |
|--------|----------|
|`htop, htop`|Creates a tab named "htop" and runs htop in the tab.|
|`journalctl, journalctl --follow`|Show only the most recent journal entries, and continuously print new entries as they are appended to the journal.|
|`home, cd ~ && clear`| Creates a tab, changes directory to your home then clears the console.|
|`shell【ツ】`|Creates a new shell tab.|
