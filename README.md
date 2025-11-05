# Transparent-Objects-Pose-Estimation-via-RGB-D-Enhancement-and-Depth-Directed-Feature-Fusion

# Abstract
Estimating the 6D pose of transparent objects remains a challenging task due to weak visual cues and incomplete depth information caused by refractions and additional reflections from the backsides of transparent objects. These challenges often lead to inaccurate perception and localization. Existing approaches struggle to jointly enhance RGB and depth features or fully exploit depth information. In this paper, we propose a depth-directed method that integrates stable diffusion and Mamba-based RGB-D augmentation to address these limitations. Specifically, we use a stable diffusion model to enhance the visibility of transparent objects in RGB images by recovering texture details and reducing background interference. Then, a Mamba-based network completes the sparse and noisy raw depth maps using guidance from the refined RGB features. To effectively fuse the two modalities, we introduce a multi-scale RGB-D fusion strategy, where the completed depth not only provides geometric information but also guides RGB feature extraction. This joint representation leads to more accurate and robust 6D pose estimation. Experimental results on challenging datasets demonstrate that our method significantly enhances object visibility and improves pose estimation accuracy in complex real-world scenes.

# Experimental Settings
<img width="1875" height="1220" alt="1" src="https://github.com/user-attachments/assets/a3830b30-e1ab-471f-887d-6fc0db5155f1" />

The estimated 6D pose and object size are transformed into a robot-executable grasp through a predefined mapping strategy. The translation and rotation predicted in the camera coordinate system are first converted into the robot base frame via hand–eye calibration. The estimated size determines the gripper opening width with a small clearance margin. Depending on the object’s orientation relative to the table, the system generates a limited set of candidate grasps, typically a top-down grasp when vertical clearance allows or side grasps aligned with the object’s principal axes otherwise. Each candidate is evaluated against table clearance, gripper limits, and kinematic feasibility, and the most suitable option is selected.

# Visualizations
<img width="1394" height="1049" alt="aac19025-0937-4918-a13f-1720529502e1" src="https://github.com/user-attachments/assets/124a33c1-54f9-4072-b9af-fd16e6da93ee" />



# Demonstration
![80c45fda7fd18b66100a8450214084be](https://github.com/user-attachments/assets/b2f3bf02-c7f0-460b-b920-4fd5a7e9cd94)

![aba395493a72776d8f0645a88a1debcf](https://github.com/user-attachments/assets/f1c5b0bc-7ead-46c3-856e-87c9b8e93e4f)

![2c21584225154c744d6430e265ca6b06](https://github.com/user-attachments/assets/19788695-2f74-460d-8e62-8648a494e8c2)

![655714100cc12c1bb7cb86c6954aa7c0](https://github.com/user-attachments/assets/c045a013-be23-47d3-b67e-37d43efdf0fd)


# Code will be released here after the paper is published.
