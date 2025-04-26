# cs3630-project-2-multi-modal-sensing-solved
**TO GET THIS SOLUTION VISIT:** [CS3630 Project 2-Multi-Modal Sensing Solved](https://www.ankitcodinghub.com/product/cs3630-3630-project-2-multi-modal-sensing-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;127061&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS3630 Project 2-Multi-Modal Sensing Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Overview

The setting for this project is that an e-puck robot is navigating a maze to find a traffic sign. You are provided code that will determine whether the traffic sign is in the camera feed of the robot. Your task will be to determine:

1. The depth (not the distance) and angle to the sign using the 2-cameras method

2. The distance and angle to the sign using camera+lidar method

In the second part, you will leverage the lidar on the robot to determine the distance and heading, using both the point cloud of the lidar, and one image captured by the robot. The lidar data is composed of an array of 360 distance values around the robot, one for each degree for 0 to 359 deg.

Webots Simulator

We will be employing the Webots simulator in this project (and in some of the future projects in this course). You will need to install it using the following installation procedure (this includes documentation for Linux, Windows, and Mac).

You will be provided with a series of world files and a controller for the e-puck robot. The assignment will then require finding the distance/depth and heading of a traffic sign, relative to the robot, in each world file. The code structure and respective functions is described in the next section.

To test out your scripts in the Webots simulator, open a world file (named either as proj2_world_vision_lidar_#.wbt or as Vision_only_world#.wbt), and run the simulation. The first few (typically 3) iterations running the controller might have blank images, however it should then allow you to see the required distance/ depth and angle values print on the Webots console.

Requirements Installation

You can use the requirements.txt file to install all necessary packages by running pip install

-r requirements.txt

Assignment

Preliminaries

The field of view is the range of the world (in this project, defined in radians) in the horizontal plane that is visible.

We provide the following formula that can be used to include the field of view in the calculation of focal length for both parts 1 and 2. focal_length = image_width / (2 * math.tan(fov / 2))

Part 1: Determine depth and angle using stereo vision

To complete part 1, you will need to fill out the vision_only_depth_calculation(image1, image2, fov, camera_translation) function in proj2_vision_only_controller/vision_only_calculation.py

The vision_only_depth_calculation(image1, image2, fov, camera_translation) function takes in two images, camera field of view, camera translation (distance between the 2 cameras) and returns the depth (perpendicular distance from the traffic sign to the line joining the cameras) and angle from the robot to the traffic sign in the images.

Hint: try using trigonometry to calculate the angle, using the parameters mentioned in the diagram above.

Part 2: Determine distance and angle using vision and lidar

To complete part 2, you will need to fill out the vision_lidar_distance_calculation(image, lidar_range_array, fov) function in proj2_vision_lidar_controller/vision_lidar_calculation.py

The vision_lidar_distance_calculation(image, lidar_range_array, fov) function takes in an image and the point cloud returned from a lidar, and returns the distance and angle from the robot to the traffic sign in the images.

Functions Provided

To complete the above two parts, you are provided with the contour.py file, which contains a function box_measure(image) that calculates the pixel values of the centroid of the identified traffic sign in the image. This file (identical copies) can be found in both the proj2_vision_lidar_controller and the proj2_vision_only_controller folders.

Submission Instructions

The files you will submit to Gradescope are vision_lidar_calculation.py and vision_only_calculation.py

To test your solution locally, you can employ the provided local_tests.py files.

– NumPy

– OpenCV

Rubric for Vision Component

Your solution for part 1 (stereo vision) will be evaluated in 5 world files. Each world will be worth 10 points for a total of 50 points possible.

Depth Evaluation

For each world, you will receive a number of points based upon how close your detected depth is from the true depth. The difference between your depth and the true depth will be evaluated as a percentage of the true depth.

For example, if the true depth is 10 cm and you say that the depth is 9 cm, then the difference is 1 cm. This is 10% of the true 10 cm, so the grade would be 8 out of 10 for that world file.

Percentage difference in distance Point Count

&lt;= 5% of true distance 5 points (full credit)

&lt;= 10% of true distance 4

&lt;= 15% of true distance 3

&lt;= 20% of true distance 2

&lt;= 25% of true distance 1

&gt; 25% of true distance 0

Angle (Heading) Evaluation

For each world, you will receive a number of points based upon how close your detected angle is from the true angle. The difference between your angle and the true angle will be evaluated as difference in degrees.

Degrees difference in heading Point Count

&lt;= 5 degrees 5 points (full credit)

&lt;= 10 degrees 3.75

&lt;= 15 degrees 2.5

&lt;= 20 degrees 1.25

&gt; 20 degrees 0

Rubric for Vision + Lidar Component

Similarly, your solution for part 2 (vision + lidar) will be evaluated in 5 world files. Each world will be worth 10 points for a total of 50 points possible for part 2.

Distance Evaluation

For each world, you will receive a number of points based upon how close your detected distance is from the true distance. The difference between your distance and the true distance will be evaluated as a percentage of the true distance.

Percentage difference in distance Point Count

&lt;= 5% of true distance 2 points (full credit)

&lt;= 10% of true distance 1.5

&lt;= 15% of true distance 1

&lt;= 20% of true distance 0.5

&gt; 20% of true distance 0

Angle (Heading) Evaluation

For each world, you will receive a number of points based upon how close your detected angle is from the true angle. The difference between your angle and the true angle will be evaluated as difference in degrees.

Degrees difference in heading Point Count

&lt;= 5 degrees 8 points (full credit)

&lt;= 10 degrees 6

&lt;= 15 degrees 4

&lt;= 20 degrees 2

&gt; 20 degrees 0
