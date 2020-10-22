# SFND 2D Feature Tracking

<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera course was to build a collision detection system - that's the overall goal for the Final Project. As a preparation for this, I buılt the feature tracking part and test various detector / descriptor combinations to see which ones perform best. This mid-term project consists of four parts:

## TASKS:
### * MP.1 Data Buffer Optimization
   In order to prevenet pushing of computer memeory to limit, we only wanted to hold a certain number of images in memory so that when a new one arrives


### * MP.2 Keypoint Detection
Implement classical and modern detectors and make them selectable by setting a string accordingly.
1. Classical detectors:
	1.	HARRIS, 
	2.	Shi-Tomas,
	3.	SIFT.
	4.	SUFT. (was not impelemented)
2. Modern detectors:
	1.	FAST,
	2.	BRISK,
	3.	ORB,
	4.	AKAZE
    
### * MP.3 Keypoint Removal
 Discard feature points that are not located on the preceding vehicle.
 
### * MP.4 Keypoint Descriptors
Implement HOG and Binary descriptors and make them selectable by setting a string accordingly.
1. HOG Descriptor
	1.	SIFT
2. Binary Descriptors:
	1.	BRISK 
	2.	BRIEF 
	3.	ORB 
	4.	FREAK 
	5.	AKAZE
    
### * MP.5 Descriptor Matching
Implement Brute Force and FLANN matching as well as k-nearest neighbor selection. 
Both methods must be selectable using the respective strings in the main function.
1.	BF     
	1.	Binary / HOG 
	2.	NN / kNN
2.	FLANN 
	1.	HOG
	2.	kNN

### * MP.6 Descriptor Distance Ratio
Use the K-Nearest-Neighbor matching to implement the descriptor distance ratio test, which looks at the ratio of best vs. 
second-best match to decide whether to keep an associated pair of keypoints.
    
### * MP.7 Performance Evaluation 1 : Keypoints
Count the number of keypoints on the preceding vehicle for all 10 images and take note of the distribution of their neighborhood size.
Do this for all the detectors you have implemented. 
    
### * MP.8 Performance Evaluation 2 : Combination of detectors and descriptors
Count the number of matched keypoints for all 10 images using all possible combinations of detectors and descriptors.
In the matching step, the FLANN approach is used with the descriptor distance ratio set to 0.8.

### * MP.9 Performance Evaluation 3 : Top-3 combination 
Log the time it takes for keypoint detection and descriptor extraction. The results must be entered into a spreadsheet 
and based on this data, the TOP3 detector / descriptor combinations must be recommended as the best choice for our purpose of detecting keypoints on vehicles.
`PS: check out README_results file. 
