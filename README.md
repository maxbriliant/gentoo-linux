<h1><span class="mw-headline" id="Downloading">Downloading Gentoo</span></h1>
<h2><span class="mw-headline" id="Introduction">Introduction</span></h2>
<h3><span class="mw-headline" id="Welcome">Welcome</span></h3>
<p>First of all, welcome to Gentoo! You are about to enter the world of choices and performance. Gentoo is all about choices. When installing Gentoo, this is made clear several times - users can choose how much they want to compile themselves, how to install Gentoo, what system logger to use, etc.
</p><p>Gentoo is a fast, modern meta-distribution with a clean and flexible design. It is built on an ecosystem of free software and does not hide what is beneath the hood from its users. Portage, the package maintenance system which Gentoo uses, is written in Python, meaning the user can easily view and modify the source code. Gentoo's packaging system uses source code (although support for pre-compiled packages is included too) and configuring Gentoo happens through regular text files. In other words, openness everywhere.
</p><p>It is very important that everyone understands that choices are what makes Gentoo run. We try not to force users into anything they do not like. If anyone believes otherwise, please <a rel="nofollow" class="external text" href="https://bugs.gentoo.org">bug report</a> it.
</p>
<h3><span class="mw-headline" id="How_the_installation_is_structured">How the installation is structured</span></h3>
<p>The Gentoo Installation can be seen as a 10-step procedure, corresponding to the next set of chapters. Each step results in a certain state:
</p>
<table class="table table-condensed table-striped">

<tbody><tr style="background-color:#dddaec">
<th scope="col" width="15%">Step</th>
<th>Result
</th></tr>
<tr>
<td>1</td>
<td>The user is in a working environment ready to install Gentoo.
</td></tr>
<tr>
<td>2</td>
<td>The Internet connection is ready to install Gentoo.
</td></tr>
<tr>
<td>3</td>
<td>The hard disks are initialized to host the Gentoo installation.
</td></tr>
<tr>
<td>4</td>
<td>The installation environment is prepared and the user is ready to chroot into the new environment.
</td></tr>
<tr>
<td>5</td>
<td>Core packages, which are the same on all Gentoo installations, are installed.
</td></tr>
<tr>
<td>6</td>
<td>The Linux kernel is installed.
</td></tr>
<tr>
<td>7</td>
<td>The user will have configured most of the Gentoo system configuration files.
</td></tr>
<tr>
<td>8</td>
<td>The necessary system tools are installed.
</td></tr>
<tr>
<td>9</td>
<td>The proper boot loader has been installed and configured.
</td></tr>
<tr>
<td>10</td>
<td>The freshly installed Gentoo Linux environment is ready to be explored.
</td></tr></tbody></table>
<p>Whenever a certain choice is presented the handbook will try to explain the pros and cons of each choice. Although the text then continues with a default choice (identified by "Default: " in the title), the other possibilities will be documented as well (marked by "Alternative: " in the title). Do not think that the default is what Gentoo recommends. It is however what Gentoo believes most users will use.
</p><p>Sometimes an optional step can be followed. Such steps are marked as "Optional: " and are therefore not needed to install Gentoo. However, some optional steps are dependent on a previously made decision. The instructions will inform the reader when this happens, both when the decision is made, and right before the optional step is described.
</p>
<h3><span class="mw-headline" id="Installation_options_for_Gentoo">Installation options for Gentoo</span></h3>
<p>Gentoo can be installed in many different ways. It can be downloaded and installed from official Gentoo installation media such as our CDs and DVDs. The installation media can be installed on a USB stick or accessed via a netbooted environment. Alternatively, Gentoo can be installed from non-official media such as an already installed distribution or a non-Gentoo bootable disk (such as Knoppix).
</p><p>This document covers the installation using official Gentoo Installation media or, in certain cases, netbooting.
</p>
<div class="alert alert-info gw-box" style="padding-top: 8px; padding-bottom: 8px;"><strong><i class="fa fa-sticky-note-o fa-rotate-180"></i> Note</strong><br />For help on the other installation approaches, including using non-Gentoo CDs, please read our <a href="/wiki/Installation_alternatives" title="Installation alternatives">Alternative installation guide</a>.</div>
<p>We also provide a <a href="/wiki/Gentoo_installation_tips_and_tricks" title="Gentoo installation tips and tricks">Gentoo installation tips and tricks</a> document that might be useful to read as well.
</p>
<h3><span class="mw-headline" id="Troubles">Troubles</span></h3>
<p>If a problem is found in the installation (or in the installation documentation), please visit our <a rel="nofollow" class="external text" href="https://bugs.gentoo.org">bug tracking system</a> and check if the bug is known. If not, please create a bug report for it so we can take care of it. Do not be afraid of the developers who are assigned to the bugs - they (generally) don't eat people.
</p><p>Note though that, although this document is architecture-specific, it might contain references to other architectures as well. This is due to the fact that large parts of the Gentoo Handbook use installation source text that is shared for all architectures (to avoid duplication of efforts and starvation of development resources). We will try to keep this to a minimum to avoid confusion.
</p><p>If there is some uncertainty whether or not the problem is a user-problem (some error made despite having read the documentation carefully) or a software-problem (some error we made despite having tested the installation/documentation carefully) everybody is welcome to join the <span style="font-family: monospace; font-size: 95%;"><a rel="nofollow" class="external text" href="irc://irc.gentoo.org/gentoo">#gentoo</a></span> channel on irc.freenode.net. Of course, everyone is welcome otherwise too as our chat channel covers the broad Gentoo spectrum.
</p><p>Speaking of which, if there are any additional questions regarding Gentoo, check out the <a href="/wiki/FAQ" title="FAQ">Frequently Asked Questions</a> article. There are also <a rel="nofollow" class="external text" href="https://forums.gentoo.org/viewforum.php?f=40">FAQs</a> on the <a rel="nofollow" class="external text" href="https://forums.gentoo.org">Gentoo Forums</a>.
</p><p><br />
</p><p><br />
</p><p><br />
</p><p><br />
</p><p><br />
</p>
<h2><span class="mw-headline" id="Hardware_requirements">Hardware requirements</span></h2>
<p>Before we start, we first list what hardware requirements are needed to successfully install Gentoo on a amd64 box.
</p><p><br />
</p>
<table class="table table-striped table-condensed" style="text-align: left;">

