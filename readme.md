# About
Translator JS is a Node JS script that I wrote to help me translate Light Novels from Chinese to English. At the current moment, the goal is to translate the series "That Time I Got Reincarnated As a Slime" from Chinese to English

## The Approach
Because the light novel doesn't seem to have full on paragraphs and each new line `\n` marks the beginning of a new phrase, I can send those into individual translator APIs to see if something reasonable would come up. Before any sentence is sent to the APIs, it is first checked through a chinese parser to see if the "subject" of the sentence is present or not. if it isn't present, then combine the current sentence with the next sentence as Chinese sometimes will have sentences without sentence subjects resulting in weird translations.

After words, the following translation APIs will be used:
Google
Microsoft
WeChat

Each output is then validated against a grammar API to check for grammar consistency and then the most grammatically correct sentence is logged down in the main file with all options logged in an additional file. If nothing passes the threshold of acceptability then log all options and annotate it.

After, the logged file will be read through to check for correctness before being passed on to editors for further corrections. 
