
## How can I have players join only X amount of jobs?

In `generalConfig.yml` you can set a global value for the maximum amount of jobs a player can join.

```yaml
# Maximum number of jobs a player can join.
# Use 0 for no maximum
# Keep in mind that jobs.max.[amount] will bypass this setting
max-jobs: 3
```

Note: the right [permission](https://Github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-permissions.md) is also needed to join any job.
