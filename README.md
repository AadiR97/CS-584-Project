Title: Forest Fire Detection
Course Name: THEORY AND APPLICATION OF DATA MINING (CS-584 FALL 2022)
Course Instructor: Professor ZIWEI ZHU
Department: Department of Computer Science, George Mason University
1.	PROJECT MOTIVATION	
There is an increase in the number of forest fires of late. These forest fires have resulted in the utter devastation of flora and fauna and are responsible for tipping the ecological balance. In the future, this ecological imbalance can create multiple adverse effects on our environment. It is of utmost importance to detect forest fires to minimize the adverse effects on nature and the economy. In this project, we attempted to develop a method of early detection of forest fires utilizing CNN and RCN in machine learning (Han et al., 2019). 
2.	PROJECT GOAL
The primary goal of the project is to apply this machine learning model to detect the early presence or the epicenter of the fire utilizing Ariel surveillance. The plan is to apply this model in real-time and low-frame rate surveillance video to initiate an alert in case of a fire (Permana et al., 2022). 
3.	DATASET INFORMATION
For this project, we have attained fire related dataset from the Kaggle website. The dataset contains two folders. Each folder contains fire and non-fire images of the earth and nature. These images represent various natural phenomena such as forests, waterfalls, foggy forests, lakes, rivers, etc. We plan to divide these images into three categories for benefit of the study.  These categories are “fire”, “no-fire” and “start fire”. We will collect and feed data into the system for training the system. This training will enable the system to differentiate between the three categories through binary classification (YANDOUZI et al., 2022).  
4.	TECHNICAL DETAILS
A machine learning model is trained and tested on the various fire and non-fire images. Image Processing and manipulation are performed using the Python Imaging Library. R-CNN and ANN are utilized for the early detection of the starting point of fire (Zhang et al., 2018). Sequential CNN from scratch, Pretrained Xception with modifications models are used (Verlekar et al., 2020). Pandas’ library is cast-off to manipulate the data and the time series. After the completion of this procedure, the fire detection model will be able to process the Ariel surveillance images and post certain values to send a fire alert.
5.	EMPIRICAL RESULTS 
5.1 Fire Detection in Images
The objective is to create a binary classification model that can be used to detect fire in images. We have used sequential CNN from scratch and Pretrained Xception. Modifications were performed in the models to customize usage.
5.2 Exploratory Data Analysis
First, the data frame was created. The created data frame contains the path to each picture and its matching label. The labels indicate fire or non-fire characteristics on the images. Once the dataset has been created we tested the dataset to ensure that the data is well shuffled. 
5.3 Visualizing the images with fire and no fire
5.4 Visualizing Shape Distribution
6.	Image Generation or Augmentation
In this phase, we have created the training and test generator. We have utilized the Image data generator class and used the flow from the data-frame method for this purpose. The training will take the path of the images from the data frame along with the labels. We have created two generators for the project. The first one is for training and the other one is for validation. Our selected labels are strings ‘fire’ and ‘non-fire’. The image generator will automatically encode them to integer labels. An image predicted 0 will indicate ‘fire’ and an image predicting 1 will indicate ‘non-fire’.
7.	Model Creation
There will be a lot of noise present in the input, and we need to capture important information. So we have increased the number of filters as we add more layers during training. As we progress through the layers, the feature maps become nuanced. We tried to capture them by adding more filters. 
8.	Plotting Metrics
9.	Example Predictions
10.	CONTRIBUTION OF TEAM MEMBERS
The project is the combined effort of the team members. First, the team members convened to discuss and select the topic of the project. Once the topic is selected, we discussed the conceptual model we were trying to create. The team members shared their insight and understanding of the concept and the proposed model. Then we discussed and selected a Python program for our project. We also selected the visualization technique to be used. The team members contributed equally to the coding. One team member performed the testing and validation, while another wrote the project. It is needless to say that our combined efforts enabled us to create a forest fire detection model.
REFERENCES
Han, J., Kim, G., Lee, C., Han, Y., Hwang, U., & Kim, S. (2019, February). Predictive models of fire via deep learning exploiting colorific variation. In 2019 International Conference on Artificial Intelligence in Information and Communication (ICAIIC) (pp. 579-581). IEEE.
Permana, S. D. H., Saputra, G., Arifitama, B., Caesarendra, W., & Rahim, R. (2022). Classification of bird sounds as an early warning method of forest fires using Convolutional Neural Network (CNN) algorithm. Journal of King Saud University-Computer and Information Sciences, 34(7), 4345-4357.
Verlekar, T. T., & Bernardino, A. (2020, October). Video Based Fire Detection Using Xception and Conv-LSTM. In International Symposium on Visual Computing (pp. 277-285). Springer, Cham.
YANDOUZI, M., GRARI, M., IDRISSI, I., BOUKABOUS, M., MOUSSAOUI, O., GHOUMID, K., & ELMIAD, A. K. (2022). Forest Fires Detection using Deep Transfer Learning. Forest, 13(8).
Zhang, Q. X., Lin, G. H., Zhang, Y. M., Xu, G., & Wang, J. J. (2018). Wildland forest fire smoke detection based on faster R-CNN using synthetic smoke images. Procedia engineering, 211, 441-446.

STEPS TO RUN THE FILE:
1. import all the necessary libraries from the first cell.
2. we next load the required data-sets for our project.(google drive link has been mentioned in the report)
3. next we visualize the datasets has to how they are individually because we have two different types, fire and non-fire.
4. we notice that the images are not of same dimensions so we reshape them using ImageGenerator class.
5. we then randomly divide the datasets into validating dataset and training dataset and classify them into two classes, "fire" which will be given a class index 0 and the other class will be "non-fire" with class index 1.
6. we then check if the training set generated is accurate or not by visualizing the images.
7. we the ncreate out model using the sequential model and then use the ADAM optimiser to get better accuracy.
8. we then apply the "Xception model" onto our already existing model to try and further increase our accuracy. 
9. we the n verufy if our model is working fine or not by giving it two types of output to check for the two classes we created earlier: fire and non-fire.
We find that our model is predicting the images accurately.
