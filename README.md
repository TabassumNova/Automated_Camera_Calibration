# Automated_Camera_Calibration
This GUI automates the whole calibration process also shows results of the calibration. One can also investigate the dataset quality using this.
 
# Usage
## Operation Tab
One can automate the whole calibration process using this tab. This tab allows to operate
the calibration process step by step and also shows results on the user interface. 
<p align="center">
  <img src="Images/gui1.gif" width="700"/>
  <img src="Images/ex_viz1.gif" width="350"/>
  <img src="Images/ex_viz2.gif" width="350"/>
 </p>

Following is the description of the features of Operation tab:
- **Select Directory**: ’Directory’ button is for loading a directory with camera image
folders and calibration object configuration file.
- **Initialization**: If ’Start Calculation’ button is pressed, then one python program
will start to calculate the initial camera and board parameters. After finishing the
calculation, one completion message will pop up in the info tab. If ’Show Camera
Poses’ button is pressed, one can visualize all the groups. Next,
one can select a master camera to perform the bundle adjustment calculation.
- **Bundle Adjustment**: If ’Start Calculation’ button is pressed, then one python
program will start to calculate the final camera and board parameters. By pressing
”Show Final Camera poses”, one can visualize final camera poses.
- **Results**: This portion will show final calibration results.
 
## Overview Tab
This tab provides a comprehensive dataset overview, presenting key information in a table
format. Within this table, one can find essential details such as the re-projection error and
the number of detected points in each view. The re-projection error is computed using
the final intrinsic parameters.
<p align="center">
  <img src="Images/overview_tab.png" width="700"/>
 </p>

Following is the description of the features of Overview tab:
- **< Load > Button**: This is for loading a previously saved dataset in device. One
can navigate through all the poses of all the cameras.
- **Images**: In the image widget, images of all the cameras of same pose are displayed.
- **Camera serial**: Under each image, one will find a button displaying the camera’s
serial number. Clicking on this button will open the ”Camera Window”.
- **Pose number**: Below the camera serial number, the pose number of the current
pose is shown.
- **Table**: In the table, the re-projection error and the detected point number of each
board are displayed
 
## Camera Window
<p align="center">
  <img src="Images/camera_tab.png" width="700"/>
 </p>

 Following is the description of the features of Camera Window:
- **Camera tabs**: At the top, one will find tabs labeled with the serial numbers of
each camera. Each of these tabs will display a detailed close-up view of the images
captured by the corresponding camera.
- **Load Intrinsic button**: By selecting this button, one can visualize the views that
are used for final intrinsic parameter calibration.
- **Load Pose-table button**: By clicking this button, one can visualize the images
that are used for extrinsic camera parameters and board parameters calibration.
- **Image**: Within this widget, the image of current pose is shown. Positioned above
the table are two additional widgets. The first one indicates the current dataset
mode, displaying ”Intrinsic” when the intrinsic dataset is selected and ”pose-table”
when the extrinsic dataset is chosen. To browse through different poses, one can
simply make a selection from the dropdown menu.
- **Table**: The table widget provides a concise overview of the current pose, including
details such as the count of detected points, re-projection error, and camera view
angle for each board. By clicking on any specific cell within the table, one can
access a detailed view that displays the detected points and view angle axes for the
corresponding board
 
## Calibration Tab
<p align="center">
  <img src="Images/calibration_tab.png" width="700"/>
 </p>

Following is the description of the features of Calibration tab:
- **Load button**: This is for loading a previously saved dataset in device. One can
explore all the poses captured by all the cameras using the pose navigation button.
- **Group selection dropdown**: This widget contains all the master camera and slave
camera utilized for hand-eye calibration. One can select any group from the drop
down menu for further analysis.
- **Images**: This widget displays views from a master and slave camera pair, accompanied by their respective view axes. The image on the left represents the master
camera, while the one on the right corresponds to the slave camera.
- **Table**: This table will show a simple summary of the group.
