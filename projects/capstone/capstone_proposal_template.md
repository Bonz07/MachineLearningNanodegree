# Machine Learning Engineer Nanodegree
## Capstone Proposal
Andrew O'Gorman 

June 27, 2018

## Proposal

### Domain Background

For my Capstone prpject I will be using a deep learning approach to attempt to solve the Humpback Whale Identification project on Kaggle <sup>[1]</sup>. This is a similar image classification challenge to the dog breed classification challenge in the Deep Learning section of the Machine Learning Nanodegree. I have chosen this domain as I care deeply about our oceans and maratime life. I have been fascinated by whales since visiting the Natural History Museum<sup>[2]</sup>, London, as a child with my father and seeing the full skeleton of the blue whale. They are truely magnificent creatures, giants of the ocean and I feel passionately about helping organisations that support and monitor them. This project appeals to me as the work will help contribute to HappyWhale's <sup>[3]</sup> understand of the movement of whales by using machine learning to dramatically increse the efficiency of this identification work. 

Whales tails (referred to as 'Flukes') are like a barcode or fingerprint, with enough information to idneitify an individual whale. Traditionally scientist and marine biologists have taken and ammassed large numbers of photogrpahs of whales and then had to manually attempt to match newly photographed whales with historic images<sup>[4]</sup>. This process is time consuming and prone to a high degree of error, also there are challenges around getting the pictures due to the geographical spread of whales and the amount of time spent underwater. These  are some of the reasons why this problem suits a machine learning approach.

Previous work was done at the University of Texas<sup>[5]</sup> in 2003 to identify Humpback and Gray Whales using a patch-mathcing technique as a follow-up phase to WhaleNet once they specified the fluke type. More recently a team at the University of Catalunya, Barelona<sup>[6]</sup> used convolutional nerual networks to test the feasibility of using deep learning in whale recognition using the NOAA Fisheries dataset. This paper outlines a successful approach to applying CNNs which I can look to build upon in this capstone project.

I am keen to test my understanding of image recognition machine learning approaches using Deep Learning as there are several additional projects I would like to conduct upon completion of my Nanodegree. Therefore I hope this Capstone Project will be the foundation of further work for me in this field.


### Problem Statement
_(approx. 1 paragraph)_

The problem is to use the existing dataset of whale fluke images to build an understanding of each whales unique characteristics of their tails. By using this understanding we should then be able to take a new picture of a whale fluke and determine whether it matches a previously seen whale or whether it is a new whale. This problem is an image recognition challenge 



*detailed description of problem to be solved and give one relevant solution
*describe the problem so its quantifiable (maths or logical terms)
*measurable
*replicable (occurs more than once)




### Datasets and Inputs
_(approx. 2-3 paragraphs)_

*what is dataset
*how does it relate to the problem, and why it should be used
*how it was obtained
*characteristics of the dataset
*how the dataset will be used in the project



### Solution Statement
_(approx. 1 paragraph)_

In this section, clearly describe a solution to the problem. The solution should be applicable to the project domain and appropriate for the dataset(s) or input(s) given. Additionally, describe the solution thoroughly such that it is clear that the solution is quantifiable (the solution can be expressed in mathematical or logical terms) , measurable (the solution can be measured by some metric and clearly observed), and replicable (the solution can be reproduced and occurs more than once).

### Benchmark Model
_(approximately 1-2 paragraphs)_

In this section, provide the details for a benchmark model or result that relates to the domain, problem statement, and intended solution. Ideally, the benchmark model or result contextualizes existing methods or known information in the domain and problem given, which could then be objectively compared to the solution. Describe how the benchmark model or result is measurable (can be measured by some metric and clearly observed) with thorough detail.

### Evaluation Metrics
_(approx. 1-2 paragraphs)_

In this section, propose at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model. The evaluation metric(s) you propose should be appropriate given the context of the data, the problem statement, and the intended solution. Describe how the evaluation metric(s) are derived and provide an example of their mathematical representations (if applicable). Complex evaluation metrics should be clearly defined and quantifiable (can be expressed in mathematical or logical terms).

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.

-----------

[1]: https://www.kaggle.com/c/whale-categorization-playground
[2]: http://www.nhm.ac.uk/discover/news/2017/july/museum-unveils-hope-the-blue-whale-skeleton.html
[3]: https://happywhale.com/home
[4]: https://www.nationalgeographic.com/adventure/adventure-blog/2016/05/04/whos-that-whale-your-photo-could-help-i-d-a-humpback/
[5]: https://link.springer.com/chapter/10.1007/3-540-45103-X_16
[6]: https://arxiv.org/pdf/1604.05605.pdf


**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?
