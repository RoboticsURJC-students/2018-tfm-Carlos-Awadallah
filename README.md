# 2018-tfm-Carlos-Awadallah

## Week 1
During the recent development of the [JdeRobot-Academy website](http://academy.jderobot.org:8000/) we have been investigating tools for its enrichment with computer vision practices. To do this, we must ensure that the Jupyter Notebook connects to the camera of the client's system, in such a way that the solution can be programmed on the images provided by that camera.

#### Selectable Video Source (Color Filter)
We begin this process by modifying the Color Filter node so that it accepts different video streams, in a configurable way. With this, the user can choose the video source he/she wants to use to solve the practice:

- Local Camera with OpenCV flow
- Video file stored in the local file system
- External camera (simulated or USB) through ROS / ICE plugins

The video source is selectable by modifying the configuration file of the exercise.

#### Solution
A solution for the exercise has been proposed in order to verify the correct functioning of the changes made. In addition, an entry has been created in the [developer's forum](https://developers.jderobot.org/t/color-filter-exercise/58) to discuss possible improvements or failures.

![alt text](http://url/to/img.png)
![alt text](http://url/to/img.png)
![alt text](http://url/to/img.png)
![alt text](http://url/to/img.png)

#### CamServerWeb + CamVizWeb
In the future we will try to make a new version of this practice via WebRTC + Electron. We started this path by running the JdeRobot [CamServerWeb + CamVizWeb tutorial](https://jderobot.org/Tutorials#Cameraserver-web_.2B_Cameraview-web), with recently developed tools. We found some execution problems related to incompatibilities between RosBridgeServer and some Python packages. We modified this tutorial and the installation instructions to incorporate the solution to the problem.

## Week 2

#### Selectable Video Source (Color Filter Notebook)
Once the node has been modified to accept video from the local camera, we have done the same with the Jupyter Notebook version. This new booklet also accepts different configurable video sources. The main one will be to obtain the flow of the student's local camera with OpenCV.

##### [YOTUBE VIDEO] Selectable Source (Camera Stream).
[![Selectable Source](https://www.youtube.com/watch?v=meVvdFs3Vt0/0.jpg)](https://www.youtube.com/watch?v=meVvdFs3Vt0 "")
##### [YOTUBE VIDEO] Selectable Source (Output).
[![Output](https://www.youtube.com/watch?v=ouDR7TC1_uI/0.jpg)](https://www.youtube.com/watch?v=ouDR7TC1_uI "")

## Weeks 3 and 4
The next steps are to modify the Academy Web Server to store the Notebooks and take advantage of the computer capacity of the student's system (local kernel and remote notebook). With this we will be able to have the Notebook on the Web and connect it with the local camera of each student, without needing them to have the Notebook.

#### Research
We explored different ways to achieve the above, learning the [internal architecture of Jupyter](https://jupyter.readthedocs.io/en/latest/architecture/how_jupyter_ipython_work.html), and found a possible solution to the problem:

LOCAL RUNTIME -> https://github.com/googlecolab/jupyter_http_over_ws
LOCAL RUNTIME -> https://research.google.com/colaboratory/local-runtimes.html

Now it's time to test it.

We also started to explore the new WebSim tool for future projects.
## Week 5 
We continued exploring and testing the 'Colaboratory' solution. We have also made a small break to become Academy Web's beta-tester to fine-tune the server and correct minor flaws in order to use it in the [IROS](https://www.iros2018.org/) PROGRAM-A-ROBOT contest.

## Week 6
We fine-tune details and complete the Jupyter Notebook of the Color Filter practice assuming that the necessary components are executed locally (camera).

### Add-Ons
We have added a button that allows the student to print several consecutive frames in the Notebook (both the video of the camera and the successive images segmented by his/her algorithm).

##### [YOTUBE VIDEO] Button to print Video (Camera Stream).
[![Print Video Button](https://www.youtube.com/watch?v=ouDR7TC1_uI/0.jpg)](https://www.youtube.com/watch?v=ouDR7TC1_uI "")
##### [YOTUBE VIDEO] Button to print Video (Filtered Images).
[![Print Video Button](https://www.youtube.com/watch?v=Qq9KgkcM5FU/0.jpg)](https://www.youtube.com/watch?v=Qq9KgkcM5FU "")
