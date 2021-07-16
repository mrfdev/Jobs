### Jobs-Reborn and the different JAR files explained

## Please note this.

Before you start making changes I will assume you have backed up your server.

Keeping your server engine and plugins current can help resolve a lot of potential issues. Does it work with .. questions, I have no idea besides "probably", because this is the setup that I use and works for me:

```
,-- Zrips CMI 9.x with CMI Economy enabled from SpigotMC.
|   '- https://www.spigotmc.org/resources/3742/
|
|-- Zrips Compiled Vault 1.7.3 from zrips.net
|   '- http://www.zrips.net/wp-content/uploads/2020/07/Vault-1.7.3.jar
|
|-- Zrips Jobs-Reborn 5.0.0.3 from SpigotMC.
|   '- https://www.spigotmc.org/resources/4216/
| 
|-- LuckPerms 5.3.51 from SpigotMC.
|   '- https://www.spigotmc.org/resources/28140/
|
|-- Spigot 1.17.1 (and Paper 1.17.1 on some other servers).
|   |- https://hub.spigotmc.org/jenkins/job/BuildTools/
|   '- https://papermc.io/downloads
```

## Okay, let's explain what's up

Now that you know what I like, let's see what you like. You might wish to use different builds of Jobs, or a different permission manager or economy manager, that's all fine. You do you. This page is to explain the different Jobs jar files that could be available for you to consider downloading.

# What are you running? (For when you have issues)

If you have an issue, back up your data, identify the issue, resolve it, or if it's a bug: report it on Zrip's Jobs github repository as a new issue. 

Server engine, version, related plugins, and their versions:
Type the following in console and share the full output if you still have an issue with the economy.
```
ver
ver Jobs
ver Vault
ver LuckPerms
cmi version
```
Go to the official download sites, and make sure your builds are the latest. Outdated builds can give unexpected results. 

# The different Jobs JAR files

The **latest stable Spigot build** that's a publicly available release on Spigot's website and recommended for most people. We advice you to at least use this. Especially if you don't know what you're doing. It's mainly meant for the latest Spigot / Paper builds, but can work on older versions, and can work on certain forks of Spigot / Paper. 

- SpigotMC download: https://www.spigotmc.org/resources/4216/

The **latest Discord Developer build** that's available sometimes, and shared by the developers through Discord. Upon request (and when there is time) a developer can make a new dev-build jar for the community to help try and confirm fixes, or to simply test newer builds. etc. This is only available on the Discord server, so please join it if you haven't already (and pick the Jobs role). The Jobs category has a #dev-builds channel where it should list it. If it's not there, you can request it, or there's a reason it's not there. We don't recommend running dev builds on a live environment. So please test it thoroughly first. 

- Discord #dev-build: https://discord.gg/dDMamN4

And finally, you can get **the latest available Github source code** that's publicly available through Zrip's Github repository for Jobs-reborn. If you need a bleeding-edge build of the code you can get the open source code by cloning it locally and use maven to install it. You will end up with a jar that's the latest and developer-updated greatest. We don't recommend using this in a live environment, but it might include some bug fixes that can help you out. We asusme you know what you're doing and only choose this option if that's the case. 

- Github Jobs repository: https://github.com/Zrips/Jobs

**How to compile?**

Basically you clone the repository locally, so make sure you have git installed on your system. And then you can use Apache maven to install it, so make sure you have maven installed. Here are some basic and quick compile instructions:
```
# Go into your gitprojects folder where you wish to clone git repositories (i.e. /Projects/Github/Clones/)
mkdir JobsReborn
cd JobsReborn

# Clone the public open source repo
git clone https://github.com/Zrips/Jobs.git

# Go into the directory with the pom.xml file
cd Jobs

# Party time, this can take a while
mvn clean install -Dmaven.test.skip=true

# Once completed, it should say something like this:
[INFO] Installing /Projects/Github/Clones/JobsReborn/Jobs/target/Jobs4.17.1.jar to /Users/whatever/.m2/repository/Jobs/jobs/4.17.1/jobs-4.17.1.jar
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS

# Note that THIS is the compiled JAR file you want to use on your server as a plugin:
# /Users/whatever/.m2/repository/Jobs/jobs/5.0.0.3/jobs-5.0.0.3.jar
# You can now copy that target file to your minecraft server plugins/ directory.
```

# Gottah get git and stuff

Some handy tutorials maybe in case you don't have git/maven on your system

- git: https://www.digitalocean.com/community/tutorials?q=install+git

- maven: https://maven.apache.org/install.html
(by the way, on macOS with Homebrew: brew install maven will do the trick)
