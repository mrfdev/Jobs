
## Jobs GUI adjustment

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

Each job has its own file, so you have to go through them and change it in each one

