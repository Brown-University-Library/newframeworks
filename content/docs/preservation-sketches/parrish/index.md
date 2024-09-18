---
weight: 21
title: "Gutenberg, dammit, by Allison Parrish"
description: ""
icon: "article"
date: "2023-10-24T14:30:22-04:00"
lastmod: "2023-10-24T14:30:22-04:00"
draft: false
toc: false
---

{{< figure src="gutenberg.gif" alt="stream of lines of poetry" width="600" class="me-3 figure float-start" caption="A stream of the three million lines of poetry in the Gutenberg Poetry Corpus." >}}

Preservation Lead: Cody Carvel 

### Our preservation approach

Allison Parrish's works, [*Gutenberg, dammit*](https://github.com/aparrish/gutenberg-dammit) and *Gutenberg Poetry Corpus* make use of the Gutenberg Project's digitization of texts and, rather than showcase Parrish's personal output from the software she created, aim to enable other users to create electronic writing of their own. Thus, the preservation approach was focused on preserving the code in order to allow others to use that code in the future. The model here focuses on containerization with Docker. Parrish's documentation of these works was so easy to follow that implementing an extra layer of software on top of her programs, initially, felt redundant. And while they don't have many dependencies, containers can help control the versions installed to ensure long term usage. 

Parrish explains that "Gutenberg, dammit is a corpus of every plaintext file in Project Gutenberg (up until June 2016), organized in a consistent fashion, with mostly consistent metadata. The intended purpose of the corpus is to “make it really easy to do creative things with this wonderful and amazing body of freely-available text”. Similarly, her Gutenberg Poetry Corpus software consists of approximately three million lines of poetry extracted from hundreds of books from Project Gutenberg. The corpus is especially suited to applications in creative computational poetic text generation. 

Each of these projects consists of Python-based scripts that interact with Gutenberg data. The project team chose to create Docker images of these repositories and add shell scripts that automate the build and run phases of the containerization process. Users with Docker Desktop installed will be able to run these projects with the appropriate dependencies installed. The project’s dependencies and requirements did not necessitate a particular operating system or cpu architecture, and so anyone with Docker Desktop installed could simply run the helper scripts our project team created and begin interacting with Parrish's works. Because Docker Desktop is available for free on macOS, Windows, and Linux, a majority of users will be able to make use of these projects for their own creative endeavors. While we believe that the use of containers for these two works simplifies their deployment, especially with regard to the use of specific versions of Python, Jupyterlab, and their dependent modules across operating systems, there was some reticence in promoting Docker Desktop as the primary application for running these containers because it is not fully open-source. Its installer and application interface, however, lower the barrier for most non-technical users to begin working with containers, in general, and these works, specifically for the foreseeable future. 

As with a majority of digital-born objects that require preservation, vigilance around the frequency of quality control checks is a must. While the Dockerfiles used to build the images and run the containers are likely to work on future versions of Docker, the Dockerfile standard is itself a versioned product that could drop or change certain commands in our files; Docker could also add commands or switches that improve the way our files run. The project team at the Brown University Library aims to regularly return to test the containerized versions of these projects to ensure they remain functional well into the future in tandem with the files stored in the Library’s digital repository. Recognizing all software is subject to eventual obsolescence, digital preservation by nature is subject to turning tides of software maintenance and abandonment. In a future scenario should Docker Desktop ever become a paid product, our docker-related files should require little effort to work on other container products such as Podman.[^1]

### References
[^1]: Podman Desktop - Containers and Kubernetes | Podman Desktop [Internet]. [cited 2024 Mar 1]. Available from: https://podman-desktop.io/
