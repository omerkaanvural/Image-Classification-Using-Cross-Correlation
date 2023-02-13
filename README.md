# Image-Classification-Using-Cross-Correlation

Approach

1- Upload image datasets and check their shapes.

2- Implement ‘Normalised Cross Correlation’. The basic principle of cross-correlation is to measure the similarity in shape between two signals. Our two signals are images in here.

3- A function implemented for template matching. Our sample signals and template signals’ shapes are different. So wee need to overlap images as bigger image shape to get best matching score one to one condition.

4- Two function implemented as get_samples and get_templates to fetch images’ paths to reach easily in main functions.

5- ‘classify’ method is implemented which contains the all essential operations. In this method I read the images from above functions using their references, convert the images grayscale format (don’t need r,g,b layers to measure ‘frame’ correlation), loop the templates for each sample and measure the ncc score, assign a letter by best score and result as predicted.

6- Then the same process is applied using HOG instead of Normalised Cross Correlation. Only differences is euclidian distance is used between computed hog vectors to get similarity value.

Normalised cross correlation accuracy: ~ %9.1

HOG accuracy: ~ %8
