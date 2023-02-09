# Face_detection
## Face Detection using OpenCV and MTCNN

### Open CV
OpenCV (Open Source Computer Vision) is a popular computer vision library. The library sets its focus on real-time image processing and implementations of the latest computer vision algorithms. It is used in image processing, video capture and analysis including features like face detection and object detection. Application of Computer Vision spreads out in every major domain from medicine, robotics to security.

### Cascade Classifier
Cascade classifiers are trained using several positive (with faces or objects) images and arbitrary negative (without faces or objects) images. Then we extract features from it.

### MTCNN
Multi-task Cascaded Convolutional Networks (MTCNN) is a framework developed as a solution for both face detection and face alignment. The process consists of three stages of convolutional networks that are able to recognize faces and landmark location such as eyes, nose, and mouth.

#### The Three Stages of MTCNN:

#### Stage 1: The Proposal Network (P-Net)
In the first stage it uses a shallow CNN(i.e. dense layer is not a part of the architecture) to quickly produce candidate windows and their bounding box regression vectors.

#### Stage 2: The Refine Network (R-Net)
All candidates from the P-Net are fed into the Refine Network. In the second stage it refines the proposed candidate windows through a more complex CNN(i.e. dense layer is the part of the CNN architecture). The R-Net outputs wether the input is a face or not, a 4 element vector which is the bounding box for the face, and a 10 element vector for facial landmark localization.

#### Stage 3: The Output Network (O-Net)
In the third stage it uses a third CNN, more complex than the others, to further refine the result and output facial landmark positions.
