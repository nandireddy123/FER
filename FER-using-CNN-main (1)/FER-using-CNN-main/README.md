**Facial-Emotion-Recognition**
1. Introduction
The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms. Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge.



In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (exZoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analysed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analysed and tracked.

1. Problem Statement
We will solve the above-mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions.

2. Face Emotion Recognition Model
Facial expression recognition system is a computer-based technology and therefore, it uses algorithms to instantaneously detect faces, code facial expressions, and recognize emotional states. It does this by analyzing faces in images or video through computer powered cameras embedded in laptops, mobile phones, and digital signage systems, or cameras that are mounted onto computer screens. Facial analysis through computer powered cameras generally follows three steps:

A. Face detection

Locating faces in the scene, in an image or video footage.

B. Facial Feature Detection

Extracting information about facial features from detected faces. For example, detecting the shape of facial components or describing the texture of the skin in a facial area.

C. Facial expression and emotion Classification

Analyzing the movement of facial features and/or changes in the appearance of facial features and classifying this information into expression-interpretative categories such as facial muscle activations like smile or frown; emotion categories happiness or anger; attitude categories like (dis)liking or ambivalence

2.1 Face Detection
Face detection can be regarded as a specific case of object-class detection. In object-class detection, the task is to find the locations and sizes of all objects in an image that belong to a given class. Examples include upper torsos, pedestrians, and cars. Face detection simply answers two question, 1. are there any human faces in the collected images or video? 2. where is the located?

Face-detection algorithms focus on the detection of frontal human faces. It is analogous to image detection in which the image of a person is matched bit by bit. Image matches with the image stores in database. Any facial feature changes in the database will invalidate the matching process.

Object Detection using Haar feature-based cascade classifiers is an effective object detection method proposed by Paul Viola and Michael Jones in their paper, "Rapid Object Detection using a Boosted Cascade of Simple Features" in 2001. It is a machine learning based approach where a cascade function is trained from a lot of positive and negative images. It is then used to detect objects in other images. Here it will train with faces. Initially, the algorithm needs a lot of positive images (images of faces) and negative images (images without faces) to train the classifier.

2.2 Facial Feature Detection and Emotion Classification.
The Haar Casscade detects face and those faces are then cropped and convert to gray images. These gray images further get converted into iamge aaray for processing. Out DNN is made up of 4 CNN blocks and 5 Dense block with dropout probabilities of 0.5. Each block has Batch Normalization layer, CNN layer (3x3) kernel, activation Function layer (ReLU) and max pooling (2x2). Dataset which is used to train this DNN is FER 2013 dataset. It has images of all 7 class of emotion.

Hyper-parameter that were used are epochs = 100,batch_size = 64 and learning_rate = 0.001

CNN2D

2.3 Evaluation Metrics
Loss and Accuracy Graph

Loss graph

Confusion Matrix

confusion matrix

3. Conclusions
Our model shows accuracy of 67.37% .

