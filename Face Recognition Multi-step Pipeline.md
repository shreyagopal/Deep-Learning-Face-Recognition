# **Face Recognition Multi-step Pipeline**

Recognizing a face is a complicated problem with several steps, but as a human, your brain is hardwired to see faces. In fact, humans are so good at 
recognizing faces, you end up seeing them in everyday objects. Computers are not capable of this kind of high-level generalization, so we have to teach them 
how to do each step in this process separately. In other words, we have to chain together several different machine learning algorithms into a pipeline to 
complete the entire task of face recognition. The steps involved in the pipeline are:<br>

Step 1: Locate & Extract Faces<br>
Step 2: Identify Facial Features<br>
Step 3: Align Faces Using Pose<br>
Step 4: Represent Face as Measurements<br>
Step 5: Compare to Other Faces

## **Step 1: Locate & Extract Faces**
* First, we need to be able to locate faces within a larger image. In this photograph, there's a person standing in front of a background. 
* We need an algorithm that can scan the image and find any faces that appear. It needs to be able to identify the area that contains a face. 
* Once we know where the face is located in the image, we'll extract that area as a new image. This is the only part of the image that will pass to the next 
step of our face recognition pipeline. 

## **Step 2: Identify Facial Features**
* Now we have a face image to work with from the previous step, but we can't compare it directly to other face images. 
* To be able to compare this face image with other faces, we need to be able to understand how the person's head was turned or posed when the photo was taken. 
* A person's face looks different from different angles. If we don't take the person's head position into account, our face recognition system will think that 
the same person is two different people just because the person's head was turned a different way.
* To do this, we'll use a machine learning algorithm that can look at a single face and identify the location of each facial feature within the face. We'll 
look for the position of the eyes, nose, and mouth. 
* We'll pass the face image and the location of each facial feature to the next step of our face recognition pipeline. 

## **Step 3: Align Faces Using Pose**
* The next step is to try to correct for the position or pose of the person's head. We know the position of each facial feature. 
* Each person's face is unique, but we can assume that all faces follow roughly the same structure. 
* The face position template shows the average position of facial features across lots of people, assuming that the person is looking directly forward. 
* By comparing the position of each point on the face image with the position of each point on the template, we can guess how far the head is turned and in 
what direction it was turned. 
* Then, we can warp our face image to roughly match the template. This is called aligning the face because we are making sure the key facial features in the 
image line up with the face template before we move on to the next step in our pipeline. 

## **Step 4: Represent Face as Measurements**
* Now that we have aligned the face image, we're ready to turn the face into a set of numbers, or measurements, that represent this unique face. 
* Other pictures of the same person should generate measurements that are very close to these numbers. 
* Pictures of a different person should generate measurements that are also very different. 
* You can imagine that we might try to measure different face characteristics, like the distance between the eyes or the position of the eyebrows, as a way 
to find out what makes this face unique, but trying to manually measure faces like that isn't very reliable. 
* Instead of trying to come up with our own way to measure faces, we'll use a neural network that was trained on millions of faces to come up with its own 
way to measure faces. 
* We'll feed the aligned image to the neural network and it will return a list of measurements. 

## **Step 5: Compare to Other Faces**
* Now that we've turned the first image into a set of measurements, we can compare it to other images by processing them the same way. 
* Let's take a second picture oand run it through the exact same face recognition pipeline. That will give us a second set of measurements 
to represent the face in the second image. 
* To compare these two faces, we'll calculate how different the measurements are using a formula called **Euclidean distance**. This formula basically 
measures how far apart the two different sets of measurements are. 
* If the measurements are close, we'll call it a match. Otherwise, we know they don't match.

# **Summary**
Here's an overview of the entire face recognition process. 
* First, we locate a face in the picture, then we find the location of each facial feature. 
* Next, we use the position of the facial features to align the face to match a standard template. 
* Then we use a neural network to create a set of measurements that represent that face. These measurements are also called a face encoding. 
* Finally, we compare that face to other faces by comparing those measurements. 
