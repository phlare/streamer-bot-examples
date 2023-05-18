# target random user but avoid bots

here is an action:    `crush` 

it's goal is to find an active viewer who is not a bot as a target.
the output is in a Twitch Message subaction at the bottom.

the output if it fails to find a non-bot user is (currently) in the C# Execute Action code.
The line `CPH.SendMessage($"{user} is crushless.");` can be edited to change this message.

