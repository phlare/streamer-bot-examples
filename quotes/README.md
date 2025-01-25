# streamer.bot quote enhancement

This import extends the native quote functionality of streamer.bot to mimic the mixitup commands for the same.

* !quote - Sends a message with a randomly selected quote.
* !quote [NUMBER] - Sends a message with the quote that has the specified number.
* !quote [TEXT] - Sends a message with the quote that contains the specified text.
* !lastquote - Sends a message with the most recently added quote.
* !addquote, !quoteadd - Adds a new quote with the text after the command itself. (EX: !addquote I'm a new quote!)
* !deletequote, !quotedelete - Deletes quote that has the specified number. (EX: !deletequote 17)

## Instructions:
1) Import [code.txt](https://raw.githubusercontent.com/phlare/streamer-bot-examples/main/quotes/code.txt) into Streamer.bot
2) Go to the commands tab and enable the relevant commands, and set permissions as desired (recommend VIP and up for !addquote and mod only for !deletequote)
3) Go to Settings -> Quotes in SB and check the "enabled" checkbox, and set the "Perm to Add" dropdown to the desired permissions
4) Enjoy