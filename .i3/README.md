- Install the i3 package - not i3wm. The former brings in a lot of useful tools by default, like i3status and i3lock.

- Packages to install:
  - xautolock so that auto-locking works properly.
  - arandr for easily changing display settings.
  - lxappearance to set gtk settings
  - feh to set background image easily
  - thunar, a file explorer
  - gnome-icon-theme-full to get icons on thunar
  - arc-theme. Needs to be added to sources - see instructions at https://github.com/horst3180/arc-theme
  - rofi, a dmenu replacement
  - compton, to support transparent windows in i3 (to beautify rofi). Compton messes up background settings, so we need to execute feh once when i3 logs in (this is in the config file). To generate the feh script, run this once: feh --bg-fill /usr/share/backgrounds/warty-final-ubuntu.png - it will generate a shell script in ~/.fehbg that the i3 config runs when it starts
  - scrot, to be able to take screenshots for locking the screen
  - imagemagick, to get the convert(1) command
  - i3blocks
  - pavucontrol for setting and fetching the volume level. i3blocks relies on pulse audio to get the correct volume level

- Fonts to install (copy the .ttf files to ~/.fonts):
  - Awesome (https://github.com/FortAwesome/Font-Awesome), for the special cute icons
  - Yosemite San Francisco (https://github.com/supermarin/YosemiteSanFranciscoFont), to set as system font with lxappearance. Note: shows up as SFNS Display on lxappearance.
    - Pro tip: use gnome-font-viewer to view all available fonts

- Icons:
  - Install moka icons theme: https://snwh.org/moka
  - Enable the icons theme on lxappearance (under the "Icon Theme" tab)

- Misc:
  - Change /usr/share/i3blocks/bandwidth to use fancy icons for download and upload instead of IN/OUT. Lines 73 and 84.