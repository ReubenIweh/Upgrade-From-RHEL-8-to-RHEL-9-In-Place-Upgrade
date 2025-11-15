# Upgrade-From-RHEL-8-to-RHEL-9-In-Place-Upgrade
**This project documents the process of upgrading a Red Hat Enterprise Linux 8 (RHEL8) system to RHEL9 using the leapp utility**

**RHEL 8 → RHEL 9 Upgrade Workflow**

1. Install Leapp 2. Run leapp preupgrade 3. Resolve Inhibitors

4. (Loop back to re-run preupgrade until clear) 5. Run leapp upgrade 6. Reboot

7. System boots into Leapp Upgrade Environment 8. Packages are upgraded

9. Reboot again Finish on RHEL 9

  **Table of Content**
- [Planning And Prerequisites](#planning-and-prerequisites)
- [Pre Upgrade Preparation](#pre-upgrade-preparation)
- [Upgrade Execution](#upgrade-execution)
- [Post Upgrade Verification](#post-upgrade-verification)
- [Troubleshooting](#Troubleshooting)
- [Leap utility documentation](#leap-utility-documentation)


## Planning And Prerequisites](#planning-and-prerequisites

- RHEL 8.6 – 8.10 system
- Root or sudo privileges
- Active Red Hat subscription
- Stable network connection
- At least 2 GB free space in `/var` for leapp data

