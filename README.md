# whzbot-resource
Translation, Card Decks and so on for whzbot
This is originally decoupled from shiki's dice. As time passes on, ideas have been added to whzbot.
whz do welcome everyone to contribute for ideas and translations.

# File Format
files are mainly in two formats:
1. loose json format, my own json interpreter do accept json format with mistakes like missing comma, missing quotes and/or even missing curly braces.
  Feel free to add card decks and translations!
2. key-value pairs separated with '='. Sone files use this format because it's flat and simple. I do have converters to change from and to json, don't worry.
  Files like command alias use this format. You are allowed to post pull requests on them, but I would selectly accept it.

# Some Hints
I build up a kind of complex system to interpret commands, card decks, translations and variables. Of course I will tell. 
Features may change over develop, but here are some of that.
1. at any time curly braces quotes for executable things.
1.1 inside curly braces, if it is not starting with a dot '.', it is hyperlink to the same context, eg. variable, carddeck, translation.
1.2 inside curly braces, use '.' to run a command, with shortened output and no error message. The command executor is whoever involves this text.
1.3 in variable, curly braces with number are used to pass context from program. 0 is reserved for the user, and other number are decided by me.
2. escape characters are accepted.
3. gacha pool is similar to card decks but probability can be controlled. I implemented kinked, uniform and remain in bot.
3.1 kinked probability means if user did not get this, counter added up. But probability remains the same until count passes a point. After that prob. will be proportional to count - kink point.
3.2 uniform distribution is uniform, obviously. It does not change.
3.3 remain fills up probability to 1. if total probability is more than 1, probability cuts at 1, in the order presented in file.
4. there is a large section of Chinese help doc and card deck being English words, that's for my friends to play with. Don't panic, bot will never force a quiz on you.
5. any new language need to be registered in Luaguage.whz; You can choose a parent language to save time, or just use dummy.
