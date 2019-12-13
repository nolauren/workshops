# Image Analysis

[Lauren Tilton](https://laurentilton.com), Assistant Professor of Digital Humanities, [@nolauren](https://twitter.com/nolauren)

This repository contains notes, code, and data for the NYU Abu Dhabi 2020 workshop,
which runs from 19-22 January on the campus of New York University in Abu Dhabi. The notes are made in collaboration with Taylor Arnold (github.com/statsmaths and @statsmaths), co-director of the Distant Viewing Lab. Feel
free to use/share/adopt these notes for other courses with proper citation. For more information on the Winter Instutue, visit https://wp.nyu.edu/widh/.

Citation: Taylor Arnold and Lauren Tilton. "Image Analysis." NYU Abu Dhabi Digitial Humanities Winter Institute. January 2020. 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a> This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

---

## Description

How can we use digital methods to analyze images such as films, manuscripts, paintings, and photographs? 
This workshop will explore how computers view images and methods for analysis including color, 
image similarity, and feature detection such as faces and objects. 
The workshop will use out-of-the-box toolkits and programming in R; 
it is designed for participants with no programming experience.

## Goals
- Possibilites for humanistic inquiry with image analysis 
- Developing familiarity with programming languages and EDA
- How to structure data for image analysis
- Understand how computers "process" images
- Begin building a methodological toolkit (i.e. feature extraction) for image analysis
- Introduce the concept of Distant Viewing

## Schedule — Overview

Our specific pace and topics will adjust given the needs of those in the workshop,
but here is an overview of what we plan to cover each day:


| Day        |  Time           | #  | Topics  |
| ------------- |:-------------:| -----:|-----:|
| Sunday, Jan 19     | 	1400-1630 | 1|  set-up - introductions, community guidelines, setting up R, setting up an image corpora |
| Monday, Jan 20     | 	1000-1230      |   2| EDA and graphics,  what is a digital image? |
| Monday, Jan 20 | 	1400-1600   |    3 |   color (hsv, brightness), EDA |
| Tuesday, Jan 21 | 	1000-1230  |    4 |  features (facial recognition; objects),  embeddings|
| Tuesday, Jan 21 | 	1400-1600  |   5 | exploring with case studies|
| Wednesday, Jan 22 | 	1400-1600  |   6 | distant viewing |

### Session 1 (Sunday)

- Introductions and Course Overview [30 minutes]
- Commmunity Guidelines [30 minutes]
- Install and Introduction to R (notes01.Rmd) [1 hour]
- What kind of data? ([Google Slides](https://docs.google.com/presentation/d/17YiuMOiuzEIq7Urw8XypAI0ErUp5PLIHEZ6UpKjtRd8/edit?usp=sharing))
- What can I do?! Ideas for Image Analysis (Google Slides)

### Session 2 (Monday)
- Grapics with R (notes02.md)
- What is an image to a computer? (Google Slides)
- A Short Introduction to Pixels and Images (Google Slides)
- Reading an image with R (notes03a.Rmd)

### Session 3 (Monday)
- Color Theory and Why (Google Slides)
- Color Analysis (notes03b.Rmd)
- What and Why EDA? (Google Slides)
- If time: Text Analysis with First Paragraph of Wikipedia (notes04.Rmd)

### Session 4 (Tuesday)
- What is Machine Learning (Google Slides)
- What are Neural Networks? (Google Slides)
- Objects and Embeddings/ Image Similiarity (notes05.Rmd)

### Session 5 (Tuesday)
- Case Study: FSA Color Photographs  (notes06.Rmd)
- Pairing Up: FSA B&W Photographs or WikiArt  (notes07.Rmd or notes08.Rmd)

### Session 6 (Wednesday)
- Distant Viewing (Google Slides)
- Case Study: Sit-Coms (notes09.Rmd)
- Reflection

## Community Expectations
We will create our expectations together. 


## Following along at home

If you would like to follow these notes on your own, start by cloning the repository
or downloading the notes as a zip file (see the green "Clone or download button" above).


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



## Software

We will be using the R and Python programming language for the workshop, as well as
several third-party packages. All of it is free and open source. Here is the
link to the Anaconda version of Python that we suggest you use:

- [Anaconda Python 3.7](https://www.anaconda.com/)

We will help you set-up these libraries in the workshop, though please make sure
your operating system is up-to-date (in particular, you will need macOS 10.13 or
10.14 for the libraries to work properly). If you have a previous version of
Anaconda, we generally suggest that you start from scratch.

