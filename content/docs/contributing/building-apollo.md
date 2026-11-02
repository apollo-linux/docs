---
title: "Building Apollo"
weight: 2
---

# Building Apollo {anchor=false}

## Building an image
Apollo is made with mkosi and bootc. You'll need mkosi, python, just, and preferably podman (docker should work too). A hypervisor is also recommended for testing images. 

You can build a bootc-compatible oci archive with mkosi (an Arch-based environment is currently recommended) using the following command:
```bash
just build-bootc $kernel # either kernel-rolling for the latest kernel, or #kernel-lts
```

To load the built oci archive into your *rootless* container storage, you can run the following:
```bash
just load
```

## Testing images in a Virtual Machine

To build a bootable image, follow the following commands:
```bash
sudo just load # the next command requires rootful podman.
sudo just generate-bootable-image
```

Then you can run the `bootable.img` as your boot disk in your preferred hypervisor, such as QEMU, Virt-Manager or GNOME Boxes.
