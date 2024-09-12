---
weight: 61
title: "An Experience, by Todd Anderson "
description: ""
icon: "article"
date: "2023-10-24T14:30:58-04:00"
lastmod: "2023-10-24T14:30:58-04:00"
draft: false
toc: false
---
{{< figure src="an_experience.png" alt="A colorful background with a parchment scroll and a kite" width="600" class="ms-3 figure float-end" caption="A screenshot of the kite character in An Experience.">}}

Preservation Lead: Cody Carvel

### Our Preservation Approach

[*An Experience*](https://chromewebstore.google.com/detail/an-experience/jgedcecajdjoaojfalbickfikinhhnjd?pli=1) is a Google Chrome browser extension authored by Todd Anderson, which offers a user the opportunity to participate in an unfolding, interactive narrative with three characters: a raven called Umberto; a Kite, at first shy, but whose confidence grows the more you interact with them, whose questions about life and language are sometimes simple and usually profound; and Elise, who seems intent on becoming AI salesbot of the year. In our interviews with Anderson on *An Experience*, he let us know that the importance of the work was in part to disrupt how the regular Internet user can spend too much time on the web. *An Experience* disrupts the Internet viewer’s experience by adding narrative elements such as an animated kite that may appear on the user’s screen. Anderson described this meaning to the work in its introduction:

> “What would happen if the internet ‘woke up’? The structure of the internet with it’s vastly interconnected web of trackers, servers and messages already strongly resembles the construction of a human brain, and with so much about consciousness still a mystery how impossible is it to think that someday, not too long from now, parts of the internet might begin to think for themselves? ‘An Experience’ explores that possibility” (*An Experience*)[1]

The need to “wake up” users on the Internet resonates well today. To preserve the work, we used the Conifer project as inspiration for our emulation of an Operating System (OS) along with the Chrome Browser bundled with An Experience.[2] While Conifer's focus is on providing a user the ability to preserve sites and pages with content not generally captured by many web archiving services and tools, our need had less to do with the preservation of a given site or page, and more to do with offering users a means for, well, experiencing, An Experience. Using open-source emulator QEMU and a small, remastered version of Windows 7 installed with Chrome and the An Experience extension.[3] In addition, the preservation model adds Bookmarks, which enable users to easily access different websites, to Chrome which helps users activate some of the features of the extension. We used screen capture software to record the majority of the interactive features unique to “An Experience.”

The BDR offers some emulation capabilities, such as displaying a website or part of a website. However, the BDR is not a full-fledged Operating System Emulator like QEMU. Given this restriction to playback, the underlying assets for An Experience and Chrome Browser Version 124.0.6367.119 with modified bookmark pages were packaged into separate zip files for ingest into the BDR alongside recordings of the extensions, narrative descriptions of the characters, and instructions to run the work via QEMU for Windows and Mac operating systems. 

### Generalizing the model
Browser extensions do not  have a lot of preservation work behind them. One could of course simply save the extension in a digital archival repository, but because our goal was also to present the work in its functioning state, we opted for an open-source emulation strategy that allows a user to run the extension in Chrome as intended. In addition to archiving the extension in a traditional way, we can store the disk image that contains the OS, Chrome, and the extension, along with the QEMU source code because QEMU creates a virtual disk drive to install an OS into. This will allow a user wishing to run the extension the opportunity to do so well into the future.

Digital preservation of this sort requires oversight at regular intervals to ensure the work in question continues to work as intended. Because our team cannot control the external variables and environmental conditions in ways that apply to traditional special collections materials--software updates and hardware releases occur far more frequently than the processes that keep a draft of the Gettysburg Address in readable condition--our team  will need to be vigilant in reproducing the workflows that successfully made Anderson's text work using emulation. All CDS projects have a project charter where project managers denote when to review the project over time so that someone from the Brown University Library regularly checks software and hardware needs at regular intervals. 

A particular area of concern is the ever-changing nature of web design and the rate at which sites and pages change their code, URLs, or disappear altogether. Because Anderson's work is a Chrome extension that depends on certain sites having been coded in the ways he encountered them while building the extension, a major overhaul of sites such as Amazon, Wikipedia, or even the source for advertising networks could result in An Experience not functioning as intended.  If, for some reason, our QEMU-based solution ceases to work on future hardware, we recorded the majority of the interactive features Anderson implemented for An Experience using screen capture software. 

### References
1. Anderson T. An Experience: A Chrome Extension-Based Alternate Reality Game [Internet]. Brown University; 2017 [cited 2024 Mar 1]. Available from: https://doi.org/10.26300/9gss-2j22 
2. Conifer [Internet]. [cited 2024 Feb 20]. Conifer. Available from: https://conifer.rhizome.org
3. QEMU [Internet]. [cited 2024 Mar 1]. Available from: https://www.qemu.org/