# FAQ - Jobs Quests

Zrips Discord @ https://discord.gg/dDMamN4

---

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> The Quests Feature

The Jobs plugin allows players to get rewarded for completing quests. While they're doing the job it seems they automatically join and participate in these quests sometimes. 

Quests are on a per job basis, daily, and are automatically joined, and restarted. 

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Players: How to join, etc.

A quest is automatically joined as the player is doing the job they're in. 

It will let the player know in the chat via a highlighted message that they've completed a job and what they've received for it.

There are no toggles, commands, etc. that a player can use at this point. 

## <g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> Setting up a Quest for a job

You can check the Jobs' [examplejob.yml](https://github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-examplejob.yml) file to see how it looks like (it also has some additional information)

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
