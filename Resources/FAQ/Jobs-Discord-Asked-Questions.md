# FAQ - Discord Asked Questions

---

## List of questions I see on Discord a lot.

This document is a start for me to keep track of questions I see on the Zrips.net Discord server in the Jobs #help channel. Hopefully throughout 2022 I will be able to build a collection and slowly get some answers to these questions. If you think information is missing, by all means make a pull request and complete the information (I will most likely review it and probably merge it).

## Questions

Some questions I saw

---

### How can I have players join only X amount of jobs? 

In `generalConfig.yml` you can set a global value for the maximum amount of jobs a player can join. 
```yaml
# Maximum number of jobs a player can join.
# Use 0 for no maximum
# Keep in mind that jobs.max.[amount] will bypass this setting
max-jobs: 3
```
Note that they need the [permission](https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-permissions.md) as well to even join any job.

---

### How can I have everybody join only X jobs, but allow another group to join even more?

Check the answer to this question first: `### How can I have players join only X amount of jobs? ` and then update your group permission to have a higher number:
```
jobs.max.5
```
e.g. `lp group VIP permission set jobs.max.5 true`

---

### Does it work on 1.18?

Yes, Jobs 5.0.1.0 or newer, with CMILib 1.1.0.7 or newer will work Minecraft 1.18.1 (made for Spigot and Paper)

---

### Is CMILib required? What is this?

---

Yes, CMILib is a library by Zrips that all his plugins require, including Jobs-Reborn. It's free to download, and you do not have to buy CMI to use it. 

---

### The plugin doesn't start!

That sucks, but we require more info, does it say in the console (latest.log has this info as well) that the error message starts with 'missing dependency, CMILib required, download it' ? If so, the reason is that there's a missing dependency, the CMILib is required. You should download it.

---

### Can I get the source code and customize it?

Jobs-Reborn is open source, you can view the source code on Github here: https://Github.com/Zrips/Jobs if you want you can clone it, and compile it yourself. More info about that here: https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-jar-files.md

---

### I have a bug, fix it!

Yeah, life is not that easy, we deal in bug reports, not magic shows. So we will need more information. Please check that you're on the latest build of your service engine; type: `/ver` and see how far behind you are. Additionally, get the latest CMILib jar from SpigotMC.org, and the latest Jobs .jar from SpigotMC.org. Try again. If it still fails, check the latest.log file to see what the errors are during startup and resolve those. If you believe you've found a bug, gather the info about your server and go to Zrips's Github and submit a new issue for review. Explain what the issue is, how to reproduce it. What you've done to mitigate it, what /ver and other versions you have of what you're trying to work with, and include the full error message.

---

### Jobs is lagging my server, shows in timings report.

This is a loaded question, because it can mean a lot of things. Another plugin can hang the main thread, forcing a queue to build up or other tasks to wait before they can complete. We will need to know much more information. Including a timings report. Github > new issue > is the best way to deal with that. Think about it first, what info will be helpful to help you the best.

---

### What are the official sites?

- Jobs-Reborn on SpigotMC.org ; https://www.SpigotMC.org.org/resources/jobs-reborn.4216/

- CMILib jar on SpigotMC.org ; https://www.SpigotMC.org.org/resources/CMILib.87610/

- Bug reports on Github ; https://Github.com/Zrips/Jobs/issues

- Source code on Github ; https://Github.com/Zrips/Jobs/

- Jobs Documentation on Zrips.net ; https://www.Zrips.net/jobs/

- Zrips Discord ; https://discord.gg/dDMamN4

---

### What are the placeholders for Jobs plugin?

In the console, type: `jobs placeholders` to get the full list.

---

### I asked a question, and I am getting ignored?

To get the best help you can get we need information, then Zrips on Github, or the community members on Discord can help you better.

- Have some patience. Post the question, provide info, and just wait.
- We always advise to stay current and make frequent backups!
- Provide the information if you can (console commands):

**# Server engine:** `ver`
**# Plugin details:** `jobs version`
**# CMI-Library:** `ver CMILib`
**# Vault version:** `ver Vault`
**# Economy manager:** `ver CMI`
**# Permission Manager:** `ver LuckPerms`

- Also keep an eye on the console/logs, to make sure you spot any console errors during startup of any plugins, and/or when you try to do something with this plugin. If you want to paste your big error msgs, please use a pastebin like service like <https://paste.md-5.net/>

---

### Jobs Economy

<https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-economy.md>

More Economy info <https://ptb.discord.com/channels/452792793631555594/526402919826849804/688267075818750053>

---

### Helping Translate Jobs

