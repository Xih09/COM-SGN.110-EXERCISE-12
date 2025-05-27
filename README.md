Download link : https://programming.engineering/product/com-sgn-110-exercise-12/

COM-SGN.110–EXERCISE 12
Please note: the provided codes require Computer Vision toolbox to run.

The tasks should be completed and presented to TA during the lab session. Do not forget to upload your solutions to Moodle! Questions about exercises should be addressed to the TA personally, through Moodle messages or via email, which can be found on the Moodle page of the course.

1. Inter-frame motion estimation

The provided file optical_flow.m contains a MATLAB example code to estimate the direction and speed of object motion through consecutive video frames. The code utilizes a built-in implementation of the Lucas-Kanade method for optical flow estimation.

    Familiarize yourself with the given code and its parameters. Use MATLAB help functionality.

    Change the NoiseThreshold parameter of opticalFlowLK function to find the best value and explain its role in motion estimation.

Note on the algorithm: refer to the slides of the lecture 12 for the general introduction to the problem and the description of a basic Exhaustive Block Matching Algorithm (EBMA). Unlike EBMA, which locates and matches similar blocks within a certain range from each other, Lucas-Kanade method computes optical flow derivatives in each image block (via linear kernels) and solves the optical flow equation with a least-squares fit. You can find further details of the Lucas-Kanade method in the MATLAB help page for the opticalFlowLK function.

2. Motion estimation in Echocardiography videos

Myocardial infarction (MI), known also as heart attack, is a life-threatening worldwide health problem. Mainly, MI happens due to a blockage or plaque in one or more arteries that feed/s the heart muscle. By the time, cardiac cells cannot get enough oxygen because of the blocked artery, and they start to die. The death of the cardiac cells accumulates, and at the end, MI happens.

Echocardiography (echo) is a non-invasive imaging technique that can monitor the heart in real time from different views using ultrasound technology. Figure 1 shows an example echo image where the bright pixels represent the heart muscle and the dark pixels inside the heart sections (right/ left ventricle and right/ left atrium) are blood. Cardiologists decide on the possibility of MI by examining the motion of the left ventricle wall in echo videos (see Figure 1). Therefore, in this exercise we need to estimate the motion of echo videos and observe the results for left ventricle wall.

Left

Ventricle

Wall

Left

Ventricle

Right

Ventricle

Left

Right Atrium

Atrium

Figure 1. Example echo image depicting the four main sections of the human heart.

The provided echo1.avi and echo2.avi contain echo videos for two different subjects. One of the videos shows a healthy heart echo while the other depicts an unhealthy one. Using the code provided in task 1, determine which one of these videos is for a healthy heart by performing motion estimation as follows:

    Estimate the objects motion using the grayscale frames of the provided echoes.

    Change the NoiseThreshold parameter to find the best value.

    Observe the results and explain the output.

    Can you determine which one of the echoes is for a healthy heart? Why?

    Smooth the grayscale frames using an adaptive wiener filter (wiener2) or an anisotropic diffusion filter (imdiffusefilt) and estimate the objects motion using the filtered grayscale frames of the provided echoes.

    What is the difference between the outputs of (c) and (e)?

    Can you determine which one of the echoes is for a healthy heart?

