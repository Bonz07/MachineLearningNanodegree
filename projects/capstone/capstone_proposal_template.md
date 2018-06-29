# Machine Learning Engineer Nanodegree
## Capstone Proposal

Andrew O'Gorman - June 29, 2018

## Proposal

### Domain Background

For my Capstone project I will be using a deep learning approach to attempt to solve the Humpback Whale Identification project on Kaggle <sup>[1]</sup>. This is a similar image classification challenge to the dog breed classification challenge in the Deep Learning section of the Machine Learning Nanodegree. I have chosen this domain as I care deeply about our oceans and maritime life. I have been fascinated by whales since visiting the Natural History Museum<sup>[2]</sup>, London, as a child with my father and seeing the full skeleton of the blue whale. They are truly magnificent creatures; giants of the ocean and I feel passionately about helping organisations that support and monitor them. This project appeals to me as the work will help contribute to Happy Whale's <sup>[3]</sup> understand of the movement of whales by using machine learning to dramatically increase the efficiency of this identification work. 

Whale tails (referred to as 'Flukes') are like a barcode or fingerprint, with enough information to identify an individual whale. Traditionally, scientists and marine biologists have taken and amassed large numbers of photograpahs of whales and then had to manually attempt to match newly photographed whales with historic images<sup>[4]</sup>. This process is time consuming and prone to a high degree of error, also there are challenges around getting the pictures due to the geographical spread of whales and the amount of time spent underwater. These are some of the reasons why this problem suits a machine learning approach.

Previous work was done at the University of Texas<sup>[5]</sup> in 2003 to identify Humpback and Gray Whales using a patch-matching technique as a follow-up phase to WhaleNet once they specified the fluke type. More recently a team at the University of Catalunya in Barcelona<sup>[6]</sup> used convolutional neural networks to test the feasibility of using deep learning in whale recognition using the NOAA Fisheries dataset. Their paper outlines a successful approach to applying CNNs which I can look to build upon in this capstone project.

I am keen to test my understanding of image recognition machine learning approaches using Deep Learning as there are several additional projects I would like to conduct upon completion of my Nanodegree, therefore I hope this Capstone Project will be the foundation of further work for me in this field.


### Problem Statement

The problem is to use the existing dataset of whale fluke images to build an understanding of each whale's unique characteristics of their tails. By using this understanding we should then be able to take a new picture of a whale fluke and determine whether it matches a previously seen whale or whether it is in fact a new whale not previously seen in our dataset. 

This problem is an image recognition challenge given the unique features of a whale's fluke as seen below:


![Fluke analysis image<sup>[7]</sup>](https://github.com/Bonz07/MachineLearningNanodegree/blob/master/projects/capstone/fluke.jpg "Fluke")


This problem is a good one to solve as understanding and tracking whale populations across the globe will help in several fields including ocean conservation and global climate change. 



### Datasets and Inputs

The dataset I will be using consists of over 25,000 images of whale flukes, with 9851 labelled images in the training set and 15,611 images in the testing set. In total the dataset contains images for 4550 different whales. Each image varies in size (number of pixels), colour, quality (sharpness) and orientation. 

The data was provided by Happy Whale, a citizen science organisation helping to track individual whales throughout the world's oceans. The images were gathered from research institutions and public contributions. The images specifically targeted whale flukes with the aim of being used to help identify the migration patterns of whales over time so as a dataset is ideally suited to the proposed problem.

I will first look to pre-process the data to standardise the size, colour and proportions of all the images. This will allow me to build, train and test a deep learning algorithm to help identify whales within the dataset. The data is already split into training and testing sets, however I will look to further subdivide these as I train the model.



### Solution Statement


I will be using a Deep Learning approach for this image identification problem. Deep Learning makes use of neural networks which aim to mimic how the brain operates with neurons uses to fire pieces of information through a network to produce an output. By using this approach and building complex neural networks, Deep Learning can be more effective at determining the important features in a given image than a human. 

Specifically, I intend to use Convolutional Neural Networks (CNNs) for this problem. I have chosen to use CNNs for several reasons:

-  CNNs maintain spatial information by taking matrices as inputs when compared to traditional Multilayer Perceptrons. This allows us to use fewer weights as some parameters are shared, hence lowering the computational cost and training time.

- CNNs work well across images where there are distortions due to lighting conditions, horizontal/vertical shifts, different poses etc.

- Very good at identifying patterns within images by using filters to find specific groups of pixel groupings that are important.




### Benchmark Model

The benchmark score I will be comparing against was achieved using a technique known as Perceptual hashing (pHash)<sup>[8]</sup>. The pHash algorithm produces a fingerprint for each image which are analogous if features in the images are similar. This technique has been used previously to identify cases of online copyright infringement and also in digital forensics work due to its ability to have a correlation between hashes so similar images can be identified. 

The pHash technique is able to identify which whale IDs the image is most similar to and then submit their 5 most likley matches for each image. This benchmark submission was then measured using the MAP formula below to get a Mean Average Position score of 0.36075.


### Evaluation Metrics

The owners of the Kaggle competition hold a labelled list of the 15,611 testing images which result submissions are compared against. For each image in the test set I will predict up to 5 labels for the whale ID (e.g. **w_1287fbc**), where a whale is not predicted to be one of the existing whales in the training data they will be labelled as **new_whale**. The submissions file will contain a header and have the following format:

    Image,Id
    
    00029b3a.jpg,new_whale w_1287fbc w_98baff9 w_7554f44 w_1eafe46
    
    0003c693.jpg,new_whale w_1287fbc w_98baff9 w_7554f44 w_1eafe46

The submissions are evaluated according to the Mean Average Precision (MAP) as seen below:

    MAP@5 = \frac{1}{U} \sum_{u=1}^{U}  \sum_{k=1}^{min(n,5)} P(k)

Where **U** is the number of images, **P(k)** is the precision at cutoff **k**, and **n** is the number predictions per image.

### Project Design
_(approx. 1 page)_

* theoretical workflow for approaching a solution
* what strategies will you consider employing
* what analysis of the data might be required before being used
* which algorithms will be considered for your implementation
* include small visualisations, pseudocode, or diagrams to aid your descriptions
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?

Preprocessing the data
Splitting the data into training subsets for use in neural net
Models deployed
Tuning models



### Resources

* https://www.kaggle.com/c/whale-categorization-playground
* http://www.nhm.ac.uk/discover/news/2017/july/museum-unveils-hope-the-blue-whale-skeleton.html
* https://happywhale.com/home
* https://www.nationalgeographic.com/adventure/adventure-blog/2016/05/04/whos-that-whale-your-photo-could-help-i-d-a-humpback/
* https://link.springer.com/chapter/10.1007/3-540-45103-X_16
* https://arxiv.org/pdf/1604.05605.pdf
* http://www.alaskahumpbacks.org/matching.html
* https://en.wikipedia.org/wiki/Perceptual_hashing

[1]: https://www.kaggle.com/c/whale-categorization-playground
[2]: http://www.nhm.ac.uk/discover/news/2017/july/museum-unveils-hope-the-blue-whale-skeleton.html
[3]: https://happywhale.com/home
[4]: https://www.nationalgeographic.com/adventure/adventure-blog/2016/05/04/whos-that-whale-your-photo-could-help-i-d-a-humpback/
[5]: https://link.springer.com/chapter/10.1007/3-540-45103-X_16
[6]: https://arxiv.org/pdf/1604.05605.pdf
[7]: http://www.alaskahumpbacks.org/matching.html
[8]: https://en.wikipedia.org/wiki/Perceptual_hashing

-----------

