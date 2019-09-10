# Image Analysis with Deep Learning

[Taylor Arnold](https://statsmaths.github.io), Assistant Professor of Statistics, [@statsmaths](https://twitter.com/statsmaths)

[Lauren Tilton](https://laurentilton.com), Assistant Professor of Digital Humanities, [@nolauren](https://twitter.com/nolauren)

This repository contains notes, code, and data for our HILT 2019 workshop,
which runs from 3-7 June on the campus of IUPUI in Indianapolis, IN. Feel
free to use/share/adopt these notes for other courses.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a> This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

---

## Code of Conduct

Our workshop is dedicated to providing a harassment-free experience
for everyone. We do not tolerate harassment of participants in any form.
If someone makes you or anyone else feel unsafe or unwelcome, please report it as
soon as possible. Harassment and other code of conduct violations reduce the value
of our event for everyone. We want you to be happy at our event. People like you
make our event a better place.

In order for this tutorial to be successful, we ask that participants take note
of the following guidelines throughout the session:

- This is an interactive workshop, and we expect everyone to, as best as possible,
follow along with the tutorial.
- At the same time, please stay at the same point with us in the tutorial. If you are
finished with a section ahead of time, you are more than welcome to hack away at our
code. We find that staying together through the tutorial works best for everyone
involved.
- Please only drive your computer. You are more than welcome to explain to your neighbors
what is going on in their notebook, but we want everyone to feel comfortable working
with the code themselves.


## Community Guidelines
- Being open minded including leaving room for exploration and creativity.
- Generous listening.
- Make sure to clearly state terms and meanings.
- Questions always encouraged!
- Respectful of the time that it takes to learn different technologies/concepts.
- Active listening.
- Provide help when/if asked.
- Aware of the space that we are in and how sound travles.
- Side conversations are great over coffee!
- Offer the benefit of the doubt toward others.
- Amplifying ideas while giving credit.
- Leave space for everyone to participate.
- Be mindful of where the group activity is going.
- Being patient and flexible in order to understand where everyone is coming from.
- Take responsibility for the effects of our actions and words, even if they were unintended.


## Description

Image Analysis with Deep Learning will examine methods for image analysis
at scale. Tasks covered include color analysis, object detection, facial
recognition, image similarity, and image clustering. The course will work
a variety of visual culture including art, photography, and moving images
to ask:

- How can we identify similar works of art using image analysis?
- How can we identify objects in 100,000 photographs?
- How can we track character’s movements in a sit-com?
- How has color in film changed over time?

While the course will introduce several out-of-the-box tools, the main
focus will be on deep learning techniques with Python. No prior programming
experience is required.

## Goals

There are many reasons that humanists might engage in image analysis.
We often characterize these into three categories:

- **Browse/ Exploration**: Using image analysis to open up exploration of a series of images.
- **Domain Specific Analysis**: Analyzing a feature or set of features in order to answer a
domain specific set of questions (ex. use of color in Film Studies)
- **Critical Data Studies**: Many of the applications of large-scale data analysis and
algorithmic decision making involve the usage of image analysis.

If you have any further questions or concerns, please let us know!

## Software

We will be using the Python programming language for the workshop, as well as
several third-party packages. All of it is free and open source. Here is the
link to the Anaconda version of Python that we suggest you use:

- [Anaconda Python 3.7](https://www.anaconda.com/)

We will help you set-up these libraries in the workshop, though please make sure
your operating system is up-to-date (in particular, you will need macOS 10.13 or
10.14 for the libraries to work properly). If you have a previous version of
Anaconda, we generally suggest that you start from scratch.

## Schedule — Overview

Our specific pace and topics will adjust given the needs of those in the workshop,
but here is an overview of what we plan to cover each day:

- **Day 1**: introductions; setting up Python; understanding how to organize an image
corpus; understand how images are stored digitally
- **Day 2**: build exploratory plots from simple image features;  machine learning terminology;
linear regression for image classification; penalized regression; applying texture filters;
motivation for deep learning; using well-known computer vision corpora
- **Day 3**: setting up tensorflow, and keras; building deep learning models
from scratch; convolutions; transfer learning; embeddings; use small CV datasets for
datasets from scratch; visualization of wikiart dataset using transfer learning
- **Day 4**: more visualization techniques; the distant viewing toolkit; working
with moving images; face detection

If there is something particular you would like us to show or would like to make
sure that we get to, please let us know as soon as possible.

## Following along at home

If you would like to follow these notes on your own, start by cloning the repository
or downloading the notes as a zip file (see the green "Clone or download button" above).

## Exploring Projects

In a group of 3, explore 1-2 of the projects below and answer the following:

- Identify the aim(s) of the project.
- Identify the types of image analysis used.
- What can one learn from the use of image analysis?
- Could you see the method(s) used being useful for other projects?

Projects:
- Cooper Hewitt: [main site](https://collection.cooperhewitt.org/)
- Film Colors: [main site](https://filmcolors.org/about/)
- Photogrammar Color Space: [main site](http://photogrammar.yale.edu/) and [Color Space Lab](http://photogrammar.yale.edu/labs/colorspace/)
- Vogue: [main site](http://dh.library.yale.edu/projects/vogue/), [slice histograms](http://dh.library.yale.edu/projects/vogue/slice_histograms/), and [covers](http://dh.library.yale.edu/projects/vogue/coveraverages/)

## References

During the workshop, we will construct a bibliography of references for both
technical and conceptual topics that arise.

- Arnold, Taylor, and Lauren Tilton. *Humanities Data in R*. New York: Springer, 2015.
[link](https://link.springer.com/book/10.1007%2F978-3-319-20702-5).
- Arnold, Taylor, and Lauren Tilton. "Distant viewing: analyzing large visual corpora"
*Digital Scholarship in the Humanities*. [link](https://doi.org/10.1093/digitalsh/fqz013)
- Olga Russakovsky, Jia Deng, Hao Su, Jonathan Krause, Sanjeev Satheesh, Sean Ma, Zhiheng Huang,
Andrej Karpathy, Aditya Khosla, Michael Bernstein, Alexander C. Berg and Li Fei-Fei.
"ImageNet Large Scale Visual Recognition Challenge". IJCV, 2015. [link](https://arxiv.org/pdf/1409.0575v1.pdf)
- Wevers, Melvin, and Thomas Smits. "The visual digital turn: Using neural networks to study historical images"
*Digital Scholarship in the Humanities*. [link](https://doi.org/10.1093/llc/fqy085)
