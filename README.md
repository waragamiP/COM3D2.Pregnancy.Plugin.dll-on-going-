# COM3D2.Pregnancy.Plugin.dll-on-going-
To make something similar to KKpregnancy
Features so far:
F1 → "COM3D2 Pregnancy" → Change hotkey
**F8 **（hotkey by defaut）to activate UI
In UI, you can set belly change.
Max vaule 500, however actual uplimit is 40.
We took some ideas from AddYotogiSlider of asyetriec. Thanks to asyetriec.
Just started a few hours ago. Eventually we aim to make something like KK pregnancy.

For my next plan:
UI Fixes
Dropdown menu selection bug (clicks were unresponsive)
Per-Maid Variables
Pregnancy status (checkbox, default false)
Time progress (0.000 - 1.000 slider, replaces existing BOTE slider)
Global Settings (F1 Menu)
Pregnancy duration (default 40 weeks, supports manual input of any number)
Time progression logic:
For each in-game day passed, add 1 / (duration * 7) to the progress of pregnant maids
Belly deformation value = progress * 40 (maximum limit changed to 40)
Save System
Runtime data is stored in a temporary file
Real-time writing to the temporary file upon every modification
When saving the game: Save as [Save Name]+preg file
When loading the game: Read the corresponding +preg file as the temporary file
