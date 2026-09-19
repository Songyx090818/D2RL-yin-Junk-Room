## Hire multiple mercenaries.
You can set the maximum number of mercenaries in the `toml` file. The maximum value is 5, and the default value is 5.(If you increase the number of mercenaries, equip them with items, and then reduce the mercenary count in the TOML file, the items on the extra mercenaries will disappear. Please keep this in mind.
)
You can give potions to each mercenary through their individual icons. If you use the hotkey, it will check the first mercenary for things like low health, poison, or being frozen. If there’s no issue, it then moves on to the next mercenary and applies the potion there instead.
Mods that allow mercenary levels above 255 are currently not supported.
I was going to do more testing, but I simply don’t have enough time, so I’m releasing it as is.
This is closer to a beta version, so please back up your save files before using it. Be aware that there may be issues, and use it at your own risk.
You can adjust the position of the arrows in the mercenary inventory by editing the JSON file inside the plugin's own MPQ.
It varies depending on the mod, but the arrow position is currently set based on the retail inventory layout.
If you are using an expanded inventory, open:
`d2rloader\plugins\d2rl-multi-mercenary.mpq\data\global\ui\layouts\multi-mercenary\MercenaryArrowshd.json`
and change:
`"rect": { "x": 500, "y": 1380, "width": 64, "height": 64 }`
If you set the `Y` value to around `1439`, the arrows should be positioned a bit lower.


plugins
d2rloader\plugins\d2rl-multi-mercenary.dll
d2rloader\plugins\d2rl-multi-mercenary.mpq

config
d2rloader\config\multi-mercenary.toml

D2RMM (if you want act4 merc)
`MultiMercenary Act IV.zip` drag and drop to D2RMM
Since I don't know which mod you're using, the mercenary skill icon config is disabled by default.
If you enable it, the default retail skill icons will be used.
Unfortunately, it's not possible to make it compatible with every mod, so I appreciate your understanding. The example mercenary is basically a Necromancer using Teeth, Bone Spear, Bone Spirit, and a few curses. I also gave him a Bone Helm, a Flail, and a Demon Head.

If you want to add an Act 4 mercenary directly
In `hireling.txt`, setting `Seller` to `367` will enable Tyrael's hire window.
For the remaining class, match them to the appropriate `index` values in `monstats.txt`.
Other elements, such as mercenary skill sprites, JSON files, and strings, should be added as appropriate for your own mod.
Please refer to the example files for guidance.

Q: Wouldn’t having too many mercenaries be overpowered?  
A: Yes, it would. That’s why the default value is set to 2. You’ll need to adjust the mercenary balance yourself as needed.

Q: Is it okay to use this without an Act 4 mercenary?  
A: Yes, there is no problem. If you do not add one in the TXT files, Tyrael’s hire window will be disabled automatically.

Q: Couldn’t you just include the skill icons and the Act 4 mercenary by default?  
A: Unfortunately, that is not practical because every mod is different.

Q: Could you change the Act 4 mercenary to something else? Or change its skill setup, damage, and so on?  
A: You can change those yourself. The included setup is only an example.

Q: I don't like the arrow sprites in the mercenary inventory.  
A: The default arrows are just examples as well. You can replace them with whatever you prefer.

Q: Does this plugin have any issues?  
A: Well... it’s a beta version.
