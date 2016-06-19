# nvme-ata-security

ATA defines the ATA Security feature set, more commonly known as the ability to 
set a “hard drive password.” Most modern SSDs use this password to derive an 
encryption key.

NVMe is a relatively new interface to attach SSDs directly to the PCIe bus 
instead of using SATA. This of course means that most ATA features are not 
directly supported, but some drives do support the ATA Security feature set 
through a compatibility layer.

This repository Linux tools to deal with such drives.

## linux/

Linux driver that improves handling of locked NVMe drives.

## mkinitcpio/

mkinitcpio hook to ask for drive passwords during boot.

## user/

Userspace tool to configure and use passwords on such drives.
