<h1>Gentoo Linux installation 
Welcome</h1>

First of all, welcome to Gentoo! You are about to enter the world of choices and performance. Gentoo is all about choices. When installing Gentoo, this is made clear several times - users can choose how much they want to compile themselves, how to install Gentoo, what system logger to use, etc.

Gentoo is a fast, modern meta-distribution with a clean and flexible design. It is built on an ecosystem of free software and does not hide what is beneath the hood from its users. Portage, the package maintenance system which Gentoo uses, is written in Python, meaning the user can easily view and modify the source code. Gentoo's packaging system uses source code (although support for pre-compiled packages is included too) and configuring Gentoo happens through regular text files. In other words, openness everywhere.

It is very important that everyone understands that choices are what makes Gentoo run. We try not to force users into anything they do not like. If anyone believes otherwise, please bug report it.

How the installation is structured
The Gentoo Installation can be seen as a 10-step procedure, corresponding to the next set of chapters. Each step results in a certain state:

Step	Result
1	The user is in a working environment ready to install Gentoo.
2	The Internet connection is ready to install Gentoo.
3	The hard disks are initialized to host the Gentoo installation.
4	The installation environment is prepared and the user is ready to chroot into the new environment.
5	Core packages, which are the same on all Gentoo installations, are installed.
6	The Linux kernel is installed.
7	The user will have configured most of the Gentoo system configuration files.
8	The necessary system tools are installed.
9	The proper boot loader has been installed and configured.
10	The freshly installed Gentoo Linux environment is ready to be explored.
Whenever a certain choice is presented the handbook will try to explain the pros and cons of each choice. Although the text then continues with a default choice (identified by "Default: " in the title), the other possibilities will be documented as well (marked by "Alternative: " in the title). Do not think that the default is what Gentoo recommends. It is however what Gentoo believes most users will use.

Sometimes an optional step can be followed. Such steps are marked as "Optional: " and are therefore not needed to install Gentoo. However, some optional steps are dependent on a previously made decision. The instructions will inform the reader when this happens, both when the decision is made, and right before the optional step is described.

Installation options for Gentoo
Gentoo can be installed in many different ways. It can be downloaded and installed from official Gentoo installation media such as our CDs and DVDs. The installation media can be installed on a USB stick or accessed via a netbooted environment. Alternatively, Gentoo can be installed from non-official media such as an already installed distribution or a non-Gentoo bootable disk (such as Knoppix).

This document covers the installation using official Gentoo Installation media or, in certain cases, netbooting.

 Note
For help on the other installation approaches, including using non-Gentoo CDs, please read our Alternative installation guide.
We also provide a Gentoo installation tips and tricks document that might be useful to read as well.

Troubles
If a problem is found in the installation (or in the installation documentation), please visit our bug tracking system and check if the bug is known. If not, please create a bug report for it so we can take care of it. Do not be afraid of the developers who are assigned to the bugs - they (generally) don't eat people.

Note though that, although this document is architecture-specific, it might contain references to other architectures as well. This is due to the fact that large parts of the Gentoo Handbook use installation source text that is shared for all architectures (to avoid duplication of efforts and starvation of development resources). We will try to keep this to a minimum to avoid confusion.

If there is some uncertainty whether or not the problem is a user-problem (some error made despite having read the documentation carefully) or a software-problem (some error we made despite having tested the installation/documentation carefully) everybody is welcome to join the #gentoo channel on irc.freenode.net. Of course, everyone is welcome otherwise too as our chat channel covers the broad Gentoo spectrum.

Speaking of which, if there are any additional questions regarding Gentoo, check out the Frequently Asked Questions article. There are also FAQs on the Gentoo Forums.






Hardware requirements
Before we start, we first list what hardware requirements are needed to successfully install Gentoo on a amd64 box.


AMD64 livedisk hardware requirements
Minimal CD	LiveDVD
CPU	Any AMD64 CPU or EM64T CPU (Core i3, i5, and i7 are EM64T)
Memory	256 MB	512 MB
Disk space	2.5 GB (excluding swap space)
Swap space	At least 256 MB
The AMD64 project is a good place to be for more information about Gentoo's amd64 support.


Gentoo Linux installation media
Minimal installation CD
 Note
As of August 23, 2018 the official Minimal CDs are capable of booting in UEFI mode. Previous versions boot in BIOS (MBR) mode only. Readers looking to make their system UEFI bootable must download the latest ISO.
The Gentoo minimal installation CD is a bootable image which contains a self-sustained Gentoo environment. It allows the user to boot Linux from the CD or other installation media. During the boot process the hardware is detected and the appropriate drivers are loaded. The image is maintained by Gentoo developers and allows anyone to install Gentoo if an active Internet connection is available.

The Minimal Installation CD is called install-amd64-minimal-<release>.iso.

The occasional Gentoo LiveDVD
Occasionally, a special DVD is crafted by the Gentoo Ten project which can be used to install Gentoo. The instructions further down this chapter target the Minimal Installation CD so might be a bit different. However, the LiveDVD (or any other bootable Linux environment) supports getting a root prompt by just invoking sudo su - or sudo -i in a terminal.

What are stages then?
A stage3 tarball is an archive containing a minimal Gentoo environment, suitable to continue the Gentoo installation using the instructions in this manual. Previously, the Gentoo Handbook described the installation using one of three stage tarballs. While Gentoo still offers stage1 and stage2 tarballs, the official installation method uses the stage3 tarball. If you are interested in performing a Gentoo installation using a stage1 or stage2 tarball, please read the Gentoo FAQ on How do I install Gentoo using a stage1 or stage2 tarball?

Stage3 tarballs can be downloaded from releases/amd64/autobuilds/ on any of the official Gentoo mirrors. Stage files update frequently and are not included on the installation images.

Downloading
Obtain the media
The default installation media that Gentoo Linux uses are the minimal installation CDs, which host a bootable, very small Gentoo Linux environment. This environment contains all the right tools to install Gentoo. The CD images themselves can be downloaded from the downloads page (recommended) or by manually browsing to the ISO location on one of the many available mirrors.
