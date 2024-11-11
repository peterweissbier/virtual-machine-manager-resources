## [How to install KVM on Linux](https://sysguides.com/install-kvm-on-linux)
---
## [How to install a Windows 11 Virtual Machine on KVM](https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm)
---
## [single gpu passthrough github guide](https://github.com/QaidVoid/Complete-Single-GPU-Passthrough)

## enable TPM v2.0 support

install the package swtpm

---
## What to do if the `default` network interface is not listed

   * If `virsh net-list` is not listing any network interface just reinitialize it with,
   
         sudo virsh net-define /usr/share/libvirt/networks/default.xml
   
   * Then just `autostart` it like so,
   
         sudo virsh net-autostart default 

---
## Reference:

Original guide - http://wood1978.dyndns.org/~wood/wordpress/2013/07/22/arch-linux-setup-kvm-with-virt-manager-gui/comment-page-1/
 
KVM @ Arch Wiki - https://wiki.archlinux.org/index.php/KVM

libvirt @ Arch Wiki - https://wiki.archlinux.org/index.php/Libvirt

QEMU @ Arch Wiki - https://wiki.archlinux.org/index.php/QEMU

Network Interface Status - http://ask.xmodulo.com/network-default-is-not-active.html

Network Interface Troubleshooting - https://blog.programster.org/kvm-missing-default-network

Networking libvirt wiki - https://wiki.libvirt.org/page/Networking#NAT_forwarding_.28aka_.22virtual_networks.22.29

Fedora Wiki - Windows Virtio Drivers - https://stg.fedoraproject.org/wiki/Windows_Virtio_Drivers

Extend disk size Windows partition KVM QEMU VM - https://www.randomhacks.co.uk/how-to-extend-increase-a-windows-partition-on-kvm-qemu-vm/

Increasing a KVM machine disk space - https://serverfault.com/questions/324281/how-do-you-increase-a-kvm-guests-disk-space

Fixing `Cannot access storage file, Permission denied Error in KVM Libvirt` - https://ostechnix.com/solved-cannot-access-storage-file-permission-denied-error-in-kvm-libvirt/
