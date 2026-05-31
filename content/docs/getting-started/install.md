---
title: "Installation Guide"
weight: 1
---

# Installation Guide {anchor=false}

Heavily WIP and incomplete.

## Pre-requisites

- A computer that meets the [system requirements](#system-requirements)
- A big enough storage drive for the install media that you are fine with erasing
- **(Optional, but recommended)**: read through the [frequently asked questions](/docs/getting-started/frequently-asked-questions)
- Any important data is backed up to a safe location

## System Requirements

> [!INFO]
> UEFI and x86_64 are the only hard requirements for Apollo to boot, however this is what we recommend for a smooth and enjoyable experience.

- **UEFI** firmware (any computer from at least the last decade, and likely longer, should have this)
- **SSD** storage with at least 40GB free for Apollo
- An **x86_64** capable processor with at least **2 cores** running at **2GHz or better**
- At least **4GB** of RAM, though we recommend at least **8GB**.
- Modern AMD/Intel graphics, or for Nvidia anything Turing (GTX/16xx or RTX 20xx) or newer using the `apollo-nvidia` image
    - Older Nvidia GPUs may still work with the regular image (`apollo`), however these only ship the open source nouveau drivers which typically have worse performance compared to the proprietary drivers.
