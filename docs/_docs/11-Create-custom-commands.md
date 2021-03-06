---
name: Create custom commands
anchor: create-custom-commands
toc: 
 - name: Configuring custom commands
   anchor: configuring-custom-commands
 - name: Mapping mascot poses to custom commands
   anchor: mapping-mascot-poses-to-custom-commands
---
This section explains how to create custom commands.


### Configuring custom commands
You can create simple custom replies using "Commands".

*Example:*
```
    "Commands": {
        "!hello": {
            "Image" : "",
            "Script" : "",
            "Enabled": true,
            "ViewerOnce": false,
            "ViewerTimeout": 0,
            "GlobalTimeout": 0,
            "Access" : "",
            "Aliases": [
                "!hi",
                "!hey"
            ],
            "Hotkey": [
                "ctrl",
                "alt",
                "f12"
            ]
        }
    }
```
**List of parameters**
* <span class="icon settings">Image</span> Optional image (has to be placed into "images" directory)
* <span class="icon settings">Script</span> Execute a script (has to be placed into "scripts" directory)
* <span class="icon settings">Access</span>
  * "" - Everyone can use the command if left empty
  * "sub" - Only subs, vips, mods or broadcaster can use the commands
  * "vip" - Only vips, mods or broadcaster can use the commands
  * "mod" - Only mods or broadcaster can use the commands
  * "broadcaster" - Only broadcaster can use the commands
* <span class="icon settings">ViewerOnce</span> (true/false) Command can be used only once per viewer during a session.
* <span class="icon settings">ViewerTimeout</span> Command can be used only once per viewer within X number of seconds (0 - disabled).
* <span class="icon settings">GlobalTimeout</span> Command can be used only once within X number of seconds (0 - disabled).
* <span class="icon settings">Enabled</span> (true/false)
* <span class="icon settings">Aliases</span> List of aliases for this comands.
* <span class="icon settings">Hotkey</span> Execute global hotkey. Supported keys:
  * all printable characters and numbers
  * ctrl, alt, shift
  * f1 - f12
  * arrow buttons (up, down, left, right)
  * print_screen, pause
  * insert, delete, home, end, page_up, page_down
  * enter, esc, tab, backspace
  * cmd (Mac keyboard)

<br>
<span class="icon info">To add text messages to custom commands, see <a class="icon doc" href="{{ site.github.url }}/documentation#customize-notifications-and-commands">Customize notifications and commands</a>.</span>

### Mapping mascot poses to custom commands
PoseMapping allows you to map available mascot poses to your custom commands.
All notification and commands will use DEFAULT mapping unless a mapping is created for them.
```
    "PoseMapping": {
        "DEFAULT": {
            "Image": "Wave",
            "Audio": "Wave"
        },
        "!hello": {
            "Image": "Happy",
            "Audio": "Happy"
        }
    }
```
