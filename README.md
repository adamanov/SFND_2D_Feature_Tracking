# SFND 2D Feature Tracking
## [Rubric](https://review.udacity.com/#!/rubrics/2549/view) Points
<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera course was to build a collision detection system what is also an overall goal for the Final Project. As a preparation for this, I buılt the feature tracker and test various detector / descriptor combinations to see which ones perform best. This mid-term project consists of four parts:

## TASKS:
### 1. Data Buffer
-	####	 Data Buffer Optimization
   	In order to prevenet pushing of computer memeory to limit, we only wanted to hold a certain number of images in memory so that when a new one arrives


### 2. Keypoints

-	####	Keypoint Detection
	Implement classical and modern detectors and make them selectable by setting a string accordingly.
```
1. Classical detectors:
	1.1	HARRIS 
	1.2	Shi-Tomas
	1.3	SIFT.
	1.4	SUFT. (was not impelemented)
2. Modern detectors:
	2.1	FAST
	2.2	BRISK
	2.3	ORB
	2.4	AKAZE
```
-	#### Keypoint Removal
	Discard feature points that are not located on the preceding vehicle.
 
### 3. Descriptors 
-	####  Keypoint Descriptors
	Implement HOG and Binary descriptors and make them selectable by setting a string accordingly.
```
1. HOG Descriptor
	1.1	SIFT
2. Binary Descriptors:
	2.1	BRISK 
	2.2	BRIEF 
	2.3	ORB 
	2.4	FREAK 
	2.5	AKAZE
```
    
-	####  Descriptor Matching
	Implement Brute Force and FLANN matching as well as k-nearest neighbor selection. 
	Both methods must be selectable using the respective strings in the main function.
```
1.	BF     
	1.1	Binary / HOG 
	1.2	NN / kNN
2.	FLANN 
	2.1	HOG
	2.2	kNN
```

-	####  Descriptor Distance Ratio
	Use the K-Nearest-Neighbor matching to implement the descriptor distance ratio test, which looks at the ratio of best vs. 
	second-best match to decide whether to keep an associated pair of keypoints.

### 4. Performance
-	#### Performance Evaluation 1 : 
	```Keypoints```
    
-	#### Performance Evaluation 2 :
	``` Combination of detectors and descriptors```

-	#### Performance Evaluation 3 : 
	```Top-3 combination ```

Results: 
Detector AKAZE and Descriptor BRISK - > 292 
AKAZE Detector and Descriptor       - > 282
Descriptor FREAK and Detector AKAZE - > 258


Descriptor SIFT and Detector ORB    - > 325
Descriptor SIFT and Detector AKAZE  - > 307
Descriptor SIFT and Detector FAST   - > 291

Above I mentioned top3 detector and Descriptor for both classical and modern methods.
As we can see SIFT Descriptor is show really good results with combination of modern Detector
algorithms and outperform modern Descriptor algorithms. However, in our case 
it is not only enough to show good detecting and matching of keypoints perform.
It is also important that we could do it in a real-time application. 
And since SIFT Descriptor is HOG family algorithms, it will show slow performance on 
a real time application. Thats why it better to choose a detector from Binary Descriptor family.
Such that AKAZE Detector suitable best for us case, and depened on further investigation 
of time required for Descriptor we could choose either BRISK or AKAZE as Descriptor


[PS: check out results of all combination.](https://github.com/adamanov/SFND_2D_Feature_Tracking/blob/master/results)
