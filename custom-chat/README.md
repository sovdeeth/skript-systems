# Custom Chat

This is a plug and play custom chat skript. It hijacks the vanilla message sent, formats it heavily, processes it, and then sends it again to the proper receivers using the ``send message`` effect.

It is formatted like this:
```
 • Nickname - chat message
```
The nickname and dot have a tooltip with username, nickname, and rank information. If you click it, it will autofill a ``/msg`` command in your chat input box.
The chat message has a tooltip with sender info, message type info, a timestamp, and the number of players that saw the message. Clicking it will paste the message text into your chat box.

**Colour and Custom Formatting**

Each player can have a custom name colour and custom text colour. By default, everyone uses the same default colour. It's up to you to decide how to change players' colours. They're stored under ``{chat::%player%::name-colour}`` and ``{chat::%player%::chat-colour}``. Additionally, the rank/role a player has determines their dot colour. By default there's only a default and a staff colour, for players with ``{chat::staff::%player%}`` set. Again, it's up to you to customize this. 

This skript also adds various emoji codes and a few custom formatting codes, as seen below:
```
# formats chat message (emojis)
replace all ":sword:" with "🗡" in {_message}
replace all ":bow:" with "🏹" in {_message}
replace all ":trident:" with "🔱" in {_message}
replace all ":potion:" with "🧪" in {_message}
replace all ":splash_potion:" with "⚗" in {_message}
replace all ":fishing_rod:" with "🎣" in {_message}
replace all ":shield:" with "🛡" in {_message}
replace all ":axe:" with "🪓" in {_message}

# formatting tags
replace all "$i" with formatted "&o" in {_message}
replace all "$b" with formatted "&l" in {_message}
replace all "$r" with formatted "<chatcolour>" in {_message} 
```


**Triggering chat redirects**

You can tell the chat skript to treat the next chat message from a player as an input, and it will store it in a variable for you to access instead of sending it as a chat message. 

Example code:
```python
# tell player to enter input
send "Enter your input in the chat." 

# set flag and wait for input    
set {chat::redirect::%player%} to true
loop 300 times:
    if {chat::redirect::%player%::message} is set:
        exit loop
    wait 4 ticks

# if no input was given
if {chat::redirect::%player%::message} is not set:
    send "&cYou waited too long to enter an input." 
    clear {chat::redirect::%player%}
    stop

# store input in local variable and clear the global variable
set {_input} to {chat::redirect::%player%::message} 
clear {chat::redirect::%player%::message} 

# confirm input to player
send "Entered %{_input}%." 
```
