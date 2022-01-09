# FAQ

---

## Jobs - Basic Permissions for Players

The Jobs-Reborn plugin requires some configuration in order for players to use the plugin, this includes the ability to use it, to browse and pick jobs, and to only get paid out in certain worlds. Below is an example of some basic permissions you can consider using to achieve that. 

```
jobs.command.browse
jobs.command.info
jobs.command.join
jobs.command.leave
jobs.command.stats
jobs.command.top
jobs.join.*
jobs.max.3
jobs.use
jobs.world.worldnamehere
jobs.world.endnamehere
jobs.world.nethernamehere
```

Do not forget to go through `generalConfig.yml` to set up the economy side of things, what gets paid out, if creative mode should be an option, etc. etc.

## More information

https://www.zrips.net/jobs/permissions/
