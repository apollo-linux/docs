---
title: "Information for Nerds"
weight: 3
---

# Information for Nerds
This is highly detailed or technical information that shouldn't matter to *most* people, but may still be interesting to some people, especially those more familiar with Linux and technology. This is a companion page to [Frequently Asked Questions](/docs/getting-started/frequently-asked-questions/).

## Based on Arch Linux

> [!NOTE]
> Apollo should be considered as an Arch derivative and as such you should not ask for support with Apollo in Arch community spaces.

Apollo uses [Arch Linux](https://archlinux.org) as a package base and [bootc](https://bootc.dev) for updates and image deployment. Apollo's image-based design makes this similar in function and behaviour to SteamOS.

### Why doesn't `pacman` work properly?

Indeed, pacman behaves differently on Apollo than on regular Arch Linux or most derivatives. This is because the **/usr** folder is mounted as read-only by default, meaning that pacman by default isn't able to install packages in the traditional manner. With Apollo, the primary method of installing software is through Flatpak, `brew`, or Distrobox. If you depend on software that isn't available through these methods, you can build a custom image.

## Distroless approach

We believe that prioritising working with our upstreams and others in the Linux community over downstream modifications and rebuilds allows us to make a more effective and usable Linux desktop for everyone. We promote the use of distro-agnostic packaging formats and containerisation over using distro packages.

## bootc under the hood

Apollo uses the bootc update system. This combines image-based updates with bootable container technology to make a more resilient and reliable Linux system.

Updating Apollo pulls a fresh copy of Apollo from the internet and deploys it for the next boot, rather than updating individual packages. This makes the system much more resilient to [configuration drift](https://www.solarwinds.com/resources/it-glossary/configuration-drift) and eliminates common issues with Linux systems from failed updates. 

Additionally, Apollo is distributed as a container, making it possible to make a customised version of Apollo, also known as a custom image, which can be customised similar to a traditional distro with only a bit of extra work at first. Additionally, we use `chunkah` on all released images, allowing layers to be reused between updates.