need more test...

For example, with Mercenary A and Mercenary B:
1. When both Mercenaries A and B are dead: You cannot replace them with a new mercenary.
2. When either Mercenary A or B is dead: You can replace the dead mercenary with a new one.

plugins
d2rloader\plugins\MultiMercenary.dll

config
d2rloader\config\multi-mercenary.toml

need to add key for switch each Mercenary inventory
global\ui\layouts\hirelinginventorypanelhd.json

such as

        {
            "type": "ButtonWidget",
            "name": "MultiMercenaryPrevious",
            "fields": {
                "rect": {
                    "x": 500,
                    "y": 1380,
                    "width": 64,
                    "height": 64
                },
                "filename": "PANEL\\Stash\\Stash_LeftArrow",
                "normalFrame": 0,
                "pressedFrame": 2,
                "hoveredFrame": 1,
                "disabledFrame": 3,
                "onClickMessage": "BankPanelMessage:SharedStashLeft"
            }
        },
        {
            "type": "ButtonWidget",
            "name": "MultiMercenaryNext",
            "fields": {
                "rect": {
                    "x": 594,
                    "y": 1380,
                    "width": 64,
                    "height": 64
                },
                "filename": "PANEL\\Stash\\Stash_RightArrow",
                "normalFrame": 0,
                "pressedFrame": 2,
                "hoveredFrame": 1,
                "disabledFrame": 3,
                "onClickMessage": "BankPanelMessage:SharedStashRight"
            }
        }