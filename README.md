## Feature-Engineering-Approach-to-improve-Plant-Species-Classification-From-Leaf-Images
I have done this project along with Apurv Patel, Sravani Subraveti and Jayagn Modh

For identifying various features in a leaf like shape, color and size, the approach is to calculate the accuracy rate for different feature combinations.To implement the idea, we have taken image classification algorithms like Support Vector Machine(SVM), Random Forest(RF),KNearest Neighbours(K-NN)etc., To improve the accuracy rate of the Algorithms in identifying the plant leaf species, we have explored other features of a Leaf.One such feature inclusion is about Hu Moments[8], which are Shape Descriptors of the leaf which is one of the focus of this research project.

Block diagram for HU moments

<img src="https://user-images.githubusercontent.com/55220359/116324190-ab3c1180-a78d-11eb-89da-db9e32949e87.JPG" width="300">

Binary Image of a Leaf

<img src="https://user-images.githubusercontent.com/55220359/116324192-ab3c1180-a78d-11eb-9535-43313f4a1d16.JPG" width="300">

Training of HU moments

<img src="https://user-images.githubusercontent.com/55220359/116324194-ab3c1180-a78d-11eb-9c7a-37b968d5dc8f.JPG" width="300">

Approach:

We implemented the SVM Algorithm in the project in Python 3 Environment. To achieve the accuracy of the leaf image, pre processing of the image is required and following are the steps:
• Conversion of RGB to Grayscale image

• Smoothing image using Guassian filter

• Adaptive image thresholding using Otsu’s thresholding method

• Closing of holes using Morphological Transformation

• Boundary extraction using contours

After the pre-processing of an image, the accuracy rate for each set of features is calculated separately for Shape features, Color Features and Texture Features and recorded the results. Then, we have calculated taking two combinations i.e., Shape and Colour, Shape and texture, Texture and Colour and noted the results Further, we trained the algorithm to take k-sized feature vector where k=5,6,7,.,17 we found every possible combination for a single k i.e., we had 17Ck combinations for each value of k and recorded the results.

Graph for feature Combination

<img src="https://user-images.githubusercontent.com/55220359/116324188-aaa37b00-a78d-11eb-82c5-7e099efbc1ad.JPG" width="300">

<img width="250" alt="Screen Shot 2021-04-27 at 7 33 00 PM" src="https://user-images.githubusercontent.com/55220359/116325146-7b8e0900-a78f-11eb-9506-5ce5fb82dc06.png">

Comparison Graph for Algorithms with and without Hu Moments

<img src="https://user-images.githubusercontent.com/55220359/116324187-aaa37b00-a78d-11eb-8c03-b97855f98c79.JPG" width="300">

After performing the experiments and training the classifier on various combinations of extracted features, we got to know from our analysis that the shape and texture features of leaf proves to be the most contributing features to classify plant species. We also found out that using Hu Moments as shape descriptors instead of the geometrical shape features yield better performance in identifying plant species because of its consideration of pixel intensities which proves to be more effective. From our results, we can deduce that there is still a room for improvement in the plant species classification task by focusing more on feature engineering. Further work can be carried out to introduce more meaningful features based on plant texture, veins and leaf margin that can enable us to train a robust classifier with state-of-the-art performance. Even bigger and more diverse data-sets in this classification task could help us to train models that can generalise well and is effective in real-time leaf pictures.

<img width="323" alt="Screen Shot 2021-04-27 at 7 33 19 PM" src="https://user-images.githubusercontent.com/55220359/116325149-7b8e0900-a78f-11eb-9181-6c46d56d48eb.png">
