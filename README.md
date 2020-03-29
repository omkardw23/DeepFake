# DeepFake
Deepfake techniques, which present realistic AI-generated videos of people doing and saying fictional things,  have the potential to have a significant impact on how people determine the legitimacy of information presented online.  
These content generation and modification technologies may affect the quality of public discourse and the safeguarding of  human rights—especially given that deepfakes may be used maliciously as a source of misinformation, manipulation, harassment, and  persuasion.  Identifying such manipulated media is of paramount importance in today's cyberspace.   

The dataset is available on Kaggle:

https://www.kaggle.com/c/deepfake-detection-challenge/data


Special thanks to courses offered by deeplearning.ai and SuperDataScience, for furnishing many valuable insights.

Following are the research paper referenced for this project :

------------------------------------------------------------------------------------------------------------------------------------------
General-Image-Processing module : 
This notebook was created to implement the code trying to extract the face/s using Viola Jones algorithm, that is by using Haar cascades designed in OpenCV. The haarcascade can be downloaded from :
https://github.com/opencv/opencv/tree/master/data/haarcascades 
or 
are available in Kaggle's data repository as well. Using the pre-defined openCV functions we were able to detect the faces successfully. 
Moreover, the code also contains necessary function defined from graying the cropped face image/s, and histogram equalizing it(in order to spread the intensity near uniformly across the gray value range). Moreover, to analyze the frequencies present, a 2D DFT was also computed. 
----------------------------------------------------------------------------------------------------------------------------------------
