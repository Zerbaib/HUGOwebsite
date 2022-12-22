---
title: "BotDiscordPython"
date: 2022-12-22T10:15:55+01:00
# weight: 1
# aliases: ["/first"]
# tags: ["dflt"]
author: "Zerbaib"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Are you interested in this project ? Perfect post is here to explain it to you !"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "" # image path/url
    alt: "note:" # alt text
    caption: "All my programs will have the download with git you can do it without with the .zip on the github page but this will not be said in the docs" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

---
# Start with
CalculaPy it's a little projet in Python
This project is used to calculate simple things (addition, subtraction, multiplication)

*Note: All my programs will have the download with git you can do it without with the .zip on the github page but this will not be said in the docs*

---
# Prerequisites
- Python3 you need 3.7 minimum and 3.10 maximum
- discord module at the lasted
- disnake module at the lasted
- aiohttp module at the lasted
- discordLevelingSystem at the lasted

# Install

## Windows
### Python
- go on the [python website](https://www.python.org/) and go to download the python version or you can go to the reccomender version [here](https://www.python.org/downloads/release/python-397/) and download it
**During the installation do not forget to click "add python to the path"**

### Module
You have 2 choices, I advise you to do both to be sure.
```
pip install discord
pip install disnake
pip install aiohttp
pip install discordLevelingSystem
```
```
pip3 install discord
pip3 install disnake
pip3 install aiohttp
pip3 install discordLevelingSystem
```

## Linux
### Python
*note: All the command is used on debian 10/11 and ubuntu*
```
sudo apt install python3.9
```

### Module
You have 2 choices, I advise you to do both to be sure.
```
pip install discord
pip install disnake
pip install aiohttp
pip install discordLevelingSystem
```
```
pip3 install discord
pip3 install disnake
pip3 install aiohttp
pip3 install discordLevelingSystem
```

---
# Start the prog
## Download
```
git clone https://github.com/Person0z/discord.py-template.git
cd discord.py-template
```

## Config
you have two files ``exemple.config.py`` and ``exemple.configlvl.py``

First you need to del the ``exemple.`` of the name of the files

Now you have ``config.py`` and ``configlvl.py``

### config.py
```py
import disnake

# Discord Token
token = 'TOKEN'

# Your Discord Server ID Will Go Here 
guild = 'GUILD ID'

# The Prefix You Want For Your Discord Bot
prefix = '!'

# Bot Status
activity = ["/help", "discord.py", "With Python", "Made by Person0z", "V.1.3-beta", "Made with Zerbaib", "In dev"]

# Colors
Success = disnake.Color.green
Error = disnake.Color.red
Random = disnake.Color.random

# Owner ID
owner_ids = [000000000000000, 000000000000000] # You can add more owner ids by adding a comma and the id

# Welcomes & Goodbyes Channel ID
welcome_channel = 0000000000000000

# Logging Channel ID
deleted_logs = [0000000000000000] # You can add more channels by doing this: [channel_id, channel_id, channel_id]
```

### configlvl.py
```py
import disnake
from discordLevelingSystem import DiscordLevelingSystem, LevelUpAnnouncement, RoleAward

lvl = DiscordLevelingSystem() # don't tuch here
lvl.connect_to_database_file(r'db/DiscordLevelingSystem.db')

nitro_booster = 00000000000000 # set your role
associate_role = 00000000000000

lvlupchan = 00000000000000 # set your chan

embed = disnake.Embed()
embed.set_author(name=LevelUpAnnouncement.Member.name, icon_url=LevelUpAnnouncement.Member.avatar_url)
embed.description = f'Congrats {LevelUpAnnouncement.Member.mention}! You are now level {LevelUpAnnouncement.LEVEL} 😎' # set our message on levelup
announcement = LevelUpAnnouncement(embed, level_up_channel_ids=[lvlupchan])
```

## Start
```
python3 main.py
```