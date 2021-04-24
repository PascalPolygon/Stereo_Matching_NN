# Stereo_Matching_NN

  # Sparse Cost Volume Neural Network (SCV-Net)[1] for Stereo Matching
  
  -----
  <p align="center">
  Mawaba Pascal Dao<br> 
  Bindi Nagda <br>
  pdao2015@my.fit.edu <br>
  bnagda2015@my.fit.edu <br>

  Spring 2021   
  </p>
  When a scene is captured by two cameras at different vantage points, it is possible to extract 3Dinformation by comparing their images. This is done by estimating the disparity at the same pixellocations between the two images. This is known as stereo matching.Using this technique, it is possible to reconstruct a 3D scene or object from 2 cameras.  Stereomatching has applications in robotics, AR/VR, manufacturing and more.In recent years, learning based stereo matching approaches have been shown to have much greaterperformance than Physics based approaches. This was demonstrated in 2015 by Zbontar et al. Theytrained a Siamese network to find correspondences between two images [3]. The best approach toend-to-end learning based stereo matching is GC-Net [4].  GC-Net treats stereo matching as aregression problem and has sub-pixel accuracy. However GC-Net’s size makes it slow to run. Thisis because the algorithm searches a large cost volume space.  This project implements a SparseCost Volume. This is done simply by increasing the stride of feature maps over the input images.This eliminates redundancy in the cost volume and creates smaller cost volumes. This Sparse CostVolume Network (SCV-Net) was first proposed in [1].
 -----
<p align="center">
 References 
  </p>
  
[1] Aznan, Nik Khadijah Nik, et al. “On the Classification of SSVEP-Based Dry-EEG Signals via Convolutional Neural Networks.” 2018 IEEE International Conference on Systems, Man, and Cybernetics (SMC), 2018, doi:10.1109/smc.2018.00631. 

 -----
 # Results
![](results/confusion_mtx.png)
 -----
 # Single channel raw EEG
![](results/single_channel.png)
 -----
 # Virtual navigation
The predictions on the EEG signals are used to move a ball in a virtual environment.
In theory, subjects whose signals were used to train the model could put on an EEG headset and control the ball 
in real time with their raw brain brain activity without any preprocessing required.
![](results/virtual_nav.png)

