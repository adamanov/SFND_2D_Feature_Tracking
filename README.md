# SFND 2D Feature Tracking
## [Rubric](https://review.udacity.com/#!/rubrics/2549/view) Points
<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera course was to build a collision detection system - that's the overall goal for the Final Project. As a preparation for this, I buılt the feature tracking part and test various detector / descriptor combinations to see which ones perform best. This mid-term project consists of four parts:

## TASKS:
### Data Buffer
##### * -	 Data Buffer Optimization
   In order to prevenet pushing of computer memeory to limit, we only wanted to hold a certain number of images in memory so that when a new one arrives


### Keypoints

##### * - Keypoint Detection
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
   
#### * - Keypoint Removal
 Discard feature points that are not located on the preceding vehicle.
 
### Descriptors 
#### * - Keypoint Descriptors
Implement HOG and Binary descriptors and make them selectable by setting a string accordingly.
1. HOG Descriptor
	1.	SIFT
2. Binary Descriptors:
	1.	BRISK 
	2.	BRIEF 
	3.	ORB 
	4.	FREAK 
	5.	AKAZE
    
#### * - Descriptor Matching
Implement Brute Force and FLANN matching as well as k-nearest neighbor selection. 
Both methods must be selectable using the respective strings in the main function.
1.	BF     
	1.	Binary / HOG 
	2.	NN / kNN
2.	FLANN 
	1.	HOG
	2.	kNN

#### * - Descriptor Distance Ratio
Use the K-Nearest-Neighbor matching to implement the descriptor distance ratio test, which looks at the ratio of best vs. 
second-best match to decide whether to keep an associated pair of keypoints.

### Performance
#### * - Performance Evaluation 1 : Keypoints 
    
#### * - Performance Evaluation 2 : Combination of detectors and descriptors

#### * - Performance Evaluation 3 : Top-3 combination 
`PS: check out README_results file. 
