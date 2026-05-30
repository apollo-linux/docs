---
title: "Frequently Asked Questions"
weight: 2
---

# Frequently Asked Questions {anchor=false}

## Who is Apollo for?
Apollo is designed to be a general purpose operating system for everyone, and is especially suited for those wanting a general day to day operating system and developers running containerised workloads. Gaming is also fully possible on Apollo, even though it's not the primary focus.

## Can I install system packages?
Apollo does not have an officially blessed way of installing distribution packages. If you need anything you can't get through Flatpak, Homebrew or Distrobox, we recommend building a custom image with the software you need.

## Can I turn off automatic updates?
Apollo is best used with automatic updates in order to keep your system up to date secure. Automatic updates take place when your system activity is low, and not when you are on a metered network. Additionally you can also pin your system image to a specific date within the last 90 days like such:
```bash
# replace $image and $tag with your currently booted image and tag (e.g. apollo:latest). 
# if you're not sure what image and tag you're running, run sudo bootc status.
# replace $date with the format YYYYMMDD (e.g. 20260519) 
sudo bootc switch ghcr.io/apollo-linux/$image:$tag.$date
```

Nontheless, if you still want to disable them you can run the following:
```bash
ajust toggle-automatic-update
```

You can run a full system update on-demand using:
```bash
ajust update
```

When filing bug reports or asking support, please make sure your issue is 