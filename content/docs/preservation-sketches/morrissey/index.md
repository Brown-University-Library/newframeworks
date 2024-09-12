---
weight: 41
title: "My Name is Captain, Captain, by Judd Morrissey and Lori Talley"
description: ""
icon: "article"
date: "2023-10-24T14:30:40-04:00"
lastmod: "2023-10-24T14:30:40-04:00"
draft: false
toc: false
---

{{< figure src="captain.jpg" alt="A visual representation with overlapping circles and a grid pattern" width="600" class="me-3 figure float-start" caption="Stills from the hypermedia work, *My Name is Captain, Captain*." >}}

Preservation lead: Cody Carvel

### Our Preservation Approach

Judd Morrissey (Brown MFA ’02) is an artist who, when he came to Brown for graduate school was an already,  wide-ranging, innovative writer that led him to produce, with Lori Talley, the extraordinary – especially for its time – [*My Name is Captain, Captain*](https://www.eastgate.com/catalog/Captain.html). While we are able to speak with Talley in creating this preservation framework, we largely worked with Morrissey due to the restrictions of the grant. In exploring *My Name is Captain, Captain*, which was authored using a very early version of Flash with ActionScript 1.0 that reached its end of life, the project team found the work difficult to experience, not because of its form or content but because the technology that helped realize this artistic vision reached its end of life and is no longer supported. 

With Morrissey, the project team  selected this work because of its importance but also because there are several other highly canonical works built with similar technology, and so the model here might be reproducible enough to preserve other important works (e.g. such as Shelley Jackson’s *Patchwork Girl*). First, the project team received the work as a hybrid CD-ROM authored to contain a partition (HFS STD) usable on Macintosh computers (of the early 2000s), and a partition of the same content built to mount and run on Windows. The CD-ROM contained a Flash executable projector that allowed users to interact with text, images, and animations that unveiled a poetic narrative that could be experienced in a wide variety of sequences and contained elements that yielded new pages and formats that might not be discovered or rediscovered even after reading the work over and over again. The system requirements listed on the CD jewel case note that the work will run on Apple’s System 7 or later and Windows 95 or later. Could the early Flash content run on a modern PC? 

Adobe ended support for Flash on December 31, 2020; had *My Name is Captain, Captain* been created with a version of Flash closer to the product’s end of life, a system for updating the code using a handful of tools built to help prepare for Flash’s discontinuation may have been possible to make use of.[1] The code used to create *My Name is Captain, Captain*, however, was authored in an early version of Flash for which conversions of its components was non-trivial. After inserting the CD into a laptop’s optical drive, running macOS 13, Carvel discovered the CD’s Mac partition was formatted in a now deprecated file system (HFS Standard) and would not mount in the current, up-to-date macOS.  The Windows partition on the CD was a more ubiquitous ISO 9660 disk image format, which opened without issue in Windows 11. In fact, the Windows Flash files opened and ran without issue on Windows 11,Windows 7, and Windows XP. Disappointingly, every version of macOS that was configured to mount the archaic HFS file system failed to recognize the Flash Projector files built for Mac systems as executable. Some of the CD's SWF-based Flash files would launch a version of Flash Player if the Mac happened to have one installed. Otherwise, the Mac partition of this CD would be for almost all Mac users, unusable.

Morrissey’s work runs without issue on x86 computers running Windows XP, and  therefore we had no trouble using open-source virtualization application, Oracle VirtualBox installed on a modern Intel-compatible x86 computer to install Windows XP as a Virtual Machine (VM) with the contents of the work  on that VM. Assuming a scenario in which a library had a number of software resources all built to run on CPU architecture compatible with current hardware and virtualization software support for these CPUs, an institution could create spaces on site with computers that could run multiple VMs containing multiple applications with antiquated code.
 
The challenge remained: beyond preserving the assets of the work, how can a user in 2024 experience this work as it was intended in a manner that does not require a high-level of expertise around software that has reached its end of life? How can this executable literary work remain usable in its original state for future users without frequent returns by the archivists to alter the source code or dependencies that interpret this code? In short, how can we create a workflow for this and similar materials in our collections that can retain its initial byte-level content into the future while also offering a way or ways to run and experience the material without needing to translate or convert the original data? To achieve a user-experience closest to that of the original work, we were able to deploy *My Name is Captain, Captain* using four separate strategies that depend on emulation, a compatibility layer, and virtualization to render the original code without error. These working versions of Morrissey’s text can be run with:


1. **Emulation-as-a-Service-Infrastructure (EaaSI)**: A cloud-hosted Emulation-as-a-Service Infrastructure (EaaSI) which hosts an instance of Windows XP SP3 and the contents of the Windows Partition of *My Name is Captain Captain*. This version of the text could theoretically be accessed on-campus only or beyond depending on rights and permissions agreements. Multiple users could also access the content individually, simultaneously.

2. **Local open-source Emulation**: A local emulated version of Windows XP SP3 installed using the open-source emulator, QEMU. Here XP is, as above, bundled with the Windows Partition of *My Name is Captain, Captain*. This version of Windows XP was remastered using nLite application for removing non-essential Windows components and creating unattended installers. This version is small enough to run on a USB drive and could be checked out to a patron to run on their own device. 

3. **Hardware Virtualization**: Using free and open-source hardware virtualization application, Virtualbox, we were able to reproduce the implementation of the work. This virtualized version of XP with the contents of *My Name is Captain, Captain* offers an institution a more intuitive set up and could serve as a permanent terminal for the use of the work and perhaps other archaic software for institutions with space available. 

4. **Wine Is Not an Emulator**: A local version that uses the Wine open-source compatibility layer to translate Windows API calls into their best matches on the host OS running WINE. In this case a local directory containing the Windows Partition of *My Name is Captain, Captain* is used by WINE to execute the .exe file responsible for the text.[2]

In the interest of preserving the experience should any of the above interactive deployments become unavailable in the future, the project team also created screencasts of the work and user interactions. The original CD-ROM, its partitions, and their contents were dumped into a RAW format for long-term storage in the Brown Digital Repository alongside documentation of the work and guidance on how to configure the files to run in an emulated environment. Finally, the project team rehoused the original CD-ROM in an archival-grade Polyester CD case for long-term storage.

### Generalizing the Model

There are variety of reasons this preservation model might be useful for other born-digital art. Given the age of this work, it posed a unique challenge to first ensure the work would run as intended, relying on Morrissey’s recollection. Then exploring infrastructures in emulation and virtualization that would enable experiencing the work:

1. **Antiquated code that would be useful to share with users in the cloud.**
	
	The goal of the Emulation-as-a-Service Infrastructure (EaaSI) product by Yale’s Digital Preservation Services Team is to expand and scale the capabilities of the Emulation-as-a-Service software. It is, in short, a portal that enables a user or organization to deploy a cloud-based emulated Operating System. This lowers the barrier to implementing a software sustainability or preservation project by offering an intuitive workflow to create bootable systems–in our case–that have reached their ‘end of life’, and/or are bound to physical hardware that takes up physical space and grows more difficult to maintain over time. 

2. **Maintaining antiquated code in-house.**

	One of the core emulation components that makes EaaSI’s emulation possible is the open-source emulator QEMU. While EaaSI gives institutions a way for users to reach a specific OS via web browser, not all materials can or should be accessible to anyone with a URL. Because QEMU can run on multiple Operating Systems and CPU architectures, building an emulated XP environment using QEMU would offer the same end result as a EaaSI node would provide and give the flexibility to implement the work on a range of modern computers. By remastering the latest version of the Windows XP (SP3) installation media to occupy approximately 300MB installed, thus creating a portable version of Windows bundled with QEMU. This could be stored on a portable storage device (USB Flash Drive or other external drive) and cataloged to loan within the library in a manner implemented by special collections divisions. While this method requires a more hands-on approach to achieve its ends, because QEMU works using the same commands whether on macOS, Linux, or Windows, the process for creating a usable, emulated environment is mostly identical regardless of the OS one uses to perform the task. 

3. **Dedicating a modern computer or computers to running antiquated code, or perhaps a variety of antiquated applications built for a variety of platforms.** 

	Moving away from emulation-based solutions, we also felt it worthwhile to explore a Virtualization-based approach to reviving Morrissey’s work. The differences between emulation and virtualization can be viewed in terms of how each method achieves its goals and the costs and benefits for each. The common view of these technologies might be reduced to these general ideas:

	* Emulation is seen as suited for executing software designed for completely distinct hardware platforms (for example, playing console games on personal computers) or for operating outdated applications on contemporary systems, but prone to bottlenecks in speed due to the necessity of extra processing for translating non-native code.
 
	* Virtualization is well-suited for enhancing server efficiency, conducting tests across various operating systems on a single device, or engaging in cloud computing practices where scalability and precise resource distribution are essential, but virtualization tends to require specific hardware, and is therefore less versatile. 

4. **If the respective institution is dependent upon WINE, an open-source ‘compatibility layer’ application, and other respective legacy applications, and has staff that are comfortable with this application, use the command line.**

	To further complicate the conversation around emulation and virtualization, WINE also facilitates the use of (exclusively) Windows applications in non-Windows environments. There is also the important recognition that relying on emulation and virtualization tools create yet another software dependency that will eventually become obsolete.[2,3]

### References
1. Logan D. Adobe Flash Support Ending - Updates and Alternatives to Flash - AWEBCO [Internet]. 2020 [cited 2024 Mar 1]. Available from: https://www.awebco.com/blog/adobe-flash-support-ending/
2. WineHQ [Internet]. [cited 2024 Mar 1]. WineHQ - Run Windows applications on Linux, BSD, Solaris and macOS. Available from: https://www.winehq.org/
3. Espenschied, Dragan; Rechert, Klaus. “Software Preservation After the Internet” [Internet]. 2023 [cited 2024 March 5]. Available from: 
https://hdl.handle.net/2142/121096   
