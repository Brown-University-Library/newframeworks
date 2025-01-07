---
weight: 31
title: "ReRites, by David Jhave Johnston "
description: ""
icon: "article"
date: "2023-10-24T14:30:32-04:00"
lastmod: "2023-10-24T14:30:32-04:00"
draft: false
toc: false
---

{{< figure src="ReRites.jpg" alt="A table with text displayed on it" width="600" class="me-3 figure float-start" caption="An image of the *ReRites* exhibit. Photo credit: Anteism Books." >}}

Preservation Leads: Khanh Vo and Ashley Champagne

### Our Preservation Approach

*ReRites* is multimodal poetry created by David Jhave Johnston with Artificial Intelligence. It includes a limited edition box set of twelve poetry books, one book of essays about AI and poetry, exhibit formats with over 120 hours of neural net text generation videos, participatory performances, and installations. Johnston produced one book of poetry per month utilizing neural networks trained on a contemporary poetry corpus to generate source texts which were then edited into the *ReRites* poems. The booksets and source texts were then curated into an exhibit. Other portions of the work included user experience with AI poetry (users generating new poetry by reading the generated text at the speed of which it is generated).

This model encapsulates not only the written word but also incorporates digital elements—code, videos, exhibit installations, and interactive components. Each facet of the work contributes to a multi-dimensional expression of human-AI made poetry meant to be viewed together to offer readers and participants a holistic and immersive experience. There are five components of *ReRites* that need to be preserved and viewed together:

1. Thirteen physical volumes of poetry and essays
2. The code and preservation of tech documents
3. The reproducibility of the experience
4. Video files that include “sculpting” or “carving” videos and participatory events
5. Exhibition that incorporates the volumes into installations

The simplest approach to preserving this work was to address each component of significance to the artist and how he wanted each piece to interact with each other and the reader. The artist placed greatest emphasis on the reader experience and dynamic interactions of human-AI generated poetry which became the priority in this preservation work. And so the model the project team determined was the best approach was to preserve the content for the long term but also to reimagine how to recreate the experiences the work encourages – such as hosting an AI poetry reading event.

Because the artist did a fantastic job documenting the project in text and video, the New Frameworks team focused on converting the files to plain text, offering context to the plain text separately and storing them in the Brown digital repository for long-term preservation. Of the accompanying documents, including images of the work’s exhibition, the artist wrote a rough chronology of the technology used and a Wikipedia page that gave an overview of the work. Conversion to plain text files was necessary for longevity as it is the simplest way to store information. Virtually all software can read and write plain text files. The format is portable across different platforms, requires a simple interface, and is easy for users to read and write plain text.

The videos included raw AI output compilations, showcase sets from GPT-2, carving videos, and live recordings of events. The video files from the artist were originally uploaded onto Vimeo. The video files were downloaded and incorporated into the BDR via video platform Panopto.

The thirteen volumes were accessioned as reference books and cataloged in the special collections at the John Hay Library. One initial challenge was determining how the books and videos were to be read ideally within the same space. The books are available through a reading room request and cannot be removed from the library and so the work cannot be read together as the artist desired. Thus, the project team linked the multimedia content of the work into the library system and added a note to the bibliography record and back of each volume to inform readers that links and QR codes provide access to accompanying videos and creator narratives in the digital repository.

While the artist viewed the code as a marginal component in this preservation work, he emphasized that the reader's experience and engagement in interacting and working with AI to produce poetry was a valuable component of the work. As the code is treated as secondary, the project team preserved each individual component in its simplest format, made that available in the BDR, and allowed others to draw on that when needed to reproduce the work’s dynamic reader experience—the text to be read as opposed to the text of the author. Without runnable code, however, the reader’s engagement in working with and editing the AI as it produces poetry with the human was no longer possible with Johnston’s code.

The main issue was restoring Johnston’s code to an executable state. This is partly accomplishable through docker containerization. However, the repositories are from 2017, taken from three corporate machine-learning libraries: TensorFlow (Google), PyTorch (Facebook), and AWSD (SalesForce). The use of corporate code is intentional to introduce AI as an alternative perspective that would complicate the commodification of human language against the “authorial beauty” of the individual. "If," Johnston suggests, "[the] corpus of poems can be filtered through an algorithmic intelligence and then converted into a fresh, flowing, infinite field of perpetually blossoming... It's an exquisite gift in some ways, even if it's constituted within the framework of surveillance capitalism."[^1] While specific language models (LMs) like GPT-2 are available, Johnston’s customized code is broken with dependency problems. To reproduce Johnston’s model exactly as it was requires the right combination of old packages and libraries that can run the code on emulatable hardware he was using (i.e., 2016-18 NVIDIA GPU) with code or plugins for the GPU to do training and generation. We decided against this approach because it is not sustainable to continuously rewrite the code every time it breaks. The technology, software, and code will always become antiquated and unavailable.

Rather, we opted to showcase the generated poetry in addition to preserving the code through directories and files that showed what the code created in the BDR. In addition, we reimagined how to create an event inspired by those that Johnston led, where we utilize the large amount of text generated in *ReRites* to train or fine-tune another GenerativeAI GPT-2 through OpenAI that can produce poetry like Johnston’s code once did.[^2] With this approach, each iteration of a LM used will not only produce new poetry but also a new training corpus for the next model, allowing a continuation and evolution of the artist’s original work.

### Generalizing the Model

For multimodal work, the components to be preserved are very specific to this work, from videos to code to the process of editing the text to the production of books to installations and the generation of interaction. Each element requires a different preservation method with the greater task of linking them back into a coherent work where each mode may be accessed simultaneously. Artist intention is a major factor in determining what aspects of a work should be preserved. If the recreation and experience of the work are more vital than the underlying code that creates the work, as it was for *ReRites*, the focus becomes on capturing the essence and spirit of the work through documentation saved in its simplest format for longevity and access.

While the original codes may be preserved and made accessible, at the rate at which AI technology and computation move, the code must constantly be recreated and retrained. Thus, by creating an event inspired by Johnston’s work using advances in GenerativeAI, the model encourages others in the future to reimagine how events with human and AI poetry might be recreated with existing technologies.

### References
[^1]: David Jhave Johnston. Second Artist Interview. [Personal interview, 1 November] Zoom; 2022.
[^2]: npm [Internet]. 2023 [cited 2024 Mar 1]. jquery. Available from: https://www.npmjs.com/package/jquery
