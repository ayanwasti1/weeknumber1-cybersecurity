# weeknumber1-cybersecurity
First cyber security setup
# Kali Linux VirtualBox Setup

## Introduction

This project involved installing Kali Linux on Oracle VirtualBox using Windows 11. The aim was to create a virtual cybersecurity lab where I could practise networking and learn about penetration testing.

## Installation

I installed 7-Zip to extract the Kali Linux files. I then installed Oracle VirtualBox and downloaded the pre-built Kali Linux virtual machine. I imported the Kali VM into VirtualBox.

## Network Configuration

I created a NAT Network called `Kali-NAT` using the subnet `10.0.0.0/24`. NAT Network allows Kali Linux to communicate with the internet through the host computer while using a virtual network.

## IP Configuration

The required Kali Linux IP address is `10.0.0.2/24`, with a subnet mask of `255.255.255.0`. The expected gateway is `10.0.0.1`. This gives the virtual machine its own address on the network.

## Clipboard and Shared Folder

I configured the VirtualBox clipboard and drag-and-drop settings to Bidirectional so files and text can be transferred between Windows and Kali Linux. I also configured a shared folder called `downloads` to make transferring files easier.

## Errors and Troubleshooting

**1. VERR_FILE_NOT_FOUND:** VirtualBox could not find the Kali virtual hard disk (`.vdi`) because it was looking in a temporary folder. I located the `.vbox` and `.vdi` files, placed them in a permanent folder and registered the virtual machine again.

**2. GRUB Rescue Error:** Kali displayed an error saying `/boot/grub/i386-pc/normal.mod` could not be found. This prevented Kali from booting normally. I investigated the virtual disk and partition, and eventually managed to get Kali Linux working again.

**3. Unknown Command – ip:** When I initially entered the `ip` command, Kali did not recognise it. This was because I was initially at the GRUB rescue screen rather than inside the Kali Linux terminal. The command must be executed after Kali has successfully booted.

## Conclusion

This project helped me learn how to install Kali Linux, configure virtual networking, understand IP addressing and troubleshoot common VirtualBox and booting problems. It also gave me practical experience setting up a basic cybersecurity lab.



