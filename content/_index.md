---
title: "Welcome to Apollo!"
layout: landing
---

# Welcome to Apollo

Apollo is a Linux desktop OS designed to be easy to use and up to date without sacrificing on usability. It uses an image-based update system and containerisation to provide a reliable base that accomdoates a wide range of workflows. Apollo should be especially appealing for everyday use and containerised development, but it can do ultimately anything you want, including gaming. 

# Key features
- Near-vanilla GNOME desktop. Minor changes to included apps and default accent colour
- No telemetry or data collection without prior consent
- Full support for Turing (GTX 16xx/RTX 20xx) or newer Nvidia graphics cards with a dedicated `apollo-nvidia` image
- [Flatpak](https://flatpak.org) with [Flathub](https://flathub.org) included out of the box as the primary method of installing and using graphical applications
- [Homebrew](https://brew.sh) installed alongside the `fish` shell are preinstalled for a better cli
- [Podman](https://podman.io) and [Distrobox](https://distrobox.it) included out of the box to promote containerised workflows.
    - Docker is also on the image to support devcontainer workflows
- Automatic background updates by default, with easy image-based rollbacks
    - The previous image is kept available as a rollback target by default so you're never left with a broken computer
    - Beyond that, up to 90 days of images are stored on GHCR, giving additional flexibility for rollbacks
- Focus on "it just works" over trying to make everything super feature-packed and customisable