<caption>AMD64 livedisk hardware requirements
</caption>
<tbody><tr style="background-color:#dddaec;">
<th>
</th>
<th>Minimal CD
</th>
<th>LiveDVD
</th></tr>
<tr>
<th>CPU
</th>
<td scope="row" colspan="2">Any AMD64 CPU or <a href="https://en.wikipedia.org/wiki/X86-64#Intel_64" class="extiw" title="wikipedia:X86-64">EM64T</a> CPU (Core i3, i5, and i7 are EM64T)
</td></tr>
<tr>
<th>Memory
</th>
<td>256 MB
</td>
<td>512 MB
</td></tr>
<tr>
<th>Disk space
</th>
<td colspan="2">2.5 GB (excluding swap space)
</td></tr>
<tr>
<th>Swap space
</th>
<td colspan="2">At least 256 MB
</td></tr></tbody></table>
<p>The <a href="/wiki/Project:AMD64" title="Project:AMD64">AMD64 project</a> is a good place to be for more information about Gentoo's <b><span style="font-family: monospace; font-size: 95%; color: #54487a">amd64</span></b> support.
</p><p><br />
</p>
<h2><span class="mw-headline" id="Gentoo_Linux_installation_media">Gentoo Linux installation media</span></h2>
<h3><span class="mw-headline" id="Minimal_installation_CD">Minimal installation CD</span></h3>
<div class="alert alert-info gw-box" style="padding-top: 8px; padding-bottom: 8px;"><strong><i class="fa fa-sticky-note-o fa-rotate-180"></i> Note</strong><br />As of <b>August 23, 2018</b> the official Minimal CDs are <b>capable</b> of booting in UEFI mode. Previous versions boot in BIOS (MBR) mode only. Readers looking to make their system UEFI bootable must download the latest ISO.</div>
<p>The Gentoo minimal installation CD is a bootable image which contains a self-sustained Gentoo environment. It allows the user to boot Linux from the CD or other installation media. During the boot process the hardware is detected and the appropriate drivers are loaded. The image is maintained by Gentoo developers and allows anyone to install Gentoo if an active Internet connection is available.
</p><p>The Minimal Installation CD is called <span style="font-family: monospace; font-size: 95%">install-amd64-minimal-&lt;release&gt;.iso</span>.
</p>
<h3><span class="mw-headline" id="The_occasional_Gentoo_LiveDVD">The occasional Gentoo LiveDVD</span></h3>
<p>Occasionally, a special DVD is crafted by the Gentoo Ten project which can be used to install Gentoo. The instructions further down this chapter target the Minimal Installation CD so might be a bit different. However, the LiveDVD (or any other bootable Linux environment) supports getting a root prompt by just invoking <span style="font-family: monospace; font-size: 95%; font-weight: bold;" class="tripleclick-separator">sudo su -</span> or <span style="font-family: monospace; font-size: 95%; font-weight: bold;" class="tripleclick-separator">sudo -i</span> in a terminal.
</p>
<h3><span id="What_are_stages_then?"></span><span class="mw-headline" id="What_are_stages_then.3F">What are stages then?</span></h3>
<p>A stage3 tarball is an archive containing a minimal Gentoo environment, suitable to continue the Gentoo installation using the instructions in this manual. Previously, the Gentoo Handbook described the installation using one of three <a href="/wiki/Stage_tarball" title="Stage tarball">stage tarballs</a>. While Gentoo still offers stage1 and stage2 tarballs, the official installation method uses the stage3 tarball. If you are interested in performing a Gentoo installation using a stage1 or stage2 tarball, please read the Gentoo FAQ on <a href="/wiki/FAQ#How_do_I_install_Gentoo_using_a_stage1_or_stage2_tarball.3F" title="FAQ">How do I install Gentoo using a stage1 or stage2 tarball</a>?
</p><p>Stage3 tarballs can be downloaded from <span style="font-family: monospace; font-size: 95%">releases/amd64/autobuilds/</span> on any of the <a rel="nofollow" class="external text" href="https://www.gentoo.org/downloads/mirrors/">official Gentoo mirrors</a>. Stage files update frequently and are not included on the installation images.
</p>
<h2><span class="mw-headline" id="Downloading">Downloading</span></h2>
<h3><span class="mw-headline" id="Obtain_the_media">Obtain the media</span></h3>
<p>The default installation media that Gentoo Linux uses are the <i>minimal installation CDs</i>, which host a bootable, very small Gentoo Linux environment. This environment contains all the right tools to install Gentoo. The CD images themselves can be downloaded from the <a rel="nofollow" class="external text" href="https://www.gentoo.org/downloads/">downloads page</a> (recommended) or by manually browsing to the ISO location on one of the many <a rel="nofollow" class="external text" href="https://www.gentoo.org/downloads/mirrors/">available mirrors</a>.
</p><p>If downloading from a mirror, the minimal installation CDs can be found as follows:
</p>
<ol><li>Go to the <span style="font-family: monospace; font-size: 95%">releases/</span> directory.</li>
<li>Select the directory for the relevant target architecture (such as <b><span style="font-family: monospace; font-size: 95%; color: #54487a">amd64/</span></b>).</li>
<li>Select the <span style="font-family: monospace; font-size: 95%">autobuilds/</span> directory.</li>
<li>For <b><span style="font-family: monospace; font-size: 95%; color: #54487a">amd64</span></b> and <b><span style="font-family: monospace; font-size: 95%; color: #54487a">x86</span></b> architectures select either the <span style="font-family: monospace; font-size: 95%">current-install-amd64-minimal/</span> or <span style="font-family: monospace; font-size: 95%">current-install-x86-minimal/</span> directory (respectively). For all other architectures navigate to the <span style="font-family: monospace; font-size: 95%">current-iso/</span> directory.</li></ol>
<div class="alert alert-info gw-box" style="padding-top: 8px; padding-bottom: 8px;"><strong><i class="fa fa-sticky-note-o fa-rotate-180"></i> Note</strong><br />Some target architectures such as <b><span style="font-family: monospace; font-size: 95%; color: #54487a">arm</span></b>, <b><span style="font-family: monospace; font-size: 95%; color: #54487a">mips</span></b>, and <b><span style="font-family: monospace; font-size: 95%; color: #54487a">s390</span></b> will not have minimal install CDs. At this time the <a href="/wiki/Project:RelEng" title="Project:RelEng">Gentoo Release Engineering project</a> does not support building <span style="font-family: monospace; font-size: 95%">.iso</span> files for these targets.</div>
<p>Inside this location, the installation media file is the file with the <span style="font-family: monospace; font-size: 95%">.iso</span> suffix. For instance, take a look at the following listing:
</p>
