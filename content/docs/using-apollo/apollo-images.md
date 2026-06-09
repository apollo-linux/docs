---
title: "Apollo Images"
weight: 3
---

# Apollo Images {anchor=false}

## Apollo release channels

> [!INFO]
> The stable channel will be changed to a *weekly* cadence at a later date yet to be determined. 

Apollo builds images with three different channels. These have different release cadences and target different users. 

- `stable`: This channel currently updates *daily* and is the default for Apollo. Recommended for most users.
- `stable-lts`: same as the above, but using the *LTS* version of the kernel. Some users may have a more stable experience with this channel.
- `latest`: This channel updates whenever a change is made to the Apollo git repo, alongside daily builds. Recommended for advanced users and testers.

## Nvidia images

> [!INFO]
> Users with older Nvidia cards can use the `apollo` image, however these images only ship the open source drivers, which may have worse performance and stability. 

Apollo builds a dedicated `apollo-nvidia` image, which includes the proprietary Nvidia GPU drivers for Turing (GTX 16xx/RTX 20xx) or newer cards. For most users on AMD or Intel cards, simply using the `apollo` image will suffice.

If you switch graphics cards, e.g., from Nvidia to AMD, or vice versa, it's recommended to switch to the appropriate image using [the instructions below](#rebasing-between-apollo-images) 


## Rebasing between Apollo images

Run `sudo bootc status` first to get the current status of your system, and then you can use `bootc switch` command as below:

```bash
# Replace $image and $channel with your desired image and/or channel.
sudo bootc switch ghcr.io/apollo-linux/$image:$channel
```

### Pinning to a specific date

In addition to regular builds, Apollo also tags each build with a date to make it easier for users to switch. If you need to pause system updates, e.g., due to a regression, you can also pin your system image to a specific date within the last 90 days like such:

```bash
# Replace $image and $channel with your current image and channel (e.g. apollo:latest)
# If you're not sure what image and channel you're running, run sudo bootc status first
# Replace $date with the format YYYYMMDD (e.g. 20260519) 
sudo bootc switch ghcr.io/apollo-linux/$image:$channel.$date
```

### Reference

- [Upstream `bootc switch` documentation](https://bootc.dev/bootc/man/bootc-switch.8.html)