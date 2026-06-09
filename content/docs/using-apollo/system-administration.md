---
title: "System Administration"
weight: 2
---

# System Administration {anchor=false}

## Managing Automatic Updates 

Automatic updates are the intended way to use Apollo. We use automatic updates by default so users always get the latest bug and security fixes as well as new features. 

If you're dealing with a regression in a recent build, you may first want to try [pinning to a specific release date](/docs/using-apollo/apollo-images/#pinning-to-a-specific-date). This will allow the rest of your system to remain up to date.

Nontheless, if you still want to disable them you can run the following:
```bash
ajust toggle-automatic-updates
```

> [!TIP]
> When filing bug reports or asking for support in community spaces, please make sure your system is up to date first, as your issue may have been fixed in an update. 

If you have disabled automatic updates, you should make sure your system is up to date regularly. You can run this command in the terminal to update everything at once:

```bash
ajust update
```