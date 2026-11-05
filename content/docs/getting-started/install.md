---
title: "Installation Guide"
weight: 1
---

# Installation Guide {anchor=false}

## Pre-requisites

- A computer that meets the [system requirements](#system-requirements)
- A USB drive (or similar storage device) that is both at least **8GB** and you are fine with erasing
- Any important data is backed up to a safe location, such as the cloud or an external drive (not the same one you're using to install)
- Secure boot should be **disabled** at this time. The specific way to do this will depend on your computer.
- An active internet connection during installation.
- **(Optional, but recommended)**: read through the [frequently asked questions](/docs/getting-started/frequently-asked-questions)

### System Requirements

> [!INFO]
> UEFI and x86_64 are the only hard requirements for Apollo to boot, however this is what we recommend for a smooth and enjoyable experience.

- **UEFI** firmware (any computer from at least the last decade, and likely longer, should have this)
- **SSD** storage with at least 40GB free for Apollo
- An **x86_64** capable processor with at least **2 cores** running at **2GHz or better**
- At least **4GB** of RAM, though we recommend at least **8GB**.
- Modern AMD/Intel graphics, or for Nvidia anything Turing (GTX/16xx or RTX 20xx) or newer using the `apollo-nvidia` image
    - See [the frequently asked questions section](/docs/getting-started/frequently-asked-questions/#does-apollo-support-my-nvidia-card) for more information on Nvidia.

## Making a bootable installer

To start, download the [most recent Apollo ISO available](https://getapollo.dev/downloads) for your graphics vendor. We recommend checking the hash to ensure you have the right, official ISO.

Next, you should write the ISO you downloaded to a USB drive. This should be at least **8GB** in size. We recommend [Balena Etcher](https://etcher.io), though most tools should work fine.

> [!WARNING]
> **Don't use Ventoy**. It is known to be problematic with non-traditional Linux distributions, and it's [heavy reliance on binary blobs](https://github.com/ventoy/Ventoy/issues/3224) means it's security is questionable.

Once you have done this, you can now shutdown your  the installer, you can now restart your computer.

## Booting the installer

You'll need to press a key on the keyboard while your computer is starting up in order to access a boot menu. The specific key depends on the computer, with manufacturer often using the same key across models, but common examples include **Escape**, **Delete**, **F9**, and **F11**. This may also be displayed on screen, or you might be able to find it through your preferred search engine.

Select your USB drive when prompted, and then select **Apollo Live ISO** when prompted. If this menu does not show up, then you should try repeating the above steps again.

> [!TIP]
> If the installer boots to a black screen, you can try booting with the **Basic Graphics Mode**. This disables graphics drivers, providing basic graphics until you install the OS.

If all goes correctly, you'll be met with the Apollo desktop and the following window:

{{< image src="screenshots/eleven.png" alt="A screenshot of an Apollo system running bootc status" title="A screenshot of the Apollo installer asking the user to try it or install it." loading="lazy" >}}

## Make sure Apollo works

Your computer will start up to a live environment. This allows you to test the functionality of your computer running Apollo. You should use this opportunity to make sure everything works as intended, such as sound, display (unless you are using the Basic Graphics Mode), network, input peripherals, etc. 

## Install Apollo

When you are ready to install Apollo, open the installer and then follow the instructions. If you closed it in the previous step, open the **Overview** either with the indicator at the top-left of your screen or with the Super Key and launch the application titled "**Install Apollo**". You will then be at the same screen you saw at the end of [Booting the installer](#booting-the-installer).

Select the drive you want to install Apollo to, and click **Install**. This will take around 5-10 minutes depending on your hardware. When the install is completed, you can then reboot again.

## Set the boot order (optional)

If you are dual booting with another operating system such as Windows, you may want to set Apollo to boot first. You should press your computer's BIOS key to access the system setup, and set the boot order in there. Once again, the specific key to press will depend on the computer.

Some BIOS manufacturers may change it automatically, you can also set this to your old operating system if you'd like to continue using that.

## Complete the Initial Setup

When you first install Apollo, you will be greeted with the initial setup. You will be asked to setup some basic system settings, such as your time zone and language, and will create a user account at this stage. Simply follow the instructions on your computer.

## Post-installation

At this point you have successfully installed Apollo to your computer and set it up to be used. We recommend restoring your files from your backups and [installing some software](/docs/using-apollo/software) to get started. Have fun and enjoy!