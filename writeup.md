# Writeup: Track 3D-Objects Over Time

## 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

This is midterm report, and what I implemented is detector using LIDAR pointcloud. I have extracted features and input the data to([darknet](https://drive.google.com/file/d/1Pqx7sShlqKSGmvshTYbNDcUEYyZwfn3A/view))detector which is pre-trained model  and obtain detection result. I also have evaluated the detector.

### 1-1. Create range image and intensity image.

I extracted features in LIDAR pointcloud. First feature is range feature in top of the image. Another feature is intensity image in bottom of the image.  
<img src="figure/../figures/range_image.png" width="1000"> 

### 1-2. Plot pointcloud

I checked features of vehicle shape using pointcloud data. Almost all Shape of vehicles looks like box.  
<img src="figure/../figures/pcl1.png" width="600">

Height of vehicles are lower than trees, and we can use this feature to extract vehicles from pointcloud.  
<img src="figure/../figures/pcl2.png" width="600">

In the center of figure, there is a truck. The shape of the truck is complicated and LIDAR pointcloud cannot be returned from the truck, but it somehow looks L-shape.  
<img src="figure/../figures/pcl3.png" width="600">

We cannot obtain pointcloud of vehicles which are occluded by other vehicle.  
<img src="figure/../figures/pcl4.png" width="600">

LIDAR can detect roof top of vehicles.  
<img src="figure/../figures/pcl5.png" width="600">

Vehicles drive on flat road. We can use this context to detect vehicles.  
<img src="figure/../figures/pcl6.png" width="600">

Shapes of vegetation does not look box or L-shape.  
<img src="figure/../figures/pcl7.png" width="600">

### 1-3. Extract features
First, I map pointcloud onto BEV.  
<img src="figure/../figures/bev_pcl_conventional.png" width="600">

I extracted height features from pointclouda and map onto BEV.  
<img src="figure/../figures/height.png" width="600">

I also extracted intensity features from pointcloud and map onto BEV.  
<img src="figure/../figures/intensity.png" width="600">

### 1-4 ML and evaluation
I prepared LIDAR and camera dataset with ground truth.  
<img src="figure/../figures/label_detected_objects.png" width="600">

For this project, I used pre-trained model, because I work on an workspace environment prepared by Udacity. I evaluate pre-trained model, so called darknet, and calculate precision, recall, uoi, and position errors.  
<img src="figure/../figures/detection_performance_metrics.png" width="600">

Lidar detector is implemented. I will implement tracker using LIDAR and camera detectors and develop sensor fusion method.

## 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)? 
TBD. This is a midterm report.

## 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
TBD. This is a midterm report.

## 4. Can you think of ways to improve your tracking results in the future?
TBD. This is a midterm report.
