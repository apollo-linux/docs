---
title: "System Administration"
weight: 2
---

# System Administration {anchor=false}

## Apollo release channels

> [!INFO]
> The `stable` channel will be changed to a *weekly* cadence at a later date yet to be determined. 

Apollo builds images with three different channels. These have different release cadences and target different users. 

- **stable**: This channel currently updates *daily* and is the default for Apollo. Recommended for most users.
- **stable-lts**: same as the above, but using the *LTS* version of the kernel. Some users may have a more stable experience with this channel.
- **latest**: This channel updates whenever a change is made to the Apollo git repo, alongside daily builds. Recommended for advanced users and testers **only**.

### Changing release channels:

For users with AMD/Intel graphics:
```bash
sudo bootc switch ghcr.io/apollo-linux/apollo:$channel # replace $channel with the desired channel above
```

For users with Nvidia GTX 16xx/RTX 20xx or newer graphics:
```bash
sudo bootc switch ghcr.io/apollo-linux/apollo-nvidia:$channel # replace $channel with the desired channel above
```

## Managing Automatic Updates 

Automatic updates are the intended way to use Apollo. We use automatic updates by default so users always get the latest bug and security fixes as well as new features. 

If you need to pause system updates, e.g., due to a regression, you can also pin your system image to a specific date within the last 90 days like such:

```bash
# replace $image and $channel with your current image and channel (e.g. apollo:latest)
# if you're not sure what image and channel you're running, run sudo bootc status first
# replace $date with the format YYYYMMDD (e.g. 20260519) 
sudo bootc switch ghcr.io/apollo-linux/$image:$channel.$date
```

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