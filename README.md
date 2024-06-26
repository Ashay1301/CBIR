# Content Based Imaged Retriveal

The aim of the project is to try out different techniques to perform CBIR. For this project, I implemented sum of squared difference, and histogram intersection as distance metrics between two images. Additionally, I used different types of histograms such as RGB, RG chromaticity, magnitude texture, Gabor and Laws textures. Based on my results, texture histograms combined with color histograms work best.

**Content-based image retrieval system**

The system receives a query image and returns a specified amount of the most similar images (sorted by similarity).


**Steps**

1. Create a **decriptor** to convert an image into vector. Vector is a list of numbers from 0 to 1, represents an HSV histogram of the image.

* *descriptor.h, descriptor.cpp*

2. **Index** a collection of images, using descriptor. Which means that every image in the collection will be converted into a vector and saved in memory (in a file, for example).

* *indexer.h, indexer.cpp*

3. Define a **similarity metric**, which will compute the level of similarity between vectors. I used historam intersection.

* *comparator.h, comparator.cpp*

4. **Search**. Convert image query to a vector and compare it to the other images in collection (saved vectors) using a similarity metric.

* *searcher.h, searcher.cpp*
