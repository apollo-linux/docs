+++
title = "Update on the recent AUR attacks"
date = 2026-06-14
categories = ['Security Announcements']
tags = ['apollo', 'security']
+++

Hi all,

Our upstream package source, Arch Linux, has recently been hit with a wave of malware attacks in it's user-submitted Arch User Repository. Apollo does not use packages from the AUR at this time and as such is not affected by the recent wave of AUR attacks. We're monitoring the situation closely, in the mean time users should continue to take care to make sure they are using software from trusted sources. 

**Users using the official Apollo images are not knowingly affected by the recent wave of malware.** Containers running Arch, such as those made with `distrobox` should be audited in order to make sure they are unaffected. We recommend deleting and rebuilding the container in the event that affected packages are found.

Custom image maintainers should make sure that any AUR packages in use, if applicable, are not affected and take appropriate actions, including removing affected packages and rebuilding images as appropriate. Arch upstream continues to recommend you manually vet PKGBUILD files before proceeding to install them. Updates on affected packages can be found on [Arch's mailing list](https://lists.archlinux.org/archives/list/aur-general@lists.archlinux.org/thread/FGXPCB3ZVCJIV7FX323SBAX2JHYB7ZS4/#NHRO2RT3VRXHQ7O4WQCPTNGNIOQQQAWX)

We take security seriously and encourage users to report any issues to maintainers.
