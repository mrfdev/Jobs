### Jobs-Reborn and Economy (Giving your players /money for doing jobs)

## Please note this.

Before you start making changes I will assume you have backed up your server.

Keeping your server engine and plugins current can help resolve a lot of potential issues. Does it work with .. questions, I have no idea besides "probably", because this is the setup that I use and works for me:

```
,-- Zrips CMI 9.0.2.8 or newer with CMI Economy enabled from SpigotMC.
|   '- https://www.spigotmc.org/resources/3742/
|
|-- Zrips CMI Library 1.0.3.6 or newer from SpigotMC
|   '- https://www.spigotmc.org/resources/87610/
|
|-- Zrips Compiled Vault 1.7.3 from zrips.net
|   '- http://www.zrips.net/wp-content/uploads/2020/07/Vault-1.7.3.jar
|
|-- Zrips Jobs-Reborn 5.0.0.6 or newer from SpigotMC.
|   '- https://www.spigotmc.org/resources/4216/
| 
|-- LuckPerms 5.3.61 or newer from SpigotMC.
|   '- https://www.spigotmc.org/resources/28140/
|
|-- Spigot 1.17.1 (or Paper 1.17.1) or newer.
|   |- https://hub.spigotmc.org/jenkins/job/BuildTools/
|   '- https://papermc.io/downloads
```

## Okay, checklist, let's go and double check your setup

Please double check your values, /stop the server before making changes, do not use plugman or /reload

# What are you running?

Server engine, version, related plugins, and their versions:
Type the following in console and share the full output if you still have an issue with the economy.
```
ver
ver Jobs
ver Vault
ver LuckPerms
cmi version
ver cmilib
```
Go to the official download sites, and make sure your builds are the latest. Outdated builds can give unexpected results. 

# Developer builds

It is always possible that there's an issue with the latest build of Paper, or LuckPerms, or Jobs, etc. It might be worth to check the LuckPerms.net website for a newer jar, or double check zrips.net to see if there's a newer build of the vault jar, stuff like that. Jobs also has a Discord dev-releases channel that might have a newer build worth testing. But of course, they are dev/snapshot builds, so again, backup before making changes. 

Using pre-compiles of Spigot is not recommended, use buildtools on the machine you're running it on, so it's made with that java version for that machine, etc. And get paper from the official site, not some package pre install stuff, you never know what's injected into jars you get from unofficial sites. 

# EssentialsX, instead of CMI.

Yeah that's great. I use EssentialsX still on a few servers. but the bigger majority these days uses CMI and it's what I use and recommend at the moment. So just logically apply essentials-steps where it shows cmi-steps. 

# UltraPerms, GroupManager, instead of LuckPerms.

Yes, just fine. I wouldn't use UltraPerms or Pex, they've shown multiple times to do things in their own way and expect other plugins to adjust. Unlike LuckPerms who seemingly and magically almost never have those type of issues. GroupManager is too old now. You use what you want to use; My support for it is: move to luckperms, do yourself a favor. 

# Start-up check.

Start the server and see an eye on the information that flies by. Especially when it comes to your economy plugin, vault, jobs, permission manager like luckperms. If you can't do this, or it goes too fast. Check the latest.log file once it's done loading. 

- Are all the plugins starting and loading successfully?
If you read through the logs, does it say it has enabled the plugin and that it was able to do stuff, it did it show errors and warnings, and other worrying things. Check with `pl` aftewards to makes ure they all are listed, and green. If something's not there that you expected, or it's showing red; check the latest.log again. 

- Did the economy plugin show it has the economy enabled, does it show that it was able to hook successfully into Vault?
If not, something might be going wrong, the warnings, etc might all disclose what's up. Keep a note of the things that go wrong, others might recognize what's up and help you.

- Did the vault plugin load successfully and say nothing that you worry about? 

- Did the Jobs plugin say it can do the economy stuff, and said that it successfully hooked into Vault?

- Finally, check if the permission manager has loaded okay, and that it can play nice with Jobs, etc.

# Permissions

Make sure your default group has `jobs.use` at the very least, and that your players have the required permissions to join, leave, stats, etc. 
```
jobs.command.browse
jobs.command.join
jobs.command.leave
jobs.command.info
jobs.command.top
jobs.use
jobs.max.3
jobs.join.*
jobs.world.worldName
```
_(`worldName` is your world where the jobs should pay)_

If you use CMI and LuckPerms you can actually use their features like /cmi haspermission, or /lp verbose, to figure out if a command is set properly. Check their documentation for more information.

# In-game double checking

Let's just double check how you are testing in-game. You'd be surprised how easy it is to make a silly mistake. 

- Are you in-game testing as operator?
- As a team member, instead of a default, regular, first time user?
- Are you in creative mode perhaps? (enable-pay-creative: false, generalConfig.yml)

Maybe go to minecraft.net and get an alt account or ask a friend to join who has never joined before and let them be that first time joining member who you can do test on. 

Make sure you're in survival mode.

# Jobs' generalConfig.yml file checking

```yaml
enable-pay-creative: false

# Enable async economy calls.
# Disable this if you have issues with payments or your plugin is not thread safe.
economy-async: true
```
If you're having issues, maybe make sure that pay creative is at least set to false, and that you are not in creative mode. Anyway, ..

Make sure you test with a /stop, set economy async from true to false, and start the server, and try again. Who knows, maybe it magically gets fixed for you particular server setup. 

If the `Economy section -> PaymentMethods part-> Money setting` is enabled, you can get money from jobs _if_ it is configured per /jobs/ file.

There is also a feature with the setting `economy-batch-delay`, you can temporary disable this to make sure you get instantly paid, you might not notice your bath-payment for a bit and _think_ it's not working.

# Enabled Limits perhaps?

Let's check if you perhaps have limits enabled and tested enough that it goes wrong, or at least has hit a limit. Turn it off to dobule check (generalConfig.yml):
```yaml
  Limit:
    # Money gain limit
    # With this enabled, players will be limited how much they can make in defined time
    # Time in seconds: 60 = 1 min, 3600 = 1 hour, 86400 = 24 hours
    Money:
      Use: true
```

# I've tried everything!

Yeah, that's possible, so, go back to step 1 and double check. Gather up the info. 

Share with the discord chat channel the info you've gathered, either in a pastebin link or by properly pasting it. This includes the outputs of all those ver things, the config file, the expected behavior, any startup error msgs, or misisng info that you expected to find, or what happens or doesn't happen in game and any console errors if any that happen. The more complete your info, the easier it can be for others to figure out what's up. 

# Finally

One of the Jobs developers also has a pinned message on Discord, it might be worth reading as well: https://ptb.discord.com/channels/452792793631555594/526402919826849804/688267075818750053

