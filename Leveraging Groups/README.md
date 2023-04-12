A handful of import codes to help leverage groups in streamer.bot
see video here: (coming soon)

# i break for bot group members(v2)

use this as a sub action in streamer bot actions you want to ignore bots.

Create a group within streamer.bot and populate it with the users you want ignored (generally bots)

import [botgroup.txt](https://raw.githubusercontent.com/phlare/streamer-bot-examples/main/Leveraging%20Groups/botgroup.txt) inside of streamer bot and use the imported action as a subaction at the top of any streamer bot action you want to ignore bots, or use as a breaking point within an action where the subactions following will not execute for bots, but the ones above will.


# join group (via command or channel points)

import [joingroup.txt](https://raw.githubusercontent.com/phlare/streamer-bot-examples/main/Leveraging%20Groups/joingroup.txt) inside of streamer bot and trigger the imported action with a command or channel point redemption to allow user to join a group themselves.   requires you to have created a group already, and specified that group name in the Set Argument subaction of this action


# autopopulate group based on follow time

import [followgroup.txt](https://raw.githubusercontent.com/phlare/streamer-bot-examples/main/Leveraging%20Groups/followergroup.txt) and assign to the "Present Viewers" event under Platform > Twitch > Events > General
Configure the group that will be populated and the number of minutes you require a user to have followed to be added to the group using the Set Argument subactions in the imported action "Iterate Present Viewers"