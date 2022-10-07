# Writeup: Track 3D-Objects Over Time

## 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

1. Create range image and intensity image.

I extracted features in LIDAR pointcloud. First feature is range feature in top of the image. Another feature is intensity image in bottom of the image.
<img src="figure/../figures/range_image.png" width="1000">

2. Create plot of pointcloud

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

3. Extract features

I extracted height features from pointclouda and map onto BEV.
<img src="figure/../figures/height.png" width="600">

I also extracted intensity features from pointcloud and map onto BEV.
<img src="figure/../figures/intensity.png" width="600">

4. ML



## 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)? 
hoge.

## 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
hoge.

## 4. Can you think of ways to improve your tracking results in the future?
hoge.