Crowdin page to suggest translations to ignore the unknown FNF messages when a string not found in your current language file. If you suggest, this translation will come to my GitHub repo and I will accept and merge it if we release it a new version.

Can be found on: <https://crowdin.com/project/jobsreborn>

- You can find translations in the ~plugins/jobs/ directory in their respected directory.

- Global phrases can also be found in the locale files under ~plugins/CMILib/translations

---

### Jobs Points Explained 

Where is Job points is used for?

It is used for jobs shop to buy custom boosted items or anything else, or even can be made in other plugins with Jobs API like in gui shop.

It much useful than boring money
Also, if you have multiple servers that have same mysql database and with jobs, you can synchronize points between servers and use it for anything.

If you prefer to not use this, just disable points payment in generalConfig. 

---

### Jobs/ files Explained

We recently made a change that changes `jobConfig` to separate job files to make job creation as easy as possible. This way, you don't have to worry about upgrading from an older version to the current one, as the old jobConfig file will be moved to the `FileBackups` directory and the jobs in it will be moved to separate files. If you still need the old jobConfig file, the server owner can use something of it for the future, but if you don't have to, feel free to remove it along with the FileBackups directory. 

So all your created jobs are transferred to separate files for simplicity. Many people have asked the question, “how do I create custom jobs?” Is very simple. Just create a file with the selected name and put ".yml" at the end of the name so that the plugin can read or copy an existing job and write its name to the selected name. 

Then, only the internal contents of the file need to be modified. Many even asked the question "what happened to the content in the old file?", Which remained in the jobConfig file, they were moved to those job files without data loss. So there is nothing to worry about, nothing is lost after the file movement.

---

### Jobs Permissions

<https://www.Zrips.net/jobs/permissions/>

---

### Dynamic Signs

<https://www.Zrips.net/jobs/signs/>

---

### Chat Titles

<https://www.Zrips.net/jobs/chat-titles/>

---

### Common Issues

<https://www.Zrips.net/jobs/common-issues/>

---

### Jobs API

<https://www.Zrips.net/jobs/api/>

---

### Jobs GUI adjustment

For anyone having issues with Stone in ./jobs browse or where ever

Change
```yaml
  Gui:
    Id: %id%
    Data: 0
```
To
```yaml
  Gui:
    Item: %item%
```
And swap out `%item%` with the item you want it to be

Each Job has their own File so you have to go through and change it per file 

---

### How do I stop registering furnaces?

Short answer: I do not know, maybe the permission can be set to 0 ?

---

### Can I stop paying out in money? (or points or exp)

Yes, `generalConfig.yml` lets you enable/disable the three payout options. 

---

### People in creative mode are getting paid!

Make sure you're not an operator or that you did not `*` wildcard your permissions. You can also negate the permission specifically in the groups to not pay out in creative mode.

The check permissions page. And make sure the setting is disabled in generalConfig.yml

---

### How can I use (short) Jobs names (in chat, etc)

My best bet is to check the `/jobs placeholders` and find the one you want to use, and use that in your chat manager, holograms, etc. 

https://www.Zrips.net/jobs/chat-titles/

```
chat-display
Display method of the title. Accepted values are full, title, job, shortfull, shorttitle, shortjob and none
```

---

### How do I give/edit a player's points?

https://Github.com/Zrips/Jobs/wiki/Commands
![image](https://user-images.Githubusercontent.com/28841349/149127652-853bfe09-1e9a-41cd-9155-6d71fa0bb96a.png)

---

### How do I open /jobs to go to /jobs browse?

> Hi, is there any way to be able to open the jobs menu using /jobs and not /jobs browse

Not by default, another plugin might be required to alias the /jobs main command, making sure that it goes to /jobs browse, or /jobs help. It would be nice ot have a toggle. 

---

### org.sqlite.SQLiteException: \[SQLITE_BUSY\]  The database file is locked (database is locked)

SQLite is just a library that reads and writes to a file on the file system, not a full SQL database. Sqlite3 databases can be busy or locked when in use by an existing long query, another query that's hanging, or when another plugin is already using it (it is a bad practice to use multiple connections when connecting to SQLite). You can try restarting the server, or /stop it, copy the original .db file to a new one. Backup your .db file, and delete the original ~ then rename the copy to the original name and start the server again. 

Reading threads might not be closing. Or maybe the Jobs plugin doesn't properly close after insert/update queries. You could consider trying to move to the MySQL database type.

More info about [sqlite3/locking](http://www.sqlite.org/draft/matrix/lockingv3.html)


---

**Contribute to this list? Make a pull request, append to the document, and i will review and probably merge it**
