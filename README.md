# ReductV3
New version of Reduct, a Revolt.chat client held together by duct tape and bad code.
Adds websockets, more features, more code, still no libraries, tries to minimise amount of requests sent to the API.
As this is a personal project to learn through doing, I don't intend to accept pull requests - send issues instead or if it's something I don't see fitting or over my capabilities, feel free to fork this.

## everything below work-in-progress

Current features as for now:
  - Websocket stuff you would expect from a chat app (provides server list, channel list, saved notes, DM and group chats, new messages, shows when someone is typing)
  - API stuff you would expect from a chat app (Getting messages older than the new ones, sending messages, deleting messages, editing messages)
  - Author name and profile picture displaying (global, not server ones. masquerades display properly, system messages do display)
  - Displaying time the messages were sent
  - Multireplies (showing and sending), attachments sending (multiple)
  - Attachment embeds + ogg/wav embed support due to a workaround
  - Regular embeds work in progress, right now you can see just the title
  - New and hardcoded emotes rendering
  - Reactions rendering (+showing names of people who reacted on hover) and posting support
  - Being able to send and read messages in a voice channel
  - Keyboard shortcuts (Enter to send message, ESC to scroll to the bottom of the message list)

The hardships you might encounter while using:
  - it only recognises people who said something in the last 50 messages, if someone new joins, their name won't be displayed until you reload. same with reactions, though with them you might not find out
  - client is not aware of your permissions so it allows you to attempt everything, even if you don't have permission to. in case you don't, it will try and fail
  - when reacting you have to tell it the emote id/unicode emoji as the emote picker is not in
  - the channel list lacks categories and is not ordered, same with server list
  - you can only see what a message replies to if that reply is on screen
  - getting older messages... let's say it has some issues
  - autoscroll option scrolls to the bottom every time someone sends a message, so it's better to scroll down pressing ESC instead unless you don't want to scroll up

The things I think this client could have and will probably add
  - masquerades sending and being able to save and switch between them so you won't have to remember
  - custom backgrounds

The things I would add but still need to think on how to implement them:
  - unread messages
  - pings
  - showing if you're typing without spamming the websocket

The things I have absolutely no idea how to add
  - voice chat
