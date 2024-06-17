## [https://github.com/joeknock90/Single-GPU-Passthrough](single gpu passthrough)
---
## [more extensive guide](https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm#0-1-configure-windows-11-virtual-hardware)
---
## [install virtio drivers](https://sysguides.com/install-kvm-on-linux#3-04-install-virtio-drivers-for-windows-guests-)
---
## enabling UEFI support for BIOS

https://github.com/tianocore/tianocore.github.io/wiki/OVMF

more information:

https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF

aur package

https://archlinux.org/packages/extra/any/edk2-ovmf/

---
## [kvm installation guide for windows 11](https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm#0-1-configure-windows-11-virtual-hardware)
---
## How to extend/increase a Windows partition

1. Shutdown the VM

        virsh shutdown hostname

2. Increase the qcow2 image

Find the qcow2 file of the VM and take a backup (just in case).

    cp hostname.qcow2 hostname.qcow2.backup
    qemu-img resize hostname.qcow2 +100GB
    
3. Start the VM

        virsh start hostname

4. Extend the partition in Window

Windows has a really good partition management utility built into it. Search for `disk management`
