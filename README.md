# CSGO KV3 SCRIPTS

> List of CSGO KV3 Files (Bot AI) to perform certain tasks

> STILL LEARNING, DON'T USE AS A KNOWLEGDE BASE JUST YET! 

Here is a list of examples of custom KV3 scripts which allow bots to perform certain tasks - some of which helps bots to perform executes or certain actions bots cannot do in their own.

Reliable resources:  [CSGO Bot Behavior Trees](https://developer.valvesoftware.com/wiki/CS:GO_Bot_Behavior_Trees#:~:text=Counter-Strike:%20Global%20Offensive%20,,%27s%20proprietary%20KeyValues3%20format%20%28%20) (List of all the possible options).

## How to activate a script

Quite simple. 
First, you need to place the scripts with the `/scripts/ai` folder in your current installed location of CS:GO.

Second, you can activate a certain script with the following command: `mp_bot_ai_bt "relative path"`

> relative path is based on the current installed directory, an example to target a script could be:
> mp_bot_ai_bt "scripts/ai/e7/bt_default.kv3", you must use absolute path if its placed else where!

Assuming no errors appear (in red), the current behaviour tree has been set to the current script that has been loaded.

Its now best to now re-add bots if you have not already, I suggest the following alias:
`alias btr "bot_kick;mp_bot_ai_bt_clear_cache;bot_add_t"`

This kicks the bots already present, then resets the tree and adds them back ( t bot in this case ).

Every change you make, call this alias. If the bot starts to wonder about, that means there is an error with the script - call the second command (`mp_bot_ai_bt`) to see where the problem is with parsing the script.

A handy command is `cv_bot_ai_bt_debug_target 2` which shows you the behaviour steps present to the bot which is activating them.

> `cv_bot_ai_bt_debug_target` will show the behaviour tree of a bot based on its parameter given, in this case we target bot 2 (1 bot in this case)

# List of scripts for example

The list of scripts stated in the [Single Bot Tests](https://github.com/TheE7Player/CSGO_KV3_SCRIPTS/tree/main/Single%20Bot%20Tests "Single Bot Tests") folder contain scripts of which was tested with only 1 bot - these scripts will make every bot present perform the same action. Do not use this if its needs to be coordinated between bots! It does make funny results...

# GIF DEMOS

## Jump Death
This script ([here](https://github.com/TheE7Player/CSGO_KV3_SCRIPTS/blob/main/Single%20Bot%20Tests/bt_deathjump.kv3)) is a demo of a bot performing a jump, waiting a few seconds then dies. Simple.
![Jump Demo](https://media.giphy.com/media/ZySZrF5hw0wbKp5VmM/giphy.gif)

## Barrel Demo (Dust 2 - A Long)
This script ([here](https://github.com/TheE7Player/CSGO_KV3_SCRIPTS/blob/main/Single%20Bot%20Tests/bt_bot_D2_ALong_Barrel.kv3)) shows how you can combine 2 Combinators ( `sequencer` and `parallel`) to make the bot perform a jump onto the barrel on A Long on Dust 2.

![Barrel Demo](https://media.giphy.com/media/gbXkJpSGajQrbQfDNM/giphy-downsized-large.gif)
