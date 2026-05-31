---
title: "System Administration"
weight: 2
---

# System Administration {anchor=false}

## Managing Automatic Updates 

Automatic updates are the intended way to use Apollo. We use automatic updates by default so users always get the latest bug and security fixes as well as new features. 

If you need to pause system updates, e.g., due to a regression, you can also pin your system image to a specific date within the last 90 days like such:

```bash
# replace $image and $tag with your currently booted image and tag (e.g. apollo:latest)
# if you're not sure what image and tag you're running, run sudo bootc status first
# replace $date with the format YYYYMMDD (e.g. 20260519) 
sudo bootc switch ghcr.io/apollo-linux/$image:$tag.$date
```

Nontheless, if you still want to disable them you can run the following:
```bash
ajust toggle-automatic-updates
```

When filing bug reports or asking support, please make sure your issue is reproducible on the latest version of Apollo, as the issue may have been fixed in an update.