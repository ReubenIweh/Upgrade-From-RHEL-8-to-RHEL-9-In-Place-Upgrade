# Upgrade-From-RHEL-8-to-RHEL-9-In-Place-Upgrade
**This project documents the process of upgrading a Red Hat Enterprise Linux 8 (RHEL8) system to RHEL9 using the leapp utility**

**RHEL 8 → RHEL 9 Upgrade Workflow**

- Install Leapp 
- Run leapp preupgrade
- Resolve Inhibitors
- Loop back to re-run preupgrade until clear
- Run leapp upgrade
- Reboot

  **Table of Content**
- [Planning And Prerequisites](#planning-and-prerequisites)
- [Pre Upgrade Preparation](#pre-upgrade-preparation)
- [Upgrade Execution](#upgrade-execution)
- [Post Upgrade Verification](#post-upgrade-verification)
- [Troubleshooting](#Troubleshooting)
- [Leap utility documentation](#leap-utility-documentation)


## Planning And Prerequisites

- RHEL 8.6 – 8.10 system
- Root or sudo privileges
- Active Red Hat subscription
- Stable network connection
- At least 2 GB free space in `/var` for leapp data

## Pre Upgrade Preparation

Backup your system using tar, rsync, or snapshot depending on the platform you are using 

- Ensure repositories are correct

`subscription-manager status`

`subscription-manager repos --enable rhel-8-for-x86_64-baseos-rpms`

`subscription-manager repos --enable rhel-8-for-x86_64-appstream-rpms`
