# playing with Viewers Queue System  Version 0.10

Add/remove viewers to/from a player queue where you can keep track of who wants to play, and get them lined up.   

Suggested use for only you and your mods to be able to use the majority of these commands, but if you want anyone to be able to add themselves, you can enable the !addme and !removeme commands as well and set permissions accordingly.

Video forthcoming eventually, but for now, have a beta release and please help me test this

## Instructions:
1)  Import [code.txt](https://raw.githubusercontent.com/phlare/streamer-bot-examples/main/playerQueue/code.txt) into Streamer.bot
2) Enable the commands as needed and set permissions as desired (recommend mod only except for !addme and !removeme)
3) Adjust "NumberActivePlayers" variable in main action (defaults to 1)
4) (optional) Assign AddMe and RemoveMe Actions to Channel Point Rewards
5) (0.9+) Toggle changeTitle argument to toggle off/on automatic title changes
6) (0.9+) Adjust titleSeparator argument to use separator other than 'with' when tagging collaborators in stream title
7) Enjoy
 
## Command descriptions:
* **!addme**\
 (optional)  set to to allow anyone to add themselves to the queue, or lock command down to vip/mods only.\
* **!addplayer**\
  allow mods to add others to the queue (set permissions accordingly)  use like !addplayer @buttsbot  (works with or without the @)\
  multiple players can be added by separating their names with spaces
* **!clearplayers**\
    clear the whole queue, including active players\
* **!nextplayer**\
    announce the next player when it's time to pull one from the queue (this also removes that player from queue and adds them as active)\
* **!nextplayer n**\
   pull multiple players from queue in order (use like !nextplayer 2, !nextplayer 3)\
* **!randomplayer**\
    announce a random player when it's time to pull one from the queue (this also removes that player from queue and adds them as active)\
* **!randomplayer n**\
   pull multiple players from queue randomly (use like !randomplayer 2, !randomplayer 3)\
* **!removeactive**\
   removes all active players from active queue (does not effect "waiting" queue)\
* **!removeme**\
   allows user to remove themselves to queue\
* **!removeplayer**\
    allows mods to remove someone from the queue (set permissions accordingly)\
* **!replaceactive**\
   this removes all active players and automatically pulls in the next from the queue\
* **!showplayers**\
    display the entire queue in chat.\

### Changing Commands is possible by adjusting the commands themselves as well as the "set argument" sub-actions in the main action. Ping phlare if you need help with this.

Likely some other uses for this and it can be made more generic to accommodate those uses, but I'd love for some help road testing this.

## Change Log
*version 0.2* (2022-11-12)
- added @ to callout in !nextplayer
- added duplicate protection

*version 0.3* (2022-11-15)
- added optional numeric parameter to !nextplayer
- added !randomplayer
- combine all commands except !addme into same "command" object in SB

*version 0.4* (2022-11-18)
- added !removeme command

*version 0.5* (2022-11-19)
- added separate export for YouTube Version
- added more flexibility to commands allowed
- removed a stray debug message
- fixed messaging when queue is empty and !nextplayer or !randomplayer is used.

*version 0.6* (2022-12-28)
- added "active players" list that keeps track of the currently active players after they have been added using !nextplayer
- configurable "numberActivePlayers" variable in main action (defaults to 1)
- proper camelCase for command arguments

*version 0.7* (2023-01-18)
- update to truncate list of players if it gets too long
- fix to prevent user being added to queue if already "active"
- AddMe and RemoveMe actions separated so they can be used as channel point rewards.

*version 0.8* (2023-02-01)
- added !removeactive to clear players from active list
- added !replaceactive to clear active players AND automatically call !nextplayer n for number of required new active players

*version 0.9* (2023-06-04)
- removed some unnecessary output that was a bit on the spammy side
- added ability to add multiple players with !addplayer command (separate with spaces)
- added (optional) ability to automatically tag active players in the stream title
- moved !showplayers to be a public command rather than moderator only

*version 0.10* (2024-08-19)
- updated to work with new streamer.bot version


## Requested / Possible Future updates
- action to pull the info on the queue for use in an overlay
- add a way so that subscribers can get a priority queue
- add a "bribing" system to allow a certain bit donation to jump the queue
- ability to run multiple queues in parallel for different activities
- extract more of the commands to their own methods so they can be tied to actions individually (for voice control / streamdeck / etc)
- some sort of html display of the queue to be able to be used as an overlay element or dock
