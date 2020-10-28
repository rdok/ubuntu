# ubuntu

### How do I change my notifications position?
- Install [Gnome Shell Integration](https://wiki.gnome.org/Projects/GnomeShellIntegrationForChrome/Installation)
- Install [panel-osd](https://extensions.gnome.org/extension/708/panel-osd/)
- Enable Tweak -> Extensions -> Panel Osd
  - Open the Panel Osd settings to customize its position.

### How do I disable my touch screen?
Append the following to your `~/.bashrc`. If you're not using an XPS laptop, you want to change the egrep filtering.
``` 
TOUCH_SCREEN_ID=$(xinput --list | egrep -io "490A.+touch.+id=([0-9]+)" | awk '{print substr($4,length($4)-1)}')
xinput disable "$TOUCH_SCREEN_ID"
```
