---
weight: 51
title: "Forever Gwen Brooks, by Lillian-Yvonne Bertram"
description: ""
icon: "article"
date: "2023-10-24T14:30:51-04:00"
lastmod: "2023-10-24T14:30:51-04:00"
draft: false
toc: false
---

{{< figure src="forever_gwen_brooks.png" alt="A dark background image with three columns of text" width="600" class="me-3 figure float-start" caption="Three side-by-side instantiations of the poems are put together in this image in order to communicate the dynamic nature of *Forever Gwen Brooks*.">}}

Preservation lead: Patrick Rashleigh

### Our Preservation Approach

The reader of *Forever Gwen Brooks* arrives at the webpage viewing a poem inspired by the poet Gwendolyn Brooks. A subsequent visit produces another poem, structurally and tonally similar, but with different word choices and surface details. Every visit (or browser refresh) yields a new poem. Bertram explains, on the project’s about page, that the project began by making a template out of Gwendolyn Brooks’s poem, “An Aspect of Love, Alice in the Ice and Fire” from her 1969 book *RIOT*.[^1] The poem itself is designed to be both “eternal and ephemeral” as no single instance of the generated poem will likely appear again, and yet also instances of the poem go on forever.

The poem generator project is built with JavaScript, HTML, and a CSS static site which are ripe for preservation, except for the code’s dependency on the aging library, jQuery. As a relatively straightforward preservation scenario, we used the jQuery dependency to explore the principle of “Code Resituation,” a term introduced by Deena Engel and Joanna Phillips.[^2] The authors argue that authorship exists not only in the final product (as viewed by a reader), but in the code-text that defines the processes that result in the product. As such, the code behind the work is as worthy of the same level of preservation care as the product of that code. Code Resituation applies the preservation principle of “minimal intervention” (commonly applied to physical artifacts) to computer code. It seeks to “minimize the invasiveness of code migration by targeting only the damaged areas and not recoding the entire artwork [... and] allow the preservation of significant parts of the original code, including its specific coding style and the artist’s original algorithms”.

When we spoke with Bertram in our first interview for the project, they described how computation is a tool that they use to explore the intellectual questions and aesthetic they want to pursue. They noted that preservation approaches are important, and that some of their past work, such as a mobile application called *Moon Slake*, does not run completely and on certain platforms anymore. In working to preserve *Forever Gwen Brooks*, two issues were primary: How should the project team preserve the work in a runnable form, thereby retaining its dynamic nature? How should we minimize modifications to the code as per the principles of “Code Resituation” in order to preserve the code as close to how the author wrote it as possible? 

In order to prepare Forever Gwen Brooks for long-term preservation, our approach aimed to not only remove the dependency on jQuery but also apply the principles of code resituation by seeking to minimize changes to the author’s code. The use of JQuery in the work can be summarized as follows: 

| Original jQuery-based code              | Explanation                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| {{< highlight js >}}$(document).ready(function() { <CODE> }){{< / highlight >}} | Run `<CODE>` once the document has finished loading in the browser.   |
| {{< highlight js >}}$('body').append( <CONTENT> );{{< / highlight >}}       | Place `<CONTENT>` onto the page. This expression is repeated 44 times with different content. |

It is worth noting that both of these functions can be easily rewritten in standards-compliant JavaScript that does not include jQuery or any other third-party libraries. However, in doing so, the code in the file would be significantly altered. The preservation challenge was to introduce the standards-compliant code without significantly modifying the original. jQuery is a fairly expansive library, capable of a wide variety of functions. All that functionality is encapsulated in a javascript object called $, which contains 149 functions, such as $.ajaxStart() and $.dequeue(). We are only interested in the two identified in the code: $().ready() and $().append().

Our solution was to replace the file that contains all the jQuery code with our own version of the jQuery object—one that only contains very simple, preservation-ready, implementations of $().ready() and $().append(). Our “fake jQuery” proxy object would also be called $ and the functions would also be called .ready() and append(), so the original code would not have to be altered in any way.

The files will be stored in the Brown Digital Repository for long term preservation and hosted on a public-facing web server. There are also open-access repositories, such as Zenodo, to hold files if artists are not part of an institution that has a repository. 

Generalizing the model: 
The approach of replacing large third-party libraries with smaller, application-targeted, preservation-oriented replacement proxies can be applied to a variety of situations.

This approach is useful to those who:

- Have a commitment to preserving code in an executable form so that it can be run in the future
- Have a commitment to archiving code in a form as close as possible to the original
- Have access to technical staff that can program
- Have a code base that relies on third party libraries that may not be maintained in the future (or are currently not maintained!), and the use of these libraries is relatively easy to reproduce using standards-compliant code

The approach has limitations, of course, as well. It may not be practical for larger, more complex works that integrate libraries more extensively. It is also worth noting that all code, to some extent, is a product of its time. We may assume that standards-compliant JavaScript from 2024 will run in 2064, but this remains to be seen. 

View the work's preservation collection and documentation in [the Brown Digital Repository](https://repository.library.brown.edu/studio/collections/bdr:hmbqypcc/).

### References
[^1]: Brooks G. RIOT. [cited 2024 Mar 1]. Available from: https://thirdworldpressfoundation.org/products/riot
[^2]: Engel, D, and Phillips J. “Introducing ‘Code Resituation’: Applying the Concept of Minimal Intervention to the Conservation Treatment of Software-based Art.” Electronic Media Review [Internet]. [cited 2024 Feb 20]. Available from: https://resources.culturalheritage.org/emg-review/volume-5-2017-2018/engel-2/
