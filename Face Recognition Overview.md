# **What is face recognition?**
Face recognition is the ability to look at the digital image of a human and recognize the person just by looking at the face. Humans have a built-in ability 
to recognize other people's faces. From just a few months old, most infants have the ability to recognize familiar faces. But teaching computers to recognize 
faces is a difficult problem that has taken decades of research to solve.

# **Early Days of Face Recognition:**
* Computer scientists have been trying to build face recognition systems nearly as long as computers have existed. 
* The first system to show real promise was created in 1964 by a team led by Woody Bledsoe. 
* The system worked by having an operator measure and locate key points on each person's face like the center of the eyes and the mouth. These measurements were recorded in a database.
* But the real advancement was that they realized that different faces would be rotated in different ways in each photograph, so they had to adjust the 
measurements based on the head rotation in each image. 
* The technology wasn't advanced enough to identify a specific person, but it could filter down a list of possible faces and exclude those that didn't match so that the user only had to manually look at a few possible matches to find the right person.

# **Continual Progress untill the 2000s**
* New techniques were developed in the 1970s through early 2000s that improved the accuracy of the early systems using a wide variety of different statistical 
approaches. Over time, face recognition systems got more accurate but required more and more computer power. 
* But it wasn't until researchers combined neural networks with greatly increased computing power in the mid 2010s that they were able to build very highly 
accurate face recognition systems.
* By reusing the same graphics processing units or GPUs that power the 3D graphics in modern video games, researchers were able to build large neural networks 
that could be trained on millions of images and recognize faces with high accuracy. 
* By 2015, key research papers from Google and Facebook demonstrated how to effectively train face recognition systems using deep learning and millions of 
training images. These newer systems were able to recognize people's faces nearly as well as humans.

# **Face Recognition Now Widely Available**
* Research done on face recognition is being shared openly within the machine learning community and is available for anyone to use. 
* But even if you now how to build a face recognition system, you still need a large data set of images of people to train it. Companies like Facebook and Google already have access to large data sets like this since they have millions of users uploading photos of themselves every day. 
* Researchers outside of these big companies have to work a little bit harder to build their own training data sets from images posted publicly online. 
* But the end result is that face recognition is now available to almost anyone in all kinds of products. 
* Whether you're uploading a picture to a social network, walking into an airport, or looking at an electronic billboard, there's a good chance that face recognition systems are in use.

# **Face Recognition Applications**
Some of the uses of face recognition technology are:
* Identity Verification
* Automatically organizing raw photo libraries by person
* Tracking a specific person
* Counting unique people
* Finding people with similar appearences or doppelganger

# **Face Recognition Tools**
## **Commercial Tools** 
Several large vendors provide face recognition APIs that you can use over the internet for a small fee. They all work similar ways and provide similar features, but they are trained with different data sets. That means that their accuracy may be better or worse, depending on your specific application.
* Amazon Rekognition API <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Face recognition, emotion detection & motion tracking
* Microsoft Azure Face API <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Face recognition, age & gender detection and face similarity matching

While commercial options are great in many cases, they require an internet connection to use, and you have to pay a small fee each time you use them. Also, using those services requires uploading all your face data to a third-party, since the face recognition happens on their computers in the cloud.
## **Open-Source Tools** 
For some applications, it's better to be able to do face recognition without a data connection and without having to share your data with anyone. In these cases, open-source face recognition systems might be a better choice. These systems can run locally on your computer, without any external connections and without sharing any data. Two of the most popular tools are:
* OpenFace <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;created by Brandon Amos at Carnegie Mellon
* Dlib <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;created by Davis King.
