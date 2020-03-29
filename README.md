# DeepFake
Deepfake techniques, which present realistic AI-generated videos of people doing and saying fictional things,  have the potential to have a significant impact on how people determine the legitimacy of information presented online.  
These content generation and modification technologies may affect the quality of public discourse and the safeguarding of  human rights—especially given that deepfakes may be used maliciously as a source of misinformation, manipulation, harassment, and  persuasion.  Identifying such manipulated media is of paramount importance in today's cyberspace.   

The dataset is available on Kaggle:

https://www.kaggle.com/c/deepfake-detection-challenge/data


Special thanks to courses offered by deeplearning.ai and SuperDataScience, for furnishing many valuable insights.

(I) General-Image-Processing module : 
------------------------------------------
This notebook was created to implement the code trying to extract the face/s using Viola Jones algorithm, that is by using Haar cascades designed in OpenCV. The haarcascade can be downloaded from :
https://github.com/opencv/opencv/tree/master/data/haarcascades 
or 
are available in Kaggle's data repository as well. Using the pre-defined openCV functions we were able to detect the faces successfully. 
Moreover, the code also contains necessary function defined from graying the cropped face image/s, and histogram equalizing it(in order to spread the intensity near uniformly across the gray value range). Moreover, to analyze the frequencies present, a 2D DFT was also computed. 

(II) Model 1 :
----------------
----------------
MTCNN :
--------
MTCNN (Multi-task Cascaded Convolutional Neural Networks) is an algorithm consisting of 3 stages, which detects the bounding 
boxes of faces in an image along with their 5 Point Face Landmarks. Each stage gradually improves the detection results by passing it’s inputs through a CNN, which returns candidate bounding boxes with their scores, followed by non max suppression.

In stage 1 the input image is scaled down multiple times to build an image pyramid and each scaled version of the image is passed through it’s CNN. In stage 2 and 3 we extract image patches for each bounding box and resize them (24x24 in stage 2 and 48x48 in stage 3) and forward them through the CNN of that stage. Besides bounding boxes and scores, stage 3 additionally computes 5 face landmarks points for each bounding box. 


Mesonet : 
--------------------------
( https://www.researchgate.net/publication/327435226_MesoNet_a_Compact_Facial_Video_Forgery_Detection_Network )
