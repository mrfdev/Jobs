# FAQ - Discord Asked Questions

---

## Questions about Jobs Reborn that people often ask on Discord

This document is a start for me to keep track of questions I see on the Zrips.net Discord server in the Jobs #help channel. Hopefully, throughout 2022 I will build a collection and slowly find answers to these questions. If you think information is missing, by all means, make a pull request and complete the information (I will most likely review it and probably merge it).

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
They also need [permission](https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-permissions.md) to join any job.

---

### How can I enable certain user groups to have more jobs than others?

Check the answer to this question first: `### How can I have players join only X amount of jobs? ` and then update your group permission to have a higher number:
```
jobs.max.5
```
For example, `lp group VIP permission set jobs.max.5 true`

---

### Does it work on 1.18?

Yes, Jobs 5.0.1.0 or newer, with CMILib 1.1.0.7 or newer, will work with Minecraft 1.18.1 (made for Spigot and Paper)

---

### Is CMILib required? What is this?

---

Yes, CMILib is a library by Zrips that all his plugins require, including Jobs-Reborn. It's free to download, and you do not have to buy CMI to use it. 

---

### The plugin doesn't start!

That sucks, but we require more info to help. Does the Jobs-related error message in your console say 'missing dependency, CMILib required, download it' ?

If so, this means you are missing a dependency. Jobs needs CMILib to work. You should [download] (https://www.spigotmc.org/resources/cmilib.87610/) it.

You can search for the error message in the logs/latest.log in your server's installation directory if you missed it in the console.

---

### Can I get the source code and customize it?

Jobs-Reborn is open source, and you can view the source code on [Github] (https://Github.com/Zrips/Jobs)

If you want, you can clone it and compile it yourself.

[Find out more here.] (https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-jar-files.md)

---

### I have a bug. Fix it!

Yeah, life is not that easy. Unfortunately, we deal in bug reports, not magic shows. So we will need more information.

First, please check that you're on the latest build of your service engine; type: `/ver` and see how far behind you are.

Update to the latest versions of [CMILib](https://www.spigotmc.org/resources/cmilib.87610/) and [Jobs](https://www.spigotmc.org/resources/jobs-reborn.4216/)

Try again. If it still fails, check the latest.log file to see the errors during startup and resolve those.

If you believe you've found a bug, gather the info about your server and go to Zrips's Github and submit a new issue for review.

Provide at least the following:
What the problem is, and how can it be reproduced
What you've done to mitigate it so far.
The output of the command /ver
Versions of other plugins related to your problem
include the entire error message.

---

### Jobs is lagging my server, shows in timings report.

That's not how the timings work. Jobs showing up as a lagging can mean many things. Another plugin can hang the main thread, forcing a queue to build up or other tasks to wait before completing.

We will need to know much more information, including your timings report.

Going to [Github](https://github.com/mrfdev/Jobs/issues) and starting a new issue is the best way to deal with that.

Read the minimum requirements for a bug report from the previous question before posting.

Gather all the information you think could be useful for us in solving the problem and provide it in the report.
---

### What are the official sites?

- Jobs-Reborn on SpigotMC.org ; https://www.SpigotMC.org.org/resources/jobs-reborn.4216/

- CMILib jar on SpigotMC.org ; https://www.SpigotMC.org.org/resources/CMILib.87610/

- Bug reports on Github ; https://Github.com/Zrips/Jobs/issues

- Source code on Github ; https://Github.com/Zrips/Jobs/

- Jobs Documentation on Zrips.net ; https://www.Zrips.net/jobs/

- Zrips Discord ; https://discord.gg/dDMamN4

---

### Where can I find a list of all Jobs Reborn placeholders?

Type: `jobs placeholders` to get the complete list in the console.

You can also do this in-game with the command `/jobs placeholders`

---

### I asked a question, and I am getting ignored?

To get the best help you can get, we need information, then Zrips on Github or the community members on Discord can help you better.

- Have some patience. Post the question, provide info, and just wait.
- We always advise you to stay current and make frequent backups!
- Provide the information if you can (console commands):

**# Server engine:** `ver`
**# Plugin details:** `jobs version`
**# CMI-Library:** `ver CMILib`
**# Vault version:** `ver Vault`
**# Economy manager:** `ver CMI`
**# Permission Manager:** `ver LuckPerms`

- Keep an eye on the console or check the logs to make sure you spot any errors during the startup of any plugins. If you see an error, try to disable the plugin causing it and retry. If there's a need to paste extensive logs and error messages, use a Pastebin type service such as  you want to paste your big error msgs, please use a text storage site like [Hastebin](https://paste.md-5.net/)

---

### Jobs Economy

<https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-economy.md>

More Economy info <https://ptb.discord.com/channels/452792793631555594/526402919826849804/688267075818750053>

---

### Helping Translate Jobs

You can [suggest translations on the Crowdin page](https://crowdin.com/project/jobsreborn).

If some piece of text is wrong or doesn't exist for your current language file, suggest new text to replace it.

We will then accept and merge the change, and it will make its way to a possible next release version.


- You can find translations in the ~plugins/jobs/ directory in their respected directory.

- Some phrases that multiple Zrips plugins use are in the locale files under ~plugins/CMILib/translations

---

### Jobs Points Explained 

How can I use the points I earn from jobs?

You can use them in the Jobs Shop to buy custom boosted items or anything else the owner of your server cares to set up.

With the Jobs API, you can also use them in other plugins like GUI shop.

If you are running multiple servers, you can use a shared MySQL database to track points between all servers.

With the API and multiserver support, you can build anything you can imagine with the points system.

You can also disable all the individual payout types in the generalConfig.yml like so:

`  PaymentMethods:
    Money: true
    Points: false
    Exp: true`

Set any of these to either true or false to enable or disable the payouts of that type.

---

### Jobs/ files Explained

We recently separated all the job files into their own files. This has made the creation and management of jobs a lot easier than before

You can rest easy if you are still running a Jobs version with the old `jobConfig`.

As you update to a new version of Jobs, all your old jobs will automatically be separated into files under `~/plugin/Jobs/Jobs`, keeping all your settings and customization. There's no data loss, so you don't need to worry.

Jobs will move the old configuration into FileBackups. If you don't need it, feel free to remove it after testing that everything works as it should.

The new system makes creating additional jobs easy. First, create a file with the job title as the name and .yml as the file type. It should look like this `newjob.yml`.

Now you can look at the example job file and start creating. It's in the same directory as the separated jobs files, but you can also [file find the example file online](https://github.com/Zrips/Jobs/blob/master/src/main/resources/jobs/_EXAMPLE.yml).

Alternatively, you can just copy an existing job and edit it directly if that feels more comfortable.


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

Each job has its own file, so you have to go through them and change it per file. 

---

### How do I stop registering furnaces?

Short answer: I do not know. Maybe you can set the permission to 0

Try it and find out.

---

### Can I stop paying out in money? (or points or exp)

Yes, `generalConfig.yml` lets you enable/disable the three payout options. 

---

### People in creative mode are getting paid!

Make sure you're not an operator or that you did not `*` wildcard your permissions. You can also negate the permission specifically in the groups to not pay out in creative mode.

The check permissions page. And make sure the setting is disabled in generalConfig.yml

---

### How can I use (short) Jobs names (in chat, etc.)

My best bet is to check the `/jobs placeholders` and find the one you want to use and use that in your chat manager, holograms, etc. 

https://www.Zrips.net/jobs/chat-titles/

```
chat-display
The display method of the title. Accepted values are full, title, job, shortfull, shorttitle, shortjob and none
```

---

### How do I give/edit a player's points?

https://Github.com/Zrips/Jobs/wiki/Commands
![image](https://user-images.Githubusercontent.com/28841349/149127652-853bfe09-1e9a-41cd-9155-6d71fa0bb96a.png)

---

### How do I open /jobs to go to /jobs browse?

> Hi, is there any way to be able to open the jobs menu using /jobs and not /jobs browse

Not by default, another plugin might be required to alias the /jobs command, ensuring that it opens /jobs browse instead of /jobs help. It would be nice to have a toggle. 

---

### org.sqlite.SQLiteException: \[SQLITE_BUSY\]  The database file is locked (database is locked)

SQLite is just a library that reads and writes to a regular file, not a full SQL database. Therefore, sqlite3 databases can be busy or locked when used by an existing long query, another query that's hanging, or when another plugin is already using it (it is a bad practice to use multiple connections when connecting to SQLite). You can try restarting the server or /stop it, copying the original .db file to a new one, backing up your .db file, deleting the original and then renaming the copy to the original name and starting the server again. 

Reading threads might not be closing. Or maybe the Jobs plugin doesn't properly close after insert/update queries. You could consider trying to move to the MySQL database type.

More info about [sqlite3/locking](http://www.sqlite.org/draft/matrix/lockingv3.html)


---

**Contribute to this list? Make a pull request, append to the document, and I will review and probably merge it**
