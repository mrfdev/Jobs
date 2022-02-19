# FAQ - Jobs Quests

Zrips Discord @ https://discord.gg/dDMamN4

This document is based on my experience using Jobs Quests, if you have any further information or seen an error feel free to open a new issue, PR, or poke me on Discord with a DM. 

---

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> The Quests Feature

The Jobs plugin allows players to get rewarded for completing randomly selected daily quests. The daily quest switches at 4:00 every morning. You can set the time in the main config file.

The player automatically joins one quest for each of his jobs every real life day. The amount of quests a player can do per day can be increased per job in the job-specific config file.

The player can choose to skip a quest and receive a replacing quest. By default they can skip once per day, but you can increase this in the main config too. You can add a cost to skipping a quest.

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Players: How to join, etc.

A quest is automatically joined as the player is doing the job they're in. 

It will let the player know in the chat via a highlighted message that they've completed a job and what they've received for it.

The player can check their daily quests and follow their progression in them with the `/jobs quests` command. Get more details by mouse-overing the information displayed in chat.

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Setting up a Quest for a job

Each job only contains one example quest, but you can add as many as you'd like. At the very least the quest has a name, an objective, reward commands and reward description, and a chance that determines how often the particular quest gets selected randomly. You can also set level restrictions for your quest.

Check the Jobs' [examplejob.yml](https://github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-examplejob.yml) file to see how to set up a quest. It also has detailed information on the features mentioned above.

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Commands

```
/Jobs quests [playername] - List available quests
/Jobs resetquest [playername] [jobname] - Resets a player's quest
/Jobs skipquest [jobname] [questname] (playerName) - Skip defined quest and get new one
```

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Permissions

```
jobs.maxquest.[jobName].[number] – Ability to specify maximum quest for the players once a day
jobs.maxquest.all.[number] – Specifying max quest for all jobs
jobs.command.admin.quests – Allows to check quest progression for another player
```
zrips.net > jobs > [permissions](https://www.zrips.net/jobs/permissions/)

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Placeholders

```
%jobsr_user_dailyquests_pending%
%jobsr_user_dailyquests_completed%
%jobsr_user_dailyquests_total%
%jobsr_user_quests%
```

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Misc

Using the above commands and permissions, and configuring the `~/plugins/jobs/jobs/<jobnames>.yml` files, together with using some placeholders, it should be possible to further this feature visually for players. 

---

`Jobs Reborn v5` Jobs Reborn resource page
<https://www.spigotmc.org/resources/jobs-reborn.4216/>

More information about Jobs: https://www.zrips.net/jobs/, here you can find info about permissions, chat titles, signs and other jobs features. 
