# enabling UEFI support for BIOS

https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF#
https://github.com/tianocore/tianocore.github.io/wiki/OVMF

## extensive installation guide for windows 11
https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm#0-1-configure-windows-11-virtual-hardware

---
  
## How to extend / increase a Windows Partition on KVM QEMU VM

We have a Windows 7 VM running on Ubuntu KVM. I needed to give the Windows 7 machine more disk space. This turns out to be really easy (when you know how).

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
