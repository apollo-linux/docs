---
title: "Frequently Asked Questions"
weight: 2
---

# Frequently Asked Questions {anchor=false}

## Who is Apollo for?

Apollo is designed to be a general purpose operating system for everyone, and is especially suited for those wanting a general day to day operating system and developers running containerised workloads. Gaming is also fully possible on Apollo, even though it's not the primary focus.

## How do I install software?

We use Flatpak for GUI applications, homebrew for CLI applications, and Distrobox for containerised distro packages where they're needed. See [Installing Software](/docs/using-apollo/software) for more information.

## Does Apollo support my Nvidia card?

Apollo fully supports Turing or newer Nvidia cards, which includes the GTX 16xx and RTX 20xx cards. Drivers for these images are included with the `apollo-nvidia` image which includes the proprietary drivers needed for the best performance. 

Pascal and older cards will work with the regular `apollo` image, however these images only support the open source drivers, which typically have worse performance and we cannot guarantee the best experience for these users. 

Simply download the Nvidia ISO to install Apollo with the Nvidia drivers. If you switch from AMD to Nvidia graphics, or vice versa, it's recommended to also [switch to the appropriate image for your GPU](/docs/using-apollo/apollo-images/#rebasing-between-apollo-images).
