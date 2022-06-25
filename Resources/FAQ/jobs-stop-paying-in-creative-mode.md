# FAQ - People in creative mode are getting paid

<topMenu>

---

Make sure you're not an operator or that you did not `*` wildcard your permissions. You can also negate the permission specifically in the groups to not pay out in creative mode.

The check permissions page. And make sure the setting is disabled in generalConfig.yml

```yaml
# Option to allow payment to be made in creative mode. This ignoring when a group has 'jobs.paycreative' permission.
enable-pay-creative: false
````generalConfig.yml`
