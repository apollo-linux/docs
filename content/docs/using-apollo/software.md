---
title: "Installing Software"
weight: 1
---

# Installing Software {anchor=false}

As an image-based operating system, Apollo is not designed with a system package manager in mind. Instead, we recommend using distro-agnostic packaging formats, in particular Flatpak. 


## Flatpak

Flatpak with the [**Bazaar**](https://usebazaar.org) frontend is our primary way of installing software on Apollo. We use [**Flathub**](https://flathub.org) by default, the Linux app store, in order to provide a large range of up to date applications.

{{< image src="screenshots/bazaar.png" alt="A screenshot of the Bazaar application center on it's default page" title="The Bazaar application center" loading="lazy" >}}

### Flatpak command line

You can also install and manage Flatpak applications from the command line with `flatpak install` and `flatpak remove`:

```bash
# Install apps
flatpak install $app_id
# Remove apps
flatpak remove $app_id
```

## Homebrew

> [!INFO]
> By default, Apollo uses [brew-proxy](https://codeberg.org/HastD/brew-proxy), which provides better security when installing applications and better multi-user support, at the expense of not supporting some brew features fully.

Homebrew (`brew`) is an additional piece of software we include in order to fill in the gaps where Flatpak isn't enough, particularly around command line tools. This is mainly going to be useful for power users and developers.

You can use `brew install` to install software with brew, and `brew remove` to uninstall them:

```bash
# Install apps
brew install $package
# Remove apps
brew remove $package
```

## Distrobox

[**Distrobox**](https://distrobox.it) makes it easy to spin up personalised pet containers of various Linux distributions through the command line. This is useful for running software that can't easily be run through Flatpak or Homebrew. 

Distroboxes can be easily discarded when not needed, and packages are installed seperate from the OS. Distroboxes are a fully mutable environment with full access to distro packaging formats, such as `deb` and `rpm`.

### Creating distroboxes

Non-exhaustive list of examples for creating Distroboxes:

```bash
# Create a generic distrobox container
distrobox create $container_name
# Create a Fedora 44 distrobox container
distrobox create --image fedora:44 $container_name
# Create a Ubuntu 26.04 distrobox container
distrobox create --image ubuntu:26.04 $container_name
# Create an Arch Linux distrobox container
distrobox create --image archlinux:latest $container_name
```

### Reference
- [Flatpak command reference](https://docs.flatpak.org/en/latest/flatpak-command-reference.html)
- [Homebrew website](https://brew.sh/)
- [Distrobox website/documentation](https://distrobox.it/)