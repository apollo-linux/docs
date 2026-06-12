---
title: "System Administration"
weight: 2
---

# System Administration {anchor=false}

## Updating Apollo

> [!TIP]
> When filing bug reports or asking for support in community spaces, please make sure your system is up to date first, as your issue may have been fixed in an update. 

Apollo by default uses automatic updates, meaning that users always get the latest bug and security fixes as well as new features. Most of the time you shouldn't need to do anything. 

If you want to update manually anyway, or you've turned automatic updates off as mentioned below, simply run the following in a terminal:

```bash
ajust update
```

You can also manage and update Flatpak apps using the Bazaar application store.

### Toggling Automatic Updates  

If you're dealing with a regression in a recent build, you may first want to try [pinning to a specific release date](/docs/using-apollo/apollo-images/#pinning-to-a-specific-date). This will keep automatic updates working for the rest of your system.

Nontheless, if you still want to disable them you can run the following:
```bash
ajust toggle-automatic-updates
```
